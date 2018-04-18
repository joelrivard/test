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

Make a copy of the [Google Sheets template](https://docs.google.com/spreadsheets/d/1ClP7IUjAIs50CLtJxRpy8zwd2PDYy0BmyDBGS8Uf00Q/edit?usp=sharing) by clicking ```File > Make a copy```.

Next, open the directory PDF and scroll to page 117. You'll see that I've begun transcribing the information from the businesses along the north side of Rideau Street onto the spreadsheet.

Each business is given its own line, and each piece of information about the business is given its own column.

{{< note title="Note" >}}
As you can imagine, modern-day geocoders work best with modern-day address data (we may be pushing it a little). Watch out for renumbered and renamed streets if you attempt this process with historical data. Reference materials such as fire insurance plans can be useful for doing a quality check of historical addresses.
{{< /note >}}


## Exporting a CSV file

Export the completed table as a CSV file by clicking ```File > Download as > Comma-separated values (.csv, current sheet)```. Save to your computer.

## Installing geocoder plug-in



You'll see that points have appeared along Rideau Street. The geocoder took a look at the street addresses and made a best guess about where they might go, based on modern-day data.

You can imagine that the buildings and their numbers have likely undergone some major changes since 1890. Fortunately, we can import a reference image to help us quality check the point placements.

## Opening FIP

Make any adjustments to the address points (sometimes addresses will be in the centres of modern-day buildings). Using the historical map as a reference, we can have a better idea of how each block looked closer to the time the directory was published.

Once you're happy with the point placement, 

export instructions
