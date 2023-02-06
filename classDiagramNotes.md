Classes usually are nouns (oop focus), but can be verbs (functional focus)

## Possible classes:
#### All tasks are living in LMS System space
### Attribute checklist:
1. Retained information. The potential class will be useful during analysis only if information about it must be remembered so that the system can function.
2. Needed services. The potential class must have a set of identifiable operations that can change the value of its attributes in some way.
3. Multiple attributes. During requirement analysis, the focus should be on “major” information; a class with a single attribute may, in fact, be useful during design but is probably better represented as an attribute of another class during the analysis activity.
4. Common attributes. A set of attributes can be defined for the potential class, and these attributes apply to all instances of the class.
5. Common operations. A set of operations can be defined for the potential class, and these operations apply to all instances of the class.
6. Essential requirements. External entities that appear in the problem space and produce or consume information essential to the operation of any solution for the system will almost always be defined as classes in the requirements model.
### system
- user type
- user name
- user pass
- login()
- register()
- logout()
### database
- collection of members  
- add() -- defined by manager
- edit() -- user, manager
- ...
### permission class
- role
- id (username?)
### Dues
- type
- amount
- payment()
### Membership Records manager
  - view/print user reports
  - create new mem record
  - login/logout
  - edit member record
  - record member dues payments
  - record admin dues payments
  - record s-charter dues
  - create new employer records
  - edit employer record
  - membership reports
  - view member records
### Membership Records user
  - view/print user reports
  - create new mem record
  - login/logout
  - edit member record
  - record member dues payments
  - membership reports
  - view member records
#### Tasks are in the LMS Admin space
### LMS Admin
  - Login/logout
  - create new LMS user
  - change user name
  - change user pass
  - change user roles
  - deactivate user
  - delete deactivated user after ...
  - create role
  - edit role
  - delete role
  - delete transaction
  - view/ print user report
### Reports
  - ...
  - ...
### Receipts?
  - ...
