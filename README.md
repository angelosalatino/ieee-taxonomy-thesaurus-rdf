# IEEE Taxonomy-Thesaurus RDF

In this GitHub repository, you will find the RDF version of the IEEE Thesaurus and the Python code we have developed to convert it into RDF from CSV.

[![Python 3.6+](https://img.shields.io/badge/python-3.6+-blue.svg)](https://www.python.org/downloads/release/python-360/)
[![License: MIT](https://img.shields.io/badge/License-MIT-yellow.svg)](https://opensource.org/licenses/MIT)


## Folders
Here is the description of the various folders.

### source
This folder contains the original PDF files of the IEEE Taxonomy and Thesaurus, and the CSV file of IEEE Thesaurus.

### code
This folder contains the Python script that converts the CSV file of the IEEE Thesaurus PDF file (in the source folder) and the corresponding RDF (in the rdf folder).

### rdf
This folder contains the serialized versions of the IEEE Thesaurus in RDF. The serialized versions available are in *ttl*, *nt*, *xml*, and *jsonld*.


## Procedure
First, we extracted the list of topics and their hierarchy from the PDF file, cleaned them manually (see source folder), and saved them as CSV file.

Then, we developed the ```extract_ieee_thesaurus-rdf.ipynb``` that reads the IEEE Thesaurus CSV file and creates the serialized RDF versions.

## Note
We analyzed that ```concepts``` in the IEEE Taxonomy are a subset of ```concepts``` in the IEEE Thesaurus and We decided to remove the IEEE Taxonomy from the repository. But, the PDF files of IEEE Taxonomy are still available in the repository (2022 onwards).

## Extraction of IEEE Taxonomy RDF file

The ```Creating RDF``` section of the ```extract_ieee_thesaurus-rdf.ipynb``` holds the following predicates along with their ```SKOS``` notations:

| Predicate   | SKOS Notation |
| ----------- | -----------   |
| BT          | broader       |
| NT          | narrower      |
| RT          | related       |
| USE         | prefLabel     |
| UF          | altLabel      |

In order to generate the RDF file of IEEE Taxonomy using this code you can just eliminate the predicates ```RT```, ```USE```, ```UF``` because IEEE Taxonomy only holds ```broader``` and ```narrower``` relations.

## Developers
This work has been developed by Alessia Pisu<sup>1</sup>, Tanay Aggarwal<sup>2</sup>, and Angelo Salatino<sup>2</sup>
<br>
<br>
University of Cagliari<sup>1</sup> 
<br>
The Open University<sup>2</sup>
