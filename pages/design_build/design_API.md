---
title: Overview
keywords: foundations
tags: [fhir,rest]
sidebar: foundations_sidebar
permalink: design_API.html
summary: "Design and Build APIs guidance "
---


## 1. API ##

This page provides an overview of the FHIR STU3 Resources that are required to build the required API messaging. Each link will take you to the resource page detail with a link to the Structure Definitions of each resource.

The previous Atomic Units concept has been moved to the Design & Build section where the API is defined.

## 2. API calls - ALL ##

The simplified call to return an EoLC message follows a RESTful FHIR Request, which

GET {BASE_URL}/QuestionnaireResponse?_id={id}&_include=*

The Questionnaire gist (also known as the spreadsheet in FHIR format) returns:
https://gist.github.com/KevinMayfield/5b15657ab584a5326c2e5fd84e2a68b8

This simplifies building the payload+api while also putting rigid rules on the payload. The rules have been formed with the EoLC project team.

UPDATE required - An example payload response (the payload conforms to the definition in the Questionnaire)

https://gist.github.com/KevinMayfield/b0b68c2160c218a330996ff7318cf4d4

The queries for the api can be:

http://PROVIDER/ccri-fhir/STU3/QuestionnaireResponse?_id=28&_include=*

http://PROVIDER/ccri-fhir/STU3/QuestionnaireResponse?patient=1210&questionnaire:identifier=https://fhir.nhs.uk/STU3/Questionnaire|CareConnect-EOLC-1&_include=*

The supports the standard operations in https://www.hl7.org/fhir/stu3/questionnaire-operations.html

## 3. API calls - NONE ##

Calling a blank EOLC QuestionnaireResponse payload from the Questionnaire.


## 4. [COMING SOON] API calls - Partial resources ##

COMING SOON - The API can also be called partially which matches the Atomic Units and calling invidual or combination of resources:
* Ability to return parts of the dataset (atomic units) as required. With Questionnaire the top level items will correspond to an atomic unit
* Ability to generate a EOL on demand. This can be based on the FHIR Questionnaire operation $populate https://www.hl7.org/fhir/stu3/questionnaire-operations.html#2.38.13.1


## 5. Extensibility ##

To support connection with NRLS the following could be used $populate and $populatehtml.
