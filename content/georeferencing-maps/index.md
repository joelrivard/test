---
title: "Georeferencing maps"
weight: 50
---

## Overview

Existing maps, floorplans and imagery are a useful source of data. They can provide information about changes over time, landcover, settlement patterns, and more. 

Georeferencing is the process of assigning real-world coordinates to each pixel of the raster. To do this, we’ll use the Ottawa roads file that we downloaded from the Ottawa open data website.


### Data files
* [1901 Fire Insurance Plan of Ottawa](http://ssimpkin.github.io/dhsite2017/files/georectify/FireInsurancePlan_1901.zip). Each person has been assigned a page of the 1901 Fire Insurance Plan of Ottawa.
* Ottawa roads vector shapefile


## Adding reference data

We will use modern road data to guide us as we align our fire insurance plan. 

## Checking the coordinate system

Check which real-world coordinate system is used for the Ottawa roads shapefile. You’ll notice that the coordinate system is set to [epsg: 2951](http://spatialreference.org/ref/epsg/2951/).

## Changing the appearance of the road data

In order to better see the roads and orient ourselves, we'll change the colour of the road layer and add labels.

## Adding the Georeferencer GDAL plug-in

To do the georeferencing, we’ll need to add the Georeferencer GDAL plug-in to QGIS. Once the plug-in has been added, we can open the Georeferencer tool and the fire insurance plan raster file.

## Configuring the raster settings

Before moving forward, we’ll have to set the proper raster settings for our raster. In some cases, a scanned map may have been created in a particular coordinate system. This is where we would put the information. In our case, the Fire Insurance Plan doesn’t have a known coordinate system. Let’s just set it to the generic WGS84. 

## Adding control points

We’ll add control points to perform our georeferencing. Control points will be used to assign known coordinates to our raster. In this case, we’ll add control points to all of the intersections of our fire insurance plans.

## Transformation settings

Once we’ve added our points, we’ll set the transformation settings. We set the target SRS to match our reference data (epsg:2951, it matches our Ottawa roads) and check off Use 0 for transparency when needed to ensure that our output image is transparent. Also, selecting  Load in QGIS when done will automatically add the image to QGIS once the georeferencing is complete.

## Running the georeferencing tool

The last step consists of running the georeferencing tool and viewing our output in QGIS. 

