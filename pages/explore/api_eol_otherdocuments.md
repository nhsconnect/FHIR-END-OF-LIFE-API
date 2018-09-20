---
title: Other Documents Atomic Unit
keywords: usecase, documents
tags: [rest, fhir, workflow,api]
sidebar: foundations_sidebar
permalink: api_eol_otherdocuments.html
summary: Atomic Unit to capture the Other Documents for a patient.
toc: false
---
{% include custom/search.warnbanner.html %}

### Other Documents ###

The dataset design makes no attempt to try to embed other formal end of life or advance care planning documents into the transmission of data.  However, for urgent and emergency care it is useful to know of the presence of formal paper documents, who generated them, and the location where they can be found.
The document list will be updated by care professionals as they produce the documents.


The following FHIR profiles are used to form the Other Documents Atomic Unit:

- [EOL-OtherDocuments-QuestionnaireResponse-1](https://fhir.nhs.uk/STU3/StructureDefinition/EOL-OtherDocuments-QuestionnaireResponse-1)

### Other Documents data item mapping to FHIR profiles ###

The Other Documents data items are fulfilled by elements within the FHIR resources listed below:

| EOL Data Item                       | FHIR resource element                                                   | Mandatory/Required/Optional |
|-------------------------------------|-------------------------------------------------------------------------|-----------------------------|
| Document Name						  | EOL-OtherDocuments-QuestionnaireResponse-1.documentName					| Mandatory			  |
| Document Location					  | EOL-OtherDocuments-QuestionnaireResponse-1.documentLocation				| Optional					  |
| Document Source					  | EOL-OtherDocuments-QuestionnaireResponse-1.documentSource				| Optional					  |	

### Other Documents ERD ###

TODO

### Other Documents Example XML ###

<script src="https://gist.github.com/IOPS-DEV/faa19f98c6d57bfe7d5fdf24511f33a9.js"></script>


