---
title: "Geocoding spreadsheets"
weight: 50
---

## Overview

Geographic clues can be hidden in all kinds of documents. In this exercise, we'll collect addresses from the 1890-1891 Ottawa Directory. Library and Archives Canada has digitized [95 microfiche versions of pre-1901 Canadian directories](http://www.bac-lac.gc.ca/eng/discover/directories-collection/Pages/directories-collection.aspx). These are useful resources for researching where people and businesses were located (and the ads are pretty cool too). The following exercise will require a Google account.

![Image of directories](/images/directory.jpg)

### Data files
* [Google Sheet with template](https://docs.google.com/spreadsheets/d/1ClP7IUjAIs50CLtJxRpy8zwd2PDYy0BmyDBGS8Uf00Q/edit?usp=sharing)
* [PDF of the Ottawa Directory from 1890-1891](http://ssimpkin.github.io/dhsite2017/files/Directory_1890.pdf)


## Installing the geocoder add-on



## Adding data to the table

Make a copy of the [Google Sheets template](https://docs.google.com/spreadsheets/d/1YOba-Bb9S_6Gr68zSujqmbtTF-mPrqSJuUG85aIXzrU/edit?usp=sharing) by clicking ```File > Make a copy```.

Next, open the directory PDF and scroll to page 83. You'll see that I've begun transcribing the information from the buildings along the south side of Lisgar Street onto the spreadsheet, beginning with the intersection at Metcalfe Street.

Each business is given its own line, and each piece of information about the business is given its own column. These columns are known as attributes.

{{< note title="Note" >}}
As you can imagine, modern-day geocoders work best with modern-day address data (we may be pushing it a little). Watch out for renumbered and renamed streets if you attempt this process with historical data. Reference materials such as fire insurance plans can be useful for doing a quality check of historical addresses.
{{< /note >}}

Refer to your assigned FIP sheet to know which portions of the directory will need to be transcribed for your section. Delete the sample data in the first three rows before proceeding to the next step.

## Exporting a CSV file

Export the completed table as a CSV file by clicking ```File > Download as > Comma-separated values (.csv, current sheet)```. Save to your computer.

## Installing the geocoder plug-in

We will use the MMQGIS plug-in to geocode our addresses.

![Add MMQGIS plug-in](http://drive.google.com/uc?export=view&id=1BJthnNboI3zCJOg_LqD1zUVcWxvJ7Fec)

## Set parameters for geocoding

Set parameters for geocoding, assigning the correct fields to each part of the address (street, city, state/province, country, etc.) and choose a web service. 

![Set parameters](http://drive.google.com/uc?export=view&id=1yxMQC92VUW26LXDYM0CFO9K8ZeML1hCi)

In this case, we’ll choose OpenStreetMap. If you were to choose Google Maps, you’d have to assign a [Google Maps API key](https://console.developers.google.com/apis/api/maps_backend/overview). Using either of these services will save our output shapefile with the epsg:4326 coordinate system.

## Start geocoding

Click OK to begin the geocoding process.

![Start geocoding](http://drive.google.com/uc?export=view&id=18aOeEMYX2pXeNLgxiZpGBZeubZZ0UgCQ)


You'll see that points have appeared along the streets (hopefully near your assigned area). The geocoder took a look at the street addresses and made a best guess about where they might go, based on modern-day data. 

Features for which there was a geocoding match (based on contemporary data) will be added to the map as points, with precision information included as additional columns in the attribute table. Take some time to review the point placement and make any adjustments to the points. 

You can imagine that the buildings and their numbers have likely undergone some major changes since 1890. Fortunately, we can import a reference image to help us quality check the point placements.

## Adjustments

Make any adjustments to the address points (sometimes addresses will be in the centres of modern-day buildings). Using the historical map as a reference, we can have a better idea of how each block looked closer to the time the directory was published.

![Make adjustments](http://drive.google.com/uc?export=view&id=1Q1UCFJFjvrKHLkC0dD9f2Ixq4KcXS_LX)

Adjustments to the points can be made using the toggle edit tool and then moving the points to the desired location. 

Once you're happy with the point placement, proceed to the joining datasets step. 
