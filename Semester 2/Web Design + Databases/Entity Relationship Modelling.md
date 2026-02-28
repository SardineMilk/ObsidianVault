Conceptual Database Design

ER Diagrams
- Notation
- Entities
- Relationships
- Attributes
- Constraints

Design choices



What are the entities?
What relationships exist between them
What information do we want to store
What are the business rules of the organisation
What integrity constraints arise from them


UML notation used in the course

Unified Modeling Language for ER representation
Not the same thing, but we use UML to represent ER concepts




Entity
- Thing
- Described by set of attributes
Entity type
- Group of entities with the same properties
Entity Occurrence
- A particular entity in the entity group

Attributes
- Simple
- Composite
	- name = first+last
- Derived
	- age from dob
- Single valued
	- one dob
- Multi valued
	- Multiple phone numbers


Primary key
- Uniquely identifies an instance
Candidate key
- key made of 2 or more attributes
Alternate key
- Other choices for pk


Relationships
Unary
- Entity and itself
Binary
- 2 distinct entities
Ternary
- Shop - Item - Supplier

Cardinality Constants
- One to one
- One to many
- Many to many

Partial Participation
- Not all entities must participate in relationship
- Cardinality lower bound of 0
Total Participation
- Each entity in the set must particiapate
- Lower bound of 1