# hCNV Data

This page serves to collect information about CNV data collections maintained
(or with involvement) by members of the hCNV community.

Please add your resources!

--------------------------------------------------------------------------------

## xxxxxx

### Resource description

...

### Online access

* resource website: []()
* documentation: []()

### Data content

...

### Data accessibility

* access restrictions: 
* License: ...

### Beacon status and steps needed for adoption

* Planned?
* Restrictions?

--------------------------------------------------------------------------------

## BANCCO

### Resource description

BANCCO is the French national database of Constitutional CNVs. This resource has been developed to identify CNVs (Copy Number Variation) resulting from clinical diagnosis.
The aim of this database is to collect phenotypic data from each patient as well as genotypic data to facilitate the interpretation of CNV in the first instance and to allow the identification of new genes involved in specific diseases.

BANCCO was supported by the Fondation pour la Recherche Médicale and the funding has been extended throug a new grant from the ANR (Agence Nationale de la Recherche)
It is developed within the framework of the "National NGS / ACPA database" project led by Prof. Damien Sanlaville with the participation of the Poitiers University Hospital (Dr. Frédéric Bilan), the University of Aix Marseille (Prof. Christophe Béroud) and the AChro-Puce network.


### Online access

* resource website: [bancco.fr](https://bancco.fr)
* documentation: []()

### Data content

Cuurently BANCCO collects CNV data identified through the network of diagnostic laboratories. As of March 2022, the database contains about 34,120 CNVs, 15,815 deletions and 18,266 duplications. These CNVs have been detected in more than 22,660 patients.

### Data accessibility

* access restrictions: Data access is restricted to french diagnostic laboratories.
* License: ...

### Beacon status and steps needed for adoption

* Planned?
  - We would like to implement BEACON v2 data standard to allow the discovery of CNVs reported in the BANCCO system. 
* Restrictions
  - We are planning to have 2 level of accessibility:
    - public to allow data discovery, observability and matchmaking purposes
    - registered to access more detailled information about specific CNVs  

--------------------------------------------------------------------------------

## Progenetix

### Resource description

The Progenetix resource is centered around our collection of >130'000 CNV profiles
from cancer related genomic profiling experiments - mostly from re-processing  of 
genomic arrays from resources sucgh as NCBI GEO, but including text-based CNV profiling data
e.g. from chromosomal CGH or NGS based studies.

Technically, Progenetix employs a custom implementation of the Beacon API on top
of a MongoDB backend.

### Online access

* resource website: [progenetix.org](http://progenetix.org)
* documentation: [docs.progenetix.org](http://docs.progenetix.org)
* information & news: [info.progenetix.org](http://info.progenetix.org)

### Data content

* cancer genome profiles and associated biological and technical "metadata"
  - clinical core data set where available (age, sex, follow-up status ...)
  - diagnostic & other data mapped to ontologies & standard classification systems
    * NCIT for cancer codes, TNM ...
    * EFO for platforms ...
    * UBERON, cellosaurus, PMID ...
* supporting data & services (publication collection, ontology data, geographic information)

### Data accessibility

* Access restrictions: open, no access-protected data
* License: CC-BY 4.0

### Technical platforms

* MongoDB backend (`variants`, `callsets`, `biosamples`, `individuals`, supporting collections)
* custom Python-based server and data management
  - [`bycon`](http://github.com/progenetix/bycon) for server & libraries
  - [`byconeer`](http://github.com/progenetix/byconeer) for utility apps & scripts - very procedural ...
* Apache

### Beacon status and steps needed for adoption

* full implementation of Beacon v2 protocol (including prototypes)
