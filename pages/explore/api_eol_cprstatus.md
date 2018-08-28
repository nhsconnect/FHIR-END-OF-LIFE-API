---
title: CPR Status Atomic Unit
keywords: usecase, NHS Number, Name, DoB
tags: [rest, fhir, workflow,api]
sidebar: foundations_sidebar
permalink: api_eol_cprstatus.html
summary: Atomic Unit to capture the CPR Status for a patient.
toc: false
---
{% include custom/search.warnbanner.html %}

{% include custom/under.construction.html %}

### CPR Status ###


The following FHIR profiles are used to form the CPR Status Atomic Unit:

- [EOL-Patient-1](https://fhir.nhs.uk/STU3/StructureDefinition/EOL-Patient-1)
- [CareConnect-Practitioner-1](https://fhir.nhs.uk/STU3/StructureDefinition/CareConnect-Practitioner-1)
- [EOL-CPRStatus-QuestionnaireResponse-1](https://fhir.nhs.uk/STU3/StructureDefinition/EOL-CPRStatus-QuestionnaireResponse-1)

### CPR Status data item mapping to FHIR profiles ###

The CPR Status data items are fulfilled by elements within the FHIR resources listed below:

| EOL Data Item                       | FHIR resource element                                                   | Mandatory/Required/Optional |
|-------------------------------------|-------------------------------------------------------------------------|-----------------------------|
| CPR Status        		       | EOL-CPRStatus-Flag-1.code           | Mandatory                   |
| Reason for CPR status | EOL-CPRStatus-QuestionnaireResponse-1.reasonForCPRStatus | Mandatory |
| CPR Status Mental Capacity | EOL-CPRStatus-QuestionnaireResponse-1.cPRStatusMentalCapacity |
| Date Time of CPR Status | EOL-CPRStatus-Flag-1.period.start|
| Review Date | EOL-CPRStatus-Flag-1.period.end|
| Persons Involved in Discussion | EOL-CPRStatus-QuestionnaireResponse-1.personsInvolvedInDiscussion (Extension)|
| Persons or Organisations Made Aware of the Decision | EOL-CPRStatus-QuestionnaireResponse-1.awarenessOfDecision (Extension)|
| Professionals Involved in Decision | EOL-CPRStatus-QuestionnaireResponse-1.professionalsInvolvedInDecision|
| Professional Recording the CPR status | EOL-CPRStatus-Flag-1.author |
| Professional Endorsing this CPR status | EOL-CPRStatus-QuestionnaireResponse-1.professionalEndorsingStatus |

### CPR Status ERD ###

<img src="images/erd/cpr-erd.svg" style="width:80%;max-width: 80%;">

### CPR Status Example XML ###

```xml
<Flag xmlns="http://hl7.org/fhir">
<id value="85c8a1c5-a8a1-41c9-bb99-20956fa66218"/>
<meta>
	<profile value="https://fhir.nhs.uk/STU3/StructureDefinition/EOL-CPRStatus-Flag-1"/>
</meta>
<extension url="http://hl7.org/fhir/StructureDefinition/flag-detail">
	<valueReference>
		<reference value="a1f701a4-0959-4992-b7e3-1c6918462f7f"/>
	</valueReference>
</extension>
<status value="active"/>
<code>
	<coding>
		<system value="http://snomed.info/sct"/>
		<code value="450475007"/>
		<display value="For cardiopulmonary resuscitation (finding)"/>			
		</coding>
</code>
<subject>
	<reference value="42d0bdc9-cff8-4db6-ade6-39604950bb95"/>
</subject>
<period>
	<start value="2018-08-01"/>
</period>
<author>
	<reference value="388b75a2-2d8e-43ba-bd01-efafa34ec8f0"/>
</author>
</Flag>
```

```xml
<QuestionnaireResponse xmlns="http://hl7.org/fhir"/>
	<id value="85c8a1c5-a8a1-41c9-bb99-20956fa66218"/>
	<meta>
		<profile value="https://fhir.nhs.uk/STU3/StructureDefinition/EOL-CPRStatus-QuestionnaireResponse-1"/>
	</meta>
	<extension url="https://fhir.nhs.uk/STU3/StructureDefinition/Extension-EOL-AwarenessOfDecision-1">
		<extension url="awarenessOfDecision">
			<valueCodeableConcept>
				<coding>
					<system value="http://snomed.info/sct"/>
					<code value="975291000000108"/>
					<display value="Family member informed of cardiopulmonary resuscitation clinical decision (situation)"/>
				</coding>
			</valueCodeableConcept>
		</extension>
		<extension url="awarenessOfDecisionInformation">
			<valueString value="Uncle Bob has been made aware of the decision"/>
		</extension>
	</extension>
	<extension url="https://fhir.nhs.uk/STU3/StructureDefinition/Extension-EOL-PersonsInvolvedInDiscussion-1">
		<extension url="personInDiscussion">
			<valueCodeableConcept>
				<coding>
					<system value="http://snomed.info/sct"/>
					<code value="713656002"/>
					<display value="Discussion about cardiopulmonary resuscitation with family member (situation)"/>
				</coding>
			</valueCodeableConcept>
		</extension>
		<extension url="discussionInformation">
			<valueString value="Supporting inforamtion not provided."/>
		</extension>
	</extension>
	<status value="completed"/>
	<subject>
		<reference value="18919735-b4dc-471e-bc08-6ed0852f4459"/>
	</subject>
	<item>
		<linkId value="reasonForCPRStatus"/>
		<text value="Reason for CPR status"/>
		<answer>
			<valueString value="The outcome of the CPR would not be of overall benefit to the patient"/>
		</answer>
	</item>
	<item>
		<linkId value="professionalsInvolvedInDecision"/>
		<text value="Professionals Involved In Decision"/>
		<answer>
			<valueReference>
				<reference value="d7679a59-4689-4d28-a9c6-7da5570c5a8d"/>
			</valueReference>
		</answer>
	</item>
	<item>
		<linkId value="professionalEndorsingStatus"/>
		<text value="Professional Endorsing Status"/>
		<answer>
			<valueReference>
				<reference value="e79575ec-5421-42b9-a78f-7673f847c48c"/>
			</valueReference>
		</answer>
	</item>
</QuestionnaireResponse>
```


