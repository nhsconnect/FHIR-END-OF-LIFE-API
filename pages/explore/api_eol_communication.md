---
title: Communication Atomic Unit
keywords: usecase, language, interpreter
tags: [rest, fhir, workflow,api]
sidebar: foundations_sidebar
permalink: api_eol_communication.html
summary: Atomic Unit to capture the communication preferences for a patient.
toc: false
---
{% include custom/search.warnbanner.html %}

### Communication ###

### WARNING: EOL PROFILES POINTING TO TEST SERVER FHIR-TEST.NHS.UK ###

The following FHIR profiles are used to form the communication Atomic Unit:

- [EOL-Patient-1](https://fhir-test.nhs.uk/STU3/StructureDefinition/EOL-Patient-1.xml)
- [Extension-EOL-NHSCommunication-1](https://fhir-test..nhs.uk/STU3/StructureDefinition/Extension-EOL-NHSCommunication-1)


### Communication data item mapping to FHIR profiles ###

The demographics data items are fulfilled by elements within the FHIR resources listed below:

| EOL Data Item                       | FHIR resource element                                                   | Mandatory/Required/Optional |
|-------------------------------------|-------------------------------------------------------------------------|-----------------------------|
| Languages Spoken			  | EOL-Patient-1.nhsCommunication (Extension) 							| Optional |
| Language Spoken Code		  | nhsCommunication.language.code  												| Optional |
| Language Spoken Text		  | nhsCommunication.language.code.text												| Mandatory |
| Language Comment 			  | nhsCommunication.languageComment												| Optional |
| Type of Interpretation Code | nhsCommunication.modeofCommunication.code 										| Optional |
| Type of Interpretation Text | nhsCommunication.modeofCommunication.code.text 								    | Optional |
| Interpreter Required        | nhsCommunication.interpreterRequired									        | Optional |


### Communication Example XML ###

<script src="https://gist.github.com/IOPS-DEV/f973859cac9ffe23d2563494a948dce7.js"></script>



