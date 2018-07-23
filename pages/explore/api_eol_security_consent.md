---
title: Foundation | Consent | End of Life
keywords: foundations, fhir, end, of, life, consent
tags: [foundation,use_case,fhir,rest,api,noccprofile]
sidebar: accessrecord_rest_sidebar
permalink: api_eol_security_consent.html
summary: A record of a healthcare consumer’s policy choices, which permits or denies identified recipient(s) or recipient role(s) to perform one or more actions within a given policy context, for specific purposes and periods of time.
---

{% include custom/search.warnbanner.html %}

{% include custom/fhir.STU3.reference.html resource="Consent" page="EOL-Consent-1" fhirname="Consent" fhirlink="consent.html" content="User Stories" userlink="engage_endoflife.html" %}

## Patient Scenario ##

Consent

On an encounter with a professional, and always on creation of the initial EPaCCS record, the patient will be asked consent to share this data more widely for the purposes of providing them with direct care.

A consent is recorded for a patient based on their meeting with a professional. The Consent FHIR resource has been chosen to represent this consent recording. It can record the status as well as the purpose of the consent, and actors involved (professionals recording this consent status).

Where there is no consent to share on the system, no EOL data will be shared to other consumer systems.
