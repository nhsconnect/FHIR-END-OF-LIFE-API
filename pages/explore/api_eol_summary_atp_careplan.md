---
title: Clinical Summary | Care Plan
keywords: usecase, care plan, problem, condition, intervention, 
tags: [rest, fhir, management,api]
sidebar: foundations_sidebar
permalink: api_eol_summary_atp_careplan.html
summary: Clinical details of problems and/or conditions that affect the patient.
---
{% include custom/search.warnbanner.html %}

{% include custom/fhir.STU3.reference.html resource="List" page="CareConnect-ProblemList-1" fhirname="List" fhirlink="list.html" content="User Stories" userlink="engage_endoflife.html" %}

## Patient Scenario ##


### Care Plan ###

The patient’s care plan provides deatils for how a condition that has been diagnosed for a patient should be treated by healthcare professionals along with any interventions that have been agreed with the patient. Each condition diagnosed has a related care plan.


```xml
<CarePlan xmlns="http://hl7.org/fhir">
<id value="2378d7d6-ce25-4eeb-b7d8-b08adbdfd9dd"/>
	<status value="active"/>
	<intent value="plan"/>
	<subject>
		<reference value="CareConnect-Patient-1/6101231234"/>
	</subject>
	<author>
		<reference value="CareConnect-Practitioner-1"/>
	</author>
	<activity>
		<detail>
		<code>
			<text value="Comfort, symptomatic treatment only"/>
		</code>
			<status value="completed"/>
			<description value="Nebulizer can be used to make patient more comfortable"/>
		</detail>
	</activity>
</CarePlan>
```