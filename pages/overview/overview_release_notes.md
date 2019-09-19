---
title: Release Notes
keywords: development, versioning
tags: [development]
sidebar: overview_sidebar
permalink: overview_release_notes.html
summary: Summary release notes of the versions released in End of Life API Implementation Guide
---

{% include important.html content="This site is under active development by NHS Digital and is intended to provide all the technical resources you need to successfully develop the End of Life API. This project is being developed using an agile methodology so iterative updates to content will be added on a regular basis." %}


## 1.2.1-alpha ##

- The End of Life Care API’s table in the Resources Overview page, has been altered, to now include links to the Atomic Units and corrections to the FHIR profile links.


## 1.2.0-alpha ##

- Atomic Units navigation section name changed to 'Resources' and API Guidance sub-section removed.
- Design & Build (APIs) section added to spec. Includes Overview, API Guidance and Open Source sub-sections:
  - Provides an overview of how the FHIR STU3 Resources that compose the EoLC message could be packaged together into an API
  - The Atomic Units concept has been represented as Questionnaire in a QuestionnaireResponse in the suggestion for an API.
  - API Guidance provides overview of the FHIR STU3 Resources that are required to build the required API messaging using the Questionnaire/ QuestionnaireResponse approach

## 1.1.0-alpha ##

Changes to the API to reflect the EoL National Minimum Dataset v2.2 requirements.

- <b>Advance Treatment Preferences:</b> Profiles added to atomic unit:
  - EOL-ADRT-Flag-1: supports Advance Decision to refuse treatment data items
    - Binds to EOL-AdvanceDecisionToRefuseTreatment-1 valueset
  - CareConnect-EOL-Procedure-1: supports Anticipatory medicines data items
    - Binds to EOL-IssueOfAnticipatoryMedicines-1 valueset
  - CareConnect-Location-1: supports Location of anticipatory medicines/just in case box data item 
- <b>Consent:</b> consentDecisionDetails(extension): EOL-ConsentDecisionSnCT-1 valueSet changes to reflect v2.2 requirements.
- <b>General:</b> Clearer guidance on how to implement the codeableConcept.coding element within End of Life API

<!--
<b>Value Sets:</b>

CONFIRM ALL V/S

<b>Extensions:</b>

CONFIRM ALL Extensions

-->







<!--
## 1.2.0-alpha ##

Advance Treatment Preferences updated:

- Advance Decision to refuse treatment data item added
- Anticipatory medicines data item added

Additional notes data can now be captured in code.coding.text data elements where the atomic unit supports this functionality

https://fhir.nhs.uk/STU3/ValueSet/EOL-ConsentDecisionSnCT-1 Value Set updated. 


## 1.1.0-alpha ##

Update to Advance Treatment Prefernces Atomic Unit to add the following additional data items:

## Profiles ##

- Issue of Anticipatory Medicines
- Advance Decision to refuse Treatment (ADRT)


https://fhir.nhs.uk/STU3/StructureDefinition/Extension-EOL-ConsentDecisionDetails-1

Added an additional extension - consentAdditionalNotes

https://fhir.nhs.uk/STU3/StructureDefinition/EOL-Prognosis-ClinicalImpression-1

New extension added to prognosisCodeableConcept for additional notes.

CareConnect-ProblemHeader-Condition-1 has been replaced with EOL-DisabilitiesProblemHeader-Condition-1 to allow the addition of the Extension-EOL-AdditionalNotes-1 which is not permitted under CareConnect rules.
CareConnect-ProblemList-1 has been replaced with EOL-DisabilitiesProblemList-1 to permit reference to EOL-DisabilitiesProblemHeader-Condition-1 via the item.entry element.

https://fhir.nhs.uk/STU3/StructureDefinition/EOL-DisabilitiesProblemHeader-Condition-1


## Value Sets ##

The following value set has been added to the API to support new data items added for ATP atomic unit:

https://fhir.nhs.uk/STU3/ValueSet/EOL-AdvanceDecisionToRefuseTreatment-1"

## Extensions ##
-->

## 1.0.0-alpha ##


- Initialization of the FHIR&reg; End of Life API implementation guide.