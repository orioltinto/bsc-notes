In this work, the authors developed lossy compression tools, 'enstools-encoding' and 'enstools-compression'. The authors outline that the manuscript and tools enable scientists to compress existing datasets and create compressed new datasets. The tool and manuscript also introduced a bisection method that automatically choose an optimal lossy compression method and/or its parameters based on given metrics. The authors further evaluate the lossy compression with forecasted kinetic energy spectra, fraction skill scores, and 3D visualisation of derived variables. The manuscript presents a practical tool for the lossy compression algorithms. The evaluations of lossy compression algorithms are stated clearly and useful for practical applications. Therefore, I recommend the publication of this manuscript once the following comments are addressed.

## Major comments:  
  
1. The proposed compression tool is used to reduce the size of, presumably, large datasets. One concern is the efficiency of the compression tool. As a perhaps extreme example, when I tried to use it with a 13G global ocean model output, the tool is very slow on my personal laptop. It would be instructive to indicate 1) are the compression algorithms pure Python, or are C/Fortran libraries used for compression? 2) can we use the parallel capability in xarray to speed up the processing? 3) can authors provide some comments on the efficiency of the tool?  
  
2. In Figure 1, 2,  axis labels and legend labels are not shown. In Figure 3, the colourbar does not have labels and values. It also does not have subfigure labels such as a), b) and c) which are used in the caption. These issues make some results difficult to interpret.

## Minor comments:  
  
1. L95, page 4, it says '...this work aims to ensure that scientists can seamlessly utilize the compressed data. Essentially, the intent...'. Does the first sentence have the same meaning as the second sentence starting from 'Essentially'? Otherwise, I feel that the meaning of "seamlessly utilize the compressed data" is unclear.  
  
2. L136, page 5, would it be better to use 'ranging from x_0 to x_1 (x_1 > x_0)' than specific values?  
  
3. In Section 2.2, authors introduces the use of CSF. It would be good to refer to the Appendix A, or briefly explain where CSF is used, i.e. in Python function call arguments and command line arguments, such that readers won't get lost on the context of these specifications as well as how to use these specifications.  
  
4. In Section 2.4, "enstools-encoding" was introduced without explicitly distinguish it from "enstools-compression" introduced in the start of Section 2. In L218, page 7, authors claim that "Additionally, we provide a command line interface...", which gives me an impression that the "enstools-compression" can only be used as command line interface but the documentation of enstools-compression seems to suggest that it has a Python API as well.  
  
5. In L254, page 9, it is not clear what is "see 2" in the bracket.  
  
6. in L272, it might be useful to highlight the "coordinate directions" in Figure 3.  
  
7. In the code availability section, although the texts are correct and I'm able to access them, links by mouse click to both the github repository (an additional bracket in the link) and the zenodo entry (only linked to https://doi) are both broken. Additionally, it is unclear if "enstools-encoding" part of the manuscript and should be included in the code availability section.