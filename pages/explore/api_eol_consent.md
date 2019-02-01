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
- [CareConnect-Practitioner-1](https://fhir.hl7.org.uk/STU3/StructureDefinition/CareConnect-Practitioner-1) (EOL mandates name.text)
- [CareConnect-PractitionerRole-1](https://fhir.hl7.org.uk/STU3/StructureDefinition/CareConnect-PractitionerRole-1)
- [EOL-Consent-1](https://fhir.nhs.uk/STU3/StructureDefinition/EOL-Consent-1)

### Consent data item mapping to FHIR profiles ###

The consent data item are fulfilled by elements within the FHIR resources listed below:

| EOL Data Item                       | FHIR resource element                                                   | Mandatory/Required/Optional |Notes |
|-------------------------------------|-------------------------------------------------------------------------|-----------------------------|------|
| Consent Status        		       | EOL-Consent-1.status          | Mandatory                   | Active = Consent Given, Inactive = Consent Refused.|
| Consent Decision Details | EOL-Consent-1.consentDecisionDetails (Extension) | Optional |
| Consent Discussion Details | EOL-Consent-1.consentDiscussionDetails (Extension) |Optional |
| Date of change in consent status	| EOL-Consent-1.dateTime | Mandatory |
| Professionals recording this consent status	| EOL-Consent-1.consentingAuthor (Extension)|Mandatory |

### EOL-Consent-1.consentDiscussionDetails Guidance ###

Where the sending system supports a terminology system:

* The condition.code element MUST be populated with:
    * the terminology system (e.g. SNOMED-CT) 
    * code
	* display value
* the condition.code.text field MUST be populated with the display value from the condition.code.display element e.g. ‘Asthma (disorder)’
* the condition.code.text field MAY contain free text to capture more detail associated with the condition.code e.g. ‘Patient uses blue inhaler to relieve symptoms’

Where the sending system does not support a terminology system:

* the condition.code.text field MUST be populated with a text description of the condition as a human readable narrative e.g ‘Asthma’. 
* the condition.code.text field MAY contain free text to capture more detail associated with the condition e.g. ‘Patient uses blue inhaler to relieve symptoms’

### Consent Example XML ###

<script src="https://gist.github.com/IOPS-DEV/4ffee155fba48bfe2d6891ab80561b6d.js"></script>



