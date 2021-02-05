Applies the arosics algorithm (https://github.com/GFZ/arosics) to perform spatial registration of WorldView3 (WV3) imagery to a Sentinel 2 MSI reference image.
The WV3 image must be on a local drive.  
The MSI image is taken from a Google Drive and brought to a local synchronized google drive.
The output corresponds to a registered version of the WV3 image in the local drive.

The user must have
1.  A Google Drive synchronized to the local drive.  Make sure the local drive does not have spaces in the name.
2.  A Google Earth Engine account associated with the Google Drive.
3.  An anaconda environment configured as follows for the first instance:

(base)>conda create --name arosicsWV3
conda activate arosicsWV3
(arosicsWV3)>conda install -c conda-forge rasterio -y
(arosicsWV3)>conda install -c conda-forge geopandas -y
(arosicsWV3)>conda install -c conda-forge folium -y
(arosicsWV3)>conda install -c conda-forge geoarray -y
(arosicsWV3)>conda install -c conda-forge arosics -y
(arosicsWV3)>conda install -c conda-forge descartes -y
(arosicsWV3)>conda install -c conda-forge jupyterlab -y
(arosicsWV3)>conda install -c conda-forge earthengine-api -y
 
4.  For execution, start anaconda and initiate a jupyter lab environment in a web browser
 
(base)>conda activate arosicsWV3
(arosicsWV3)>jupyter lab

5.  Open the file arosicsWV3.ipynb as a notebook

6.  Change the first notebook cell with your paths.  
    Leave the output image path empty if you dont want to actually save a registration. 
    Leave the output report path empty if you dont want to save an registration report.


7.  Change the first notbook cell with a selection of either Global or Local registration.  

8.  Run the notebook.  You will have to enter your Google Earth Engine authentication code into cell 4 when requested.
