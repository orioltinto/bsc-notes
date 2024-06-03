

**Summary of NEMO party 2024**

A significant portion of the discussion revolved around trend diagnostics. Gurvan and Seb suggested that trend diagnostics are not a high priority for NEMO5 due to their minimal user base and lack of thorough testing. This aligns with the broader theme of the meeting, which emphasized the need for robust validation processes.

The validation of the RK3 time-stepping scheme was another focal point. It was noted that the current validation status for RK3 is unclear, with many components remaining untested. This underscores the necessity of developing a more robust validation framework to ensure all parts of the code are properly evaluated, benefiting overall development.

Andrew C. mentioned that validation of the GEOMETRIC configuration is pending the hiring of a new team member, indicating that this may not happen within the current year. There was also a discussion about the type of validation information needed for CMEMS (Copernicus Marine Services), including performance data and comparisons between NEMO versions 4 and 5. Concerns were raised about the lack of proper ERA5 forcing for these validations.

In terms of performance, the eORCA36 tests showed a 30% improvement with the RK3 scheme, although further confirmation is needed with NEMO5. Similarly, in the Black Sea MFC, NEMO5 demonstrated reproducibility with comparable results to version 4.2.2, aside from a small degradation in sea level anomalies (SLA).

The adoption of XIOS3 was highlighted for its improved memory footprint. For instance, at the MetOffice, XIOS2 required more nodes for input/output operations than computing, an issue addressed by XIOS3.

The timeline for NEMO5's release was discussed, with a consensus that serious validation by June was unrealistic, leading to a postponement until September. There was also a debate on whether to adopt XIOS3 as the default, given its beta status and ongoing developments.

Testing within NEMO was another critical topic. The limitations of SETTE, which tests entire configurations and makes it difficult to pinpoint specific failures, were acknowledged. The introduction of unit tests using the pFUnit framework was suggested as a complementary approach.

During the scientific validation session, it was noted that SETTE verifies physical consistency but does not detect all potential issues, as exemplified by missing simulations that were not flagged. In GitLab, discussions focused on updating templates, naming conventions, and merging protocols. Clement is currently reviewing and closing irrelevant merge requests and issues to streamline the process.

A detailed overview of the RK3 scheme was provided, emphasizing its activation steps. Additionally, a knowledge mapping exercise was conducted to assess familiarity with different parts of the code.

Timings routines have been rewritten to minimize overhead and include additional features like MPI statistics in netCDF format. A tutorial on setting up a local GitLab runner was also presented, enhancing the continuous integration process.

The session included a demonstration of XIOS3 usage, showing how different servers can be assigned various purposes and a script to compute chunk sizes based on target space requirements. The cleanup session focused on removing obsolete code to streamline the development process.

Christopher Bladwell from the Bureau of Meteorology in Australia presented comparisons between NEMO and other models, including examples with data assimilation.

Single precision NEMO was another topic of interest. Sam Hatfield presented on making NEMO work in single precision, detailing the numerous bug fixes required. Despite efforts, the results were not very promising for large configurations using ECMWF's coupling because the atmosphere requires much more resources and with these resources NEMO is mostly bounded by network latency.

In discussions about single and mixed precision, it was noted that NEMO5 does not currently work in single precision, but efforts are ongoing to address this issue.

The meeting concluded with a wrap-up summarizing the key points and an outline for sharing the document. Support for working groups was also addressed, with an emphasis on organizing meetings and improving processes and pages for the HPC, Verification and Validation, and Kernel working groups. There is a clear need to enhance the activity and visibility of these groups to ensure ongoing development and support.