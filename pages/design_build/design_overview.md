---
title: Overview
keywords: foundations
tags: [fhir,rest]
sidebar: foundations_sidebar
permalink: design_overview.html
summary: "Design and Build APIs focuses on how to combine the resources in a callable API "
---


## 1. Design & Build Overview ##

This page provides an overview of how the FHIR STU3 Resources that compose the EoLC message could be packaged together into an API to start the Design & Build process. 

The previous Atomic Units concept has been represented as Questionare in a QuestionareResponse in the suggestion for an API.

## 2. API's ##

Combining the [FHIR Resources](explore.html) into an API has involved the following assumptions:
1. End of Life Care Interoperability Use Cases and User Stories
2. EoL National Minimum Dataset Relationship Diagram 

This API has been establised as a useful starting point for EoLC but the concept of forming the APIs could be used in other solutions depending on the architecture and technological need.


## 3. API approach ##

For simplicity and to enable Provider and Consumer testing the Questionare and QuestionareResponse profiles have been used to provide a simple starting point to form the complicated questions and work performed in EoLC to date.

## 4. Other possible approaches ##

Other approaches have been considered during this work, such as:
1. Atomic units becoming a bundled parameter extended operation
2. Non-attested Document
3. RESTful calls to form your own EoLC




