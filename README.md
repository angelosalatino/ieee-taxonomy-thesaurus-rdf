# IEEE Taxonomy RDF

In this GitHub repo you will find the rdf version of the IEEE Taxonomy as well as the Python code we have developed to convert it.

[![Python 3.6+](https://img.shields.io/badge/python-3.6+-blue.svg)](https://www.python.org/downloads/release/python-360/)
[![License: MIT](https://img.shields.io/badge/License-MIT-yellow.svg)](https://opensource.org/licenses/MIT)


## Folders
Here follows the description of the various folders.

### source
This folder contains the original files of the IEEE Taxonomy, both the PDF and extracted txt file.

### code
This folder contains the python script that converts the txt file (in source) and created the serialised versions (in rdf folder).

### rdf
This folder contains the serialised versions of the IEEE Taxonomy in RDF. The serialised versions available are in *ttl*, *nt*, *xml*, and *jsonld*.


## Procedure
First, we manually extracted the list of topics and their hierarchy from the pdf (see source folder) and saved in a txt file.

Then, we developed the ```extract_ieee_taxonomy-rdf.ipynb``` that reads the txt file and creates the serialised RDF versions.

## Developers

This work has been developed by Tanay Aggarwal (MSIT, Guru Gobind Singh Indraprastha University) and Angelo Salatino (KMi, The Open University).
