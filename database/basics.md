# Basic terminlogy
- `Database`: A collection of relations
- `Table`/`Relation` (consists of 2 parts) (**it's not a collection of data, it is a description of an entity**)
  - `Schema`: description (or metadata), for example `wish`
  - `Instance`: An actual set of data satisfying the schema, for example: 1st `Rollerblades`, 2nd `Chair`


> **_We design database based on logic/semantics that we want to convey._**

### Note structure
tables **_must have only primitive types_** like: `strings`, `numerics`, `data and time`

**`For examples`**: We have a **wishlist** (_a collection of **wishes**_), each wishlist is themed ("holydays", "birthday", etc.),
but since we cannot have in DB just a table `wishlist`, that has field `wishes` (since it is not a primitive and a bad practice), we need to divide to a simplest form:  
- `wishlist`: Relation with a name (name is the filter)
- `wish`: Relation with description of a wish iteself

**`The way to go`**: Associate a relation, to where it belongs (groups, concentrate) in a DB (based on semantics).  
S
