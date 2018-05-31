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
<td><a href="api_eol_entity_patient.html">EOL Patient (L2)</a></td>
</tr>
<tr>
<td>Contacts</td>
<td>Patient</td>
<td><a href="api_eol_entity_patient.html">EOL Patient (L2)</a></td>
</tr>
<tr>
<td>LPA Lasting Power of Attorney</td>
<td>Related Person</td>
<td><a href="api_eol_entity_lpa_relatedperson.html">EOL LPA Related Person (L3)</a></td>
</tr>
<tr>
<td>Consent</td>
<td>Consent<br/>Practitioner<br/>Practitioner Role</td>
<td><a href="api_eol_security_consent.html">EOL Consent (L3)*</a><br/>
 <a href="api_eol_individuals_practitioner.html">EOL Practitioner (L2)</a><br/>
 <a href="api_eol_individuals_practitionerrole.html">EOL Practitioner Role (L2)</a></td>
</tr>
<tr>
<td>CPR Status</td>
<td>Flag<br/>Encounter</td>
<td><a href="api_eol_management_flag_cprstatus.html">EOL CPR Status Flag (L3)</a><br/>
<a href="api_eol_management_encounter_cprstatus.html">EOL CPR Status Encounter (L3)</a></td>
</tr>
<tr>
<td>Advance Treatment Preferences</td>
<td>Conditions (Problem)<br/>Practitioner<br/>Practioner Role</td>
<td><a href="api_eol_summary_condition.html">EOL ATP Condition (L3)*</a><br/>
<a href="api_eol_individuals_practitioner.html">EOL Practitioner (L2)</a><br/>
<a href="api_eol_individuals_practitionerrole.html">EOL Practitioner Role (L2)</a></td>
</tr>
<tr>
<td>End of Life Register</td>
<td>Flag</td>
<td><a href="api_eol_management_flag_register.html">EOL Register Flag (L3)</a></td>
</tr>
<tr>
<td>Prognosis</td>
<td>Encounter<br/>Observation</td>
<td><a href="api_eol_management_encounter_prognosis.html">EOL Prognosis Encounter (L3)</a><br/>
<a href="api_eol_diagnostics_prognosis_observation.html">EOL Prognosis Observation (L3)</a></td>
</tr>
<tr>
<td>Disability</td>
<td>Conditions (Problem)<br/>Practitioner<br/>Practioner Role</td>
<td><a href="api_eol_summary_disability_condition.html">EOL Disability Condition (L3)*</a><br/>
<a href="api_eol_individuals_practitioner.html">EOL Practitioner (L2)</a><br/>
<a href="api_eol_individuals_practitionerrole.html">EOL Practitioner Role (L2)</a></td>
</tr>
<tr>
<td>Functional Status</td>
<td>Conditions (Problem)<br/>Practitioner<br/>Practioner Role</td>
<td><a href="api_eol_summary_functional_condition.html">EOL Functional Status Condition (L3)*</a><br/>
<a href="api_eol_individuals_practitioner.html">EOL Practitioner (L2)</a><br/>
<a href="api_eol_individuals_practitionerrole.html">EOL Practitioner Role (L2)</a></td>
</tr>
<tr>
<td>Preferences</td>
<td>Encounter<br/>Location</td>
<td><a href="api_eol_management_encounter_preferences.html">EOL Preferences Encounter (L3)*</a><br/>
<a href="api_eol_entities_location_preferences.html">EOL Preferences Location (L3)*</a></td>
</tr>
<tr>
<td>Other Docs</td>
<td>Document Reference</td>
<td><a href="api_eol_documents_documentreference.html">EOL Document Reference (L3)</a></td>
</tr>
</table>