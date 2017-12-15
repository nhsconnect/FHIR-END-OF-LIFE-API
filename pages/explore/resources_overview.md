---
title: Resources Overview
keywords: getcarerecord, structured, rest, resource
tags: [rest,fhir,api]
sidebar: foundations_sidebar
permalink: explore.html
summary: "Overview of the Resources section"
---

{% include custom/search.warnbanner.html %}

{% include custom/api_overview.svg %}

## 1. Pre-Requisites for FHIR Servers ##

### 1.1 API Requirements ###

- SHALL support HL7 FHIR STU3
- SHALL Implement REST behavior according to the [FHIR specification](http://www.hl7.org/fhir/dstu2/http.html)
- Resources SHALL identify the profile supported as part of the [FHIR Base Resource](https://hl7.org/fhir/DSTU2/resource-definitions.html#Resource.meta)
- SHALL support XML **or** JSON formats for all CareConnectAPI interactions and SHOULD support both formats.


### 1.2 FHIR Conformance ###

SHALL declare a Conformance identifying the list of profiles, operations, search parameter supported.

### 1.3 NHS Number ###

Only verified NHS Number SHALL be used with profiles. This can be achieved using a spine accredited system, a [Demographics Batch Service (DBS)](https://developer.nhs.uk/library/systems/demographic-batch-service-dbs/) batch-traced record (CSV), or using a [Spine Mini Services Provider (HL7v3)](https://nhsconnect.github.io/spine-smsp/) to verify the NHS Number.

{% include custom/contribute.html content="Get in touch with careconnect@interopen.org to improve the Prerequisites." %}

## 2. Resource API Structure ##
The FHIR Visitors and Migrants profile API's described in the Explore section of this implementation guide have been structured consistently in the following way:
- `0.` References
- `1.` Read
- `2.` Search Parameters
- `3.` Example

### 2.1 Resource API Structure Details ###

<table style="min-width:100%;width:100%">
<tr id="clinical">
<th style="width:20%;">General</th>
<th style="width:80%;">Description </th>
</tr>
<tr>
<td>0. References</td>
<td>Links to other parts of the implementation guide which might help with context and understanding the API's described</td>
</tr>
<tr>
<td>1. Read</td>
<td>A description of how to get the API</td>
</tr>
<tr>
<td>2. Search Parameters</td>
<td>List of search parameters for the profile being described, including any tips for searching. This section shows examples of how to search using the provided search parameters</td>
</tr>
<tr>
<td>3. Example</td>
<td>Description of of the Request & Response headers, example of how to search on a server and the expected response body as an example</td>
</tr>
</table>

## 3. Resource API's ##
This section looks at the Visitors and Migrants profile API's covered within this implementation guide.


<table style="min-width:100%;width:100%">
<tr id="clinical">
<th style="width:33%;">Clinical</th>
<th style="width:33%;">&nbsp;</th>
<th style="width:33%;">&nbsp;</th>
</tr>
<tr id="clinicald">
<th>Diagnostics</th>
<th>&nbsp;</th>
<th style="width:33%;">&nbsp;</th>
</tr>
<tr>
<td><a href="api_pec-observation.html">PEC-Observation</a></td>
<td>&nbsp;</td>
<td>&nbsp;</td>
</tr>
</table> 

<table style="min-width:100%;width:100%">
<tr id="conformance">
<th style="width:33%;">Foundation</th>
<th style="width:33%;"></th>
<th style="width:33%;"></th>
</tr>
<tr id="conformanced">
<th>Conformance</th>
<th>Terminology</th>
<th>&nbsp;</th>
</tr>
<tr>
<td><a href="api_foundation_capabilitystatement.html">Capability Statement</a></td>
<td><a href="api_foundation_valueset.html">ValueSet</a></td>
<td>&nbsp;</td>
</tr>
</table>
