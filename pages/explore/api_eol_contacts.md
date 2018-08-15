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



