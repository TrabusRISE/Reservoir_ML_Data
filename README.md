# Reservoir_ML_Data

This repository contains datasets used to generate models in the *Near_Term Forecasting of Water Reservoir Storage Capacities Using Long Short-Term Memory* by Eric Rohli, Nicholas Woolsey and David Sathiaraj. 

The data used are available at: [![DOI](https://zenodo.org/badge/DOI/10.5281/zenodo.8032486.svg)](https://doi.org/10.5281/zenodo.8032486)

The data are divided into two folders.

## PRISMdata

The PRISMdata folder contains daily **precipitation** and **average temperature** data over a watershed from 2010-2022. The watersheds are determined using the 8-digit USGS Hydrologic Unit Code. Gridded values come from the [PRISM](https://prism.oregonstate.edu/) dataset, which is made available via the [Applied Climate Informatics Service](https://builder.rcc-acis.org/). The value for the given day is the weighted average of all gridded values that cover the watershed.

Files are identified using the HUC.

## ResDatasets

The ResDatasets folder contains reservoir data for the studied sites. There are two types of files for each site. Each file is identified by **USGS Reservoir ID**.

### EAC Data

These files map **reservoir elevation** to **reservoir storage capacity** and are used to convert between the two units. Values are obtained from the [Texas Water Development Board](https://www.waterdatafortexas.org/reservoirs/statewide)

### Res Data

These files contain daily observed **reservoir storage** and/or **reservoir elevation**. Data come from the [USGS Water Data for the Nation API](https://waterdata.usgs.gov/nwis/uv).

TRABUS has decided to provide all reservoir data for a particular site in a single file. To reproduce our study, split the data sequentially such that data on or prior to December 31, 2020 are used for training and data on or after January 1, 2021 are used for testing. 
