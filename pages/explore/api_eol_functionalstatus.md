---
title: Functional Status Atomic Unit
keywords: usecase, questionnaire, response, preferences
tags: [rest, fhir, workflow,api]
sidebar: foundations_sidebar
permalink: api_eol_functionalstatus.html
summary: Questionnaire Response to capture the functional status of a patient using established scales where available.
toc: false
---
{% include custom/search.warnbanner.html %}

{% include custom/under.construction.html %}

### Functional Status ###

The patient’s functional status is recorded by clinicians during encounters with the patient and gives consumers of the data a general indication of the wellness of the patient. The status can be codified using either the Karnofsky scale or Electronic Frailty Index and there is a mandatory textual field for systems that do not store this data as a codeable concept.

The following FHIR profiles are used to form the Functional Status Atomic Unit:

- [EOL-Patient-1](https://fhir-test.nhs.uk/STU3/StructureDefinition/EOL-Patient-1)
- [CareConnect-Organization-1](https://fhir.hl7.org.uk/STU3/StructureDefinition/CareConnect-Organization-1)
- [CareConnect-Practitioner-1](https://fhir.hl7.org.uk/STU3/StructureDefinition/CareConnect-Practitioner-1)
- [CareConnect-PractitionerRole-1](https://fhir.hl7.org.uk/STU3/StructureDefinition/CareConnect-PractitionerRole-1)
- [EOL-FunctionalStatus-QuestionnaireResponse-1](https://fhir.nhs.uk/STU3/StructureDefinition/EOL-FunctionalStatus-QuestionnaireResponse-1)

### Functional Status event data item mapping to FHIR profiles ###

The Functional Status data items are fulfilled by elements within the FHIR resources listed below:

| EOL Data Item                       | FHIR resource element                                                   | Mandatory/Required/Optional |
|-----------------------------------|-------------------------------------------------------------------------|-----------------------------|
| Functional Status Type			| EOL-FunctionalStatus-QuestionnaireResponse-1.item.text.functionalStatusType | Optional |
| Functional Status Value			| EOL-FunctionalStatus-QuestionnaireResponse-1.item.valueCoding.functionalStatusValue | Optional |
| Functional Satus Text				| EOL-FunctionalStatus-QuestionnaireResponse-1.item.text.functionalStatusText | Mandatory |

### Functional Status ERD ###

TODO

### Example XML ###

<script src="https://gist.github.com/IOPS-DEV/d99075703df69b8ad5ec6233dbda2caf.js"></script>


