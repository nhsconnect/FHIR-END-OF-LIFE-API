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

### CPR Status Examples XML ###

<script src="https://gist.github.com/IOPS-DEV/48b4578c9c7e75cdeb5630b100723d70.js"></script>

<script src="https://gist.github.com/IOPS-DEV/c5aa7323383044de66673dca7ad2644b.js"></script>


