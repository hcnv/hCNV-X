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
