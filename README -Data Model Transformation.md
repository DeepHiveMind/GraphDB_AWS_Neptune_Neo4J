# Data Model Transformation from RDBMS Data Model to GraphDB Data Model

Let us look at some of the key components in a relational data model and translate those into components of a graph data model. The transformation begins!

|RDBMS Model Components | GraphDB  Model Components | Observations|
| :--: | :--: | :--: |
|Table| Node Label /  Vertex Label |Table to Node Label – each entity table in the relational model becomes a label on nodes in the graph model.| 
|Row| Node / Vertices |Row to Node – each row in a relational entity table becomes a node in the graph.|
|Column| Property  |*Column to Node Property* – columns (fields) on the relational tables become node properties in the graph. *Column to Edge Property*|
| Join Tables | Edges (Relationships) | Join tables in RDBMS Models are transformed into relationships (Edges), columns on those tables become relationship properties |
|Technical primary keys (PK / FK) |  No Technical  primary keys (Business primary keys only)| GraphDB removes technical primary keys, keep business primary keys.|

In GraphDB Data Model additional observable points vis-a-vis RDBMS Data Model are:

 - No defaults – remove data with default values, no need to store those.
 - Add Constraints/Indexes – add unique constraints for business primary keys, add indexes for frequent lookup attributes.
 - Index Columns to Array – indexed column names (like email1, email2, email3) might indicate an array property.
 - Foreign keys to Relationships – replace foreign keys to the other table with relationships, remove them afterwards.
 - Clean up data – duplicate data in denormalized tables might have to be pulled out into separate nodes to get a cleaner model.

