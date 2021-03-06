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

The following FHIR profiles are used to form the Demographics Atomic Unit:

- [EOL-Patient-1](https://fhir.nhs.uk/STU3/StructureDefinition/EOL-Patient-1)

### Demographics data item mapping to FHIR profiles ###

The demographics data items are fulfilled by elements within the FHIR resources listed below:

| EOL Data Item                       | FHIR resource element                                                   | Mandatory/Required/Optional |
|-------------------------------------|-------------------------------------------------------------------------|-----------------------------|
| NHS Number        		       | EOL-Patient-1.identifier.nhsNumber           | Mandatory                   |
| Surname				  | EOL-Patient-1.name.family	| Mandatory |
| Forename						  | EOL-Patient-1.name.given  | Mandatory |
| Date of Birth			  | EOL-Patient-1.birthDate												| Mandatory |
| Contact Name				  | EOL-Patient-1.contact.name 							| Mandatory |
| Contact Role				  | EOL-Patient-1.relationship.text												| Optional |
| Contact Type				  | EOL-Patient-1.contact.telecom.system												| Optional |
| Contact Detail			  | EOL-Patient-1.contact.telecom.value												| Mandatory |
| Organisation Name			  | EOL-Patient-1.contact.organization									| Optional |
| Additional Information About Contact	 | EOL-Patient-1.contact.additionalContactInformation (Extension)	    | Optional |
| Languages Spoken			  | EOL-Patient-1.nhsCommunication (Extension) 							| Optional |
| Language Spoken Code		  | nhsCommunication.language.code  												| Optional |
| Language Spoken Text		  | nhsCommunication.language.code.text												| Mandatory |
| Language Comment 			  | nhsCommunication.languageComment												| Optional |
| Type of Interpretation Code | nhsCommunication.modeofCommunication.code 										| Optional |
| Type of Interpretation Text | nhsCommunication.modeofCommunication.code.text 								    | Optional |
| Interpreter Required        | nhsCommunication.interpreterRequired									        | Optional |



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
