---
title: Management | Problem Header Condition
keywords: usecase, header, condition, problem, care connect
tags: [rest, fhir, management,api]
sidebar: foundations_sidebar
permalink: api_eol_summary_problemheader_condition.html
summary: Clinical details of problems and/or conditions that affect the patient.
---
{% include custom/search.warnbanner.html %}

{% include custom/fhir.STU3.reference.html resource="List" page="CareConnect-ProblemList-1" fhirname="List" fhirlink="list.html" content="User Stories" userlink="engage_endoflife.html" %}

## Patient Scenario ##


### Problem or Condition ###

The patient’s problems and/or conditions are recorded by clinicians during encounters with the patient and gives consumers of the data a general indication of the wellness of the patient. 


```xml
<Condition xmlns="http://hl7.org/fhir">
	<id value="9fa0541c-67a2-4946-a7e3-ef3c4a8991f1"/>
	<meta>
		<profile value="https://fhir.nhs.uk/STU3/StructureDefinition/CareConnect-ProblemHeaer-Condition-1"/>
	</meta>
	<extension url="https://fhir.hl7.org.uk/STU3/StructureDefinition/Extension-CareConnect-RelatedClinicalContent-1">
		<valueReference>
			<reference value="EOL-AdvanceTreatmentPreferences-CarePlan-1/41e7045d-f5a0-4650-be70-536134858fd2"/>
		</valueReference>
	</extension>
	<clinicalStatus value="active"/>
	<category>
		<coding>
			<system value="http://hl7.org/fhir/condition-category"/>
			<code value="Problem-List-Item"/>
			<display value="Problem List Item"/>
		</coding>
	</category>
	<code >
		<text value="Asthma"/>
	</code>
	<subject>
		<reference value="CareConnect-Patient-1/6101231234"/>
	</subject>
</Condition>
```