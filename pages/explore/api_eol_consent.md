---
title: Consent Atomic Unit
keywords: usecase, NHS Number, Name, DoB
tags: [rest, fhir, workflow,api]
sidebar: foundations_sidebar
permalink: api_eol_consent.html
summary: Atomic Unit to capture the consent status for a patient.
toc: false
---
{% include custom/search.warnbanner.html %}

{% include custom/under.construction.html %}

### consent ###


The following FHIR profiles are used to form the CPR Status Atomic Unit:

- [EOL-Patient-1](https://fhir.nhs.uk/STU3/StructureDefinition/EOL-Patient-1.xml)

### consent data item mapping to FHIR profiles ###

The consent data item are fulfilled by elements within the FHIR resources listed below:

| EOL Data Item                       | FHIR resource element                                                   | Mandatory/Required/Optional |
|-------------------------------------|-------------------------------------------------------------------------|-----------------------------|
| Consent Status        		       | EOL-Consent-1.status          | Mandatory                   |
| Consent Decision Details | EOL-Consent-1.consentDecisionDetails (Extension) | Optional |
| Consent Discussion Details | EOL-Consent-1.consentDiscussionDetails (Extension) |Optional |
| Date of change in consent status	| EOL-Consent-1.dateTime | Mandatory |
| Professionals recording this consent status	| EOL-Consent-1.actor |Mandatory |

### Consent ERD ###

<img src="images/erd/erd-consent.svg" style="width:80%;max-width: 80%;">

### Consent Example XML ###

```xml
<Consent xmlns="http://hl7.org/fhir">
	<id value="981dbc45-9ff9-4570-836c-eb3e93763189"/>
	<meta>
		<profile value="https://fhir.nhs.uk/STU3/StructureDefinition/EOL-Consent-1"/>
	</meta>
	<status value="active"/>
	<patient>
		<reference value="62b29d73-b405-44f0-8533-3a26a3ffce7d"/>
	</patient>
	<dateTime value="2018-08-20T15:00:00+00:00"/>
	<actor>
		<role>
			<coding>
				<system value="http://hl7.org/fhir/v3/ParticipationType"/>
				<code value="PROV"/>
				<display value="Healthcare Provider"/>
			</coding>
		</role>
		<reference>
				<reference value="urn:uuid:12692f55-56cf-4ddf-3ef5-e9ed13f6bd923"/>
		</reference>
	</actor>
</Consent>
```



