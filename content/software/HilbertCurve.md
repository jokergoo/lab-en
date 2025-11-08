---
title: HilbertCurve
---




Visualize genomic data using [Hilbert Curve](https://en.wikipedia.org/wiki/Hilbert_curve).

### Basic

<div id="soft-info">

软件包 | 链接 
:------ | :----------
Language | R
Bioconductor | https://bioconductor.org/packages/HilbertCurve/ 
GitHub | https://github.com/jokergoo/HilbertCurve
Documentation | https://jokergoo.github.io/HilbertCurve/
Publication | Zuguang Gu, et al., [HilbertCurve: an R/Bioconductor package for high-resolution visualization of genomic data](https://doi.org/10.1093/bioinformatics/btw161). _Bioinformatics_ 2016.


</div>

### Example

Distribution of genes on human chromosome 1.


``` r
library(GenomicRanges)
library(HilbertCurve)
library(circlize)
load(system.file("extdata", "refseq_chr1.RData", package = "HilbertCurve"))
hc = GenomicHilbertCurve(chr = "chr1", level = 5, reference = TRUE, 
    reference_gp = gpar(lty = 1, col = "grey"), arrow = FALSE)
hc_segments(hc, g, gp = gpar(lwd = 6, col = rand_color(length(g))))
```

<img src="/lab-en/software/HilbertCurve_files/figure-html/unnamed-chunk-2-1.png" width="768" />


<script>
$( function() {
    $("table thead").css("display", "none");
} );
</script>

