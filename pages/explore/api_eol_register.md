---
title: End of Life Register Atomic Unit
keywords: usecase, Disability
tags: [rest, fhir, workflow,api]
sidebar: foundations_sidebar
permalink: api_eol_register.html
summary: Atomic Unit to capture the End of Life Register for a patient.
toc: false
---
{% include custom/search.warnbanner.html %}

{% include custom/under.construction.html %}

### End of Life Register ###


The following FHIR profiles are used to form the Disabilities Atomic Unit:

- [EOL-Patient-1](https://fhir.nhs.uk/STU3/StructureDefinition/EOL-Patient-1.xml)
- [EOL-Register-1](https://fhir.nhs.uk/STU3/StructureDefinition/EOL-Register-Flag-1.xml)

### End of Life Register data item mapping to FHIR profiles ###

The End of Life Register data items are fulfilled by elements within the FHIR resources listed below:

| EOL Data Item                       | FHIR resource element                                                   | Mandatory/Required/Optional |
|-------------------------------------|-------------------------------------------------------------------------|-----------------------------|
| End of Life Register				  | EOL-Register-Flag-1.code														| Mandatory					  |

### End of Life Register Example XML ###

<script src="https://gist.github.com/IOPS-DEV/bfb6dffd85e06a44b0c690f58d027407.js"></script>


