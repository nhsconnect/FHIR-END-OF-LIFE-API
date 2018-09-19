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

### Consent ###

When a patient has a record created on the EPaCCS they will discuss whether they consent to electronic record sharing.  Some systems do not record refusal to share as such, because if patients refuse to share then there is just no record created.  
Other systems may not have a specific consent for sharing the EoL dataset bundle, this may be included in a wider discussion and decision with reference to information sharing.


The following FHIR profiles are used to form the Consent Atomic Unit:

- [EOL-Patient-1](https://fhir.nhs.uk/STU3/StructureDefinition/EOL-Patient-1)
- [CareConnect-Organization-1](https://fhir.hl7.org.uk/STU3/StructureDefinition/CareConnect-Organization-1)
- [CareConnect-Practitioner-1](https://fhir.hl7.org.uk/STU3/StructureDefinition/CareConnect-Practitioner-1)
- [CareConnect-PractitionerRole-1](https://fhir.hl7.org.uk/STU3/StructureDefinition/CareConnect-PractitionerRole-1)
- [EOL-Consent-1](https://fhir.nhs.uk/STU3/StructureDefinition/EOL-Consent-1)

### Consent data item mapping to FHIR profiles ###

The consent data item are fulfilled by elements within the FHIR resources listed below:

| EOL Data Item                       | FHIR resource element                                                   | Mandatory/Required/Optional |
|-------------------------------------|-------------------------------------------------------------------------|-----------------------------|
| Consent Status        		       | EOL-Consent-1.status          | Mandatory                   |
| Consent Decision Details | EOL-Consent-1.consentDecisionDetails (Extension) | Optional |
| Consent Discussion Details | EOL-Consent-1.consentDiscussionDetails (Extension) |Optional |
| Date of change in consent status	| EOL-Consent-1.dateTime | Mandatory |
| Professionals recording this consent status	| EOL-Consent-1.consentingAuthor (Extension)|Mandatory |


### Consent Example XML ###

<script src="https://gist.github.com/IOPS-DEV/4ffee155fba48bfe2d6891ab80561b6d.js"></script>



