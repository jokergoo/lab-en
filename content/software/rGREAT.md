---
title: rGREAT
---




Functional enrichment analysis on genomic regions.

### Basic

<div id="soft-info">

软件包 | 链接 
:------ | :----------
Language | R, C++
Bioconductor | https://bioconductor.org/packages/rGREAT/ 
GitHub | https://github.com/jokergoo/rGREAT
Documentation | https://jokergoo.github.io/rGREAT/
Publication | Zuguang Gu, et al., [rGREAT: an R/bioconductor package for functional enrichment on genomic regions](https://doi.org/10.1093/bioinformatics/btac745). _Bioinformatics_ 2023.



</div>

### Example


``` r
library(rGREAT)
gr = randomRegions(nr = 1000, genome = "hg19")
res = great(gr, "MSigDB:H", "TxDb.Hsapiens.UCSC.hg19.knownGene")
tb = getEnrichmentTable(res)
head(tb)
```

```
##                                           id genome_fraction
## 1            HALLMARK_ESTROGEN_RESPONSE_LATE     0.019761793
## 2                HALLMARK_TGF_BETA_SIGNALING     0.007140288
## 3           HALLMARK_ESTROGEN_RESPONSE_EARLY     0.024463198
## 4                 HALLMARK_PROTEIN_SECRETION     0.009545438
## 5 HALLMARK_EPITHELIAL_MESENCHYMAL_TRANSITION     0.030187448
## 6             HALLMARK_INFLAMMATORY_RESPONSE     0.021400596
##   observed_region_hits fold_enrichment    p_value  p_adjust mean_tss_dist
## 1                   29        1.584750 0.01179918 0.3992542        254762
## 2                   13        1.966150 0.01774463 0.3992542        249538
## 3                   31        1.368477 0.05274030 0.7323745        238970
## 4                   14        1.583876 0.06509996 0.7323745        149002
## 5                   35        1.252076 0.10694419 0.9609538        240512
## 6                   25        1.261546 0.14432481 0.9609538        229830
##   observed_gene_hits gene_set_size fold_enrichment_hyper p_value_hyper
## 1                 25           198              1.633143  0.0103653538
## 2                 11            54              2.634804  0.0024570576
## 3                 26           198              1.698469  0.0054923334
## 4                 13            95              1.769983  0.0308609265
## 5                 31           199              2.014921  0.0001401821
## 6                 23           197              1.510119  0.0310192081
##   p_adjust_hyper
## 1    0.116610230
## 2    0.055283797
## 3    0.082385001
## 4    0.232644061
## 5    0.006308193
## 6    0.232644061
```


<script>
$( function() {
    $("table thead").css("display", "none");
} );
</script>
