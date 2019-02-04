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

{% include custom/under.construction.html %}

### Functional Status ###

The patient’s functional status is recorded by clinicians during encounters with the patient and gives consumers of the data a general indication of the wellness of the patient. The status can be codified using either the Karnofsky scale or Electronic Frailty Index and there is a mandatory textual field for systems that do not store this data as a codeable concept.

The following FHIR profiles are used to form the Functional Status Atomic Unit:

- [EOL-Patient-1](https://fhir.nhs.uk/STU3/StructureDefinition/EOL-Patient-1)
- [CareConnect-Organization-1](https://fhir.hl7.org.uk/STU3/StructureDefinition/CareConnect-Organization-1)
- [CareConnect-Practitioner-1](https://fhir.hl7.org.uk/STU3/StructureDefinition/CareConnect-Practitioner-1) (EOL mandates name.text)
- [CareConnect-PractitionerRole-1](https://fhir.hl7.org.uk/STU3/StructureDefinition/CareConnect-PractitionerRole-1)
- [CareConnect-EOL-FunctionalStatus-Observation-1](https://fhir.nhs.uk/STU3/StructureDefinition/CareConnect-EOL-FunctionalStatus-Observation-1)

### Functional Status event data item mapping to FHIR profiles ###

The Functional Status data items are fulfilled by elements within the FHIR resources listed below:

| EOL Data Item                       | FHIR resource element                                                   | Mandatory/Required/Optional |
|-----------------------------------|-------------------------------------------------------------------------|-----------------------------|
| Functional Status Type			| EOL-FunctionalStatus-Observation-1.code | Mandatory |
| Functional Status Value			| EOL-FunctionalStatus-Observation-1.value or | Optional |
|									| EOL-FunctionalStatus-Observation-1.component.value[x] | Optional |
| Functional Satus Text				| EOL-FunctionalStatus-Observation-1.code.text | Mandatory |


### CareConnect-EOL-FunctionalStatus-Observation-1.Code (codeableConcept) Guidance ###

Where the sending system supports a terminology system:

* The codeableConcept.coding element MUST be populated with:
    * system: identity of the terminology system (e.g. SNOMED-CT) 
    * code: symbol in syntax defined by the system
	* display: representation defined by the system
* the codeableConcept.text field MUST be populated with the display value from the codeableConcept.coding.display element e.g. ‘Asthma (disorder)’
* the codeableConcept.text field MAY contain free text to capture more detail associated with the codeableConcept.coding.code e.g. ‘Patient uses blue inhaler to relieve symptoms’

Where the sending system does not support a terminology system:

* the codeableConcept.text field MUST be populated with a text description of the concept as a human readable narrative e.g ‘Asthma’. 
* the codeableConcept.text field MAY contain free text to capture more detail associated with the concept e.g. ‘Patient uses blue inhaler to relieve symptoms’.

<!--
### Functional Satus Text Guidance ###

Where the sending system supports a terminology system:

* The condition.code element MUST be populated with:
    * the terminology system (e.g. SNOMED-CT) 
    * code
	* display value
* the condition.code.text field MUST be populated with the display value from the condition.code.display element e.g. ‘Asthma (disorder)’
* the condition.code.text field MAY contain free text to capture more detail associated with the condition.code e.g. ‘Patient uses blue inhaler to relieve symptoms’

Where the sending system does not support a terminology system:

* the condition.code.text field MUST be populated with a text description of the condition as a human readable narrative e.g ‘Asthma’. 
* the condition.code.text field MAY contain free text to capture more detail associated with the condition e.g. ‘Patient uses blue inhaler to relieve symptoms’

-->

### Functional Status ERD ###

TODO

### Example XML ###

<script src="https://gist.github.com/IOPS-DEV/d03b3083ef79a8d2c146648a56838223.js"></script>


