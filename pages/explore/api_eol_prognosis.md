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

### Prognosis ###

At any encounter with the patient, the professional offering care may re-assess the overarching life expectancy (prognosis) of the patient.  This prognosis is immensely useful to urgent and emergency care in helping them to decide the best course of action for the patient.
Across England, there is not yet a standard in place for commonly SNOMED-coding the prognosis.  The ambition of all respondents was to standardise the SNOMED-coded part of the dataset to the four GSF values, however they all accepted that some localities were not using those values.  Therefore, the prognosis (coded) data item allows for a wider selection of SNOMED codes to be transmitted.  Additionally, the prognosis (textual) has been provided so that providers without any coding can still transmit the value in text.


The following FHIR profiles are used to form the prognosis Atomic Unit:

- [EOL-Patient-1](https://fhir.nhs.uk/STU3/StructureDefinition/EOL-Patient-1)
- [CareConnect-Organization-1](https://fhir.hl7.org.uk/STU3/StructureDefinition/CareConnect-Organization-1)
- [CareConnect-Practitioner-1](https://fhir.hl7.org.uk/STU3/StructureDefinition/CareConnect-Practitioner-1) (EOL mandates name.text)
- [CareConnect-PractitionerRole-1](https://fhir.hl7.org.uk/STU3/StructureDefinition/CareConnect-PractitionerRole-1)
- [EOL-Prognosis-ClinicalImpression-1](https://fhir.nhs.uk/STU3/StructureDefinition/EOL-Prognosis-ClinicalImpression-1)

### Prognosis data item mapping to FHIR profiles ###

The prognosis data items are fulfilled by elements within the FHIR resources listed below:

| EOL Data Item                       | FHIR resource element                                                   | Mandatory/Required/Optional |
|-------------------------------------|-------------------------------------------------------------------------|-----------------------------|
| Prognosis Coded        		       | EOL-ClinicalImpression-Prognosis-1.prognosisCodeableConcept          | Optional                   |
| Prognosis Textual | EOL-Prognosis-ClinicalImpression-1.prognosisCodeableConcept.text    | Mandatory |
| Date of Prognosis | EOL-Prognosis-ClinicalImpression-1.date    |Optional |
| Awareness of Prognosis | EOL-Prognosis-ClinicalImpression-1-1.awrenessOfPrognosis (Extension) | Optional |
| Professional Recording Prognosis | EOL-Prognosis-ClinicalImpression-1.assessor | Mandatory |

### Prognosis Example XML ###

<script src="https://gist.github.com/IOPS-DEV/22c1c28de21a1c341deff1145d113de0.js"></script>



