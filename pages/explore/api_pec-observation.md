---
title: Clinical | API PEC Observation
keywords: getcarerecord, structured, rest, condition
tags: [rest,fhir,condition,clinical,api]
sidebar: accessrecord_rest_sidebar
permalink: api_pec-observation.html
summary: Measurements and simple assertions made about a patient, device or other subject.
---
{% include custom/search.warnbanner.html %}

{% include custom/fhir.reference.html resource="Observation" page="pec-observation-1" fhirlink="[Observation](https://www.hl7.org/fhir/observation.html)" content="N/A" userlink=" " %}


## 1. Read ##

GET the average, min, max and count of a series of BP measurements for a patient (Request):
<div markdown="span" class="alert alert-success" role="alert">
GET [base]/Observation/$stats?subject=Patient/123&code=55284-4&system=http://loinc.org&duration=1&statistic=average&statistic=min&statistic=max&statistic=count</div>

## 2. Search ##

<div markdown="span" class="alert alert-success" role="alert">
GET [baseUrl]/Observation?[searchParameters]</div>

{% include custom/search.header.html resource="Observation" %}

### 2.1. Search Parameters ###

{% include custom/search.parameters.html resource="Observation"     link=" http://hl7.org/fhir/OperationDefinition/Observation-stats" %}

## 3. Example ##

#### 3.1 Http Body ####

    <?xml version="1.0" encoding="UTF-8"?>
    <Observation xmlns="http://hl7.org/fhir">
    <id value="76e39290-d1aa-11e6-9598-1234567c9a66"/>
    	<meta>
    		<profile value="https://fhir.nhs.uk/StructureDefinition/pec-observation-1"/>
    	</meta>
    	<status value="final"/>
    	<code>
    		<coding>
    			<system value="https://fhir.nhs.uk/PEC-observation-code-1"/>
    			<code value="0001"/>
    			<display value="Patient has paid appropriate charges"/>
    		</coding>
    	</code>
    	<subject>
    		<reference value="Patient/9900005896"/>
    		<display value="BRIDGE, Joanne (Mrs)"/>
    	</subject>
    	<effectiveDateTime value="2018-12-31T00:00:00+00:00"/>
    </Observation>