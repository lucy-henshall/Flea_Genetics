---
layout: page
title: 3D FCA plot
visible: true
author: "Lucy Henshall"
date: "2023-05-09"
output: html_document
---

```{r setup, include=FALSE}
options(rgl.use.NULL = TRUE)
rgl::setupKnitr(autoprint = TRUE)
library(rgl)
```

## FCA Plots relating to Lucy Henshall's Poster at EEID 2023

The following plot is an interactive plot showing the first three axes of the correspondence analysis 

```{r echo = FALSE}
scores2 <- read.csv("Genetics/Population_RR_ACTUALLYallsites_forFCAplotting.csv", header = T, row.names = 1, stringsAsFactors = T)

plot3d(scores2[,1:3],
        size = 15,
        col = scores2$Colour, xlab = "25.50%", ylab = "11.17%", zlab = "7.21%")
text3d(scores2[,1:3],
        texts= row.names(scores2), 
        cex= 0.8, pos=3) 
```

Rendered site: https://lucy-henshall.github.io/FCA
