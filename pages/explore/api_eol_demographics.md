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

- [CareConnect-EOL-Patient-1](https://fhir.nhs.uk/STU3/StructureDefinition/CareConnect-EOL-Patient-1.xml)

### Demographics data item mapping to FHIR profiles ###

The demoigraphics data items are fulfilled by elements within the FHIR resources listed below:

| DCH Data Item                       | FHIR resource element                                                   | Mandatory/Required/Optional |
|-------------------------------------|-------------------------------------------------------------------------|-----------------------------|
| NHS Number        		       | CareConnect-EOL-Patient-1.identifier.nhsNumber           | Mandatory                   |
| Surname				  | CareConnect-EOL-Patient-1.name.family	| Mandatory |
| Forename						  | CareConnect-EOL-Patient-1.name.forename  | Optional |
| Date of Birth			  | CareConnect-EOL-Patient-1.birthDate												| Mandatory |


### Demographics Example XML ###

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



