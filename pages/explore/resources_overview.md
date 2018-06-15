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
<th style="width:33%;">FHIR Profile(s)</th>
</tr>
<tr id="clinical">
<td>EOL Record</td>
<td>Bundle</td>
<td><a href="api_eol_bundle.html">EOL Bundle -  PENDING</a></td>                                                                                                                       
</tr>
<tr>
<td>Communication</td>
<td>Patient</td>
<td><a href="api_eol_entity_patient.html">Care Connect Patient</a></td>
</tr>
<tr>
<td>Contacts</td>
<td>Patient</td>
<td><a href="api_eol_entity_patient.html">Care Connect Patient</a></td>
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
 <a href="api_eol_individuals_practitioner.html">Care Connect Practitioner</a><br/>
 <a href="api_eol_individuals_practitionerrole.html">Care Connect Practitioner Role</a></td>
</tr>
<tr>
<td>CPR Status</td>
<td>Flag<br/>Encounter<br/>Observation</td>
<td><a href="api_eol_management_flag_cprstatus.html">EOL CPR Status Flag</a><br/>
<a href="api_eol_management_encounter_cprstatus.html">Care Connect EOL CPR Status Encounter</a><br/>
<a href="api_eol_diagnostics_observation_cprstatus.html">EOL CPR Status Observation</a></td>
</tr>
<tr>
<td>End of Life Register</td>
<td>Flag</td>
<td><a href="api_eol_management_flag_register.html">EOL Register Flag</a></td>
</tr>
<tr>
<td>Prognosis</td>
<td>Encounter<br/>Observation</td>
<td><a href="api_eol_management_encounter_prognosis.html">Care Connect EOL  Prognosis Encounter</a><br/>
<a href="api_eol_diagnostics_observation_prognosis.html">EOL Prognosis Observation</a></td>
</tr>
<tr>
<td>Advance Treatment Preferences</td>
<td>Conditions (Problem)<br/>Questionnaire Response<br/>Practitioner<br/>Practioner Role</td>
<td><a href="api_eol_summary_atp_condition.html">Care Connect ATP Condition</a><br/>
 <a href="api_eol_diagnostics_questionnaireresponse.html">EOL Questionnaire Response</a><br/>
 <a href="api_eol_individuals_practitioner.html">Care Connect Practitioner</a><br/>
 <a href="api_eol_individuals_practitionerrole.html">Care Connect Practitioner Role</a></td>
</tr>
<tr>
<td>Disability</td>
<td>Conditions (Problem)<br/>List<br/>Practitioner<br/>Practioner Role</td>
<td><a href="api_eol_summary_disability_condition.html">Care Connect Disability Condition</a><br/>
<a href="api_eol_summary_disability_list.html">Care Connect Disability List</a><br/>
<a href="api_eol_individuals_practitioner.html">Care Connect Practitioner</a><br/>
<a href="api_eol_individuals_practitionerrole.html">Care Connect Practitioner Role</a></td>
</tr>
<tr>
<td>Functional Status</td>
<td>Questionnaire Response<br/>Practitioner<br/>Practioner Role</td>
<td><a href="api_eol_diagnostics_questionnaireresponse.html">EOL Questionnaire Response</a><br/>
<a href="api_eol_individuals_practitioner.html">Care Connect Practitioner</a><br/>
<a href="api_eol_individuals_practitionerrole.html">Care Connect Practitioner Role</a></td>
</tr>
<tr>
<td>Preferences</td>
<td>Questionnaire Response</td>
<td><a href="api_eol_diagnostics_questionnaireresponse.html">EOL Questionnaire Response</a></td>
</tr>
<tr>
<td>Other Docs</td>
<td>Document Reference</td>
<td><a href="api_eol_documents_documentreference.html">EOL Document Reference</a></td>
</tr>
</table>