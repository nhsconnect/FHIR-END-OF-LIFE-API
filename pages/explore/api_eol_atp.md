---
title: Advance Treatment Preferences Atomic Unit
keywords: usecase, problemList, problemHeader, CarePlan
tags: [rest, fhir, workflow,api]
sidebar: foundations_sidebar
permalink: api_eol_atp.html
summary: Atomic Unit to capture the advance treatment preferences for a patient.
toc: false
---
{% include custom/search.warnbanner.html %}

### Advance Treatment Preferences ###


The following FHIR profiles are used to form the Advance Treatment Preferences Atomic Unit:

- [CareConnect-EOL-Patient-1](https://fhir.nhs.uk/STU3/StructureDefinition/CareConnect-EOL-Patient-1.xml)
- [CareConnect-Organization-1](https://fhir.hl7.org.uk/STU3/StructureDefinition/CareConnect-Organization-1)
- [CareConnect-Practitioner-1](https://fhir.hl7.org.uk/STU3/StructureDefinition/CareConnect-Practitioner-1)
- [CareConnect-PractitionerRole-1](https://fhir.hl7.org.uk/STU3/StructureDefinition/CareConnect-PractitionerRole-1)
- [CareConnect-EOL-ProblemList-1](https://fhir.nhs.uk/STU3/StructureDefinition/CareConnect-EOL-ProblemList-1.xml)
- [CareConnect-EOL-ProblemHeader-Condition-1](https://fhir.nhs.uk/STU3/StructureDefinition/CareConnect-EOL-ProblemHeader-Condition-1.xml)
- [EOL-CarePlan-1](https://fhir.nhs.uk/STU3/StructureDefinition/EOL-ATP-CarePlan-1.xml)


### Advance Treatment Preferences data item mapping to FHIR profiles ###

The Advance Treatment Preferences data items are fulfilled by elements within the FHIR resources listed below:

| DCH Data Item                       | FHIR resource element                                                   | Mandatory/Required/Optional |
|-------------------------------------|-------------------------------------------------------------------------|-----------------------------|
| Problem or Condition                | CareConnect-EOL-ProblemHeader-Condition-1.code.text           | Mandatory                   |
| Treatment Level					  | EOL-ATP-CarePlan-1.activity.detail.code.text	| Optional |
| Intervention						  | EOL-ATP-CarePlan-1.activity.detail.description  | Optional |
| ReSPECT Care Priority  			  | 												| Mandatory |
| 									  | Extension.respectPriorityScale.valueInteger		| Mandatory |
|									  | Extension.respectPriorityScaleStatement			| Optional |
| Professional recording changes to Problems and Interventions | CareConnect-EOL-ProblemList-1.date | Mandatory |

### Problem List Example XML ###

```xml
<List xmlns="http://hl7.org/fhir"/>
	<id value="33a33b58-648a-4453-b981-e21ea9ebc6ea"/>
	<meta>
		<profile value="https://fhir.nhs.uk/STU3/StructureDefinition/CareConnect-EOL-ProblemList-1.xml"/>
	</meta>
	<extension url="https://fhir.nhs.uk/STU3/StructureDefinition/Extension-EOL-ReSPECTScale-1">
		<extension url="respectPriorityScale">
			<valueInteger value="50"/>
		</extension>
		<extension url="respectPriorityScaleStatement">
			<valueString value="Considering the above priority, what is most important to you?"/>
		</extension>
	</extension>
	<status value="current"/>
	<mode value="working"/>
	<code>
		<text value="ATP Problem / Condition List"/>
	</code>
	<subject>
		<reference value="urn:uuid:12692f55-56cf-4ddf-3ef5-e9ed13f6bd923"/>
	</subject>
	<entry>
		<item>
			<reference value="urn:uuid:02692f55-56cf-4dda-8ef5-e9ec13f6bd99"/>
		</item>
	</entry>
</List>
```

### Problem Header Example XML ###

<Condition>
<id value="f74658b4-f667-4385-9b6f-7c4305b4f743"/>
	<meta>
		<profile value="https://fhir.nhs.uk/STU3/StructureDefinition/CareConnect-EOL-ProblemHeader-Condition"/>
	</meta>
	<extension url="https://fhir.hl7.org.uk/STU3/StructureDefinition/Extension-CareConnect-RelatedClinicalContent-1">
				<valueReference>
					<reference value="f74658b4-f667-4385-9b6f-7c4305b4f743"/>
				</valueReference>
			</extension>
	<code>
		<text value="Breathlessness"/>
	</code>
	<subject>
		<reference value="urn:uuid:12692f55-56cf-4ddf-3ef5-e9ed13f6bd923"/>
	</subject>
</Condition>	

### Care Plan Example XML ###

<CarePlan xmlns="http://hl7.org/fhir">
<id value="f74658b4-f667-4385-9b6f-7c4305b4f743"/>
	<meta>
		<profile value="https://fhir.nhs.uk/STU3/StructureDefinition/EOL-ATP-CarePlan-1"/>
	</meta>
	<status value="active"/>
	<intent value="plan"/>
	<subject>
		<reference value="urn:uuid:7368c5fe-bbb4-4e9c-a585-234e06b84e82"/>
	</subject>
	<activity>
		<detail >
		<code>
			<text value="Comfort, symptomatic treatment only"/>
		</code>
		<status value="completed"/>
		<description value="Patient should be made comfortable"/>
		</detail>	
	</activity>
</CarePlan>


