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

- [EOL-Patient-1](https://fhir.nhs.uk/STU3/StructureDefinition/EOL-Patient-1)

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

### Care Connect Profiles ###

Where possible, Care Connect profiles have been used to develop the End of Life API. On this occasion it has not been possible to do this. The table below highlights the Care Connect profile(s) replaced with a bespoke version and the rationale behind this.

| Care Connect Profile 	| Rationale for Change								     | New Component Required					 	   |
|-----------------------|--------------------------------------------------------|-------------------------------------------------|
| CareConnect-Patient-1 | Addition to nhsCommunication complex extension		 | nhsCommunication.languageComment   			   |
|						| Add extension to Contact element 			 		     | Contact.AdditionalContactInformation		       |
|						| Additional code adding to LanguageAbilityMode valueste | Add code 'TSGN' and display of 'Tactile Signing'|

End of Life will engage with the healthcare community and INTEROPen in the future to propose these changes to the Care Connect profiles(s).


