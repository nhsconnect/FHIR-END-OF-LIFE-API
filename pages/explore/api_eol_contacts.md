---
title: Contacts Atomic Unit
keywords: usecase, emergency, phone
tags: [rest, fhir, workflow,api]
sidebar: foundations_sidebar
permalink: api_eol_contacts.html
summary: Atomic Unit to capture the emergency contact preferences for a patient.
toc: false
---
{% include custom/search.warnbanner.html %}

### Contacts ###

### WARNING: EOL PROFILES POINTING TO TEST SERVER FHIR-TEST.NHS.UK ###

The following FHIR profiles are used to form the contacts Atomic Unit:

- [EOL-Patient-1](https://fhir-test.nhs.uk/STU3/StructureDefinition/EOL-Patient-1)

### Contact data item mapping to FHIR profiles ###

The contact data item are fulfilled by elements within the FHIR resources listed below:

| EOL Data Item                       | FHIR resource element                                                   | Mandatory/Required/Optional |
|-------------------------------------|-------------------------------------------------------------------------|-----------------------------|
| Contact Name				  | EOL-Patient-1.contact.name 							| Mandatory |
| Contact Role				  | EOL-Patient-1.relationship.text												| Optional |
| Contact Type				  | EOL-Patient-1.contact.telecom.system												| Optional |
| Contact Detail			  | EOL-Patient-1.contact.telecom.value												| Mandatory |
| Organisation Name			  | EOL-Patient-1.contact.organization									| Optional |
| Additional Information About Contact	 | EOL-Patient-1.contact.additionalContactInformation (Extension)	    | Optional |



### Contact Example XML ###

<script src="https://gist.github.com/IOPS-DEV/31ea699515e4ad684dc4961c848531d1.js"></script>



