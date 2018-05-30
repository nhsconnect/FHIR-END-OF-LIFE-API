---
title: Resources Overview
keywords: getcarerecord, structured, rest, resource
tags: [rest,fhir,api]
sidebar: foundations_sidebar
permalink: explore.html
summary: "Overview of the Resources section"
---

{% include custom/search.warnbanner.html %}

## 1. End of Life Recording ##

This page provides an overview of the FHIR STU3 Resources that are required to build the required API messaging. Each link will take you to the resource page detail with a link to the Structure Defnitions of each resource.

## 2. End of Life Care API's ###

<table style="min-width:100%;width:100%">
<tr id="clinical">
<th style="width:33%;">EOL Requirement</th>
<th style="width:33%;">FHIR Resource(s)</th>
<th style="width:33%;">&nbsp;</th>
</tr>
<tr id="clinical">
<td>Communication</td>
<td>Patient</td>
<td><a href="api_eol_entity_patient.html">EOL Patient</a></td>
</tr>
<tr>
<td>Contacts</td>
<td>Patient</td>
<td><a href="api_eol_entity_patient.html">EOL Patient</a></td>
</tr>
<tr>
<td>LPA Lasting Power of Attorney</td>
<td>Related Person</td>
<td><a href="api_eol_entity_lpa_relatedperson.html">EOL LPA Related Person</a></td>
</tr>
<tr>
<td>Consent</td>
<td>Consent<br/>Practitioner<br/>Practitioner Role</td>
<td><a href="api_eol_security_consent.html">EOL Consent</a><br/>
 <a href="api_eol_individuals_practitioner.html">EOL Practitioner</a><br/>
 <a href="api_eol_individuals_practitionerrole.html">EOL Practitioner Role</a></td>
</tr>
<tr>
<td>CPR Status</td>
<td>Flag<br/>Encounter</td>
<td><a href="api_eol_management_flag_cprstatus.html">EOL CPR Status Flag</a><br/>
<a href="api_eol_management_encounter_cprstatus.html">EOL CPR Status Encounter</a></td>
</tr>
<tr>
<td>Advance Treatment Preferences</td>
<td>Conditions (Problem)<br/>Practitioner<br/>Practioner Role</td>
<td><a href="api_eol_summary_condition.html">EOL ATP Condition</a><br/>
<a href="api_eol_individuals_practitioner.html">EOL Practitioner</a><br/>
<a href="api_eol_individuals_practitionerrole.html">EOL Practitioner Role</a></td>
</tr>
<tr>
<td>Prognosis</td>
<td>Flag<br/>Encounter<br/>Observation</td>
<td><a href="api_eol_management_flag_register.html">EOL Register Flag</a><br/>
<a href="api_eol_management_encounter_prognosis.html">EOL Prognosis Encounter</a><br/>
<a href="api_eol_diagnostics_prognosis_observation.html">EOL Prognosis Observation</a></td>
</tr>
<tr>
<td>Disability</td>
<td>Conditions (Problem)<br/>Practitioner<br/>Practioner Role</td>
<td><a href="api_eol_summary_disability_condition.html">EOL Disability Condition</a><br/>
<a href="api_eol_individuals_practitioner.html">EOL Practitioner</a><br/>
<a href="api_eol_individuals_practitionerrole.html">EOL Practitioner Role</a></td>
</tr>
<tr>
<td>Functional Status</td>
<td>Conditions (Problem)<br/>Practitioner<br/>Practioner Role</td>
<td><a href="api_eol_summary_functional_condition.html">EOL Functional Status Condition</a><br/>
<a href="api_eol_individuals_practitioner.html">EOL Practitioner</a><br/>
<a href="api_eol_individuals_practitionerrole.html">EOL Practitioner Role</a></td>
</tr>
<tr>
<td>Preferences</td>
<td>Encounter<br/>Location</td>
<td><a href="api_eol_management_encounter_preferences.html">EOL Preferences Encounter</a><br/>
<a href="api_eol_entities_location_preferences.html">EOL Preferences Location</a></td>
</tr>
<tr>
<td>Other Docs</td>
<td>Document Reference</td>
<td><a href="api_eol_documents_documentreference.html">EOL Document Reference</a></td>
</tr>
</table>