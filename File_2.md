<!DOCTYPE html>

<html>

<head>

<meta charset="utf-8" />
<meta name="generator" content="pandoc" />
<meta http-equiv="X-UA-Compatible" content="IE=EDGE" />



<title>FCA Plots relating to Lucy Henshall's Poster at EEID 2023</title> 
        
</div>

        
<div class="sourceCode" id="cb2">```<pre class="sourceCode r"><code class="sourceCode r">></a>{r setup<span class="ot">&lt;-</span>,<span class="fu">include =</span>FALSE<span class="st">

<span id="cb2-2"><a href="#cb2-2" aria-hidden="true" tabindex="-1"></a>                     <span class="at">stringsAsFactors =</span> <span class="cn">TRUE</span>)</span>
<span id="cb2-3"><a href="#cb2-3" aria-hidden="true" tabindex="-1"></a></span>        

```{r setup, include=FALSE}
options(rgl.use.NULL = TRUE)
rgl::setupKnitr(autoprint = TRUE)
library(rgl)
```        

<p> </p>
<p>The following plot is an interactive plot showing the first three axes of the correspondence analysis</p>

```{r echo = FALSE}
scores2 <- read.csv("Genetics/Population_RR_ACTUALLYallsites_forFCAplotting.csv", header = T, row.names = 1, stringsAsFactors = T)

plot3d(scores2[,1:3],
        size = 15,
        col = scores2$Colour, xlab = "25.50%", ylab = "11.17%", zlab = "7.21%")
text3d(scores2[,1:3],
        texts= row.names(scores2), 
        cex= 0.8, pos=3) 
```
