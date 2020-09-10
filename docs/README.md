# STIG Manager

## What is STIG Manager?
STIG Manager is an API and Web client for managing the assessment of Information Systems for compliance with [security checklists](https://public.cyber.mil/stigs/) published by the United States (U.S.) Defense Information Systems Agency (DISA). STIG Manager supports DISA checklists [distributed](https://public.cyber.mil/stigs/downloads/) as either a Security Technical Implementation Guide (STIG) or a Security Requirements Guide (SRG).

Our Project incorporates software developed since 2012 by the [U.S. Naval Undersea Warfare Center Division Newport (NUWCDIVNPT)](https://www.navsea.navy.mil/Home/Warfare-Centers/NUWC-Newport/). Our initial goal is to modernize the original software, available as [STIG Manager Classic](https://github.com/NUWCDIVNPT/stig-manager/tree/classic) (see below), to provide services via a REST API that supports a choice of data storage backends.  



## Getting Started with STIG Manager

### QuickStart User Guide
A quick walkthrough to help users get started evaluating STIGs.

### QuickStart Admin Guide
A quick walkthrough aimed at Administrators of STIG Manager.

### Contribution Guide

Please read our [CONTRIBUTING](CONTRIBUTING.md) document. It explains:
- How you can get involved in the project and contribute
- How to set up a development environment to work with the project's code 

### STIG Manager Strategic Planning Text

##### 5.0 STIG Manager 
_____

The STIG Manager is a data base driven, web application that offers collaborative tooling for completing the assessment of Information Systems for compliance with STIG checklists published by DISA. STIG Manager Implements a collaborative, multiuser service with comprehensive role based access controls for establishing STIG test plans, collecting evidence, reporting findings, and managing the STIG assessment workflow. The service exposes a standardized interface for interacting with third-party tools such as the other NAVSEA strategic products in this document.   

#### 5.1 Challenge 
____

The STIG assessment process produces large data sets that have traditionally been managed by using ad hoc, standalone technologies that scale poorly, such as spreadsheets and file collections. Data that requires collection and processing include artifacts from the following:  

Determining which STIG assessments have been associated with each information system component.  

Collecting the evidence from manual and automated STIG assessments.  

Identifying STIG checks requiring reassessment when quarterly revisions get released.  

Assigning STIG assessment efforts to specific workforce members. Generating and tracking artifacts for upstream tools such as eMASS. 

##### 5.2 A Better Way 
_____

STIG Manager displays base STIG data within its own web application. It supports searching and viewing STIG content, mapping STIG content to RMF controls, and identifying opportunities for automated assessment. Once modernized, it will support access to this base STIG data from other cybersecurity tools (such as NAVSEA native and DISA tools) so they can implement STIG-related features. 

STIG Manager supports the STIG evaluation process by mapping STIG assessments to components of an information system, providing an interface for recording manual STIG evaluations and managing automated evaluations when they are available. STIG Manager provides workflows that automatically generate complex and traditionally labor-intensive artifacts, such as a Plan of Action & Milestone (POA&M), for incorporation into RMF packages.  

The modernized project will retain these capabilities and provide a standardized data interface for cybersecurity tools that can incorporate this information. Enhancements to STIG Managers’s workflows could allow output that enable real-time analysis of the STIG compliance process for visualization. This enhancement can support automatically submitting this information to upstream tools such as eMASS.  

The STIG Manager Client provides efficient workspaces for creating Collections of Assets and their associated STIGs, and assigning specific users to evaluate those STIGs. User tasking can be managed in real time by granting collection roles with varying levels of access, down to individual STIGs on specific assets. Users have access to efficient STIG review workspaces that provide resources to guide their evaluations, such as their previous answers for other assets or whether an automated check is available, as well as allow them to evaluate multiple assets at once.  Every user gets real time reports and statistics about their progress and the status of their reviews, scoped to their level of access in each collection.  

Throughout the RMF Step 4 process, STIG Manager can serve as single point of truth for users, evaluators, managers, RMF Package reviewers, and automated tools for assigned STIGs and their current status.  


##### roadmap stuff:
_____
 Further enhancements to this capability will distinguish between having access to a particular STIG evaluation and the tasking to evaluate it. 

The Collection Management workspace provides real-time totals for level of work required as changes to assets and STIGs are made. 

## Status

This repository is receiving several commits each day as we work [Phase 1 of the Project](docs/roadmap.md). During Phase 1, the `master` branch will contain buildable, development-quaity code. Daily commits are being made to the `phase-1-dev` branch and some of these commits may include unbuildable code.


## STIG Manager Classic for Docker

We encourage you to [checkout the Classic branch](https://github.com/NUWCDIVNPT/stig-manager/tree/classic) and run a demonstration of STIG Manager Classic. Although STIG Manager Classic uses deprecated technologies, it is useful as a reference until our new API achieves parity.

## Roadmap

All new contributions to the Project will be directed towards stable production releases of the software in accordance with our [Roadmap](docs/roadmap.md).
