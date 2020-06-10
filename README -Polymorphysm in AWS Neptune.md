# Polymorphysm in AWS Neptune


***
AWS Neptune exhibits Polymorphysm by supporting BOTH the Data Domains for GraphDB -
- **PG Model/Tinkerpop Gremlin or CQL**
- **RDF Model / SPARQL**

Customers in domains using 
	- **triple entities** with **subject-predicate-object** such as **knowledge graphs** or **clinical data** stores prefer **RDF Model**,
	- while customers from **variably structured data sources** such as **social media** prefer **PG Model**
	
{Property Graph (PG) model:Apache TinkerPop Gremlin,or, Cypher Query Language (CQL) }
{Resource Description Framework (RDF) model: SAPRQL}
***


- Supports both 
	- the **Property Graph (PG) model** and its open source query language - **Apache TinkerPop Gremlin** ,&
 	- the W3C standard **Resource Description Framework (RDF) model** and its standard query language, **SPARQL**.{**PG Model / Tinkerpop Gremlin** and  **RDF Model / SPARQL**}. 
- But, Once you declare which choice to use, the two *models are not interoperable*. This does not come as a suprise as bridging the two models is not trivial. 
- AWS chose not to include **RDF inference** in Amazon Neptune citing it's impact on scalability. If you want support for these, you have to use a **reasoner engine** *in addition to* Neptune.

- Inference provides the ability to process **RDFS or OWL rules** *used to declare schema when adding data*. Schema declared often includes **classes, inheritances, types, restrictions for nodes, edges and properties**.

- Amazon Neptune is a **fully-managed cloud-based** high-performance graph database that is generally available on AWS. You can use open and popular graph query languages such as **Gremlin and SPARQL** to query connected data. AWS handles **provisioning, patching, backup, recovery, failure detection and repair** for you.
