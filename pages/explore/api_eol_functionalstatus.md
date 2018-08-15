---
title: Functional Status Atomic Unit
keywords: usecase, questionnaire, response, preferences
tags: [rest, fhir, workflow,api]
sidebar: foundations_sidebar
permalink: api_eol_functionalstatus.html
summary: Questionnaire Response to capture the functional status of a patient using established scales where available.
toc: false
---
{% include custom/search.warnbanner.html %}

### Functional Status ###

The patient’s functional status is recorded by clinicians during encounters with the patient and gives consumers of the data a general indication of the wellness of the patient. The status can be codified using either the Karnofsky scale or Electronic Frailty Index and there is a mandatory textual field for systems that do not store this data as a codeable concept.

The following FHIR profiles are used to form the Functional Status Atomic Unit:

- [DCH-MessageHeader-1](https://fhir.nhs.uk/STU3/StructureDefinition/DCH-MessageHeader-1.xml) - where the coding and display for the event element is fixed to 'Birth Details'
- [CareConnect-DCH-Organization-1](https://fhir.nhs.uk/STU3/StructureDefinition/CareConnect-DCH-Organization-1.xml)
- [DCH-HealthcareService-1](https://fhir.nhs.uk/STU3/StructureDefinition/DCH-HealthcareService-1.xml)
- [CareConnect-DCH-Baby-Patient-1](https://fhir.nhs.uk/STU3/StructureDefinition/CareConnect-DCH-Baby-Patient-1.xml)
- [CareConnect-DCH-Birth-Encounter-1](https://fhir.nhs.uk/STU3/StructureDefinition/CareConnect-DCH-Birth-Encounter-1.xml)
- [CareConnect-DCH-ProblemAtBirth-Condition-1](https://fhir.nhs.uk/STU3/StructureDefinition/CareConnect-DCH-ProblemAtBirth-Condition-1.xml)
- [CareConnect-DCH-ProblemDuringDelivery-Condition-1](https://fhir.nhs.uk/STU3/StructureDefinition/CareConnect-DCH-ProblemDuringDelivery-Condition-1.xml)
- [CareConnect-DCH-APGARScore-Observation-1](https://fhir.nhs.uk/STU3/StructureDefinition/CareConnect-DCH-APGARScore-Observation-1.xml)
- [CareConnect-DCH-LengthOfGestation-Observation-1](https://fhir.nhs.uk/STU3/StructureDefinition/CareConnect-DCH-LengthOfGestation-Observation-1.xml)
- [CareConnect-DCH-NumberOfBirths-Observation-1](https://fhir.nhs.uk/STU3/StructureDefinition/CareConnect-DCH-NumberOfBirths-Observation-1.xml)
- [CareConnect-DCH-SpontaneousRespirationOnset-Observation-1](https://fhir.nhs.uk/STU3/StructureDefinition/CareConnect-DCH-SpontaneousRespirationOnset-Observation-1.xml)
- [CareConnect-DCH-NeonatalResuscitationMethod-Procedure-1](https://fhir.nhs.uk/STU3/StructureDefinition/CareConnect-DCH-NeonatalResuscitationMethod-Procedure-1.xml)
- [CareConnect-DCH-TypeOfDelivery-Procedure-1](https://fhir.nhs.uk/STU3/StructureDefinition/CareConnect-DCH-TypeOfDelivery-Procedure-1.xml)
- [CareConnect-DCH-PutToBreastIndicator-Observation-1](https://fhir.nhs.uk/STU3/StructureDefinition/CareConnect-DCH-PutToBreastIndicator-Observation-1.xml)
- [CareConnect-DCH-FraternalTwinIndicator-Observation-1](https://fhir.nhs.uk/STU3/StructureDefinition/CareConnect-DCH-FraternalTwinIndicator-Observation-1.xml)
- [CareConnect-DCH-Delivery-Location-1](https://fhir.nhs.uk/STU3/StructureDefinition/CareConnect-DCH-Delivery-Location-1.xml)

### Functional Status event data item mapping to FHIR profiles ###

The Functional Status data items are fulfilled by elements within the FHIR resources listed below:

| DCH Data Item                       | FHIR resource element                                                   | Mandatory/Required/Optional |
|-------------------------------------|-------------------------------------------------------------------------|-----------------------------|
| Location of Birth                   | CareConnect-DCH-Delivery-Location-1.identifier (ODS Site Code)           | Mandatory                   |
| Delivery Place Type Code            | CareConnect-DCH-Delivery-Location-1.physicalType                        | Mandatory                   |
| Birth Order                         | CareConnect-DCH-Baby-Patient-1.multipleBirthInteger                     | Mandatory                   |
| Length of Gestation at Birth        | CareConnect-DCH-LengthOfGestation-Observation-1.valueQuantity           | Mandatory                   |
| Number of Births in confinement     | CareConnect-DCH-NumberOfBirths-Observation-1.valueQuantity                  | Mandatory                    |
| Problems during Delivery            | CareConnect-DCH-ProblemDuringDelivery-Condition-1.code                          | Required                    |
| Physical Problems detected at Birth | CareConnect-DCH-ProblemAtBirth-Condition-1.code            | Required                    |
| Neonatal Resuscitation Method       | CareConnect-DCH-NeonatalResuscitationMethod-Procedure-1.code                           | Required                 |
| Date and Time of Birth              | CareConnect-DCH-Baby-Patient-1.birthDate                           | Mandatory                 |
| Type of Delivery                    | CareConnect-DCH-TypeOfDelivery-Procedure-1.code   | Mandatory                    |
| Attempted Type of Delivery          | CareConnect-DCH-TypeOfDelivery-Procedure-1.code where the 'status' element is presented as 'aborted'  | Required                    |
| Onset of Spontaneous Respiration    | CareConnect-DCH-SpontaneousRespirationOnset-Observation-1.valueQuantity  | Optional                    |
| APGAR Score (1 Minute)              | CareConnect-DCH-APGARScore-Observation-1.valueRange                 | Mandatory                   |
| APGAR Score (5 Minute)              | CareConnect-DCH-APGARScore-Observation-1.valueRange                  | Mandatory                   |
| APGAR Score (10 Minute)             | CareConnect-DCH-APGARScore-Observation-1.valueRange                | Optional                    |
| Put To Breast                       | CareConnect-DCH-PutToBreastIndicator-Observation-1.code                  | Required                    |
| Identical Twin Indicator		      | CareConnect-DCH-FraternalTwinIndicator-Observation-1.code               | Optional                    |







### Example XML ###

```xml
<QuestionnaireResponse xmlns="http://hl7.org/fhir"/>
<id value="9fa0541c-67a2-4946-a7e3-ef3c4a8991f1"/>
	<meta>
		<profile value="https://fhir.nhs.uk/STU3/StructureDefinition/EOL-FunctionalStatus-QuestionnaireResponse-1"/>
	</meta>
	<status value="completed"/>
	<subject>
		<reference value="https://demographics.spineservices.nhs.uk/STU3/CareConnect-Patient-1/6101231234"/> 
	</subject>
	<author>
		<reference value="https://directory.spineservices.nhs.uk/CareConnect-Practitioner-1/12345678"/>
	</author>
	<item>
		<linkId value="functionalStatusType"/>
		<text value="Functional StatusType"/>
		<answer>
			<valueCoding>
				<system value="http://snomed.info/sct"/>
				<code value="761869008"/>
				<display value="Karnofsky Performance Status score (observable entity)"/>
			</valueCoding>
		</answer>
	</item>
	<item>
		<linkId value="functionalStatusValue"/>
		<text value="Functional Status Value"/>
		<answer>
			<valueString value="50"/>
		</answer>
	</item>
	<item>
		<linkId value="functionalStatusText"/>
		<text value="Functional Status Text"/>
		<answer>
			<valueString value="Considerable assistance and frequent medical care required"/>
		</answer>
	</item>
</QuestionnaireResponse>

```


