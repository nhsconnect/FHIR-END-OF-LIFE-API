---
title: Advance Treatment Preferences Atomic Unit
keywords: usecase, problemList, problemHeader, CarePlan
tags: [rest, fhir, workflow,api]
sidebar: foundations_sidebar
permalink: api_eol_atp.html
summary: Atomic Unit to capture the advance treatment preferences for a patient.
toc: false
---
{% include custom/search.warnbanner.html %}

### Advance Treatment Preferences ###


The following FHIR profiles are used to form the Advance Treatment Preferences Atomic Unit:

- [CareConnect-EOL-Patient-1](https://fhir.nhs.uk/STU3/StructureDefinition/CareConnect-EOL-Patient-1.xml)
- [CareConnect-Organization-1](https://fhir.hl7.org.uk/STU3/StructureDefinition/CareConnect-Organization-1)
- [CareConnect-Practitioner-1](https://fhir.hl7.org.uk/STU3/StructureDefinition/CareConnect-Practitioner-1)
- [CareConnect-PractitionerRole-1](https://fhir.hl7.org.uk/STU3/StructureDefinition/CareConnect-PractitionerRole-1)
- [CareConnect-EOL-ProblemList-1](https://fhir.nhs.uk/STU3/StructureDefinition/CareConnect-EOL-ProblemList-1.xml)
- [CareConnect-EOL-ProblemHeader-Condition-1](https://fhir.nhs.uk/STU3/StructureDefinition/CareConnect-EOL-ProblemHeader-Condition-1.xml)
- [EOL-CarePlan-1](https://fhir.nhs.uk/STU3/StructureDefinition/EOL-ATP-CarePlan-1.xml)


### Advance Treatment Preferences data item mapping to FHIR profiles ###

The Advance Treatment Preferences data items are fulfilled by elements within the FHIR resources listed below:

| DCH Data Item                       | FHIR resource element                                                   | Mandatory/Required/Optional |
|-------------------------------------|-------------------------------------------------------------------------|-----------------------------|
| Problem or Condition                | CareConnect-EOL-ProblemHeader-Condition.code.text           | Mandatory                   |
| Treatment Level					  | EOL-ATP-CarePlan-1.activity.detail.code.text	| Optional |
| Intervention						  | EOL-ATP-CarePlan-1.activity.detail.description  | Optional |
| ReSPECT Care Priority  			  | 												| Mandatory |
| 									  | Extension.respectPriorityScale.valueInteger		| Mandatory |
|									  | Extension.respectPriorityScaleStatement			| Optional |
| Professional recording changes to Problems and Interventions | CareConnect-EOL-ProblemList-1.date | Mandatory |

### Problem List Example XML ###


### Problem Header Example XML ###

### Care Plan Example XML ###




