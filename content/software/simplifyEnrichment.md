---
title: simplifyEnrichment
---




Simplify the Gene Ontology enrichment results.

### Basic

<div id="soft-info">

软件包 | 链接 
:------ | :----------
Language | R
Bioconductor | https://bioconductor.org/packages/simplifyEnrichment/ 
GitHub | https://github.com/jokergoo/simplifyEnrichment
Documentation | https://jokergoo.github.io/simplifyEnrichment/
Publication | Zuguang Gu, et al., [simplifyEnrichment: A Bioconductor Package for Clustering and Visualizing Functional Enrichment Results](https://doi.org/10.1016/j.gpb.2022.04.008). _Genomics, Proteomics & Bioinformatics_ 2023.


</div>

### Example


``` r
library(simplifyEnrichment)
set.seed(888)
go_id = random_GO(500)
simplifyGO(go_id)
```

<img src="/lab-en/software/simplifyEnrichment_files/figure-html/unnamed-chunk-2-1.png" width="816" />


<script>
$( function() {
    $("table thead").css("display", "none");
} );
</script>
