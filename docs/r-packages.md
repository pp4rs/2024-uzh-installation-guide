# Additional R Packages

We will need some additional libraries to conduct our statistical analysis.

## All Users

Proceed as follows:

* Open RStudio
* In the **console**, copy and paste the following:

```r
to_install <-c( "sandwich", "knitr",
                "tidyverse", "lmtest",
                "fixest", "lubridate", 
                "dplyr"
                )

install.packages(to_install)
```

* If you are asked if you want to install packages that need compilation, type `y` followed by `Return` to confirm this.
* Wait until all the packages have been installed and the you are done.
  * It *may* take a while, so be patient

Note that many dependencies get installed along the way.