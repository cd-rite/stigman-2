# User GUIDE

TOC:
1. [Introduction](#introduction)
2. [STIGMAN Layout](#layout)
3. [Reports](#reports)
4. [Data Organization](#data-org)

## Introduction <a name="introduction"></a>

 #### Terminology

## STIGMan Layout <a name="layout"></a>
 ### Home Panel
 ### Nav Panel
  #### Nav Tree
   ##### Collections
   ##### COLLECTION MANAGEMENT
   ###### STIGS
   ###### ASSETS
   ###### REPORTS
  ### STIG Evaluation
  #### STIG Rules Panel
  #### Rule Info Panel
  #### Evaluation Panel
  #### Resources Panel
 ### Reports <a name="reports"></a>
  #### Findings Report
  #### Status Report
 ### Collection Management
#### Collection Data Panel
#### Assets Panel
#### Users Panel
#### STIGs Panel
### Admin Functions
#### Users
#### Collections
#### STIGs

## Data Organization <a name="data-org"></a>
### Collections
### Assets
### STIGs
#### Users


## Other Functions

## User Access Info


### Collection Grants
- User can be granted access to one or more Collections
- Each User/Collection grant has a required `accessLevel` property for that User in that Collection

- | `accessLevel` | Asset/STIG access | Collection management | Collection Delete
    |:---:|:---:|:---:|:---:|
    |Restricted|Assigned only|No|No|
    |Full|All|No|No|
    |Manage|All|Yes|No|
    |Owner|All|Yes|Yes|

