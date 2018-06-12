---
title: Workflow | Flag | CPR Status
keywords: usecase, flag, cpr, status
tags: [rest, fhir, workflow,api]
sidebar: foundations_sidebar
permalink: api_eol_management_flag_cprstatus.html
summary: Workflow Flag for CPR Status
---

{% include custom/search.warnbanner.html %}

{% include custom/fhir.STU3.reference.html resource="Flag" page="CareConnect-EOL-CPRStatus-Flag-1" fhirname="Flag" fhirlink="flag.html" content="User Stories" userlink="engage_endoflife.html" %}

## Patient Scenario ##

The CPR Status is the result of a clinical encounter, clinicians will assess the clincal benefit of providing CPR to the patient. Patient can make an advance decision to refuse treatment. The clinician decides the status of the flag during an encounter and also makes some observations about the patient. 

The Date time of CPR Status is captured as well as the review date, this is an ioptional entry to provide an agreed review date for the status. Blank implies that this is an indefinite decision. A CPR status that has gone beyond the review date in then invalid.

All none clinical participants are captured who may have had direct involvement or are notified of the decision at a later date. 

Persons involved in discussion, Persons or organisations made aware of the decision, Professionals Involved In Decision, Professional endorsing this CPR status

## 1. Read ##

<div markdown="span" class="alert alert-success" role="alert">
GET /Flag/[id]</div>

Return a single `Flag` for the specified id


## 2. Search Parameters ##

<div markdown="span" class="alert alert-success" role="alert">
GET /Flag?[searchParameters]</div>

Search for all flag (alert) resources for a patient. Fetches a bundle of all `Flag` resources for the specified patient.

{% include custom/search.parameters.html resource="Flag"     link="flag.html#search" %}


| Name | Type | Description | SHALL | Path |
|------|------|-------------|-------|------|
| `date` | `date` | Time period when flag is active |  | Flag.period |
| `patient` | `reference` | The patient for the vaccination record | Y | Flag.subject <br>(Patient) |
| `status` | `token` | Flag status: active, inactive or entered-in-error | Y | Flag.status |


{% include custom/search.patient.html para="2.1." content="Flag" %}

{% include custom/search.status.html para="2.2." content="Flag" options="active | inactive | entered-in-error" selected="active" %}
