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

CPR Status

The CPR Status is the result of an encounter where clinicians will assess the clinical benefit of providing CPR to the patient. Clinicians must consider the wishes of the patient where they have made a legal Advance Decision to Refuse Treatment. 

The underlying reason for the CPR decision and the mental capacity of the patient at the time of this decision-making are recorded as observations.

The date and time of CPR Status (encounter) is captured as well as (optionally) a review date.

The review date is an effective end date of this CPR status.  Once the review date has passed, this CPR status becomes invalid.  Where the review date is blank/null, this is an indefinite decision (at least until another CPR status is recorded with a later date and time.

All non-clinical participants are captured who may have had direct involvement, as are others who have been notified of the decision later.

Another, more senior, professional must endorse the status where the professional recording the status does not have enough seniority to make the final decision.

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
