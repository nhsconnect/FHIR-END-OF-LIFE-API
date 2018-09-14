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

### WARNING: EOL PROFILES POINTING TO TEST SERVER FHIR-TEST.NHS.UK ###

A feature of primary care is a requirement for GPs to place the patient on an end of life register, where they adjudge the patient as being a person coming towards the end of their life.  There are several register formats, such as the QOF (Palliative Care) or GSF Palliative Care register.  As the specific type of register chosen varies, the national dataset has employed a simple SNOMED-coded marker that the patient has been recorded on an EoL register.

The following FHIR profiles are used to form the End of Life Register Atomic Unit:

- [EOL-Patient-1](https://fhir.nhs.uk/STU3/StructureDefinition/EOL-Patient-1)
- [EOL-Register-Flag1](https://fhir-test.nhs.uk/STU3/StructureDefinition/EOL-Register-Flag-1)

### End of Life Register data item mapping to FHIR profiles ###

The End of Life Register data items are fulfilled by elements within the FHIR resources listed below:

| EOL Data Item                       | FHIR resource element                                                   | Mandatory/Required/Optional |
|-------------------------------------|-------------------------------------------------------------------------|-----------------------------|
| End of Life Register				  | EOL-Register-Flag-1.code														| Mandatory			  |

### End of Life Register Example XML ###

<script src="https://gist.github.com/IOPS-DEV/bfb6dffd85e06a44b0c690f58d027407.js"></script>



