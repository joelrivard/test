---
title: "Joining datasets"
weight: 60
---

## Spatial join


A spatial join will merge attribute information from two shapefiles into one based on its location. In this case, we’ll merge the information from the city directory points to our digitized buildings polygon file. 

![Join](http://drive.google.com/uc?export=view&id=16ugG-cj5qnv9DrYDdn7fTFSOgTswiyw7)

![City Directory](http://drive.google.com/uc?export=view&id=1Ai2cxqBdUrIOma6ECMWDjbAefp8wB057)

![Buildings](http://drive.google.com/uc?export=view&id=1xs4HnboXn8wZOqRK8hPm7INIo-Rjb8vI)

These are images, not animated gifs. They are here to show the original and output tables.

In QGIS, open the Spatial Join tool from the MMQGIS menu.

![Start spatial join](http://drive.google.com/uc?export=view&id=1yXW55w3ANO0wL6yGbVssbF6KEfbltXwP)

Select buildings at the output shape and the city directory as the Join Layer. This will merge the attribute information from the city directory to the buildings polygone file.

![Run spatial join](http://drive.google.com/uc?export=view&id=1f4pApLr4q-JtF5a27KYrOEHqaldG-Lgo)