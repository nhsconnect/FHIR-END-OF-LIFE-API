---
title: Workflow | Functional Status Questionnaire Response
keywords: usecase, questionnaire, response, preferences
tags: [rest, fhir, workflow,api]
sidebar: foundations_sidebar
permalink: api_eol_functionalstatus_questionnaireresponse.html
summary: An interaction between a patient and healthcare provider(s) for the purpose of providing healthcare service(s) or assessing the health status of a patient.
---
{% include custom/search.warnbanner.html %}

{% include custom/fhir.STU3.reference.html resource="QuestionnaireResponse" page="EOL-FunctionalStatus-QuestionnaireResponse-1" fhirname="QuestionnaireResponse" fhirlink="questionnaireresponse.html" content="User Stories" userlink="engage_endoflife.html" %}

## Patient Scenario ##


### Functional Status ###

The patient’s functional status is recorded by clinicians during encounters with the patient and gives consumers of the data a general indication of the wellness of the patient. The status can be codified using either the Karnofsky scale or Electronic Frailty Index and there is a mandatory textual field for systems that do not store this data as a codeable concept.


```xml
    <QuestionnaireResponse xmlns="http://hl7.org/fhir">
	<id value="9fa0541c-67a2-4946-a7e3-ef3c4a8991f1"/>
	<meta>
		<profile value="https://fhir.nhs.uk/STU3/StructureDefinition/EOL-FunctionalStatus-QuestionnaireResponse-1"/>
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
		<linkId value="functionalStatus/> 
		<text value="Functional Status"/> 
		<answer> 
			<valueCoding>
				<system value="http://snomed.info/sct"/>
				<code value="https://fhir.nhs.uk/STU3/ValueSet/EOL-FunctionalStatusType-Code-1"/>
				<display value="Karnofsky Performance Status score (observable entity)"/>
			</valueCoding>
		</answer> 
		</item> 
		<item> 
		<linkId value="functionalStatusValue/> 
		<text value="Functional Status Value"/> 
		<answer> 
			<valueString value="50   Considerable assistance and frequent medical care required"/> 
		</answer> 
		</item>
		<item> 
		<linkId value="functionalStatusText"/> 
		<text value="Functional Status Text"/> 
		<answer> 
			<valueString value="I can function on my own most of the time"/> 
		</answer> 
		</item> 		
	</item> 
	</QuestionnaireResponse>
```


