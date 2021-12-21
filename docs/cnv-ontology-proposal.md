## CNV Ontology Proposal

This document represents a draft of a basic CNV ontology, which is essential for
a robust implementation of CNV representation and querying in standards such as
e.g. VRS and Beacon.

This document is though for h-CNV community discussion & editing. A mature version
should be incorporated in - preferably - Sequence Ontology but possibly also
[EFO](https://www.ebi.ac.uk/ols/ontologies/efo/terms?short_form=EFO_0004798).

* Gene Ontology [copy number assessment subtree proposal](https://github.com/The-Sequence-Ontology/SO-Ontologies/issues/568)

#### CNV Ontology draft

The entities represented here represent a basic _ad hoc_ hierarchy, based on
common practices. The terms are specifically designed to be "sequence context agnostic",
i.e. avoiding any statement about e.g. genomic placement of duplicated genomic regions
or elements.


```
id: SO:nnnn01
label: copy number assessment
description: root class of the CNV ontology which can become a child of different classes, e.g. referring to structural or to quantitative genome changes
  |
  |-id: SO:nnnn02
  | label: base ploidy
  | description: relative allel count equal to regional base allele count
  |   |
  |   |-id: SO:nnnn04
  |     label: copy-neutral loss of heterozygosity
  |     description: regional loss of heterozygosity w/o change of allele count
  |
  |-id: SO:nnnn03
    label: copy number variation
    description: assertive root class for a copy number change ("CNV")
      |
      |-id: SO:nnnn05
      | label: copy number loss
      | description: copy number reduced compared to regional base allele count
      |   |
      |   |-id: SO:nnnn07
      |   | label: incomplete copy number loss
      |   | description: deletion of fewer alles than the regional base allele count
      |   |
      |   |-id: SO:nnnn08
      |     label: complete genomic deletion
      |     description: deletion of all alleles of the genomic region or element
      |
      |-id: SO:nnnn06
        label: copy number gain
        description: copy number increased compared to regional base allele count
          |
          |-id: SO:nnnn09
          | label: low-level copy number gain
          | description: gain of one or few genomic copies, operationally defined
          |
          |-id: SO:nnnn10
            label: genomic amplification
            description: gain of multiple genomic copies, e.g. more than from a
              simple duplication of the base allele count; operationally defined
```
