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

This page provides an overview of the FHIR STU3 Resources that are required to build the required API messaging.

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
<td><a href="https://fhir.hl7.org.uk/STU3/StructureDefinition/CareConnect-Patient-1"><b>*</b>CareConnect-Patient-1</a></td>
</tr>
<tr>
<td>Contacts</td>
<td>Patient</td>
<td><a href="https://fhir.hl7.org.uk/STU3/StructureDefinition/CareConnect-Patient-1"><b>*</b>CareConnect-Patient-1</a></td>
</tr>
<tr>
<td><a href="api_eol_lastingpowerofattorney.html">Lasting Power of Attorney (LPA)</a></td>
<td>Patient<br/>Flag<br/>Related Person</td>
<td>
<a href="https://fhir.nhs.uk/STU3/StructureDefinition/EOL-Patient-1">EOL-Patient-1</a><br/>
<a href="https://fhir.nhs.uk/STU3/StructureDefinition/EOL-LPA-Flag-1">EOL-LPA-Flag-1</a><br/>
<a href="https://fhir.nhs.uk/STU3/StructureDefinition/EOL-LPA-RelatedPerson-1">EOL-LPARelatedPerson-1</a></br>
</td>
</tr>
<tr>
<td><a href="api_eol_consent.html">Consent</a></td>
<td>Patient<br/>Organization<br/>Practitioner<br/>PractitionerRole<br/>Consent<br/></td>
<td>
<a href="https://fhir.nhs.uk/STU3/StructureDefinition/EOL-Patient-1">EOL-Patient-1</a><br/>
<a href="https://fhir.hl7.org.uk/STU3/StructureDefinition/CareConnect-Organization-1">CareConnect-Organization-1</a><br/>
<a href="https://fhir.hl7.org.uk/STU3/StructureDefinition/CareConnect-Practitioner-1">CareConnect-Practitioner-1</a><br/>
<a href="https://fhir.hl7.org.uk/STU3/StructureDefinition/CareConnect-PractitionerRole-1">CareConnect-PractitionerRole-1 </a><br/>
<a href="https://fhir.nhs.uk/STU3/StructureDefinition/EOL-Consent-1">EOL-Consent-1</a>
</td>
</tr>
<tr>
<td><a href="api_eol_cprstatus.html">CPR Status</a></td>
<td>Patient<br/>Organization<br/>Practitioner<br/>PractitionerRole<br/>Flag<br/>QuestionnaireResponse<br/></td>
<td>
<a href="https://fhir.nhs.uk/STU3/StructureDefinition/EOL-Patient-1">EOL-Patient-1</a><br/>
<a href="https://fhir.hl7.org.uk/STU3/StructureDefinition/CareConnect-Organization-1">CareConnect-Organization-1</a><br/>
<a href="https://fhir.hl7.org.uk/STU3/StructureDefinition/CareConnect-Practitioner-1">CareConnect-Practitioner-1</a><br/>
<a href="https://fhir.hl7.org.uk/STU3/StructureDefinition/CareConnect-PractitionerRole-1">CareConnect-PractitionerRole-1</a><br/>
<a href="https://fhir.nhs.uk/STU3/StructureDefinition/EOL-CPRStatus-Flag-1">EOL-CPRStatus-Flag-1</a></br>
<a href="https://fhir.nhs.uk/STU3/StructureDefinition/EOL-CPRStatus-QuestionnaireResponse-1">EOL-CPRStatus-QuestionnaireResponse-1</a>
</td>
</tr>
<tr>
<td><a href="api_eol_register.html">End of Life Register</a></td>
<td>Patient<br/>Flag</td>
<td>
<a href="https://fhir.nhs.uk/STU3/StructureDefinition/EOL-Patient-1">EOL-Patient-1</a><br/>
<a href="https://fhir.nhs.uk/STU3/StructureDefinition/EOL-Register-Flag-1">EOL-Register-Flag-1</a>
</td>
</tr>
<tr>
<td><a href="api_eol_prognosis.html">Prognosis</a></td>
<td>Patient<br/>Organization<br/>Practitioner<br/>PractitionerRole<br/>ClinicalImpression</td>
<td>
<a href="https://fhir.nhs.uk/STU3/StructureDefinition/EOL-Patient-1">EOL-Patient-1</a><br/>
<a href="https://fhir.hl7.org.uk/STU3/StructureDefinition/CareConnect-Organization-1">CareConnect-Organization-1</a><br/>
<a href="https://fhir.hl7.org.uk/STU3/StructureDefinition/CareConnect-Practitioner-1">CareConnect-Practitioner-1</a><br/>
<a href="https://fhir.hl7.org.uk/STU3/StructureDefinition/CareConnect-PractitionerRole-1">CareConnect-PractitionerRole-1</a><br/>
<a href="https://fhir.nhs.uk/STU3/StructureDefinition/EOL-Prognosis-ClinicalImpression-1">EOL-Prognosis-ClinicalImpression-1</a></br>
</td>
</tr>
<tr>
<td><a href="api_eol_atp.html">Advance Treatment Preferences</a></td>
<td>Patient<br/>Organization<br/>Practitioner<br/>PractitionerRole<br/>Location<br/>Procedure<br/>List<br/>Condition<br/>CarePlan<br/>Flag</td>
<td>
<a href="https://fhir.nhs.uk/STU3/StructureDefinition/EOL-Patient-1">EOL-Patient-1</a><br/>
<a href="https://fhir.hl7.org.uk/STU3/StructureDefinition/CareConnect-Organization-1">CareConnect-Organization-1</a><br/>
<a href="https://fhir.hl7.org.uk/STU3/StructureDefinition/CareConnect-Practitioner-1">CareConnect-Practitioner-1</a><br/>
<a href="https://fhir.hl7.org.uk/STU3/StructureDefinition/CareConnect-PractitionerRole-1">CareConnect-PractitionerRole-1</a><br/>
<a href="https://fhir.hl7.org.uk/STU3/StructureDefinition/CareConnect-Location-1">CareConnect-Location-1</a><br/>
<a href="https://fhir.nhs.uk/STU3/StructureDefinition/CareConnect-EOL-Procedure-1">CareConnect-EOL-Procedure-1</a><br/>
<a href="https://fhir.nhs.uk/STU3/StructureDefinition/EOL-ATPProblemList-List-1">EOL-ATPProblemList-List-1</a><br/>
<a href="https://fhir.nhs.uk/STU3/StructureDefinition/EOL-ATPProblemHeader-Condition-1">EOL-ATPProblemHeader-Condition-1</a><br/>
<a href="https://fhir.nhs.uk/STU3/StructureDefinition/EOL-ATP-CarePlan-1">EOL-ATP-CarePlan-1</a><br/>
<a href="https://fhir.nhs.uk/STU3/StructureDefinition/EOL-ADRT-Flag-1">EOL-ADRT-Flag-1</a><br/>
</td>
</tr>
<tr>
<td><a href="api_eol_disabilities.html">Disabilities</a></td>
<td>Patient<br/>List<br/>Condition<br/>Practitioner<br/>PractitionerRole<br/>Organization<br/></td>
<td>
<a href="https://fhir.nhs.uk/STU3/StructureDefinition/EOL-Patient-1">EOL-Patient-1</a><br/>
<a href="https://fhir.hl7.org.uk/STU3/StructureDefinition/CareConnect-ProblemList-1">CareConnect-ProblemList-1</a><br/>
<a href="https://fhir.hl7.org.uk/STU3/StructureDefinition/CareConnect-ProblemHeader-Condition-1">CareConnect-ProblemHeader-Condition-1</a><br/>
<a href="https://fhir.hl7.org.uk/STU3/StructureDefinition/CareConnect-Practitioner-1">CareConnect-Practitioner-1</a><br/>
<a href="https://fhir.hl7.org.uk/STU3/StructureDefinition/CareConnect-PractitionerRole-1">CareConnect-PractitionerRole-1</a><br/>
<a href="https://fhir.hl7.org.uk/STU3/StructureDefinition/CareConnect-Organization-1">CareConnect-Organization-1</a>
</td>
</tr>
<tr>
<td><a href="api_eol_functionalstatus.html">Functional Status</a></td>
<td>Patient<br/>Organization<br/>Practitioner<br/>PractitionerRole<br/>Observation</td>
<td>
<a href="https://fhir.nhs.uk/STU3/StructureDefinition/EOL-Patient-1">EOL-Patient-1</a><br/>
<a href="https://fhir.hl7.org.uk/STU3/StructureDefinition/CareConnect-Organization-1">CareConnect-Organization-1</a><br/>
<a href="https://fhir.hl7.org.uk/STU3/StructureDefinition/CareConnect-Practitioner-1">CareConnect-Practitioner-1</a><br/>
<a href="https://fhir.hl7.org.uk/STU3/StructureDefinition/CareConnect-PractitionerRole-1">CareConnect-PractitionerRole-1</a><br/>
<a href="https://fhir.nhs.uk/STU3/StructureDefinition/CareConnect-EOL-FunctionalStatus-Observation-1">CareConnect-EOL-FunctionalStatus-Observation-1</a>
</td>
</tr>
<tr>
<td><a href="api_eol_preferences.html">Preferences</a></td>
<td>Patient<br/>Organization<br/>Practitioner<br/>PractitionerRole<br/>QuestionnaireResponse</td>
<td>
<a href="https://fhir.nhs.uk/STU3/StructureDefinition/EOL-Patient-1">EOL-Patient-1</a><br/>
<a href="https://fhir.hl7.org.uk/STU3/StructureDefinition/CareConnect-Organization-1">CareConnect-Organization-1</a><br/>
<a href="https://fhir.hl7.org.uk/STU3/StructureDefinition/CareConnect-Practitioner-1">CareConnect-Practitioner-1</a><br/>
<a href="https://fhir.hl7.org.uk/STU3/StructureDefinition/CareConnect-PractitionerRole-1">CareConnect-PractitionerRole-1</a><br/>
<a href="https://fhir.nhs.uk/STU3/StructureDefinition/EOL-Preferences-QuestionnaireResponse-1">EOL-Preferences-QuestionnaireResponse-1</a>
</td>
</tr>
<tr>
<td><a href="api_eol_otherdocuments.html">Other Documents</a></td>
<td>QuestionnaireResponse</td>
<td><a href="https://fhir.nhs.uk/STU3/StructureDefinition/EOL-OtherDocuments-QuestionnaireResponse-1">EOL-OtherDocuments-QuestionnaireResponse-1</a></td>
</tr>
</table>

<b>*</b>Please note the implementation uses CareConnect-Patient-1 instead of the EOL-Patient-1.