---
title: GlobalOptions
---




Setting global options.

### Basic

<div id="soft-info">

软件包 | 链接 
:------ | :----------
Language | R
CRAN | https://cran.r-project.org/package=GlobalOptions
GitHub | https://github.com/jokergoo/GlobalOptions
Documentation | https://jokergoo.github.io/GlobalOptions/

</div>

### Example


``` r
library(GlobalOptions)
opt = set_opt(
    "a" = 1,
    "b" = "text"
)
```

then global options can be get or set via the following ways.

```r
opt()
opt("a")
opt$a
opt[["a"]]
opt(c("a", "b"))
opt("a", "b")
opt("a" = 2)
opt$a = 2
opt("a" = 2, "b" = "new_text")
```



<script>
$( function() {
    $("table thead").css("display", "none");
} );
</script>
