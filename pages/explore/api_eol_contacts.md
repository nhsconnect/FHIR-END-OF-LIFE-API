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


The following FHIR profiles are used to form the contacts Atomic Unit:

- [CareConnect-EOL-Patient-1](https://fhir.nhs.uk/STU3/StructureDefinition/CareConnect-EOL-Patient-1.xml)

### Contact data item mapping to FHIR profiles ###

The demographics data items are fulfilled by elements within the FHIR resources listed below:

| DCH Data Item                       | FHIR resource element                                                   | Mandatory/Required/Optional |
|-------------------------------------|-------------------------------------------------------------------------|-----------------------------|
| Contact Name				  | CareConnect-EOL-Patient-1.contact.name 							| Mandatory |
| Contact Role				  | CareConnect-EOL-Patient-1.relationship.text												| Optional |
| Contact Type				  | CareConnect-EOL-Patient-1.contact.telecom.system												| Optional |
| Contact Detail			  | CareConnect-EOL-Patient-1.contact.telecom.value												| Mandatory |
| Organisation Name			  | CareConnect-EOL-Patient-1.contact.organization									| Optional |
| Additional Information About Contact	 | CareConnect-EOL-Patient-1.contact.additionalContactInformation (Extension)	    | Optional |



### Contact Example XML ###

<script src="https://gist.github.com/IOPS-DEV/31ea699515e4ad684dc4961c848531d1.js"></script>



