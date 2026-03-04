Name
- PascalCase
- Unique
Fixed set of attributes (columns)
- camelCase (or snake_case)
- Unique within relation
	- sometimes useful to make unique within part or all of database
Tuples (a row of values)
Degree (number of attributes)
Cardinality (number of tuples)


Data Types
- allows validation
- minimise storage space used
	- appropriate type
	- variable length types

### Primary Keys
#### Natural Key
- Exists beyond the database
- SSN, address
#### Automatically Generated
- Used if natural key isn't viable

#### Foreign Key
- Matches primary key of some other relation
- Department name is a bad foreign key
	- What if it changes
- Department number/ID is better


### ER mapping
1. Create relations for strong entities
2. Create relations for weak entities
3. Create relations for specialisations
4. Add foreign keys for 1:N relationships
5. Add foreign keys for 1:1 relationships
6. Create relation for M:N relationships
7. Non-binary relationships
8. Multi-Valued Attributes 

1-3: Entity Boxes
4-7: Relationship Lines
8: Multi-Valued Attributes


#### 1.
For each strong entity, create a relation with:


#### 3.
Mandatory And
- Create a single relation
	- Add boolean attributes to distinguish type
	- Add all additional attributes from subtypes to the supertype