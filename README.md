# Eucalyptus classification

* Step 1: Prepare an AOI file and modify the GT data (QGIS)
  * Make a geojson file of an AOI in **EPSG:4326**.
  * Clip and reproject (e.g. EPSG:28350 in Albany) the GT data and rasterize it.
    * Load the GT data
    * `Raster > Extraction > Clip by mask layer`
    * `Raster> Projections > Warp (reproject)` (the output resolution should be matched to that of S2)
    * Export as geotiff
* Step 2: Data downloading and preprocessing  (`S2_download_and_preprocessing.ipynb`)
  * Download an ECARR and NDVI image via GEE
  * Preprocess the GT data
  * Preprocess the index data (reprojection, shape adjustment, etc)
* Step 3: Main analysis (`eucalyptus_classification.ipynb`)
  * Train and validate the model for eucalyptus classification (logistic regression)
  * Export the result as a vector map

# Workflow eucalyptus classification
<img width="250" alt="workflow_eucalyptus_classification" src="https://github.com/jutak0228/eucalyptus_classification/assets/159540763/5c3bae42-924b-4375-8d80-e3832bc4a6eb">
