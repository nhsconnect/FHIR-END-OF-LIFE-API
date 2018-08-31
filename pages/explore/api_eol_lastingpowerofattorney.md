---
title: Lasting Power of Attorney Atomic Unit
keywords: usecase, LPA
tags: [rest, fhir, workflow,api]
sidebar: foundations_sidebar
permalink: api_eol_lastingpowerofattorney.html
summary: Atomic Unit to capture the Lasting Power of Attorney for a patient.
toc: false
---
{% include custom/search.warnbanner.html %}

### Lasting Power of Attorney ###


The following FHIR profiles are used to form the Lasting Power of Attorney Atomic Unit:

- [EOL-Patient-1](https://fhir.nhs.uk/STU3/StructureDefinition/EOL-Patient-1)
- [EOL-LPA-Flag-1](https://fhir.nhs.uk/STU3/StructureDefinition/EOL-LPA-Flag-1)
- [EOL-LPA-RelatedPerson-1](https://fhir.nhs.uk/STU3/StructureDefinition/EOL-LPA-RelatedPerson-1)

### Lasting Power of Attorney data item mapping to FHIR profiles ###

The Lasting Power of Attorney data items are fulfilled by elements within the FHIR resources listed below:

| EOL Data Item                       | FHIR resource element                                                   | Mandatory/Required/Optional |
|-------------------------------------|-------------------------------------------------------------------------|-----------------------------|
| Lasting Power of Attorney For Health and Welfare | EOL-LPA-Flag-1.code				   					    | Mandatory|
| Contact Relationship							| EOL-LPA-RelatedPerson-1.relationship.code						| Mandatory|
| Contact Name									| EOL-LPA-RelatedPerson-1.name									| Mandatory|
| Contact Type									| EOL-LPA-RelatedPerson-1.telecom.use							| Mandatory||
| Contact Detail 								| EOL-LPA-RelatedPerson-1.telecom.value							| Mandatory||

### Business Rule ###

The EOL-LPA-Flag-1 MUST exist where an EOL-LPA-RelatedPerson-1 instance exists. This flag MUST be created when a related person instance is created with LPA relationship types. 
The flag indicates the presence of one or more RelatedPerson instances that may be used to identiofy person or persons who have the power to make critical decisions where the patient is unable to do so.

### Lasting Power of Attorney ERD ###

<img src="images/erd/lpa-erd.svg" style="width:80%;max-width: 80%;">

### Lasting Power of Attorney Example XML ###

<script src="https://gist.github.com/IOPS-DEV/2bba72ff566322ed463bd6ecf8ed7efe.js"></script>



