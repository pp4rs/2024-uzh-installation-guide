# Additional R Packages

We will need some additional libraries to conduct our statistical analysis.

## All Users

Proceed as follows:

* Open RStudio
* In the **console**, copy and paste the following:

```r
to_install <-c( "reshape", "rmarkdown",
                "plm", "Hmisc", "sandwich",
                "Ecdat", "knitr",
                "httr", "xml2",
                "xtable","tidyverse", "AER",
                "rdd", "car", "aod", "lmtest",
                "fixest", "nlme", "lme4",
                "multiwayvcov",
                "lubridate", "haven", 
                "ivpack", "readxl",
                "ggrepel",
                "dbplyr", "devtools",
                "rticles", "here",
                "optparse", "rlist"
                )

install.packages(to_install)
```

* If you are asked if you want to install packages that need compilation, type `y` followed by `Return` to confirm this.
* Wait until all the packages have been installed and the you are done.
  * It *may* take a while, so be patient

Note that many dependencies get installed along the way.

We also want some packages to be installed from Github - these typically still under development:

```{r}
from_gh <- c("ddsjoberg/gtsummary",
             "vincentarelbundock/modelsummary",
             "rstudio/fontawesome",
             "rstudio/gt",
             "rstudio/renv"
             )

devtools::install_github(from_gh)
```

!!! warning "Package List May Update"

    This list of packages may be updated during the course.
    There has been a raft of new, easier to use packages for some tools that we will introduce.
    Before we list them here, we want to test them out a little more rigorously.

    Check back here before Week 3 of the course to see if there are changes.