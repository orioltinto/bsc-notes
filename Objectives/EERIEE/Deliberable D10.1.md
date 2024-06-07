
- [ ] Escriure part sobre mixed-precision.
Fonts:
      Deliverables Destination Earth:
  - https://tt.eduuni.fi/sites/csc-rdi-fileshare/_layouts/15/WopiFrame2.aspx?sourcedoc=%7B0B0C5A23-27D3-4E69-8738-E2E8E2C93541%7D&file=DE_340_D340.3.1.2_202310_PerformanceEngineeringOfClimateModelsFirstImprovements_v2.docx&action=default
      
	[Pàgina d'eerie](https://eerie-project.eu/research/modelling/our-models/)
No hi ha limits d'espai

Arxiu a modificar:
https://docs.google.com/document/d/1bPLSkLK7NYaQV9531RITI6gQaupHXDSZ/edit


# Text from deliverable:
Mixed precision techniques have gained popularity in the last 10 years as they promise a very high impact on performance just by tuning the precision of each variable in the code in the appropriate way. This would be, anyway, a very complex task if one were to implement it by hand. Barcelona Supercomputing Center in the past years has been working on a tool [1], named AutoRPE, to automate this implementation in Fortran codes. The tool itself is based on the RPE library, a reduced-precision emulator developed at ECMWF by A. Dawson and P. Düben [2]. Given an input Fortran 90 code, and a given run configuration, this tool is able to highlight the list of those variables that need to retain double precision in order to get accurate results.  

  

We are going to use this tool here to produce a mixed-precision version of NEMO to be coupled with IFS, which is already running in single precision. While for newer releases of NEMO (V4.2), a mixed-precision version is already available, for the version chosen for Destination Earth (V4.0) we needed to start from scratch. The first challenge that we faced was to integrate the ifs-bundle into our workflow. The original tool is intended to work in a completely automatic way, which includes downloading the sources from official repos (gitlab, bitbucket, svn, etc.), and downloading the data from the cloud (in the specific case of NEMO for example official input datasets are stored on Zenodo). Here we needed to deviate from the intended behavior, since the code is a modified version of NEMO, coming from NextGems configuration, and the input data we used came from the spin-up runs and were not stored on any cloud repository. So we adapted those parts of the workflow accordingly. Additionally, we needed to modify some ifs-bundle cmake rules so that the compilation process produces intermediate pre-processed files for NEMO, needed by our tool to implement the RPE Emulator. Although this last part looks trivial, it was not. Due to the complexity of the compilation process, the fact that the compiling time for the ifs-bundle is around 2 hours, and the fact that very often the compilation, when not started from scratch, fails, it took us some time to adapt this part of the workflow.  

  

We are not going to enter here into the detail of the implementation, but we will just mention that the emulator needs to parse the preprocessed files. Once these were produced, we needed to develop a couple of additional features for the tool, to be able to cope with some specific coding patterns not present in the codes analyzed so far with the emulator. Finally, when we started running the workflow for the precision analysis the MultIO implementation was not yet ready, so not to waste time we decided to use XIOS, the default I/O server used by NEMO. This implied spending some time tuning the XML files used by XIOS since the spin-ups were run with native NEMO output and so no one had used this set-up yet.

  

Once everything was ready, we started running a first analysis with 1896 variables, with an eORCA1 configuration. It has been run on Marenostrum4, the Barcelona Supercomputing Center HPC since LUMI has proved quite unstable, and we don’t make use of a fault-tolerant workflow for submitting the runs of the analysis. It runs a total of 847 simulations, highlighting a list of 431 variables (~ 23% of the total) that needed to be kept in double precision. Once we had this list, we started implementing the changes in the real code, so that we would be able to run a simulation without the emulator to check that everything is working as expected and there are no errors in the results. At this point, we noticed that something did not work correctly, since too many variables were being cast to double precision: the reason was that the list of used variables that we considered when starting the analysis was incomplete. So we needed to recompute the number of variables to analyze and start a new analysis with 2876 variables this time. The analysis did not need to be run all over again since a lot of the previous runs could be reused. It is now running toward the end, and we estimate that it will be finished by next week.

  

Once the analysis with the full variable set is complete, the next step is to update the variable's precision in the original code, as well as apply some additional modifications required to make it compatible with the changes. Then, we will validate the mixed precision version against reference simulations (an experiment in double precision) to ensure that the results do not deviate substantially from one another. All of this will be done using an eORCA1 grid, but the final objective is to create a version that works with an eORCA12 configuration. However, for the eORCA12 grid, we will not repeat the analysis, as the time to run all of the simulations would be too long. Instead, we will use the same precisions of the variables obtained with the eORCA1 analysis. This configuration will then be validated against observational data instead of reference simulations. Again, the reason for that is to avoid having to compute reference runs for eORCA12, which are too computationally expensive.


# Modified text

