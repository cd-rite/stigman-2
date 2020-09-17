# STIG Manager

## What is STIG Manager?
STIG Manager is an Open Source API and Web client for managing the assessment of Information Systems for compliance with [security checklists](https://public.cyber.mil/stigs/) published by the United States (U.S.) Defense Information Systems Agency (DISA). STIG Manager supports DISA checklists [distributed](https://public.cyber.mil/stigs/downloads/) as either a Security Technical Implementation Guide (STIG) or a Security Requirements Guide (SRG).

Our Project incorporates software developed since 2012 by the [U.S. Naval Undersea Warfare Center Division Newport (NUWCDIVNPT)](https://www.navsea.navy.mil/Home/Warfare-Centers/NUWC-Newport/). More information, and the software itself, is available on GitHub: [STIG Manager](https://github.com/NUWCDIVNPT/stig-manager/)


## STIG Manager supports STIG Assessments in Steps 3 and 4 of the RMF Process

Throughout the RMF process, STIG Manager serves as the single source of truth for users, evaluators, managers, RMF Package reviewers, ISSEs, NQVs, and automated tools about Assets, STIGs, and their current assessment status.  By allowing everyone involved in the process to refer to the same set of data and reports, the RMF process can be executed efficiently and it's progress monitored effectively. Something about automated tooling engaging with the API here for both direction and submitting results.


STIG Manager provides data structures, assessment workspaces, and Reports for managing these Steps of the RMF process.  

### Collections, Assets, STIGs, and Reviews
STIG Manager's primary organizational structure is the Collection. A Collection can be created to mirror components of an RMF Package, requirements identified in a Security Assessment Plan, or an entirely different principle that may be more convenient, such as by an organization's Lab or by Asset OS.

Collections are composed of:
  * Assets
  * STIGs attached to those Assets
  * Reviews of the Rules that compose each attached STIG
  * User Grants providing access to some or all of the Assets/STIGs in that Collection
  * Reports providing Status and Findings information
  
Migrating to STIG Manager is easy because it can use your existing artifacts to build and update Collections. Assets, STIGs, and Reviews can be populated with the .ckls produced by STIG Viewer or the automated STIG assessments in XCCDF format produced by the SCC tool, as well as manually from the Collection Configuration tab.  Once a Collection is created in STIG Manager, Users can be granted access to see the current results for each STIG on an Asset, or the whole Collection. Users can see automated tool evaluations, and Rules that still require evaluation. 

[Collection Video](assets/videos/sc-3.mp4 ':include height=400px controls')


### Workspaces
The STIG Manager Client provides efficient workspaces for creating Collections of Assets and their associated STIGs, and assigning specific Users to evaluate those STIGs. User tasking can be managed in real time by granting Collection roles with varying levels of access, down to individual STIGs on specific Assets. Users have access to efficient STIG Review workspaces that provide resources to guide their evaluations, such as their previous answers for other Assets or whether an automated check is available, as well as allow them to evaluate multiple Assets at once.  Every User gets real time reports and statistics about their progress and the status of their Reviews, scoped to their level of access in each Collection. 

### Workflow
STIG Manager supports an "RMF Package Workflow" that allows designated Collection Owners to "Return" Reviews to evaluators for further revision or clarification, such as when a Finding requires further Detailing. Collection Owners can also "Accept" a Review, locking it from further revision by evaluators while they prepare their POA&M. 

### Reporting
Reports adjust as new STIGs are assigned, results imported, or when new DISA STIG revesions are imported, to provide information on the status and progress of evaluations.

The Collection Configuration workspace provides real-time totals for level of work required as changes to Assets and STIGs are made.

### User Access Controls
STIG Manager provides granular Role-Based Access Controls that can give Users access to some or all of the Assets and their STIGs in a Collection.

### STIG Manager integrates with the RMF Lifecycle approach
STIG Manager is (almost) ready to support a life-cycle approach to RMF. With the implementation of the "Continuous" Workflow, STIG Manager will play a vital part of the RMF lifecycle.  When new STIGs are released, systems or the SAP changes, or new STIGs are applied, only the new content needs to be asessed.  STIG Manager timestamps every review, to help determine compliance with the Continuous Evaluation approach.


## Getting Started with STIG Manager

### Users
[A quick walkthrough to familiarize Users with STIG Manager and help them get started evaluating STIGs.](Quickstart_Guide.md)

### Admins
A quick walkthrough aimed at Administrators of STIG Manager.

### Operations
STIG Manager is available on GitHub and as a [Docker image](Docker.md).

### Terminology used in STIG Manager
An explanation of the [Terms and concepts](terminology.md) used in STIG Manager.

### Contribution Guide

Please read our [CONTRIBUTING](CONTRIBUTING.md) document. It explains:
- How you can get involved in the project and contribute
- How to set up a development environment to work with the project's code 


## STIG Mnager is an active, Open Source project

STIG Manager is actively under development. Get the latest info here: [STIG Manager](https://github.com/NUWCDIVNPT/stig-manager/)


STIG Manager is participating in the [Code.mil Open Source initiative](https://code.mil/).

The STIG Manager project is chiefly composed of the STIG Manager API and the STIG Manager Client. The STIG Manager API provides a well-defined programmatic interface for engaging with the resources and data it maintains. The STIG Manager Client is just one use of the API that this architecture enables. In a modern, open source microservice-oriented ecosystem, other developers will be able to contribute new utilities and services that will expand functionality. User Stories, Feature Requests, Bugs, and Issues will be tracked in GitHub to help determine future efforts. Several candidate utilities, such as automated imports of HBSS SCAP evaluations and a STIG Browser, are already listed in the STIG Manager Github repo.

### More Devopsy/containery/OSSy/APIy outro stuff

STIG Manager is a modern, containerized application built to take full advantage of a CI/CD DevOps pipeline. Updates to STIG Manager will trigger automatic testing and image creation. Organizations will have the option to engage with the pipeline to automatically deploy new versions to their test environments, or directly to production.





### Status

This repository is receiving several commits a week as we work [Phase 1 of the Project](roadmap.md). During Phase 1, the `main` branch will contain buildable, development-quaity code. Daily commits are being made to the `phase-1-dev` branch and some of these commits may include unbuildable code.

## Roadmap

All new contributions to the Project will be directed towards stable production releases of the software in accordance with our [Roadmap](roadmap.md).



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