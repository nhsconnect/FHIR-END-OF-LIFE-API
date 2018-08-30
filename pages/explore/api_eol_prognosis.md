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

{% include custom/under.construction.html %}

### Consent ###


The following FHIR profiles are used to form the prognosis Atomic Unit:

- [EOL-Patient-1](https://fhir.nhs.uk/STU3/StructureDefinition/EOL-Patient-1)
- [EOL-Prognosis-ClinicalImpression-1](https://fhir.nhs.uk/STU3/StructureDefinition/EOL-Prognosis-ClinicalImpression-1)

### Prognosis data item mapping to FHIR profiles ###

The prognosis data items are fulfilled by elements within the FHIR resources listed below:

| EOL Data Item                       | FHIR resource element                                                   | Mandatory/Required/Optional |
|-------------------------------------|-------------------------------------------------------------------------|-----------------------------|
| Prognosis Coded        		       | EOL-ClinicalImpression-Prognosis-1.prognosisCodeableConcept          | Optional                   |
| Prognosis Textual | EOL-ClinicalImpression-Prognosis-1.prognosisCodeableConcept.text    | Mandatory |
| Date of Prognosis | EOL-ClinicalImpression-Prognosis-1.date    |Optional |
| Awareness of Prognosis | EOL-ClinicalImpression-Prognosis-1.awrenessOfPrognosis (Extension) | Optional |
| Professional Recording Prognosis | EOL-ClinicalImpression-Prognosis-1.assessor | Mandatory |


### Prognosis Example XML ###

<script src="https://gist.github.com/IOPS-DEV/22c1c28de21a1c341deff1145d113de0.js"></script>



