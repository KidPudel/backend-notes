# Basic terminlogy
- `Database`: A collection of relations
- `Table`/`Relation` (consists of 2 parts) (**it's not a collection of data, it is a description of an entity**)
  - `Schema`: description (or metadata), for example `wish`
  - `Instance`: An actual set of data satisfying the schema, for example: 1st `Rollerblades`, 2nd `Chair`


> **_We design database based on logic/semantics that we want to convey._**

### Note about how to structure a database
tables **_must have only primitive types_** like: `strings`, `numerics`, `data and time`

**`For examples`**: We have a **wishlist** (_a collection of **wishes**_), each wishlist is themed ("holydays", "birthday", etc.),
but since we cannot have in DB just a table `wishlist`, that has field `wishes` (since it is not a primitive and a bad practice), we need to divide to a simplest form, so at the base, those entities are:
- `wish`: table, with wish description schema
- `wishlist`: table, with name for the wish's group

**`The way to go`**: Associate a relation, to where it belongs (groups, concentrate) in a DB (based on semantics).  
In this example: Wish is accociated with it's list (wishlist), so by associating name of the wish group to each wish, we endup with wishes, that at its own instances all bounded to group/groups.

# Relationship types
## One to Many
1 to many: When one record groups (bounding) depending on it, records (from other table), by appearing in other records multiple times (1 record, appears in many (many depend/relates on it) other records from other table)
