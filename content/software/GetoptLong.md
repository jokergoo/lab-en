---
title: GetoptLong
---




Command-line argument parser.

### Basic

<div id="soft-info">

软件包 | 链接 
:------ | :----------
Language | R, Perl
CRAN | https://cran.r-project.org/package=GetoptLong
GitHub | https://github.com/jokergoo/GetoptLong
Documentation | https://jokergoo.github.io/GetoptLong/

</div>


### Example

Add in the beginning of the R script:

```r
library(GetoptLong)

cutoff = 0.05
GetoptLong(
    "number=i", "Number of items.",
    "cutoff=f", "Cutoff for filtering results.",
    "verbose!", "Print message."
)
```

then in the command-line mode, arguments in the following formats can be called:

```
~\> Rscript foo.R --number 4 --cutoff 0.01 --verbose
~\> Rscript foo.R --number=4 --cutoff=0.01 --no-verbose
~\> Rscript foo.R -n 4 -c 0.01 -v
~\> Rscript foo.R -n 4 --verbose
```

Help messages are automatically generated.

```
~\> Rscript foo.R --help 
Usage: Rscript foo.R [options]

Options:
  --number, -n integer
    Number of items.
 
  --cutoff, -c numeric
    Cutoff for filtering results.
    [default: 0.05]
 
  --verbose
    Print message.
 
  --help, -h
    Print help message and exit.
 
  --version
    Print version information and exit.
```

GetoptLong also implements simple variable interpolation.


``` r
library(GetoptLong)
r = c(1, 2)
value = 4
name = "name"
qq("region = (@{r[1]}, @{r[2]}), value = @{value}, name = '@{name}'")
```

```
## [1] "region = (1, 2), value = 4, name = 'name'"
```

<script>
$( function() {
    $("table thead").css("display", "none");
} );
</script>

