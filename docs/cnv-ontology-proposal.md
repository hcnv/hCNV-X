## CNV Ontology Proposal

This document represents a draft of a basic CNV ontology, which is essential for
a robust implementation of CNV representation and querying in standards such as
e.g. VRS and Beacon.

This document is though for h-CNV community discussion & editing. A mature version
should be incorporated in - preferably - Sequence Ontology but possibly also
[EFO](https://www.ebi.ac.uk/ols/ontologies/efo/terms?short_form=EFO_0004798).

* Sequence Ontology [copy number assessment subtree proposal](https://github.com/The-Sequence-Ontology/SO-Ontologies/issues/568)

##### Update 2022-01-18: The subtree has been accepted into EFO and should appear there soon. The tree below has been updated accordingly. 

#### CNV Ontology draft

The entities represented here represent a basic _ad hoc_ hierarchy, based on
common practices. The terms are specifically designed to be "sequence context agnostic",
i.e. avoiding any statement about e.g. genomic placement of duplicated genomic regions
or elements.

Also, while the terms carry an `SO` prefix & "compatible" local part, this is for
drafting purposes only and will have to be provided by the adopting ontology.

```
id: EFO:0030063
label: copy number assessment
  |
  |-id: EFO:0030064
  | label: regional base ploidy
  |   |
  |   |-id: EFO:0030065
  |     label: copy-neutral loss of heterozygosity
  |
  |-id: EFO:0030066
    label: relative copy number variation
      |
      |-id: EFO:0030067
      | label: copy number loss
      |   |
      |   |-id: EFO:0030068
      |   | label: low-level copy number loss
      |   |
      |   |-id: EFO:0030069
      |     label: complete genomic deletion
      |
      |-id: EFO:0030070
        label: copy number gain
          |
          |-id: EFO:0030071
          | label: low-level copy number gain
          |
          |-id: EFO:0030072
             label: high-level copy number gain
             note: commonly but not consistently used for >=5 copies on a bi-allelic genome region
              |
              |-id: EFO:0030073
                 label: focal genome amplification
                 note: >-
                   commonly used for localized multi-copy genome amplification events where the
                   region does not extend >3Mb (varying 1-5Mb) and may exist in a large number of
                   copies
```
