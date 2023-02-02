# Software Requirements Specification for Local Management System Notes
## Introduction
### Purpose
- For International Union of Operating Engineers (IUOE)
- This is a group of heavy equipment operators & stationary Engineers
---
### Doc convention
- shall means strict!
- should means possibilities
- may means a course of action permissible
---
### Product Features
- add new members
- update member's info
- update member's membership status
- add new contractor
- record payments from members
- record administrative dues paid by third parties
- record S-charter dues by contractor
- view and print member information for reporting to the membership,IOUE, and regulatory bodies
---
### Additional Features
- shall be implemented using client/server model
- shall allow mult users to access via LAN(TCP/IPv4) or Internet
- shall enforce privelege levels for group roles and indiv roles
- shall include ability to record each access attempt and action performed for auditing
- shall secure info in transit and in rest (db, over network)
---
### Inclusion of the following modules
- training record for each member
- dispatch record (job assignments) for each member
- allows for view of Local contracts and other docs by members
---
## Overall Description
### Perspective
- currently using Access and paper method (disgustin')
- all libs/software must be open source
---
#### Project Features
### Membership Management
- includes the roles: Membership Records manager, LMS Admin, membership records users
- view pg 12-13 fig 2.1, 2.2
---
### Functions
#### Add new member
- details data types, size of storage, constraints, primary keys/ids

#### Update member information
- search roster
- select member
- edit selected member record
- details constraints

#### Update member's membership status
- search roster
- select member
- edit member's status (only status!)
---
### Contractor Management
#### Add Contractor
- require login and appropriate priv
- log to audit log
- describes the data types, size of storage, constraints, defaults
#### Update Contractor
## NonFunctional Requirements
## Standards and References


### Questions to do list
- what defines a member vs a contractor
- what is included in members info
- what are the different membership statuses
- how payment from members
- what are s-charter dues
- what are administrative dues
