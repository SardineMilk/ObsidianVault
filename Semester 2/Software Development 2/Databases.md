Identify
Analyse
Design
Create and use through web


Purpose
- Capture, edit, store, analyze, share, display

Data
- Facts, concepts or instructions 
- Suitable for communication between people

Processing data:
Date of birth -> Age
Salary -> Highest page employee

Useful for large colections of data

![[Pasted image 20260225091529.png]]

![[Pasted image 20260225091548.png]]
End User:
Use through applications, no knowledge of underlying database

Application developers:
Query database, know the structure

Database Designer:
Manages database
Extensive knowledge




Client/server platform
- Client computers receive services from a server computer
Database server
- A program running on server hardware
- Provides database servers to client machines


Database Models:
Flat file
- Text file
Hierarchical
- Tree based
Network
- Progression from hierarchical
- Child record can have multiple records
- Child -> Parent could be "x is employed by y"
Relational *<- We will use this*
- Table of values
- Each row is a tuple (record)
- Each tuple element is an entity or relationship
- Class, Teacher related through the common attribute TeacherID
- Advantages
	- Simple
	- Easy data retrieval
	- Data integrity
	- Flexibility
	- Consistent standard
- Disadvantages
	- Performance
	- Rigid, limited structure
	- Cost?
Object Oriented
- State (attributes)
- Behaviour (operations)
- Relationships
	- Association
		- Like relations
	- Aggregation
	- Composition 
	- Inheritance
		- Parent database object, subclass database objects
- Advantages
	- Rich capabilities
	- Reusable
- Disadvantages
	- Nobody uses it

Object Relational
- Relational model that uses OOM when required
- Advantages
	- very rich capabilities
	- Literally nobody uses it



|     |     |     |
| --- | --- | --- |
|     |     |     |
|     |     |     |
|     |     |     |
|     |     |     |
|     |     |     |
|     |     |     |


DMBS
- CRUD - Create Read Update Delete
- Data dictionary describing items
- Transactions
	- either all or none of the task is done
- Concurrency control
- Recovery
- Authorisation
- Integrity
- Security

DMBS components
- Query processor
- Storage manager
- Database

ANSI-SPARC architecture
Many external views
^
Conceptual schema
^
Internal schema
^
Database 


Development Lifecycle
- Application design
- Prototyping
- Data loading
- Testing 
- Deployment
- Maintenance