
Note from the Editor:
```
Dear Authors,  
  
Thank you for submitting your work to GMD.  
  
Before we proceed with the public peer review, please revise the preprint addressing the following points:  
  
- Title: it is required to include software name and version in the title (e.g., by adding ": a case study using enstools-compression 2023.11.1") See: https://www.geoscientific-model-development.net/about/manuscript_types.html#item2  
  
- Figures 3-8: please use vector graphics for all line plots, and preferably also for other plots with raster elements embedded in vector-rendered axes and labels (essentially, save all figure files as pdfs in plot-generating scripts)  
  
- Figures: ensure that text within plots has uniform large-enough size across all figures and roughly matches the font size in the main body of the manuscript  
  
- Code & data availability: please note that GMD requires all associated files to be labelled with a version identification, licensing terms and persistently archived at a repository such as Zenodo. GitHub link can be provided as additional information, but neither github.com nor pypi.org are considered as persistent. The scope of this requirement encompasses not only the software package described, but also scripts needed for reproduction of all presented figures by the reviewers and readers.  
  
- Author contributions, Competing interests and Acknowledgements take 3.5 pages in total, while could fit in just a half  
  
- References (see https://www.geoscientific-model-development.net/submission.html#references):  
- use journal acronyms consistently  
- add author information and a DOI link (https://doi.org/10.17487/rfc...) for RFC 8878,  
see also https://datatracker.ietf.org/doc/html/draft-carpenter-rfc-citation-recs-01#section-5.2  
- Alted 2010: add DOI  
- Ayachit: add DOI (https://doi.org/10.1201/b12985-31)  
- Bray 2017: switch to DOI link, no need for "accessed" field then  
- Burden & Faires: could a more modern edition be cited? (https://cengage.uk/c/numerical-analysis-10e-faires/9781305253667/)  
- Deutsch & Gailly: switch to DOI link (https://doi.org/10.17487/rfc...)  
- Caron 2014: for such type of web URL, I'd generally suggest linking to archive.org (https://web.archive.org/web/20141024232623/https://www.unidata.ucar.edu/blogs/developer/entry/compression_by_bit_shaving)  
- Craig et al. 2021a: isn't it a repeated entry (see 2021b)  
- Craig et al. 2021b: fix DOI URL (https://doi.org/https://doi.org)  
- h5netcdf: URL should not have the "www." prefix? - it seems to only work without it  
- Lawrence et al. 2018: add book info (incl. editors) + persistent URL: http://hdl.handle.net/2128/22029  
- Lindstrom 2017: add persistent URL: https://osti.gov/biblio/1526183  
- Liu et al. 2021: could this reference be used insteap of arXiv eprint: https://doi.org/10.1109/Cluster48925.2021.00034 ?  
- Matsunobu et al. 2022: please cite the final manuscript, not an e-print (note different title and author list): https://doi.org/10.5194/wcd-3-1273-2022  
- Matsunobu et al. 2024: add DOI https://doi.org/10.1002/qj.4713  
- Norton and Clyne: add DOI https://doi.org/10.1201/b12985-33  
- Tao et al. 2018: cite this instead (note different year)? https://doi.org/10.1109/TPDS.2019.2894404  
  
Please note that the preprint pdfs are made public for the purpose of peer review without any modifications to the text or layout - in exactly the form as uploaded by the authors.  
  
Note the comment from file validation review: "Please ensure that the colour schemes used in your maps and charts allow readers with colour vision deficiencies to correctly interpret your findings. Please check your figures using the Coblis – Color Blindness Simulator (https://www.color-blindness.com/coblis-color-blindness-simulator/) and revise the colour schemes accordingly. => Figs. 4, 7"  
  
Best regards,  
Sylwester Arabas
```

Point by point:

- [x] Title: it is required to include software name and version in the title (e.g., by adding ": a case study using enstools-compression 2023.11.1") See: https://www.geoscientific-model-development.net/about/manuscript_types.html#item2  
  Done.
- [x] Figures 3-8: please use vector graphics for all line plots, and preferably also for other plots with raster elements embedded in vector-rendered axes and labels (essentially, save all figure files as pdfs in plot-generating scripts)
	- [x] Redo:
		- [x] 3  -> Smaller font?
		- [x] 4 -> Tobias' figure (might need to have a bit bigger font).
		- [x] 5 -> Takumi's figure (mail sent)
		- [x] 6 -> Old Figure 4
		- [x] 7 -> Old Figure 6 (need to merge them) Might want to increase font size.
			- [x] Redo parts with proper figure and font sizes
		- [x] 8 -> Old Figure 5
	- [x] Update in document.
- [x] Figures: ensure that text within plots has uniform large-enough size across all figures and roughly matches the font size in the main body of the manuscript  

- [x] Code & data availability: please note that GMD requires all associated files to be labelled with a version identification, licensing terms and persistently archived at a repository such as Zenodo. GitHub link can be provided as additional information, but neither github.com nor pypi.org are considered as persistent. The scope of this requirement encompasses not only the software package described, but also scripts needed for reproduction of all presented figures by the reviewers and readers.  
  
- [x] Author contributions, Competing interests and Acknowledgements take 3.5 pages in total, while could fit in just a half  
  
- [x] References (see https://www.geoscientific-model-development.net/submission.html#references):  
	- [x] use journal acronyms consistently  
	- [x] add author information and a DOI link (https://doi.org/10.17487/rfc...) for RFC 8878,  
	see also https://datatracker.ietf.org/doc/html/draft-carpenter-rfc-citation-recs-01#section-5.2  
	- [x] Alted 2010: add DOI  
	- [x] Ayachit: add DOI (https://doi.org/10.1201/b12985-31)  
	- [x] Bray 2017: switch to DOI link, no need for "accessed" field then  
	- [x] Burden & Faires: could a more modern edition be cited? (https://cengage.uk/c/numerical-analysis-10e-faires/9781305253667/)  
	- [x] Deutsch & Gailly: switch to DOI link (https://doi.org/10.17487/rfc...)  
	- [x] Caron 2014: for such type of web URL, I'd generally suggest linking to archive.org (https://web.archive.org/web/20141024232623/https://www.unidata.ucar.edu/blogs/developer/entry/compression_by_bit_shaving)  
	- [x] Craig et al. 2021a: isn't it a repeated entry (see 2021b)  
	- [x] Craig et al. 2021b: fix DOI URL (https://doi.org/https://doi.org)  
	- [x] h5netcdf: URL should not have the "www." prefix? - it seems to only work without it  
	- [x] Lawrence et al. 2018: add book info (incl. editors) + persistent URL: http://hdl.handle.net/2128/22029  
	- [x] Lindstrom 2017: add persistent URL: https://osti.gov/biblio/1526183  
	- [x] Liu et al. 2021: could this reference be used insteap of arXiv eprint: https://doi.org/10.1109/Cluster48925.2021.00034 ?  
	- [x] Matsunobu et al. 2022: please cite the final manuscript, not an e-print (note different title and author list): https://doi.org/10.5194/wcd-3-1273-2022  
	- [x] Matsunobu et al. 2024: add DOI https://doi.org/10.1002/qj.4713  
	- [x] Norton and Clyne: add DOI https://doi.org/10.1201/b12985-33  
	- [x] Tao et al. 2018: cite this instead (note different year)? https://doi.org/10.1109/TPDS.2019.2894404  
  
Please note that the preprint pdfs are made public for the purpose of peer review without any modifications to the text or layout - in exactly the form as uploaded by the authors.  
  
Note the comment from file validation review: "Please ensure that the colour schemes used in your maps and charts allow readers with colour vision deficiencies to correctly interpret your findings. Please check your figures using the Coblis – Color Blindness Simulator (https://www.color-blindness.com/coblis-color-blindness-simulator/) and revise the colour schemes accordingly. => Figs. 4, 7"  
  
Best regards,  
Sylwester Arabas



# EXTRA NOTES

I modified the caption of Tobi's figure.