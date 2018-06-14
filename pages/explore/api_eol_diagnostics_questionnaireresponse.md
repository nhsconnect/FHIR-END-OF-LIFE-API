---
title: Workflow | Questionnaire Response
keywords: usecase, questionnaire, response, preferences
tags: [rest, fhir, workflow,api]
sidebar: foundations_sidebar
permalink: api_eol_diagnostics_questionnaireresponse.html
summary: An interaction between a patient and healthcare provider(s) for the purpose of providing healthcare service(s) or assessing the health status of a patient.
---
{% include custom/search.warnbanner.html %}

{% include custom/fhir.STU3.reference.html resource="QuestionnaireResponse" page="CareConnect-EOL-Preferences-QuestionnaireResponse-1" fhirname="QuestionnaireResponse" fhirlink="questionnaireresponse.html" content="User Stories" userlink="engage_endoflife.html" %}

## Patient Scenario ##

### Advance Treatment Preferences ###

Advance treatment preferences are recorded as a table of the problem/condition/anticipated event, coupled with the intervention required and an indicator of the level of intervention.

Most of the ReSPECT data can be captured within the minimum dataset, however the ReSPECT care priority values cannot be accommodated elsewhere and so must be recorded separately.  As many localities have or will implement ReSPECT, it important that these additional ReSPECT values can be transmitted.

### Preferences ###

This is used to record a patient’s preferred place of death and any other preferences and wishes, including wishes for care and cultural, religious and social needs.  Additionally, there is an option to record domestic information and access instructions for the patient’s residence. 

### Functional Status ###

The patient’s functional status is recorded by clinicians during encounters with the patient and gives consumers of the data a general indication of the wellness of the patient. The status can be codified using either the Karnofsky scale or Electronic Frailty Index and there is a mandatory textual field for systems that do not store this data as a codeable concept.


...

    <QuestionnaireResponse xmlns="http://hl7.org/fhir">
    <id value="f201"/> 
	<text> 
	<status value="generated"/> 
	<div xmlns="http://www.w3.org/1999/xhtml">
	<p> <b> Generated Narrative with Details</b> </p>
	</div> 
	</text> 
	<status value="completed"/>
	<subject> 
		<reference value="Patient/f201"/> 
		<display value="Daniel Briggs"/> 
	</subject> 
	<authored value="2013-06-18T00:00:00+01:00"/> 
	<author> 
		<reference value="Practitioner/f201"/> 
	</author> 
	<source> 
		<reference value="Practitioner/f201"/> 
	</source> 
	<item> 
		<linkId value="1"/> 
		<item> 
		<!--   ReSPECT Care Priority answer   -->
	<linkId value="1.1"/> 
		<text value="ReSPECT Care Priority"/> 
		<answer> 
			<valueInteger value="50"/> 
		</answer> 
		<answer> 
			<valueString value="I will let the medical professional take the decision"/> 
		</answer> 
		</item> 
	</item> 
	<item> 
		<!--   Answers to Preferences   -->
		<linkId value="2"/> 
		<text value="Preferences"/> 
		<item> 
		<linkId value="2.1"/>
		<text value="Preferred Place of Death - Coded"/>
		<answer>
			<valueCoding>
				<system value="http://snomed.info/sct"/>
				<code value="https://fhir.nhs.uk/STU3/ValueSet/EOL-PreferredPlaceDeath-Code-1"/>
				<display value="Preferred place of death: discussion not appropriate (finding)"/>
			</valueCoding>
		</answer>
		</item> 
		<item> 
		<linkId value="2.2"/> 
		<text value="Preferred Place of Death - Textual"/> 
		<answer> 
			<valueString value="Care Home"/>
		</answer> 
		</item> 
		<item> 
		<linkId value="2.3"/> 
		<text value="Preferences and Wishes"/> 
		<answer> 
			<valueString value="I want to have a cremation"/> 
		</answer> 
		</item> 
		<item> 
		<linkId value="2.4"/> 
		<text value="Domestic Access and Information"/> 
		<answer> 
			<valueString value="I have a dog at home"/>
		</answer> 
		</item> 
	</item> 
	<item> 
		<!--   Answers to Functional Status   -->
		<linkId value="3"/> 
		<text value="Functional Status"/> 
		<item> 
		<linkId value="3.1"/> 
		<text value="Functional Status Type"/> 
		<answer> 
			<valueCoding>
				<system value="http://snomed.info/sct"/>
				<code value="https://fhir.nhs.uk/STU3/ValueSet/EOL-FunctionalStatusType-Code-1"/>
				<display value="Karnofsky Performance Status score (observable entity)"/>
			</valueCoding>
		</answer> 
		</item> 
		<item> 
		<linkId value="3.2"/> 
		<text value="Functional Status Value"/> 
		<answer> 
			<valueString value="50   Considerable assistance and frequent medical care required"/> 
		</answer> 
		</item>
		<item> 
		<linkId value="3.3"/> 
		<text value="Functional Status Text"/> 
		<answer> 
			<valueString value="I can function on my own most of the time"/> 
		</answer> 
		</item> 		
	</item> 
	</QuestionnaireResponse>

....

## 1. Read ##

<div markdown="span" class="alert alert-success" role="alert">
GET [baseUrl]/Encounter/[id]</div>

{% include custom/read.response.html resource="Encounter" content="" %}

## 2. Search ##

<div markdown="span" class="alert alert-success" role="alert">
GET [baseUrl]/Encounter?[searchParameters]</div>

Fetches a bundle of all `Encounter` resources for the specified patient.

{% include custom/search.header.html resource="Encounter" %}

### 2.1. Search Parameters ###

{% include custom/search.parameters.html resource="Encounter" link="encounter.html#search" %}


<table style="min-width:100%;width:100%">
<tr id="clinical">
    <th style="width:10%;">Name</th>
    <th style="width:15%;">Type</th>
    <th style="width:40%;">Description</th>
    <th style="width:5%;">Conformance</th>
    <th style="width:30%;">Path</th>
</tr>
<tr>
    <td><code class="highlighter-rouge">date</code></td>
    <td><code class="highlighter-rouge">date</code></td>
    <td>A date within the period the Encounter lasted</td>
    <td>MAY</td>
    <td>Encounter.period</td>
</tr>
<tr>
    <td><code class="highlighter-rouge">patient</code></td>
    <td><code class="highlighter-rouge">reference</code></td>
    <td>The identity of a patient to list encounters for</td>
    <td>MAY</td>
    <td>Encounter.patient <br>(Patient)</td>
</tr>
</table>

<!--
Systems SHOULD support the following search combinations:

 * patient
 -->

{% include custom/search.date.html para="2.1.1." content="Encounter" %}

{% include custom/search.patient.html para="2.1.2." content="Encounter" %}

{% include custom/search.response.html resource="Encounter" %}

## 3. Example ##

### 3.1 Request Query ###

<h3 id="32-response-headers">3.1 cURL</h3>

Return all Encounter resources with an id of 4, the format of the response body will be xml. The Reference Implementation is hosted at '{{ site.fhir_ref_impl }}'.

{% include custom/embedcurl.html title="Search Patient" command="curl -X GET -H 'Accept: application/xml+fhir' -H 'Authorisation: BEARER [token]' -v 'http://yellow.testlab.nhs.uk/careconnect-ri/STU3/Encounter?patient=4'" %}

<h3 id="32-response-headers">3.2 Explore the Response</h3>

Explore the response in XML & JSON on the Reference Implementation below
<div class="language-http highlighter-rouge">
<pre class="highlight">
<p style="font-size: 110%;">Reference Implementation</p>
XML <a target="_blank" href="{{ site.fhir_ref_impl }}search?serverId=home&pretty=true&resource=Encounter&param.0.0=&param.0.1=4&param.0.name=patient&param.0.type=reference&resource-search-limit=&encoding=xml">Patient id search RI viewer</a>
JSON <a target="_blank" href="{{ site.fhir_ref_impl }}search?serverId=home&pretty=true&resource=Encounter&param.0.0=&param.0.1=4&param.0.name=patient&param.0.type=reference&resource-search-limit=&encoding=json">Patient id search RI viewer</a>
</pre>
</div>
