---
title: Workflow | Advance Treatment Preferences Questionnaire Response
keywords: usecase, questionnaire, response, preferences
tags: [rest, fhir, workflow,api]
sidebar: foundations_sidebar
permalink: api_eol_advancetreatmentpreferences_questionnaireresponse.html
summary: Questionnaire Response to capture the ReSPECT values for a patient.
---
{% include custom/search.warnbanner.html %}

{% include custom/fhir.STU3.reference.html resource="QuestionnaireResponse" page="EOL-AdvcanceTreatmentPreferences-QuestionnaireResponse-1" fhirname="QuestionnaireResponse" fhirlink="questionnaireresponse.html" content="User Stories" userlink="engage_endoflife.html" %}

## Patient Scenario ##

### Advance Treatment Preferences ###

Advance treatment preferences are recorded as a table of the problem/condition/anticipated event, coupled with the intervention required and an indicator of the level of intervention.

Most of the ReSPECT data can be captured within the minimum dataset, however the ReSPECT care priority values cannot be accommodated elsewhere and so must be recorded separately.  As many localities have or will implement ReSPECT, it important that these additional ReSPECT values can be transmitted.

```xml
    <QuestionnaireResponse xmlns="http://hl7.org/fhir">
	<id value="8fa0541c-a7a2-4846-a7e4-ef3c4a8991e1"/>
	<meta>
		<profile value="https://fhir.nhs.uk/STU3/StructureDefinition/EOL-AdvanceTreatmentPreferences-QuestionnaireResponse-1"/>
	</meta>
	<status value="completed"/>
	<subject> 
		<reference value="CareConnect-Patient-1/6101231234"/> 
	</subject> 
	<authored value="2018-06-18T00:00:00+01:00"/> 
	<author> 
		<reference value="CareConnect-Practitioner-1/12345678"/> 
	</author> 
	<item> 
		<linkId value="respectCarePriorityScale"/> 
		<text value="ReSPECT Care Priority Scale"/> 
			<answer> 
				<valueInteger value="50"/> 
			</answer> 
		<item> 
	<linkId value="respectCarePriorityText"/> 
		<text value="ReSPECT Care Priority Text"/> 
		<answer> 
			<valueString value="I will let the medical professional take the decision"/> 
		</answer> 
	</item>
	</QuestionnaireResponse>
```

