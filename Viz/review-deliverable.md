# What do they present:

## Premises:
	- Data is in gsv+HEALPix.

## What do we have in the document?
- Data retrieval:
	- Basically they say pip install gsv ...
- Visualisation techniques:
	- The only part here that is specific for high-resolution data is the fact that one must have in mind the resolution of the displays as well. Interpolating to a more-than-needed resolution represents a significant added cost with 0 return.
- Parallelization with Dask:
	- It is a nice point to rely on existing tools to improve performance. However, instead of using dask to accelerate something that is inherently super-slow like matplotlib, one would think that exploring healpy would be a more interesting option.
	- Also, If we start from a netcdf, it means that we needed a previous step to get and save the data from gsv, isn't it?
- Combining images to an animation:
	- Really?
- Future Directions:
	- Is this the state-of-the-art or just blind thrown ideas?


# My comments:

Dear,

In general my feeling is that the content does not address the topic of the deliverable.

In my opinion the biggest challenge in relation to dealing with the visualisation of high resolution data is it's heaviness. Two points are relevant, how to improve the performance and how to reduce the demand (i.e. not using more resolution than needed). Everything else besides these points feels like filling. I would expand in the point about the resolution of the data is bigger than the resolution of the displays and how this can be exploited to reduce data demand by interpolating to smaller grids or cropping to a certain region. The performance part is somehow addressed with the suggestion of using Dask, however it is used to parallelise a plot using matplotlib, when other more performant alternatives would be more relevant. Given that the data is stored in HEALPix grids, wasn't the option of using healpy explored?  

About the future plans, was the state-of-the-art on interactive data exploration explored?
Again, the biggest constrain on any interactive exploration will be the data bottleneck. I would mention that regardless of the front-end used to visualise the data, how the data is provided will be the critical part.

I hope the comments are helpful.

Best,
Oriol

Dear,

Overall, my feeling is that the content presented does not adequately address the key topic of the deliverable.

The principal challenge with handling high-resolution data is its inherent "heaviness." There are two critical issues: enhancing performance and reducing data demands—specifically, avoiding the use of higher resolutions than necessary. Any content that does not directly contribute to these discussions seems superfluous.

I suggest elaborating on how the discrepancy between data resolution and display resolution can be leveraged. Techniques like interpolating to smaller grids or cropping to specific regions could significantly reduce data demands. While the use of Dask to parallelize plotting with matplotlib points to the right direction, it would be important to consider more efficient alternatives than matplotlib that are better suited to handling large datasets. For example, given that the data is stored in HEALPix grids, exploring the use of 'healpy' might offer optimized solutions.

Regarding future plans, it is crucial to investigate the current state-of-the-art in interactive data exploration. The predominant limitation for any interactive system will be the data bottleneck. It is essential to emphasize that, regardless of the visualization front-end employed, the manner in which data is managed and delivered will be pivotal.

I hope you find these comments constructive.

Best regards,

Oriol