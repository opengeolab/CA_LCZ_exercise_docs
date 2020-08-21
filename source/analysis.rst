
.. _analysis:

Hands-on Exercise with QGIS
=============================

Now that you are aware of all the necessay backround information, it is time to do work with the Milan case study. To asses differences in the average air temperature within different LCZ, you will perform the following steps:

 * download in your home folder the raw air temperature data from the `C3S CDS <https://cds.climate.copernicus.eu/#!/home>`_ in `netCDF <https://www.ogc.org/standards/netcdf>`_ format) and the LCZ map for Milan.
 * open and manipulate the netCDF in QGIS to obtain an analysis-ready raster layer containg the average air temperature for a given time period.
 * open the LCZ map in QGIS and perform raster layer zonal statistics to compute the average air temperature within each LCZ class
 * plot and compare the averages using statistical graphs 



Materials
------------------------------------

Data specification and software tools that you will use for the analysis are reported below. 


LCZ map
+++++++++++++++++++++++

The LCZ raster map of Milan you will use in the exercise has been derived by [4]_ from a Sentinel-2 image acquired in summer 2016. The map includes the subset of LCZ characterizing the Milan area. Some of the contiguous classes have been aggregated (as shown in the table below) with the purpose of obtaining zones with marked differences in the urban land-use features thus easing their comparison in terms of air temperature. As argued in [4]_, contiguous LCZ classes may be more easily confused during the classification procedure and differences in their contributions to air temperature may be to low to be observed.   

.. figure:: /images/lcz_map.png
   :alt: text 
   :scale: 100%

   LCZ map of Milan

+------------------+---------------------------------------------------------------+
| **Raster Value** |                        **Description**                        |
+------------------+---------------------------------------------------------------+
|         1        |                        Compact midrise                        |
+------------------+---------------------------------------------------------------+
|         2        | Compact low-rise, Open midrise, Open low-rise, Large low-rise |
+------------------+---------------------------------------------------------------+
|         3        |                        Scattered trees                        |
+------------------+---------------------------------------------------------------+
|         4        |                           Low plants                          |
+------------------+---------------------------------------------------------------+
|         5        |                             Water                             |
+------------------+---------------------------------------------------------------+


The LCZ map of Milan (*s2_lcz_milan.tif*) toghether with its predfined QGIS style file (*s2_lcz_milan.qml*) can be download `here <https://github.com/danioxoli/CA_LCZ_exercise_docs/raw/master/source/files/lcz.zip>`_.

.. tip::

   Keep in the same folder both the raster map and its predefined QGIS style file to allow QGIS to automatically style the map when imported in a project.

Air temperature data
+++++++++++++++++++++++

Air temperature data at a city level are included in the `Climate variables for cities in Europe from 2008 to 2017 <https://cds.climate.copernicus.eu/cdsapp#!/dataset/sis-urban-climate-cities?tab=overview>`_ of the C3S CDS, which contains air temperature, specific humidity, relative humidity and wind speed for 100 European cities for the current climate. The variables are provided as netCDF files with an hourly temporal resolution on a 100m x 100 m spatial grid (CRS: ETRS89/LAEA Europe | EPSG: 3035). 

.. figure:: /images/cds_city_data.png
   :alt: text 
   :scale: 50%

   Climate variables for cities in Europe from 2008 to 2017 (https://cds.climate.copernicus.eu/cdsapp#!/dataset/sis-urban-climate-cities) 

After `register and login <https://cds.climate.copernicus.eu/user/register>`_ to the C3S CDS web portal, data can be download for a single city by specifying the variables of interest together with a time period (year and month). The selected data can be then downloaded as a *.zip* or *.tar* file. For this exercise you have to specify the following options for the download:

 * Variable = *Air temperature*
 * City = *Milan*
 * Year = *2016*
 * Month = *July*
 * Format = *Zip file (.zip)*


.. figure:: /images/nc_milan_download.png
   :alt: text 
   :scale: 50%

   Data download panel

The netCDF file is structured as a multidimensional spatial grid where each layer includes air temperature observations over Milan area at each time step (hour) in July 2016. 

.. figure:: /images/netcdf.png
   :alt: text 
   :scale: 100%

   Schematic of the netCDF structure 

.. note::

   The name of the original downloaded file should be "*tas_Milan_UrbClim_2016_07_v1.0.nc*"


Software tools
+++++++++++++++++++++++


Data Processing
------------------------------------


Results
------------------------------------






..  [4] *Oxoli, D., Ronchetti, G., Minghini, M., Molinari, M. E., Lotfian, M., Sona, G., & Brovelli, M. A. (2018). Measuring urban land cover influence on air temperature through multiple geo-data—The case of Milan, Italy. ISPRS International Journal of Geo-Information, 7(11), 421.*

