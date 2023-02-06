# Software Requirements Specification for Local Management System Notes
---
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
---
#### Update member information
- search roster
- select member
- edit selected member record
- details constraints
---
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
---
#### Update Contractor
- require login and appropriate priv
- browse contractor list
- select a contractor
- edit selected contractor record
- details constraints
---
### Dues Payments
#### Record member's dues payment
- require login and appropriate priv
- search the member list
- select a member
- enter a payment for the member
- opens payment entry screen
  - display member info
  - Cash, check, ACH
  - ... lots here describing how the payment entry is calculated & displayed
- details constraints
---
#### Record S-charter dues by contractor
- require login and appropriate priv
- search the contractor list
- select a contractor
- enter dues w/associated contractor
- display dues entry
---
### Reporting
#### Members Dues Receipt - Union Book pg. 22
- require login and appropriate priv
- log to audit log
- receipt printed when member pays dues or on demand
- print
- reprint, need search, select for member
---
#### Daily Receipts and Deposit Summary
- require login and appropriate priv
- log to audit log
- select date range
- has heading, pg num
- has all payments collected, summary by payment type
---
#### Contractor Receipts
- require login and appropriate priv
- log to audit log
- select date range
- lists total dues payments
- has heading, pg num
- has all payments collected, summary by payment type
---
#### Member Information Change Report
- require login and appropriate priv
- log to audit log
- lists all changes made for all member records in date range
- has heading, pg num
- has title, date range, cur date
- has member name, register num, old/new info
---
#### Membership Per-Capita Activity Report
- require login and appropriate priv
- log to audit log
- lists membership status type changes
- report heading (...)
- heading, pg num
- lists status changes by type for each charter type
- total at bottom
---
#### Member's Transaction summary
- require login and appropriate priv
- log to audit log
- lists the total payments by mem in date range
- search, select by member
- select date range
- include cur date, memb name address, list of mem payments
---
#### Active Members and Retirees Total Report
- require login and appropriate priv
- log to audit log
- lists the membership by charter type
- only active/retiree
- heading(...)
- heading, pg num
- body - memb name, address, init date, pay thru date
- alpha sort
- grouping by charter
---
#### EEOC Report
- require login and appropriate priv
- log to audit log
- list total memb with status type
- abstract to totals only
---
#### Years of Service
- require login and appropriate priv
- log to audit log
- lists active and retiree types by years of service
- enter num years since init
- list all mem with num years
- heading(...)
- header, pg num
- include mem name, init date
- alpha sort
---
#### Member Arrears Report
- require login and appropriate priv
- log to audit log
- list mem who are past due
- split into past due categories
- header(...)
- heading, pg num
- list mem name, charter, paid thru date
- alpha sort
---
### User Identification, Authentication, and Authorization
3 cat:
- managing roles
- managing users
- auditing users
#### roles
- Every task must have a required privilege level
---
#### management operations
- create new role
- edit a role - privileges
- delete role (only if no assignees)
- role report
  - list names and priv
---
#### management user operations
- create new user
- change username
- change user pass
- change user role
- deactivate user
- delete inactive user
- user report
  - specify user or all
  - include users, roles, last login date
---
#### pass guidelines
- len = 8-64 char
- periodic pass resets not required
- new/changed pass checked vs common pass list
- allow paste for pass
- allow show pass
- limit num of fialed pass attempts before lockout
---
#### pass storage
- meets SP 800-63B
---
#### Failed login attempts
- display login failure gui
- login failure message for too many failed attempts
- reset failed when success
---
### User Auditing
- formatting guidelines for logs
- spec guidelines for logs
---
#### Delete transaction
- require login and appropriate priv
- log to audit log
- LMS admin
- audit entry
- deleted transaction retained
---
### Global Config
- Report heading format
- min pass length
- login attempts
- conven fee
- charter types
- dues types
- status types
---
### Operating Environment
#### Client/Server Model - multiuser
- C++, witty, gui, may use SQL installed on host
---
## NonFunctional Requirements
### Performance
- requires multiuser access concurrently
---
### Security
#### Secure Network Connection
- TLS 1.2/1.3
---
#### Secure PII Storage
- requirements in 2.2.5 for pass and users
---
### Software Quality Attributes
#### User Documentation
- install
- configure
- use LMS
- detailed instructs using screenshots, diagrams, charts, tables, other visuals
---
#### Source code
- formal code doc
---
#### Support for future modules
- modules for future:
  - training record for each member
  - dispatch record for each member
  - allow members to view Local contracts and other docs
  ---
