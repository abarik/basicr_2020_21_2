--- 
title: "Basic R"
author: "Kálmán Abari"
date: "Last updated: 2021-03-31"
site: bookdown::bookdown_site
output: bookdown::gitbook
documentclass: book
bibliography: [book.bib, packages.bib]
biblio-style: apalike
link-citations: yes
github-repo: abarik/basicr_2020_21_2
description: "Course materials for Basic R"
---

# Preface {-}

As a researcher we need to know how to work with data. One of the best ways to do that is with R. R is a free and an open source language that was specifically developed for reading, manipulating, analysing data and publishing results. In this book, we'll take a look at how we can get started with R. This is an introductory book, so you don't need to have experience with R or with computer programming.

In order to start work with R, you need to install the *Base R* and *RStudio*. 


## Setup Instructions {-}

The first step to working with R is to actually get *Basic R* on your computer. This is easy and it's free. The most common way by far to work with R is within a desktop application called *RStudio*. Like *Basic R*, this is free and it's open source and available for multiple platforms. *Basic R* is the underlying statistical computing environment, but using R alone is no
fun. *RStudio* is a graphical integrated development environment (IDE) that makes
using R much easier and more interactive. You need to install *Basic R* before you
install *RStudio*. 

### Windows {-}

* Download R from
  the [CRAN website](http://cran.r-project.org/bin/windows/base/release.htm).
* Run the `.exe` file that was just downloaded
* Go to the [RStudio download page](https://www.rstudio.com/products/rstudio/download/#download)
* Under *Installers* select **RStudio x.yy.zzz - Windows
  XP/Vista/7/8** (where x, y, and z represent version numbers)
* Double click the file to install it
* Once it's installed, open RStudio to make sure it works and you don't get any
  error messages.

### macOS {-}

* Download R from
  the [CRAN website](http://cran.r-project.org/bin/macosx).
* Select the `.pkg` file for the latest R version
* Double click on the downloaded file to install R
* Go to the [RStudio download page](https://www.rstudio.com/products/rstudio/download/#download)
* Under *Installers* select **RStudio x.yy.zzz - Mac OS X 10.6+ (64-bit)**
  (where x, y, and z represent version numbers)
* Double click the file to install RStudio
* Once it's installed, open RStudio to make sure it works and you don't get any
  error messages.

### Linux {-}

* Follow the instructions for your distribution
  from [CRAN](https://cloud.r-project.org/bin/linux), they provide information
  to get the most recent version of R for common distributions. For most
  distributions, you could use your package manager (e.g., for Debian/Ubuntu run
  `sudo apt-get install r-base`, and for Fedora `sudo yum install R`), but we
  don't recommend this approach as the versions provided by this are
  usually out of date. In any case, make sure you have at least R 4.0.0.
* Go to the
  [RStudio download page](https://www.rstudio.com/products/rstudio/download/#download)
* Under *Installers* select the version that matches your distribution, and
  install it with your preferred method (e.g., with Debian/Ubuntu `sudo dpkg -i
  rstudio-x.yy.zzz-amd64.deb` at the terminal).
* Once it's installed, open RStudio to make sure it works and you don't get any
  error messages.





