---
title: Workflow | Preferences Questionnaire Response
keywords: usecase, questionnaire, response, preferences
tags: [rest, fhir, workflow,api]
sidebar: foundations_sidebar
permalink: api_eol_preferences_questionnaireresponse.html
summary: An interaction between a patient and healthcare provider(s) for the purpose of providing healthcare service(s) or assessing the health status of a patient.
---
{% include custom/search.warnbanner.html %}

{% include custom/fhir.STU3.reference.html resource="QuestionnaireResponse" page="EOL-Preferences-QuestionnaireResponse-1" fhirname="QuestionnaireResponse" fhirlink="questionnaireresponse.html" content="User Stories" userlink="engage_endoflife.html" %}

## Patient Scenario ##

### Preferences ###

This is used to record a patient’s preferred place of death and any other preferences and wishes, including wishes for care and cultural, religious and social needs.  Additionally, there is an option to record domestic information and access instructions for the patient’s residence. 

```xml
	<QuestionnaireResponse xmlns="http://hl7.org/fhir">
	<id value="8fa0541c-a7a2-4846-a7e4-ef3c4a8991e1"/>
	<meta>
		<profile value="https://fhir.nhs.uk/STU3/StructureDefinition/EOL-Preferences-QuestionnaireResponse-1"/>
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
		<linkId value="preferredPlaceOfDeathCoded"/>
		<text value="Preferred Place of Death - Coded"/>
		<answer>
			<valueCoding>
				<system value="http://snomed.info/sct"/>
				<code value="517131000000106"/>
				<display value="Preferred place of death: discussion not appropriate (finding)"/>
			</valueCoding>
		</answer>
		</item> 
		<item> 
		<linkId value="preferencesAndWishes"/> 
		<text value="Preferences and Wishes"/> 
		<answer> 
			<valueString value="I want to have a cremation"/> 
		</answer> 
		</item> 
		<item> 
		<linkId value="domesticAccessAndInformation/> 
		<text value="Domestic Access and Information"/> 
		<answer> 
			<valueString value="I have a dog at home"/>
		</answer> 
		</item> 
	</QuestionnaireResponse>
```
