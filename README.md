# shub_cloudless
 Sentinel Hub configuration for downloading cloudless images from selcted extents in a selected time frame
 
 > **PROBLEM:** accessing server for Landsat data (token not found).
 > 
 > **SOLUTION:** Install `sentinelhub` package using pip, anaconda does not have the latest version!


## Data Collections

For detailed list visit the links below. Some examples include:

```
DataCollection.SENTINEL2_L1C
DataCollection.SENTINEL2_L2A
DataCollection.SENTINEL1
DataCollection.LANDSAT_OT_L1
DataCollection.LANDSAT_OT_L2
```

[Data Collections Tutorial](https://sentinelhub-py.readthedocs.io/en/latest/examples/data_collections.html)

[Documentation](https://docs.sentinel-hub.com/api/latest/data/)


### Available bands and data

[Sentinel-2 L2A](https://docs.sentinel-hub.com/api/latest/data/sentinel-2-l2a/#available-bands-and-data)

[S-2 Cloud Masks](https://docs.sentinel-hub.com/api/latest/user-guides/cloud-masks/)

- CLM: 0 (no clouds), 1 (clouds), 255 (no data)
- CLP: 0–255 (divide by 255 to get to the [0-1] range)

[Landsat-8 L2](https://docs.sentinel-hub.com/api/latest/data/landsat-8-l2/#available-bands-and-data)

Cloud mask from the `BQA` band (= Quality Assessment band). Use [decodeL8C2Qa](https://docs.sentinel-hub.com/api/latest/evalscript/functions/#decodel8c2qa) function to get values.

[https://www.sentinel-hub.com/faq/how-can-i-access-data-landsat-8-quality-assessment-band/](https://www.sentinel-hub.com/faq/how-can-i-access-data-landsat-8-quality-assessment-band/)

(Custom script: Č8 cloud segmentation)[https://github.com/sentinel-hub/custom-scripts/tree/master/landsat-8/clouds_segmentation]
