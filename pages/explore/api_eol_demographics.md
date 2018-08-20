---
title: Demographics Atomic Unit
keywords: usecase, NHS Number, Name, DoB
tags: [rest, fhir, workflow,api]
sidebar: foundations_sidebar
permalink: api_eol_demographics.html
summary: Atomic Unit to capture the demographics for a patient.
toc: false
---
{% include custom/search.warnbanner.html %}

### Demographics ###


The following FHIR profiles are used to form the Demographics Atomic Unit:

- [CareConnect-EOL-Patient-1](https://fhir.nhs.uk/STU3/StructureDefinition/CareConnect-EOL-Patient-1.xml)

### Demographics data item mapping to FHIR profiles ###

The demographics data items are fulfilled by elements within the FHIR resources listed below:

| DCH Data Item                       | FHIR resource element                                                   | Mandatory/Required/Optional |
|-------------------------------------|-------------------------------------------------------------------------|-----------------------------|
| NHS Number        		       | CareConnect-EOL-Patient-1.identifier.nhsNumber           | Mandatory                   |
| Surname				  | CareConnect-EOL-Patient-1.name.family	| Mandatory |
| Forename						  | CareConnect-EOL-Patient-1.name.given  | Mandatory |
| Date of Birth			  | CareConnect-EOL-Patient-1.birthDate												| Mandatory |


### Demographics Example XML ###

<script src="https://gist.github.com/IOPS-DEV/daf35a12e3d7723c0ed0d9c49c18ec99.js"></script>



