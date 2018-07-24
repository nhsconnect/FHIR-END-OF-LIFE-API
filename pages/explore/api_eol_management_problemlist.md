---
title: Management | Problem List
keywords: usecase, condition, probem, care connect
tags: [rest, fhir, management,api]
sidebar: foundations_sidebar
permalink: api_eol_management_problemlist.html
summary: A list of the patient's conditions and/or problems.
---
{% include custom/search.warnbanner.html %}

{% include custom/fhir.STU3.reference.html resource="List" page="CareConnect-ProblemList-1" fhirname="List" fhirlink="list.html" content="User Stories" userlink="engage_endoflife.html" %}

## Patient Scenario ##


### Problem List ###

The patient's problem list is made up of one or more conditions or problems that have been identified by a healthcare professional. The problem list is dynamic in nature, with conditions or problems being added or removed from the list over the lifetime of the patient. Any condition or problem is captured as a text value.


```xml
<List xmlns="http://hl7.org/fhir" xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance" xsi:schemaLocation="http://hl7.org/fhir file:///C:/stu3/list.xsd">
	<id value="9fa0541c-67a2-4946-a7e3-ef3c4a8991f1"/>
	<meta>
		<profile value="https://fhir.nhs.uk/STU3/StructureDefinition/CareConnect-ProblemList-1"/>
	</meta>
	<status value="current"/>
	<mode value="working"/>
	<code>
		<coding>
			<system value="http://hl7.org/fhir/list-example-use-codes"/>
			<code value="Problems"/>
			<display value="Problem List"/>
		</coding>
	</code>
	<subject>
		<reference value="CareConnect-Patient-1/6101231234"/>
	</subject>
	<date value="2018-06-18T00:00:00+01:00"/>
	<source>
		<reference value="CareConnect-Practitioner-1/12345678"/>
	</source>
	<entry>
		<item>
			<reference value="CareConnect-ProblemHeader-Condition-1/4adbbc2b-468a-4517-a5ae-f1d0db19cce5"/>
		</item>
	</entry>
</List>
```