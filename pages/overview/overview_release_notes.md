---
title: Release Notes
keywords: development, versioning
tags: [development]
sidebar: overview_sidebar
permalink: overview_release_notes.html
summary: Summary release notes of the versions released in End of Life API Implementation Guide
---

{% include important.html content="This site is under active development by NHS Digital and is intended to provide all the technical resources you need to successfully develop the End of Life API. This project is being developed using an agile methodology so iterative updates to content will be added on a regular basis." %}

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


## 1.0.0-alpha ##


- Initialization of the FHIR&reg; End of Life API implementation guide.