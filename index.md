---
title: Introduction to End of Life API
keywords: homepage
tags: [overview]
sidebar: overview_sidebar
permalink: index.html
toc: false
summary: A brief introduction to getting started with the FHIR&reg; APIs.
---

{% include important.html content="This site is under active development by NHS Digital and is intended to provide all the technical resources you need to successfully develop the APIs. This project is being developed using an agile methodology so iterative updates to content will be added on a regular basis." %}

{% include warning.html content="This site is provided for information only and is intended for those engaged with NHS Digital on the development of the APIs. It is advised not to develop against these specifications until a formal announcement has been made." %}

# Introduction #

Welcome to the End of Life API site, this work is currently under development and as such currently contains:

-

# Development Phases #
Proof of Concept Part One - Internal within NHS Digital
Define standards
Create Test batch data based on these standards
Change Spine data formats to hold additional exemption data
Calculate Age exemptions based on Spine current data
Display Exemption Flag and End Date on Spine
Test.

Proof of Concept Part Two – End to End
BSA produce Test file in data and tested standard (as proven in POC part one) using a minimum of Maternity dataset
SPINE process batch
Restricted number of sites to be used for the Proof of Concept (tba)
Pharmacy system(s) contacts SPINE and pulls exemption data
Pharmacy system(s) supplier amends system to show Exemption Flag and End date
Pharmacy system(s) displays Exemption Flag and End Date
Test.

Pilot, in Live Production system
BSA sends data to NHS Digital in agreed format using a minimum of Maternity dataset
SPINE process batch
Pharmacy system contacts SPINE and pulls exemption data
A single Pharmacy system supplier amends system to show Exemption Flag and End date in Live
Pharmacy system displays Exemption Flag and End Date
Single Pharmacy utilises data when processing prescriptions.

Rollout, part one
Pharmacy system from Pilot, rolls out across all pharmacies utilising this system.

Rollout, overall
BSA to incorporate data from other sources where and when possible.
DWP
HMRC
Other pharmacy systems to take feed and displaying Exemption Flag and Exemption End Date.

# Using this guide #

This guide has been created to support the adoption of profiles and FHIR resources. As such the site is structured around stakeholders including API users, developers and architects.  

{% include custom/api_overview.svg %}

The above steps outline a complete API journey from imagination and exploring to developing local APIs using profiles all the way to deploying a live API.

{% include custom/contribute.html content="If you want to get involved in any part of this then please get in touch with careconnect@interopen.org "%}

# Focus #

The current site focuses on a typical API Developer's Journey as highlighted by the green boxes below in the developer journey:

<img src="images/roadmap/guide-focus.png" style="width:100%;max-width: 100%;">

NHS Digital is contributing to progressing the profile developmenet.

Please see the explanation of the complete development roadmap.

{% include custom/contribute.html content="Please contact [careconnect@interopen.org] to get involved." %}



# Resource Roadmap #

The [API journey](overview_api_journey.html) outlines the development roadmap for the RESTful APIs outlined within this site.

<img src="images/roadmap/roadmap-online.png" style="width:100%;max-width: 100%;">

The above roadmap illustrates the steps necessary to create, test and verify the profiles as well as some of the supporting tooling which might be necessary to build to provide viable APIs.

{% include custom/contribute.html content="To get involved in any parts of the roadmap or to discuss the other elements please get in touch with careconnect@interopen.org "%}
