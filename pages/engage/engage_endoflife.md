---
title: "End of Life Care User Stories and Use Cases"
keywords: user stories, epics, scenarios, nhsnumber
tags: [foundations,userstories, epics, scenarios]
sidebar: engage_sidebar
permalink: engage_endoflife.html
summary: "User stories with links to profiles"
---

{% include important.html content="This page has been added to promote discussion in INTEROPen of the use cases and scenarios. This project is being developed using an agile methodology so iterative updates to content will be added on a regular basis." %}

 
## 1.	Overview ##
To support the End of Life National Minimum Dataset, this section explains the user stories and use cases that will (or possibly will) employ the FHIR resources that will be produced as part of delivery of this interoperability dataset.
The purpose of this document is to explain those user stories and use cases to those developing the FHIR resources and those technicians and clinicians that will be reviewing the FHIR resources as part of the INTEROPen curation process.
The FHIR resources will be used to deliver both API “pull” of data from source systems and also messaging to “push” data to receiving systems.  The nature of the fragmented delivery of EPaCCS across the NHS in England means that the implementation of the resources will depend upon what solutions are being employed locally.
 
The first of type (FoT) implementation will be by the **One London** LHCRE.  One London will offer U&EC users access to the data held with some London EPaCCS by using pointers stored within the London Health and Care Information Exchange (LHCIE).

## 2.	Use Cases ##
The required data flows are described as use cases.

## 2.1.	111/999 Call Handler takes call for patient with EoL plans and preferences. ##
This is the primary use case for the first of type (FoT) delivery by One London.  One London is developing a system that enables Londonwide users to access source systems such as Co-ordinate My Care (CMC) to provide EoL and other data.
Alternate flows are outside of the FoT scope.

**Trigger:** Call received – EoL patient is unwell or exhibiting changed status.

**Actors:** Call handler, paramedic

**Main Flow**
	
1.	Call handler confirms details of the patient and traces them on Spine using their own system.
2.	Local U&EC system links directly to the patient’s EPaCCS record via a national or local record locator system, using the national EoL dataset API, which returns the EoL dataset for the patient from provider systems.
3.	Local U&EC system renders the EoL dataset within the application for the call handler.
4.	Call handler follows agreed escalation procedures for this problem/condition.  This indicates that paramedics should be despatched.
5.	Call handler despatches paramedics.
6.	Paramedics attend patient, their handheld system also displays EoL dataset details.
7.	Paramedics can access the patient’s residence using access details supplied in the EoL dataset details.
8.	Paramedics are fully aware of the patient’s current prognosis and treat the patient, taking as full an account as possible of their personal wishes.
9.	Patient is stabilised reflecting their advance/anticipatory plans.
10.	Patient remains at residence in a situation where it is likely they would have been admitted if the emergency teams were unaware of their advance plans and preferences.

**Alternate Flows**

2a
* Local U&EC system retrieves locally-held EoL dataset details that have been previously supplied by provider systems.
* Go to 3

2b
* Local U&EC system links directly to the patient’s SCR, which returns the SCR additional information. SCR additional information includes elements of the EoL dataset.
* Go to 3.

2c
* Local U&EC system offers click-thru to local shared record or the call handler opens the local shared record in a separate window.
* Local shared record links directly to the patient’s EPaCCS record via a national or local record locator system, using the national EoL dataset API, which returns the EoL dataset for the patient from provider systems.
* Local shared record displays EoL dataset details within its own window.
* Go to 4

10a
* Patient is taken to Hospital if their planned treatment level indicates this, based on their current condition.
* End

## 2.2.	Patient agrees advance care plan and preferences with community palliative care team (GP update) ##

**Trigger:** Patient agrees advance care plan and preferences with community palliative care team.
The local EPaCCS is not also the patient’s GP system.

**Actors:** EPaCCS user, patient, GP

**Main Flow**	

1.	EPaCCS user accesses patient record.  Patient is traced in Spine for latest GP details.
2.	EPaCCS user updates EoL dataset details on the local EPaCCS.
3.	EPaCCS automatically generates a FHIR EoL dataset update message to be routed to the patient’s GP system.
4.	FHIR update is routed to GP system.
5.	GP reviews incoming changes and accepts them into their GP system.
6.	EoL dataset details are automatically updated to the SCR.

## 2.3.	Patient agrees advance care plan and preferences with community palliative care team (U&EC update) ##

**Trigger:**	Patient agrees advance care plan and preferences with community palliative care team.
The local EPaCCS is set up to automatically update the local U&EC system.

**Actors:** EPaCCS user, patient

**Main Flow**	

1.	EPaCCS user accesses patient record.  Patient is traced in Spine.
2.	EPaCCS user updates EoL dataset details on the local EPaCCS.
3.	EPaCCS automatically generates a FHIR EoL dataset update message to be routed to the local U&EC system.
4.	FHIR update is routed to the U&EC system.
5.	U&EC system accepts the changes.

## 2.4.	Patient agrees advance care plan and preferences with GP (EPaCCS update) ##

**Trigger:** Patient agrees advance care plan and preferences with a GP or care team.
The local EPaCCS is not also the patient’s GP system.

**Actors:** GP system user, patient, EPaCCS user

**Main Flow**	

1.	GP system user accesses patient record.
2.	GP system user updates EoL dataset details on the GP system.
3.	EoL dataset details are automatically updated to the SCR.
4.	GP system automatically generates a FHIR EoL dataset update message to be routed to the patient’s EPaCCS.
5.	FHIR update is routed to EPaCCS.
6.	EPaCCS user reviews incoming changes and accepts them into their system.

**Alternate Flows**	

4a.
* GP system links directly to partner EPaCCS.

4b.
* GP system uses FHIR EoL dataset API available on partner EPaCCS to update the patient EoL data.


## 3.	User Stories ##

Requirements are described as user stories to enable a better understanding of the issues that require resolution by any integrated system.

## 3.1.	EoL data and preferences viewable by all care professionals ##

**In order to** remove the need to repeat my statement of preferences and for those preferences to be respected when I’m unable to communicate them successfully\
**As a** patient\
**I want** my EoL data and preferences to be shared so that they can be accessed by all health and care professionals attending to my needs.

**Commentary**

Having to repeat preferences can be both distressing and time-consuming for both patients and carers and the professionals providing care.  Having the EoL data and preferences accessible to all care professionals will lower unwarranted admissions to hospital.
This broad user story explains the aim of the project from the patient’s perspective

**Acceptance Criteria**

* Care professionals with access must include: Acute care professionals, community palliative care teams, general practice professionals, care home or hospice carers, 111 call handlers, paramedic control teams, paramedics, UTC clinicians.
* EoL preferences to be viewed must, as a minimum, comply with the agreed End of Life National Minimum Dataset.
* The care professional must only be able to amend those data items over which they have jurisdiction.
* The care professional may be able to view the current EoL data and preferences via a viewer portal or embedded within their own native IT system.
* Any changes must be capable of being shared promptly so that other care professionals will have access to the changed record. 

## 3.2.	Up to date preferences are accessible to care professionals ##

**In order to** ensure that care professionals always respond to my latest wishes\
**As a** patient\
**I want to** be assured that any updates to my preferences will be promptly shared to systems that will be used by my care professionals.

**Acceptance Criteria**

* EoL preferences to be updated and shared must, as a minimum, comply with the agreed End of Life National Minimum Dataset.
* Updates to EoL preferences must be promptly shared with all systems that will be used to deliver the patient’s care, with little or no user interaction.

## 3.3.	Patient/carers can directly view EoL preferences ##

**In order to** ensure that my statement of preferences is completely up to date with my current wishes\
**As a** patient or an authorised proxy of the patient\
**I want to** be able to independently (or with help from my carers) view my statement of preferences whenever I wish to.

**Commentary**

Commitments have been made that patients/carers will have access to their EoL preferences via their own IT applications.  This story will be eventually delivered by the NHS Online programme. The first version of the software released in 2018 will only have limited EoL functionality.  However, as the software is further developed it is expected to use the End of Life National Minimum Dataset. 

## 3.4.	Patient/carers can directly amend EoL preferences ##

**In order to** ensure that my statement of preferences is completely up to date with my current wishes\
**As a** patient or an authorised proxy of the patient\
**I want to** be able to independently (or with help from my carers) update my statement of preferences whenever I wish to.

**Commentary**

Commitments have been made that patients/carers will have access to their EoL preferences and in some circumstances, be able to effect changes to those preferences via their own IT applications.  Consideration must be taken to ensure that the patient can only amend those preferences where it is safe for the patient to do so without professional support.

**Acceptance Criteria**

* The patient must only be able to alter those items of the preferences over which they have jurisdiction.

## 3.5.	Urgent and Emergency Care View Current EoL Data ##

**In order that** the EoL patient receives the appropriate care for their current condition and wishes\
**As an** urgent or emergency care user\
**I want to** quickly view the latest EoL information from the EPaCCS that supports this patient’s EoL care

**Commentary**

In the FoT solution to be delivered by the One London, the LHCIE brokerage will direct the urgent or emergency care user’s system to the correct source EPaCCS via pointers.\
Other urgent care systems may employ “click through” technology to access partner EPaCCS, using the national minimum dataset

**Acceptance Criteria**

* EoL information to be viewed must, as a minimum, comply with the agreed End of Life National Minimum Dataset.

## 3.6.	Update Urgent and Emergency Care with EoL Data ##

**In order that** EoL patients receive the appropriate care for their current condition and wishes\
**As an** urgent or emergency care user\
**I want to** receive updates for changes of patient EoL information from source systems

**Commentary**

Some local solutions require changes made to EPaCCS data to be transmitted directly to partner urgent and emergency care systems for later use. This is due to the current systems having no realtime access to their partner EPaCCS. Implementation of the national minimum dataset FHIR message structure will enable consuming urgent and emergency care systems to accept changes from a variety of provider systems in a common format.

**Acceptance Criteria**

* EoL information to be viewed must, as a minimum, comply with the agreed End of Life National Minimum Dataset.

## 3.7.	Update GP Systems (and hence SCR) with EoL Data ##

**In order that** EoL patients receive the appropriate care for their current condition and wishes\
**As a** GP system user\
**I want to** receive updates for changes of patient EoL information from source systems

**Commentary**

A key issue with standalone EPaCCS is that at least some EoL data must be rekeyed into patients’ GP systems.  Changes made to EPaCCS data can be transmitted directly to the patient’s registered GP system.  The national minimum dataset FHIR message may be delivered by national exchange systems such as MESH or via whatever exchange is employed locally.  Receiving GP systems will (hopefully) be able to accept the changes within a minimum of rekeying.

Additionally, Trust systems may use the message standard to transmit changes in EoL data and preferences that have come about as part of an acute episode of care.  Respondents indicate that these changes will probably be triggered by the process of discharge.

Receipt of EoL data in this standard format will make it easier for GP systems to seamlessly pass that data onto SCR, where the patient has given consent for the sharing of SCR additional information.

**Acceptance Criteria**
* EoL information to be updated and shared must, as a minimum, comply with the agreed End of Life National Minimum Dataset.
* Updates to EoL preferences must be promptly shared with GP systems, with little or no user interaction.

## 3.8.	Update EPaCCS with EoL Data ##

**In order that** EoL patients receive the appropriate care for their current condition and wishes\
**As an** EPaCCS system user\
**I want to** receive updates for changes of patient EoL information from source systems

**Commentary**

There are occasions where GP systems or acute systems have updated EoL information, but that information must be rekeyed into the locality’s official EPaCCS. Changes made elsewhere can be transmitted directly to the patient’s EPaCCS.  The national minimum dataset FHIR message may be delivered by national exchange systems such as MESH or via whatever exchange is employed locally.  Receiving EPaCCS will (hopefully) be able to accept the changes within a minimum of rekeying.

Additionally, Trust systems may use the message standard to transmit changes in EoL data and preferences that have come about as part of an acute episode of care.  Respondents indicate that these changes will probably be triggered by the process of discharge.

**Acceptance Criteria**

* EoL information to be updated and shared must, as a minimum, comply with the agreed End of Life National Minimum Dataset.
* Updates to EoL preferences must be promptly shared with GP systems, with little or no user interaction

## 4.	Out of Scope User Stories ##
The following stories may be supported by delivery of the EoL National Minimum Dataset FHIR resources, but they are **not** to be delivered by the initial implementation.

## 4.1.	National Reporting – death in preferred place ##

**In order that** the benefits of integrated EPaCCS and the quality of EoL care can be better measured\
**As a** nationally-based EoL professional\
**I want** national reporting to show the incidence of people dying in their preferred place of death.

**Acceptance Criteria**

* Data must be capable of being split across time bands  eg. monthly and yearly figures based upon the date of death of the patient.
* Data must be capable of being split across geographic and organisational boundaries.
* Data must show totals of preferred place of death vs. actual place of death.
* Data should be capable of reporting counts by the reason for variance where the actual place of death does not match the preferred place of death.

## 4.2.	National Reporting – three or more emergency admissions in final 90 days of life ##

**In order that** the benefits of integrated EPaCCS and the quality of EoL care can be better measured\
**As a** nationally-based EoL professional\
**I want** national reporting to show the incidence of people with three or more emergency admissions in the last 90 days of life.

**Commentary**

This is data that will be collected from other urgent and emergency care data collections.  It is out of scope for this current piece of work.

## 4.3.	National Reporting – days in hospital in final 90 days of life ##

**In order that** the benefits of integrated EPaCCS and the quality of EoL care can be better measured\
**As a** nationally-based EoL professional\
**I want** national reporting to show data for number of days people are spending in hospital during their final 90 days of life.

**Commentary**

This is data that will be collected from other urgent and emergency care data collections.  It is out of scope for this current piece of work.

## 4.4.	National Reporting – when EoL care plan was recorded ##

**In order that** the benefits of integrated EPaCCS and the quality of EoL care can be better measured\
**As a** nationally-based EoL professional\
**I want** national reporting to show data for when an EoL care plan was recorded and whether the person consented to sharing of this data.

**Commentary**

Further investigation must be undertaken to understand where and how this data can be extracted.

**Acceptance Criteria**

* Data must be capable of being split across time bands  eg. monthly and yearly figures based upon the date of death of the patient.
* Data must be capable of being split across geographic and organisational boundaries.
* Data must be capable of being split across the patient’s primary diagnosis.
