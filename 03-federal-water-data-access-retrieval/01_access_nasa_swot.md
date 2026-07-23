# Retrieve NASA SWOT water surface elevation data

There are many ways to find, access, and download NASA SWOT data. This module is going to spend the most time focusing on the recommended patterns for hydrology applications using the water surface elevation (`wse`) data from the SWOT mission. To help build the framework, you need to know that there are two ways to programmatically get access to SWOT data:

1. `earthaccess`: this is a Python library that allows users to access all of the NASA Earthdata stored in the cloud, including SWOT mission data. It streamlined what used to be complex access patterns across different systems and tools in order to help scientists get to the data faster (see more in [this blog post](https://nasa-openscapes.github.io/news/2024-03-04-earthaccess-tech-spotlight/)). Using `earthaccess`, a user can easily authenticate using the Earthdata login, find what data is available, and download or access a variety of products in NASA's cloud storage buckets.
1. `hydrocron`: this is an API built specifically to help streamline timeseries data access to the `SWOT_L2_HR_RIVERSP` data product. The queries allow users to access data across temporal ranges for specific locations, which is in contrast to how the SWOT data are archived (individual shapefiles per timestamp). It allows users who may be interested in a timeseries of data at a small number of locations the ability to easily retrieve that without a lot of extra effort. More on how `hydrocron` works is available in [this NASA news article](https://www.earthdata.nasa.gov/news/hydrocron-new-tool-swot-time-series-analysis).

## Programmatic data discovery

[earthdata login, CMR, Amazon AWS S3 bucket access all packaged up in `earthaccess`]

## Programmatic data downloads

[remind about the differences between hydrocron/earthaccess + some info about cloud-native data access vs "downloads"]

### `earthaccess`

[what data types this accesses and how to use the results]

### `hydrocron`

While a user can access SWOT data through `earthaccess`, if timeseries data for specific rivers are the desired outcome, then the `hydrocron` API is the tool for the job. As the []`hydrocron` documentation](https://podaac.github.io/hydrocron) states, 

> SWOT data is archived as individually timestamped shapefiles, which would otherwise require users to perform potentially thousands of file IO operations per river feature to view the data as a timeseries. Hydrocron makes this possible with a single API call.

[get into the use-cases for hydrocron and examples for install, etc]

## Best practices FAQs

See sections below for answers and code examples to the following questions.

* What is the recommended way to download data for **one location across the full period of record**?
* What is the recommended way to download data across **all locations for a small time range**?
* If I am working on improving efficiency through **code parallelization**, what should I do vs avoid?
* [...]

### Temporal scaling

What is the recommended way to download data for one location but the full period of record?

### Spatial scaling

What is the recommended way to download data for all locations but a small time range?

### Parallelization

If I am working on improving efficiency of my code through parallelization, what should I do vs avoid?

### [...]

## Further reading

[links out to agency pages on more information, can be duplicates of pages already referenced above]
