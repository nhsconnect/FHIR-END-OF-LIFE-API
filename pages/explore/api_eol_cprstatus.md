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

The “CPR Status” collection of data is used to transmit the kind of data often recorded on DNACPR forms and also recorded as part of the ReSPECT form.  This collection of data reflects a clinical decision that has been made.  The decision may be made by one or more professionals in discussion with the patient and/or their representatives.  Once the decision is made, it can also be shared after the time of decision with other individuals that were not present for the discussion.


The following FHIR profiles are used to form the CPR Status Atomic Unit:

- [EOL-Patient-1](https://fhir-test.nhs.uk/STU3/StructureDefinition/EOL-Patient-1)
- [CareConnect-Organization-1](https://fhir.hl7.org.uk/STU3/StructureDefinition/CareConnect-Organization-1)
- [CareConnect-Practitioner-1](https://fhir.hl7.org.uk/STU3/StructureDefinition/CareConnect-Practitioner-1)
- [CareConnect-PractitionerRole-1](https://fhir.hl7.org.uk/STU3/StructureDefinition/CareConnect-PractitionerRole-1)
- [EOL-CPRStatus-QuestionnaireResponse-1](https://fhir.nhs.uk/STU3/StructureDefinition/EOL-CPRStatus-QuestionnaireResponse-1)

### CPR Status data item mapping to FHIR profiles ###

The CPR Status data items are fulfilled by elements within the FHIR resources listed below:

| EOL Data Item                       | FHIR resource element                                                   | Mandatory/Required/Optional |
|-------------------------------------|-------------------------------------------------------------------------|-----------------------------|
| CPR Status        		       | EOL-CPRStatus-Flag-1.code           | Mandatory                   |
| Reason for CPR status | EOL-CPRStatus-QuestionnaireResponse-1.reasonForCPRStatus | Optional |
| CPR Status Mental Capacity | EOL-CPRStatus-QuestionnaireResponse-1.cPRStatusMentalCapacity | Optional
| Date Time of CPR Status | EOL-CPRStatus-Flag-1.period.start| Mandatory
| Review Date | EOL-CPRStatus-Flag-1.period.end| Optional
| Persons Involved in Discussion | EOL-CPRStatus-QuestionnaireResponse-1.personsInvolvedInDiscussion (Extension)| Optional
| Persons or Organisations Made Aware of the Decision | EOL-CPRStatus-QuestionnaireResponse-1.awarenessOfDecision (Extension)| Optional
| Professionals Involved in Decision | EOL-CPRStatus-QuestionnaireResponse-1.professionalsInvolvedInDecision| Optional
| Professional Recording the CPR status | EOL-CPRStatus-Flag-1.author | Mandatory
| Professional Endorsing this CPR status | EOL-CPRStatus-QuestionnaireResponse-1.professionalEndorsingStatus | Optional

### CPR Status ERD ###

<img src="images/erd/cpr-erd.svg" style="width:80%;max-width: 80%;">

### CPR Status Examples XML ###

<script src="https://gist.github.com/IOPS-DEV/48b4578c9c7e75cdeb5630b100723d70.js"></script>

<script src="https://gist.github.com/IOPS-DEV/c5aa7323383044de66673dca7ad2644b.js"></script>


