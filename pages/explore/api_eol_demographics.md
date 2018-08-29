---
title: Demographics Atomic Unit
keywords: usecase, NHS Number, Name, DoB
tags: [rest, fhir, workflow,api]
sidebar: foundations_sidebar
permalink: api_eol_demographics.html
summary: Atomic Unit to capture the demographics for a patient.
toc: false
---
{% include custom/search.warnbanner.html %}

### Demographics ###

### WARNING: EOL PROFILES POINTING TO TEST SERVER FHIR-TEST.NHS.UK ###

The following FHIR profiles are used to form the Demographics Atomic Unit:

- [EOL-Patient-1](https://fhir-test.nhs.uk/STU3/StructureDefinition/EOL-Patient-1)

### Demographics data item mapping to FHIR profiles ###

The demographics data items are fulfilled by elements within the FHIR resources listed below:

| EOL Data Item                       | FHIR resource element                                                   | Mandatory/Required/Optional |
|-------------------------------------|-------------------------------------------------------------------------|-----------------------------|
| NHS Number        		       | EOL-Patient-1.identifier.nhsNumber           | Mandatory                   |
| Surname				  | EOL-Patient-1.name.family	| Mandatory |
| Forename						  | EOL-Patient-1.name.given  | Mandatory |
| Date of Birth			  | EOL-Patient-1.birthDate												| Mandatory |


### Demographics Example XML ###

<script src="https://gist.github.com/IOPS-DEV/daf35a12e3d7723c0ed0d9c49c18ec99.js"></script>


### Care Connect Profiles ###

Where possible, Care Connect profiles have been used to develop the End of Life API. On this occasion it has not been possible to do this. The table below highlights the Care Connect profile(s) replaced with a bespoke version and the rationale behind this.

| Care Connect Profile 	| Rationale for Change								     | New Component Required					 	   |
|-----------------------|--------------------------------------------------------|-------------------------------------------------|
| CareConnect-Patient-1 | Addition to nhsCommunication complex extension		 | nhsCommunication.languageComment   			   |
|						| Add extension to Contact element 			 		     | Contact.AdditionalContactInformation		       |
|						| Additional code adding to LanguageAbilityMode valueste | Add code 'TSGN' and display of 'Tactile Signing'|

End of Life will engage with the healthcare community and INTEROPen in the future to propose these changes to the Care Connect profiles(s).
