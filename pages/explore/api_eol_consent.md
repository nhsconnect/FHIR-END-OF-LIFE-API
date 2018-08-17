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

### consent ###


The following FHIR profiles are used to form the CPR Status Atomic Unit:

- [CareConnect-EOL-Patient-1](https://fhir.nhs.uk/STU3/StructureDefinition/CareConnect-EOL-Patient-1.xml)

### consent data item mapping to FHIR profiles ###

The consent data item are fulfilled by elements within the FHIR resources listed below:

| DCH Data Item                       | FHIR resource element                                                   | Mandatory/Required/Optional |
|-------------------------------------|-------------------------------------------------------------------------|-----------------------------|
| Consent Status        		       | EOL-CPRStatus-Flag-1.code           | Mandatory                   |
| Consent Decision Details |
| Date of change in consent status	|
| Professionals recording this consent status	|
| 

### Consent ERD ###

<img src="images/erd/erd-consent.svg" style="width:80%;max-width: 80%;">

### Consent Example XML ###

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



