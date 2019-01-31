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

The following FHIR profiles are used to form the Advance Treatment Preferences Atomic Unit:

- [EOL-Patient-1](https://fhir.nhs.uk/STU3/StructureDefinition/EOL-Patient-1)
- [CareConnect-Organization-1](https://fhir.hl7.org.uk/STU3/StructureDefinition/CareConnect-Organization-1)
- [CareConnect-Practitioner-1](https://fhir.hl7.org.uk/STU3/StructureDefinition/CareConnect-Practitioner-1) (EOL mandates name.text)
- [CareConnect-PractitionerRole-1](https://fhir.hl7.org.uk/STU3/StructureDefinition/CareConnect-PractitionerRole-1)
- [EOL-Procedure-1](https://fhir.nhs.uk/STU3/StructureDefinition/EOL-Procedure-1) **NOT BUILT. TBD**
- [EOL-Location-1](https://fhir.nhs.uk/STU3/StructureDefinition/EOL-Location-1) **NOT BUILT. TBD**
- [EOL-ATPProblemList-List-1](https://fhir.nhs.uk/STU3/StructureDefinition/EOL-ATPProblemList-List-1)
- [EOL-ATPProblemHeader-Condition-1](https://fhir.nhs.uk/STU3/StructureDefinition/EOL-ATPProblemHeader-Condition-1)
- [EOL-ATP-CarePlan-1](https://fhir.nhs.uk/STU3/StructureDefinition/EOL-ATP-CarePlan-1)
- [EOL-ATP-Flag-1](https://fhir.nhs.uk/STU3/StructureDefinition/EOL-ATP-Flag-1)


### Advance Treatment Preferences data item mapping to FHIR profiles ###

The Advance Treatment Preferences data items are fulfilled by elements within the FHIR resources listed below:

| EOL Data Item                       | FHIR resource element                                                   | Mandatory/Required/Optional |
|-------------------------------------|-------------------------------------------------------------------------|-----------------------------|
| Date of Change in List			  | EOL-ATP-ProblemList-List.date				| Mandatory |
| Problem or Condition				  | EOL-ATPProblemList-List.entry.item.reference | Optional |
| Details of Problem or Condition     | EOL-ATPProblemHeader-Condition-1.code.text           | Mandatory                   |
| Treatment Level					  | EOL-ATP-CarePlan-1.activity.detail.code.text	| Optional |
| Intervention						  | EOL-ATP-CarePlan-1.activity.detail.description  | Optional |
| ReSPECT Care Priority  			  | 												| Optional |
| 									  | Extension.respectPriorityScale.valueInteger		| Mandatory |
|									  | Extension.respectPriorityScaleStatement.valueString			| Optional |
| Professional recording changes to List of Problems and Interventions | EOL-ATP-ProblemList-1.source | Mandatory |
| Advance Decision to Refuse Treatment Coded | EOL-ATP-Flag-1.code	| Optional |
| Advance Decision to Refuse Treatment Additional Notes | EOL-ATP-Flag-1.code.text	| Optional |
| Date of Advance Decision to Refuse Treatment | EOL-ATP-Flag-1.period.start | Mandatory |
| Issue of Anticipatory Medicines Code		| EOL-Procedure-1.code | Optional |** TO BE BUILT **
| Issue of Anticipatory Medicines Additional Note	| EOL-Procedure-1.code.text | Optional |** TO BE BUILT **
| Location of Anticipatory Medicines	| CareConnect-Location-1.name | Optional |


### Advance Treatment Preferences ERD ###

<img src="images/erd/atp-erd.svg" style="width:80%;max-width: 80%;">

### Problem List Example XML ###

<script src="https://gist.github.com/IOPS-DEV/68d09895595b33dc1370560a8b287f39.js"></script>

### Problem Header Condition Example XML ###

<script src="https://gist.github.com/IOPS-DEV/16afab712dda04db1af18dfa1d9f722e.js"></script>

### Care Plan Example XML ###

<script src="https://gist.github.com/IOPS-DEV/f82218432c8103a8b73c2481733d5039.js"></script>

### Flag Example XML ###

<script src="https://gist.github.com/IOPS-DEV/d6b7f1d06503ae08f620ec46faabfc75.js"></script>

### Care Connect Profiles ###

Where possible, Care Connect profiles have been used to develop the End of Life API. On this occasion it has not been possible to do this. The table below highlights the Care Connect profile(s) replaced with a bespoke version and the rationale behind this.

| Care Connect Profile 				    | Rationale for Change					   | New Component Required					 	   			  |
|---------------------------------------|------------------------------------------|----------------------------------------------------------|
| CareConnect-List-1 and				| ReSPECT scale complex extension required | extension.resPECTScale   			 					  |
| CareConnect-ProblemList-1	    		|  			 							   | 	     												  |
| CareConnect-Condition-1 and			| Problem description is mandatory	       | Change of cardinality to 'code' element from 0..1 to 1..1  |
| CareConnect-ProblemHeader-Condition-1 | 										   | 														  |
| CareConnect-Procedure-1				| Additional notes extension required	   | extension-EOL-Procedure-1									|
| CareConnect-

End of Life will engage with the healthcare community and INTEROPen in the future to propose these changes to the Care Connect profiles(s).