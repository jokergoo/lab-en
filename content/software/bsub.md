---
title: bsub
---




Send R code to LSF clusters.

### Basic

<div id="soft-info">

软件包 | 链接 
:------ | :----------
Language | R
CRAN | https://CRAN.R-project.org/package=bsub
GitHub | https://github.com/jokergoo/bsub
Documentation | https://jokergoo.github.io/bsub/

</div>

### Example


```r
library(bsub)

# R code
bsub_chunk(name = "example", memory = 10, hours = 10, cores = 4, 
{
    fit = NMF::nmf(...)
    saveRDS(fit, file = "/path/of/fit.rds")
})
```


<script>
$( function() {
    $("table thead").css("display", "none");
} );
</script>

