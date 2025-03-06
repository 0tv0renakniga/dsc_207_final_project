# change local links fpaths once removed from main notebook
## Datasets

#### ICESat-2
1. Description
- explain general
- altimeter data, lots of diff data products.. see image below
![alt text](./icesat2_data_products.png "ICESat-2 Data Products")
- Read more [here](https://nsidc.org/data/icesat-2/products)
- formats: h5py
2. where to access
- use icepyx to access
    - Read more[here](https://icepyx.readthedocs.io/en/latest/example_notebooks/IS2_data_access.html)
- use earthaccess 
    - Read more [here](https://earthaccess.readthedocs.io/en/latest/quick-start/)
- hosted by nasa earthdata.nasta.gov
    - see more public data [here](earthdata.nasa.gov)
3. Specific Processing Tools
- [icepyx](https://github.com/icesat2py/icepyx/blob/main/doc/source/example_notebooks/IS2_data_access.ipynb)
- [earthaccess](https://github.com/nsidc/earthaccess)
    - add instructions for [.netrc] creation.. need account on [urs.earthdata.gov](https://earthaccess.readthedocs.io/en/latest/quick-start/)
- spacepy or h5py
4. Potential applications
- look at elevation changes of land ice, sea ice, vegetation, atmosphere etc. see data products
#### GRACE & GRACE-FO
1. Description
- explain general
    - The GRACE and GRACE-FO “mascons” (e.g. RL06M) add *why*(pg 29-30 L3 handbook)
    - Read more [here](./resources/data_docs/GRACE-FO_L3_Handbook_JPL.pdf)
- version: JPL RL06M Version 2.0
    - Read more [here](./resources/data_docs/GRACE_GRACE-FO_ReleaseNotes_JPL_MASCON.txt)
- formats: *netcdf, ascii, geotiff* (land only).
- find other docs [here](https://podaac.jpl.nasa.gov/gravity/gracefo-documentation)
2. Data Access
- access through PO.DAAC at JPL or ISDC at GFZ(pg 28 L3 GRACE handbook)
    - [PO.DAAC data here](https://podaac.jpl.nasa.gov/dataset/TELLUS_GRAC-GRFO_MASCON_CRI_GRID_RL06_V2)
    - note: ocean and land girds are published separately
    - [ISDC data here](https://isdc.gfz.de/homepage/)
3. Specific Processing Tools
- Tool 1 see L3 hand book for guidence
    - github link
- Tool 2 need something for handling data formats(*netcdf, ascii, geotiff*)
4. Potential Applications
- Weather Forecasting, Earthquake Observation, Ice Mass Change, etc.
5. Step Summary
- preliminary exploration:explore data using GRACE(-FO) Data Analysis Tool to find areas of interest 
    - [GRACE(-FO) Data Analysis Tool here](https://grace.jpl.nasa.gov/data/data-analysis-tool/)
- download data sets for areas of interest
- pre-processing: multiply mascon by gain factor(also called scale factor) to enhance spatial resolution(L3 handbook pg 30)
- visualize data(see example L3 handbook pg 31)