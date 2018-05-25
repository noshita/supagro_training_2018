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

Activate the *openalea* environment (do not type 'source' on windows):

    [source] activate openalea


Install the different packages

    conda install -c openalea openalea.mtg alinea.caribu notebook matplotlib pandas

    conda install -c openalea -c conda-forge pvlib-python alinea.astk


### Windows: fix for Caribu

Unzip [this archive](./mingw_dll.zip) to C:\MinGW_dll.

Add MinGW_dll in the PATH (search for path in the command bar / choose Modifier les variables d'environnement /
  Variables d'environnement / PATH):
  
..;C:\MinGW_dll

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


