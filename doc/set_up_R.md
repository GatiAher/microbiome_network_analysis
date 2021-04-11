# How To Set Up R On Ubuntu Linux 20.04

## 1. Get R version >= 4.0.3

R is a free software environment for statistical computing and graphics. Download and install the correct version for your operating system by following instructions from [the Comprehensive R Archive Network (CRAN)](https://cran.rstudio.com/).

If R is installed correctly, typing `R` in the terminal should start it.

## 2. Install RStudio

RStudio is an integrated development environment, or IDE, for R programming. Download and install it from [rstudio](http://www.rstudio.com/download).

Then install downloaded package by running:

```bash
# in terminal
sudo apt install ./rstudio-1.4.1106-amd64.deb
```

To run rstudio:

```bash
# in terminal
rstudio
```

## 3. Install tidyverse R Package

The [tidyverse](https://tidyverse.tidyverse.org/) is a set of packages that work in harmony because they share common data representations and API design. The tidyverse package is designed to make it easy to install and load core packages from the tidyverse in a single command.

```R
# Install from CRAN
install.packages("tidyverse")
```

If you run into issue "R ERROR: dependencies ‘xml2’, ‘httr’ are not available for package":

```bash
# in terminal
sudo apt install build-essential libcurl4-gnutls-dev libxml2-dev libssl-dev
```

## 4. Get Bioconductor verison 3.12 (compatible for R version >= 4.0.3)

[Bioconductor](https://www.bioconductor.org/install/) is open source software for bioinformatics.

```R
# To install Bioconductor, start R and enter commands:
if (!requireNamespace("BiocManager", quietly = TRUE))
    install.packages("BiocManager")
BiocManager::install(version = "3.12")
```