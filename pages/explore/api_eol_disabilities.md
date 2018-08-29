---
title: Disabilities Atomic Unit
keywords: usecase, Disability
tags: [rest, fhir, workflow,api]
sidebar: foundations_sidebar
permalink: api_eol_disabilities.html
summary: Atomic Unit to capture the disabilities for a patient.
toc: false
---
{% include custom/search.warnbanner.html %}

{% include custom/under.construction.html %}

### Disabilities ###


The following FHIR profiles are used to form the Disabilities Atomic Unit:

- [EOL-Patient-1](https://fhir.nhs.uk/STU3/StructureDefinition/EOL-Patient-1.xml)
- [CareConnect-List-1](https://fhir.hl7.org.uk/STU3/StructureDefinition/CareConnect-Condition-1)
- [CareConnect-Condition-1](https://fhir.hl7.org.uk/STU3/StructureDefinition/CareConnect-List-1)
- [CareConnect-Practitioner-1](https://fhir.hl7.org.uk/STU3/StructureDefinition/CareConnect-Practitioner-1)
- [CareConnect-PractitionerRole-1](https://fhir.hl7.org.uk/STU3/StructureDefinition/CareConnect-PractitionerRole-1)
- [CareConnect-Organization-1](https://fhir.hl7.org.uk/STU3/StructureDefinition/CareConnect-Organization-1)


### Disabilities data item mapping to FHIR profiles ###

The disabilities data items are fulfilled by elements within the FHIR resources listed below:

| EOL Data Item                       | FHIR resource element                                                   | Mandatory/Required/Optional |
|-------------------------------------|-------------------------------------------------------------------------|-----------------------------|
| List of Disabilities				  | CareConnect-List-1.entry.item											| Optional					|
| Patient Disability Code				  | CareConnect-Condition-1.code | Optional |
| Patient Disability Textual | CareConnect-Condition-1.code.text | Mandatory |
| Professional Recording Disabilities | CareConnect-Condition-1.asserter | Mandatory |
| 

### Disabilities Example XML ###

<script src="https://gist.github.com/IOPS-DEV/5648828bd8b611fa938b3562a5c3e162.js"></script>

### Care Connect Profiles ###

Where possible, Care Connect profiles have been used to develop the End of Life API. On this occasion it has not been possible to do this. The table below highlights the Care Connect profile(s) replaced with a bespoke version and the rationale behind this.

| Care Connect Profile 	| Rationale for Change								     | New Component Required					 	   |
|-----------------------|--------------------------------------------------------|-------------------------------------------------|
| CareConnect-Condition-1 | Cardinality change									 | code.text requires 1:1 cardinality   		   |


End of Life will engage with the healthcare community and INTEROPen in the future to propose these changes to the Care Connect profiles(s).
