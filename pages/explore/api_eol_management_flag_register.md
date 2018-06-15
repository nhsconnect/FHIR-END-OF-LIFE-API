---
title: Workflow | Flag | End of Life Register
keywords: usecase, flag, cpr, status
tags: [rest, fhir, workflow,api]
sidebar: foundations_sidebar
permalink: api_eol_management_flag_register.html
summary: Workflow Flag for End of Life Register
---

{% include custom/search.warnbanner.html %}

{% include custom/fhir.STU3.reference.html resource="Flag" page="EOL-Register-Flag-1" fhirname="Flag" fhirlink="flag.html" content="User Stories" userlink="engage_endoflife.html" %}

## Patient Scenario ##

End of Life Register

Whether the patient has been placed on the local end of life register.

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
