# EvoCell 2021

## Introduction

This course covers the installation and use of SAMAP for single-cell cross-species alignment. In addition, some introductory materials for the 2019 course are also saved here. These introductory materials come from [Casey Dunn](http://dunnlab.org), [Cat Munro](http://www.catrionamunro.science/), Francesco Lamanna, Jonathan Landry, and Jacob Musser.

## Installation of SAMap

### Manual Installation in Conda Environment

A) If you don't already have Anaconda or Miniconda installed, download Miniconda here: [Miniconda](https://docs.conda.io/en/latest/miniconda.html)

B) Download SAMap github directory: [SAMap Github](https://github.com/atarashansky/SAMap)

- click "Code#, then "Download ZIP#, save zip file to an easy-to-remember location
- unzip directory

C) In Mac/Linux, open a Terminal Window. In Windows click on start and open "Anaconda Prompt (miniconda)#. Then, change directory to the SAMap github directory that you just saved and unzipped.

D) Create a new conda environment for installing SAMap using the following command:
``` conda create -n SAMap2 -c conda-forge python=3.7 pip pybind11 h5py=2.10.0 leidenalg python-
 igraph texttable jupyterlab=1.2.0
 ```
 
E) Activate the new conda environment: `conda activate SAMap`
 
F) Install SAMap with the command `pip install .`

G) Open the jupyter lab notebook with the command `jupyter lab`


### Installing SAM GUI

A) Install additional python libraries:
```
conda install -c conda-forge -c plotly ipywidgets plotly=4.0.0 colorlover ipyevents```

B) For using SAM GUI in jupyterlab (vs. the classic jupyter notebook), there is one more installation step:
```conda install nodejs```

C) Enable ipythonwidgets in Jupyter Lab:
```
jupyter labextension install @jupyter-widgets/jupyterlab-manager@1.0 --no-build
jupyter labextension install plotlywidget@1.1.0 --no-build
jupyter labextension install jupyterlab-plotly@1.1.0 --no-build
jupyter lab build
```
