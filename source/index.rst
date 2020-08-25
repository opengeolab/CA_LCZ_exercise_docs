.. LCZ and tempertature analysis with QGIS documentation master file, created by
   sphinx-quickstart on Mon Aug 17 11:52:45 2020.
   You can adapt this file completely to your liking, but it should at least
   contain the root `toctree` directive.

Hands-on exercise: LCZ and air tempertature analysis with QGIS
===========================================================================

This tutorial will focus on the use of `Copernicus <https://www.copernicus.eu/en>`_ data for assessing local differences in air temperature according to land-use features within highly urbanized cities. 

Through a computer exercise, you will analyse the case of `Milan <https://en.wikipedia.org/wiki/Milan>`_ (Italy) using air temperature data from the `Copernicus Climate Change Service (C3S) <https://climate.copernicus.eu>`_ and the `Local Climate Zones (LCZ) <http://www.wudapt.org>`_ map of the city, derived from `Sentinel-2 <https://sentinel.esa.int/web/sentinel/missions/sentinel-2>`_ imagery.

You will learn how to access and download `C3S data <https://cds.climate.copernicus.eu/#!/home>`_ and how to process them in `QGIS <https://qgis.org/en/site/forusers/download.html>`_ |qgisicon| to obtain a quantitative insight into the LCZ influence on air temperature. The question you are going to answer with this exercise is *"Can we observe and quantify differences in the average air temperature within different LCZ of a city?"*

.. |qgisicon| image:: images/qgis_icon.png
   :scale: 8% 

.. important::

   Basic knowledge of QGIS and raster data analysis is required. Before starting, you have to `install QGIS 3.10 <https://qgis.org/en/site/forusers/download.html>`_ (or higher) on your machine and `create a personal account <https://cds.climate.copernicus.eu/user/login?destination=%2F%23!%2Fhome>`_ to access C3S data. 



.. toctree::
   :maxdepth: 3
   :caption: Table of Contents

   cop_climate
   lcz
   analysis
 
.. Env:
   % . /Users/daniele/opt/anaconda3/bin/activate && conda activate /Users/daniele/opt/anaconda3/envs/sphinx;

.. Path:

.. cd /Users/daniele/Desktop/copernicus_exercise/CA_LCZ_exercise_docs

.. Build HTML:

.. sphinx-build -b html /Users/daniele/Desktop/copernicus_exercise/CA_LCZ_exercise_docs/source /Users/daniele/Desktop/copernicus_exercise/CA_LCZ_exercise_docs/build

.. Build Latext: 

.. sphinx-build -M latexpdf /Users/daniele/Desktop/copernicus_exercise/CA_LCZ_exercise_docs/source /Users/daniele/Desktop/copernicus_exercise/CA_LCZ_exercise_docs/build

.. Git actions:

.. vim .gitignore
.. git status
.. git add .
.. git commit -m"commit comment"
.. git push origin master

.. External links to new panel:

.. add to build/_static/js/theme.js on the same row: $(document).ready(function () {$('a[href^="http://"], a[href^="https://"]').not('a[class*=internal]').attr('target', '_blank');});

 

