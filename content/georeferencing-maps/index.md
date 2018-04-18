---
title: "Georeferencing maps"
weight: 30
---

## Overview

Existing maps, floorplans and imagery are a useful source of data. They can provide information about changes over time, landcover, settlement patterns, and more. 

Georeferencing is the process of assigning real-world coordinates to each pixel of the raster. To do this, we’ll use the Ottawa roads file that we downloaded from the Ottawa open data website.


### Data files
* [1901 Fire Insurance Plan of Ottawa](https://drive.google.com/open?id=1JITpaNCJqIFHrd1aKkMq6IV2OUC3bEuy). Each person has been assigned a page of the 1901 Fire Insurance Plan of Ottawa.
* [Ottawa roads vector shapefile](https://drive.google.com/open?id=1JITpaNCJqIFHrd1aKkMq6IV2OUC3bEuy)

Download these files to a folder on your computer before proceeding. 

## Adding reference data

We will use modern road data to guide us as we align our fire insurance plan. Open QGIS and load the OttawaRoads.shp file found within your OttawaRoads directory by clicking ```Layer > Add Layer > Add Vector Layer```.

![Add vector layer](http://drive.google.com/uc?export=view&id=1k6BWGyDnjRkNtVz5s7NISK0Fx5TdHVWv)

## Checking the coordinate system

Check which real-world coordinate system is used for the Ottawa roads shapefile. You’ll notice that the coordinate system is set to [epsg: 4326](http://spatialreference.org/ref/epsg/4326/).

![Check coordinate system](http://drive.google.com/uc?export=view&id=1dV0yBoeuRU8wx91y4wNygmq6MqtfgO9b)

## Changing the appearance of the road data

In order to better see the roads and orient ourselves, we'll change the colour of the road layer.

![Change colour](http://drive.google.com/uc?export=view&id=16gjYLLl4z6XzJ4XZqe2DkFoBDT4DQvQ7)

Then, we'll add labels to identify the street names.

![Add labels](http://drive.google.com/uc?export=view&id=10iXtLXQZeE4oDDAMaRyBUHTZvf31zVF6)

## Adding the Georeferencer GDAL plug-in

To do the georeferencing, we’ll need to add the Georeferencer GDAL plug-in to QGIS. 

![Add GDAL plug-in](http://drive.google.com/uc?export=view&id=18iDKdghtqlukP5bKBpDhsIckD_62JDb-)

Once the plug-in has been added, we can open the Georeferencer tool and the fire insurance plan raster file.

![Open Georeferencer tool](http://drive.google.com/uc?export=view&id=1nISIqkfUGIiuoaotvE7fD10zY2spNRR7)

## Configuring the raster settings

Before moving forward, we’ll have to set the proper raster settings for our raster. In some cases, a scanned map may have been created in a particular coordinate system. This is where we would put the information. In our case, the Fire Insurance Plan doesn’t have a known coordinate system. Let’s just set it to the generic WGS84. 

![Change raster settings](http://drive.google.com/uc?export=view&id=1tshsgoX9anoRGYTUuCyP12gzZTnrlIPW)

## Adding control points

We’ll add control points to perform our georeferencing. Control points will be used to assign known coordinates to our raster. In this case, we’ll add control points to all of the intersections of our fire insurance plans.

![Add control points](http://drive.google.com/uc?export=view&id=1P8rNCX8DWIIMRfVVtsatBORKhG7XPQzt)

## Transformation settings

Once we’ve added our points, we’ll set the transformation settings. We set the target SRS to match our reference data (epsg:2951, it matches our Ottawa roads) and check off Use 0 for transparency when needed to ensure that our output image is transparent. Also, selecting  Load in QGIS when done will automatically add the image to QGIS once the georeferencing is complete.

![Transformation settings](http://drive.google.com/uc?export=view&id=1Tr5m0VEKm9uNR5npuQvITpZHUWRJgCUR)

## Running the georeferencing tool

The last step consists of running the georeferencing tool and viewing our output in QGIS. 

![Run georeferencing tool](http://drive.google.com/uc?export=view&id=1nt8I3RsgksV_GqE0kbOOgG7lwdCjj-VY)

