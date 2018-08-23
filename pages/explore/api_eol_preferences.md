---
title: Preferences Atomic Unit
keywords: usecase, preferences
tags: [rest, fhir, workflow,api]
sidebar: foundations_sidebar
permalink: api_eol_preferences.html
summary: Atomic Unit to capture the Preferences for a patient.
toc: false
---
{% include custom/search.warnbanner.html %}


### Preferences ###


The following FHIR profiles are used to form the Preferences Atomic Unit:

- [EOL-Patient-1](https://fhir.nhs.uk/STU3/StructureDefinition/EOL-Patient-1.xml)
- [EOL-Practitioner-1](https://fhir.nhs.uk/STU3/StructureDefinition/EOL-Practitioner-1.xml)
- [EOL-Preferences-QuestionnaireResponse-1] (https://fhir.nhs.uk/STU3/StructureDefinition/EOL-Preferences-QuestionnaireResponse-1.xml)

### Preferences data item mapping to FHIR profiles ###

The preferences data items are fulfilled by elements within the FHIR resources listed below:

| EOL Data Item                       | FHIR resource element                                                   | Mandatory/Required/Optional |
|-------------------------------------|-------------------------------------------------------------------------|-----------------------------|
| Preferred Place of Death			  |																			| Optional |
| 									  | EOL-Preferences-QuestionnaireResponse-1.item.preferredPlaceOfDeathCoded | Optional |
| 									  | EOL-Preferences-QuestionnaireResponse-1.item.preferredPlaceOfDeathText  | Mandatory |
| Preferences and Wishes			  | EOL-Preferences-QuestionnaireResponse-1.item.preferencesAndWishes		| Optional |
| Domestic Access and Information	  | EOL-Preferences-QuestionnaireResponse-1.item.domesticAccessAndInformation | Optional |
| Date of Preferences (create/update) | EOL-Preferences-QuestionnaireResponse-1.item.authored					| Mandatory |
| Professional Recording Preferences  | EOL-Preferences-QuestionnaireResponse-1.item.author						| Mandatory |

### Preferences Example XML ###

<script src="https://gist.github.com/IOPS-DEV/397ffb0aa86e6d0de65c7c952f92d6c4.js"></script>



