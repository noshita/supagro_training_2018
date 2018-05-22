# Installation of OpenAlea environment and R

## Installation of OpenAlea

### Conda Installation

[Conda](https://conda.io) is a package manager that can be installed on Linux, Windows, and Mac.
If you have not yet installed conda on your computer, follow these instructions:

[Conda Installation](https://conda.io/docs/user-guide/install/index.html). Follow instructions for Miniconda.

[Conda Download](https://conda.io/miniconda.html). Use the Python 2.7 based installation.

#### Windows, Linux, Mac

Create an environment named *openalea*:

    conda create -n openalea -c openalea openalea.plantgl boost=1.66

Activate the *openalea* environment:

    [source] activate openalea


Install the different packages

    conda install -c openalea openalea.mtg alinea.caribu notebook matplotlib pandas

    conda install -c openalea -c conda-forge pvlib-python alinea.astk


### WINDOWS: Fix for MinGW and Caribu

From the key, install MinGW (C:\MinGW)

Add MinGW in the PATH (either in the console or on the computer (environment variables)):
set PATH=C:\MinGW\bin;%PATH%

Launch a console (cmd.exe) and activate openalea:
    
    activate openalea
    
Test if caribu is working:

    canestrad -h


## Installation of R & co

You can install everything by yourself, or using the r channel in conda.

With **conda**:

### Install RStudio, Rmarkdown


    [source] deactivate
    conda create -n renv -c r rstudio r-rmarkdown r-car r-lme4
    
    [source] activate renv
    

### Install R packages
* PerformanceAnalytics
* lme4
* car
* agricolae
* sensitivity
* lhs
* planor

Under **R**, you can install everything using:
    
    install.packages(c('PerformanceAnalytics','agricolae','sensitivity','lhs','planor') )


