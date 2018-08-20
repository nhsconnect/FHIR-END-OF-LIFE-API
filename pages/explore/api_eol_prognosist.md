---
title: Prognosis Atomic Unit
keywords: usecase, clinial impression, prognosis
tags: [rest, fhir, workflow,api]
sidebar: foundations_sidebar
permalink: api_eol_prognosis.html
summary: Atomic Unit to capture the prognosis for a patient.
toc: false
---
{% include custom/search.warnbanner.html %}

### consent ###


The following FHIR profiles are used to form the prognosis Atomic Unit:

- [CareConnect-EOL-Patient-1](https://fhir.nhs.uk/STU3/StructureDefinition/CareConnect-EOL-Patient-1.xml)

### Prognosis data item mapping to FHIR profiles ###

The prognosis data items are fulfilled by elements within the FHIR resources listed below:

| DCH Data Item                       | FHIR resource element                                                   | Mandatory/Required/Optional |
|-------------------------------------|-------------------------------------------------------------------------|-----------------------------|
| Prognosis Coded        		       | EOL-ClinicalImpression-Prognosis-1.prognosisCodeableConcept          | Optional                   |
| Prognosis Textual | EOL-ClinicalImpression-Prognosis-1.prognosisCodeableConcept.text    | Mandatory |
| Date of Prognosis | EOL-ClinicalImpression-Prognosis-1.date    |Optional |
| Awareness of Prognosis | EOL-ClinicalImpression-Prognosis-1.awrenessOfPrognosis (Extension) | Optional |
| Professional Recording Prognosis | EOL-ClinicalImpression-Prognosis-1.assessor | Mandatory |


### Prognosis ERD ###

<img src="images/erd/erd-prognosis.svg" style="width:80%;max-width: 80%;">

### Prognosis Example XML ###

<script src="https://gist.github.com/IOPS-DEV/22c1c28de21a1c341deff1145d113de0.js"></script>



