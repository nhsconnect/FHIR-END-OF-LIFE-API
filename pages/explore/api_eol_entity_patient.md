---
title: Individuals | Patient - End of Life
keywords: getcarerecord, structured, rest, patient
tags: [rest, fhir, identification,api]
sidebar: accessrecord_rest_sidebar
permalink: api_eol_entity_patient.html
summary: Demographics and other administrative information about an individual receiving care or other health-related services.
toc: false
---

{% include custom/search.warnbanner.html %}

{% include custom/fhir.reference.html resource="Patient" page="CareConnect-Patient-1" fhirname="Patient" fhirlink="patient.html" content="User Stories" userlink="engage_endoflife.html" %}

## Communication ##

It is proposed to use the exisiting extension under the Care Connect Patient profile which covers the Communication requirements. the profile can be viewed here: 
<a href="https://fhir.hl7.org.uk/STU3/StructureDefinition/Extension-CareConnect-NHSCommunication-1">NHS communication preferences</a>

## Contacts ##

It is proposed to use the exisiting element under the Care Connect Patient profile named Patient.contact which can be used to record End of Life contacts.

## Read ##

<div markdown="span" class="alert alert-success" role="alert">
GET [baseUrl]/Patient/[id]</div>

{% include custom/read.response.html resource="Patient" content="" %}


