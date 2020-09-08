===============
 NAC
===============

Date Created: March 10, 2019

The NAC code takes collections of Landsat 5 TM, Landsat 7 ETM+, and Landsat 8 OLI data in a specified boundary and from 1986 to 2016 and combines it into one merged collection.
In this process, it also applies a correction to make Landsat 8 OLI data more comparable to Landsat 5 TM and Landsat 7 ETM+ data. Each dataset is also masked to remove cloud cover
using the QA bands in each dataset. This merged collection of data is then used to calculate the maximum NDVI value for each month within each year. This results in a collection of single
band NDVI images with 2 properties associated with each file: month and year. This is collection of monthly NDVI maximums for each year from 1986 to 2016 is then used to
calculate the mean NDVI maximum for each month across all years. This collection of mean NDVI maximums for each month is then exported to Google Drive at a 30 meter resolution.


 Parameters
-------------
1. Import the shapefile of your area of interest as a Google Earth Engine Asset
2. Modify the variable "shape" to point to the correct location to load in the converted shapefile (ex: shape = ee.FeatureCollection("users/account_name_here/asset_name_here")
3. Modify the "Map.setCenter()" to center on the shapefile. This may take trial and error or calling a Google Earth Engine function.


 Contact
---------
Name(s): Anna Stamatogiannakis
E-mail(s): annastamatog@gmail.com
