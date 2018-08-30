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
- [EOL-LastingPowerOfAttorney-Contract-1](https://fhir.nhs.uk/STU3/StructureDefinition/EOL-LastingPowerOfAttorney-Contract-1)

### Lasting Power of Attorney data item mapping to FHIR profiles ###

The Lasting Power of Attorney data items are fulfilled by elements within the FHIR resources listed below:

| EOL Data Item                       | FHIR resource element                                                   | Mandatory/Required/Optional |
|-------------------------------------|-------------------------------------------------------------------------|-----------------------------|
| Lasting Power of Attorney For Health and Welfare | EOL-LastingPowerOfAttorney-Contract-1.type				    ||
| Contact Name									| EOL-LPA-RelatedPerson-1.name									||
| Contact Type									| EOL-LPA-RelatedPerson-1.telecom.use							||
| Contact Detail 								| EOL-LPA-RelatedPerson-1.telecom.value							||

### Lasting Power of Attorney Example XML ###

<script src="https://gist.github.com/IOPS-DEV/2bba72ff566322ed463bd6ecf8ed7efe.js"></script>



