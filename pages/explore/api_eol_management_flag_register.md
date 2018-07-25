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

```xml
<Flag xmlns="http://hl7.org/fhir">
	<id value="9fa0541c-67a2-4946-a7e3-ef3c4a8991f1"/>
	<meta>
		<profile value="https://fhir.nhs.uk/STU3/StructureDefinition/EOL-Register-Flag-1"/>
	</meta>
	<status value="active"/>
	<code>
		<coding>
			<system value="http://snomed.info/sct"/>
			<code value="526631000000108"/>
			<display value="On end of life care register (finding)"/>
		</coding>
	</code>
	<subject>
		<reference value="CareConnect-Patient-1/6101231234"/>
	</subject>
</Flag>
```
