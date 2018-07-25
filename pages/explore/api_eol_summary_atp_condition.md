---
title: Clinical | Condition
keywords: getcarerecord, structured, rest, condition
tags: [rest,fhir,condition,clinical,api]
sidebar: accessrecord_rest_sidebar
permalink: api_eol_summary_atp_condition.html
summary: Use to record detailed information about conditions, problems or diagnoses recognized by a clinician. There are many uses e.g. recording a diagnosis during an encounter; populating a problem list or a summary statement, such as a discharge summary.
---
{% include custom/search.warnbanner.html %}

{% include custom/fhir.STU3.reference.html resource="Condition" page="CareConnect-ProblemHeader-Condition-1" fhirname="Condition" fhirlink="condition.html" content="User Stories" userlink="engage_endoflife.html" %}

```xml
<Condition xmlns="http://hl7.org/fhir">
	<id value="9fa0541c-67a2-4946-a7e3-ef3c4a8991f1"/>
	<meta>
		<profile value="https://fhir.nhs.uk/STU3/StructureDefinition/CareConnect-ProblemHeader-Condition-1"/>
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

{% include custom/under.construction.html %}