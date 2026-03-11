### Categories of Constraints
#### Inherent Model-Based / Implicit
Attribute values cannot be composite
This is a feature of the flat relational model

#### Schema-based / Explicit
Specified using **Data Definition Language** (DDL)
- Required Data (NOT NULL)
- Domain Constraint (Data Types)
- Entity Integrity (PRIMARY KEY & NOT NULL)
- Validity Checking (CHECK)
- Referential Identity (FOREIGN KEY)

#### Application-Based / Semantic
Rules that cannot be defined in the schema
Business policy
Enforced through external applications etc


### Specifying Constraints
A **constraint name** uniquely identifies a constraint in a database
#### Syntax
```
CONSTRAINT <constraint name> <constraint type>

CREATE TABLE employees 
(
emp_id INT,
emp_name VARCHAR(50)
PRIMARY KEY (emp_id)
CONSTRAINT PK_Employees PRIMARY KEY (emp_id)
)
```