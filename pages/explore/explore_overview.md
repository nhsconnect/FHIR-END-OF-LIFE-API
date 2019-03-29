---
title: Resources Overview
keywords: getcarerecord, structured, rest, resource
tags: 
sidebar: foundations_sidebar
permalink: explore.html
summary: "Overview of the Resources section"
---

{% include custom/search.warnbanner.html %}

## 1. End of Life Recording ##

This page provides an overview of the FHIR STU3 Resources that are required to build the required API messaging. Each link will take you to the resource page detail with a link to the Structure Definitions of each resource.

The previous Atomic Units concept has been moved to the Design & Build section where the API is defined.

## 2. End of Life Care API's ###

<table style="min-width:100%;width:100%">
<tr id="clinical">
<th style="width:33%;">EOL Requirement</th>
<th style="width:33%;">FHIR Resource(s)</th>
<th style="width:33%;">FHIR Profile(s)</th>
</tr>
<tr>
<td>Communication</td>
<td>Patient</td>
<td><a href="api_eol_entity_patient.html">CareConnect-Patient-1</a></td>
</tr>
<tr>
<td>Contacts</td>
<td>Patient</td>
<td><a href="api_eol_entity_patient.html">CareConnect-Patient-1</a></td>
</tr>
<tr>
<td>LPA Lasting Power of Attorney</td>
<td>Related Person</td>
<td><a href="api_eol_entity_lpa_relatedperson.html">EOL-LPARelatedPerson-1</a></td>
</tr>
<tr>
<td>Consent</td>
<td>Consent<br/>Practitioner<br/>Practitioner Role</td>
<td><a href="api_eol_security_consent.html">EOL-Consent-1</a><br/>
 <a href="api_eol_individuals_practitioner.html">CareConnect-Practitioner-1</a><br/>
 <a href="api_eol_individuals_practitionerrole.html">CareConnect-PractitionerRole-1 </a></td>
</tr>
<tr>
<td>CPR Status</td>
<td>Flag<br/>Encounter<br/>Observation</td>
<td><a href="api_eol_management_flag_cprstatus.html">EOL-CPRStatus-Flag-1</a><br/>
<a href="api_eol_management_encounter_cprstatus.html">EOL-CPRStatus-Encounter-1</a><br/>
<a href="api_eol_diagnostics_observation_cprstatus.html">EOL-CPRStatus-Observation-1</a></td>
</tr>
<tr>
<td>End of Life Register</td>
<td>Flag</td>
<td><a href="api_eol_management_flag_register.html">EOL-Register-Flag-1</a></td>
</tr>
<tr>
<td>Prognosis</td>
<td>Encounter<br/>Observation</td>
<td><a href="api_eol_management_encounter_prognosis.html">EOL-Prognosis-Encounter-1</a><br/>
<a href="api_eol_diagnostics_observation_prognosis.html">EOL-Prognosis-Observation-1</a></td>
</tr>
<tr>
<td>Advance Treatment Preferences</td>
<td>Condition<br/>List<br/>CarePlan<br/>Questionnaire Response<br/>Practitioner<br/>Practioner Role</td>
<td><a href="api_eol_management_problemlist.html">CareConnect-ProblemList-1</a><br/>
 <a href="api_eol_summary_problemheader_condition.html">CareConnect-ProblemHeader-Condition-1</a><br/>
 <a href="api_eol_summary_atp_careplan.html">EOL-AdvanceTreatmentPreferences-CarePlan-1</a><br/>
 <a href="api_eol_advancetreatmentpreferences_questionnaireresponse.html">EOL-AdvanceTreatmentPreferences-QuestionnaireResponse-1</a><br/>
 <a href="api_eol_individuals_practitioner.html">CareConnect-Practitioner-1</a><br/>
 <a href="api_eol_individuals_practitionerrole.html">CareConnect-PractitionerRole-1</a></td>

</tr>
<tr>
<td>Disability</td>
<td>Condition (Problem)<br/>List<br/>Practitioner<br/>Practioner Role</td>
<td><a href="api_eol_summary_disability_condition.html">CareConnect-ProblemHeader-Condition-1</a><br/>
<a href="api_eol_summary_disability_list.html">CareConnect-ProblemList-1</a><br/>
<a href="api_eol_individuals_practitioner.html">CareConnect-Practitioner-1</a><br/>
<a href="api_eol_individuals_practitionerrole.html">CareConnect-PractitionerRole-1</a></td>
</tr>
<tr>
<td>Functional Status</td>
<td>Questionnaire Response<br/>Practitioner<br/>Practioner Role</td>
<td><a href="api_eol_functionalstatus_questionnaireresponse.html">EOL-FunctionalStatus-QuestionnaireResponse-1</a><br/>
<a href="api_eol_individuals_practitioner.html">CareConnect-Practitioner-1</a><br/>
<a href="api_eol_individuals_practitionerrole.html">CareConnect-PractitionerRole-1</a></td>
</tr>
<tr>
<td>Preferences</td>
<td>Questionnaire Response</td>
<td><a href="api_eol_preferences_questionnaireresponse.html">EOL-Preferences-QuestionnaireResponse-1</a></td>
</tr>
<tr>
<td>Other Docs</td>
<td>Document Reference</td>
<td><a href="api_eol_documents_documentreference.html">EOL Document Reference</a></td>
</tr>
</table>