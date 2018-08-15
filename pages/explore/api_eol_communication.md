---
title: Communication Atomic Unit
keywords: usecase, language, interpreter
tags: [rest, fhir, workflow,api]
sidebar: foundations_sidebar
permalink: api_eol_communication.html
summary: Atomic Unit to capture the communication preferences for a patient.
toc: false
---
{% include custom/search.warnbanner.html %}

### communication ###


The following FHIR profiles are used to form the communication Atomic Unit:

- [CareConnect-EOL-Patient-1](https://fhir.nhs.uk/STU3/StructureDefinition/CareConnect-EOL-Patient-1.xml)
- [Extension-CareConnect-EOL-NHSCommunication-1] (https://fhir.nhs.uk/STU3/StructureDefinition/Extension-CareConnect-EOL-NHSCommunication-1)

### communication data item mapping to FHIR profiles ###

The demoigraphics data items are fulfilled by elements within the FHIR resources listed below:

| DCH Data Item                       | FHIR resource element                                                   | Mandatory/Required/Optional |
|-------------------------------------|-------------------------------------------------------------------------|-----------------------------|
| Languages Spoken			  | CareConnect-EOL-Patient-1.nhsCommunication (Extension) 							| Optional |
| Language Spoken Code		  | nhsCommunication.language.code  												| Optional |
| Language Spoken Text		  | nhsCommunication.language.code.text												| Mandatory |
| Language Comment 			  | nhsCommunication.languageComment												| Optional |
| Type of Interpretation Code | nhsCommunication.modeofCommunication.code 										| Optional |
| Type of Interpretation Text | nhsCommunication.modeofCommunication,code.text 								    | Optional |
| Interpreter Required        | nhsCommunication.interpreterRequired									        | Optional |


### Communication Example XML ###

```xml
<Patient>
	<id value="7368c5fe-bbb4-4e9c-a585-234e06b84e82"/>
		<meta>
			profile value="https://fhir.nhs.uk/STU3/StructureDefinition/CareConnect-EOL-Patient-1"/>
		</meta>
	<identifier>
		<extension url="https://fhir.hl7.org.uk/STU3/StructureDefinition/Extension-CareConnect-NHSNumberVerificationStatus-1">
			<valueCodeableConcept>
				<coding>
					<system value="https://fhir.hl7.org.uk/STU3/CodeSystem/CareConnect-NHSNumberVerificationStatus-1"/>
					<code value="01"/>
					<display value="Number present and verified"/>
				</coding>
			</valueCodeableConcept>
		</extension>
			<system value="https://fhir.nhs.uk/Id/nhs-number"/>
				<value value="9912003888"/>
	</identifier>				
	<name>
		<use value="official"/>
		<family value="DAWKINS"/>
		<given value="Jack"/>
	</name>
	<birthDate value="2017-10-02"/>				
</Patient>
```



