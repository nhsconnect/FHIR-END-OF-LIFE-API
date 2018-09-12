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

### WARNING: EOL PROFILES POINTING TO TEST SERVER FHIR-TEST.NHS.UK ###

The following FHIR profiles are used to form the Advance Treatment Preferences Atomic Unit:

- [EOL-Patient-1](https://fhir-test.nhs.uk/STU3/StructureDefinition/EOL-Patient-1)
- [CareConnect-Organization-1](https://fhir.hl7.org.uk/STU3/StructureDefinition/CareConnect-Organization-1)
- [CareConnect-Practitioner-1](https://fhir.hl7.org.uk/STU3/StructureDefinition/CareConnect-Practitioner-1)
- [CareConnect-PractitionerRole-1](https://fhir.hl7.org.uk/STU3/StructureDefinition/CareConnect-PractitionerRole-1)
- [EOL-ATP-List-1](https://fhir-test.nhs.uk/STU3/StructureDefinition/EOL-ATP-List-1)
- [EOL-ATP-Condition-1](https://fhir-test.nhs.uk/STU3/StructureDefinition/EOL-ATP-Condition-1)
- [EOL-AdvanceTreatmentpreferences-CarePlan-1](https://fhir-test.nhs.uk/STU3/StructureDefinition/EOL-AdvanceTreatmentPreferences-CarePlan-1)


### Advance Treatment Preferences data item mapping to FHIR profiles ###

The Advance Treatment Preferences data items are fulfilled by elements within the FHIR resources listed below:

| EOL Data Item                       | FHIR resource element                                                   | Mandatory/Required/Optional |
|-------------------------------------|-------------------------------------------------------------------------|-----------------------------|
| Date of Change in List			  | EOL-ATP-List.date				| Mandatory |
| Problem or Condition				  | EOL-ATP-List.entry.item.reference | Optional |
| Details of Problem or Condition     | EOL-ATP-Condition-1.code.text           | Mandatory                   |
| Treatment Level					  | EOL-ATP-CarePlan-1.activity.detail.code.text	| Optional |
| Intervention						  | EOL-ATP-CarePlan-1.activity.detail.description  | Optional |
| ReSPECT Care Priority  			  | 												| Optional |
| 									  | Extension.respectPriorityScale.valueInteger		| Mandatory |
|									  | Extension.respectPriorityScaleStatement.valueString			| Optional |
| Professional recording changes to List of Problems and Interventions | EOL-ATP-List-1.source | Mandatory |

### Advance Treatment Preferences ERD ###

TODO

### List Example XML ###

<script src="https://gist.github.com/IOPS-DEV/68d09895595b33dc1370560a8b287f39.js"></script>

### Condition Example XML ###

<script src="https://gist.github.com/IOPS-DEV/16afab712dda04db1af18dfa1d9f722e.js"></script>

### Care Plan Example XML ###

<script src="https://gist.github.com/IOPS-DEV/f82218432c8103a8b73c2481733d5039.js"></script>

### Care Connect Profiles ###

Where possible, Care Connect profiles have been used to develop the End of Life API. On this occasion it has not been possible to do this. The table below highlights the Care Connect profile(s) replaced with a bespoke version and the rationale behind this.

| Care Connect Profile 				    | Rationale for Change					   | New Component Required					 	   			  |
|---------------------------------------|------------------------------------------|----------------------------------------------------------|
| CareConnect-List-1 and				| ReSPECT scale complex extension required | extension.resPECTScale   			 					  |
| CareConnect-ProblemList-1	    		|  			 							   | 	     												  |
| CareConnect-Condition-1 and			| Problem description is mandatory	       | Change of cardinality to 'code' element from 0:1 to 1:1  |
| CareConnect-ProblemHeader-Condition-1 | 										   | 														  |

End of Life will engage with the healthcare community and INTEROPen in the future to propose these changes to the Care Connect profiles(s).