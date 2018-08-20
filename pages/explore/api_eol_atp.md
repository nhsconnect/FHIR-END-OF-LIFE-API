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
| Date of Change in List			  | CareConnect-EOL-ATP-ProblemList.date				| Mandatory |
| Problem or Condition                | CareConnect-EOL-ATP-ProblemHeader-Condition-1.code.text           | Mandatory                   |
| Treatment Level					  | EOL-ATP-CarePlan-1.activity.detail.code.text	| Optional |
| Intervention						  | EOL-ATP-CarePlan-1.activity.detail.description  | Optional |
| ReSPECT Care Priority  			  | 												| Mandatory |
| 									  | Extension.respectPriorityScale.valueInteger		| Mandatory |
|									  | Extension.respectPriorityScaleStatement.valueString			| Optional |
| Professional recording changes to Problems and Interventions | CareConnect-EOL-ProblemList-1.date | Mandatory |

### Problem List Example XML ###

<script src="https://gist.github.com/IOPS-DEV/68d09895595b33dc1370560a8b287f39.js"></script>

### Problem Header Example XML ###

<script src="https://gist.github.com/IOPS-DEV/16afab712dda04db1af18dfa1d9f722e.js"></script>

### Care Plan Example XML ###

<script src="https://gist.github.com/IOPS-DEV/f82218432c8103a8b73c2481733d5039.js"></script>

