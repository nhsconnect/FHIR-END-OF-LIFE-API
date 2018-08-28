---
title: Consent Atomic Unit
keywords: usecase, NHS Number, Name, DoB
tags: [rest, fhir, workflow,api]
sidebar: foundations_sidebar
permalink: api_eol_consent.html
summary: Atomic Unit to capture the consent status for a patient.
toc: false
---
{% include custom/search.warnbanner.html %}

{% include custom/under.construction.html %}

### Consent ###


The following FHIR profiles are used to form the Consent Atomic Unit:

- [EOL-Patient-1](https://fhir.nhs.uk/STU3/StructureDefinition/EOL-Patient-1)
- [CareConnect-Practitioner-1](https://fhir.nhs.uk/STU3/StructureDefinition/CareConnect-Practitioner-1)
- [EOL-Consent-1](https://fhir.nhs.uk/STU3/StructureDefinition/EOL-Consent-1)

### Consent data item mapping to FHIR profiles ###

The consent data item are fulfilled by elements within the FHIR resources listed below:

| EOL Data Item                       | FHIR resource element                                                   | Mandatory/Required/Optional |
|-------------------------------------|-------------------------------------------------------------------------|-----------------------------|
| Consent Status        		       | EOL-Consent-1.status          | Mandatory                   |
| Consent Decision Details | EOL-Consent-1.consentDecisionDetails (Extension) | Optional |
| Consent Discussion Details | EOL-Consent-1.consentDiscussionDetails (Extension) |Optional |
| Date of change in consent status	| EOL-Consent-1.dateTime | Mandatory |
| Professionals recording this consent status	| EOL-Consent-1.actor |Mandatory |

### Consent ERD ###

<img src="images/erd/erd-consent.svg" style="width:80%;max-width: 80%;">

### Consent Example XML ###

<script src="https://gist.github.com/IOPS-DEV/4ffee155fba48bfe2d6891ab80561b6d.js"></script>



