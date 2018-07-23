---
title: Workflow | Encounter | Prognosis
keywords: usecase, encounter, prognosis
tags: [rest, fhir, workflow,api]
sidebar: foundations_sidebar
permalink: api_eol_management_encounter_prognosis.html
summary: An interaction between a patient and healthcare provider(s) for the purpose of providing healthcare service(s) or assessing the health status of a patient.
---
{% include custom/search.warnbanner.html %}

{% include custom/fhir.STU3.reference.html resource="Encounter" page="CareConnect-EOL-Prognosis-Encounter-1" fhirname="Encounter" fhirlink="encounter.html" content="User Stories" userlink="engage_endoflife.html" %}

## Patient Scenario ##

Prognosis

A prognosis is a clinical decision made during an encounter to estimate a patient’s life expectancy. The prognosis is then captured as an observation in coded and textual format. 

Persons or organisations aware of the prognosis are also captured in the encounter participants.  There may be times when someone is subsequently made aware of the prognosis some time after the encounter. On these occasions, an update record will be actioned on the encounter to include this information.

{% include custom/under.construction.html %}