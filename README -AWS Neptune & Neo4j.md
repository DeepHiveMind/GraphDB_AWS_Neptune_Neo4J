# AWS Neptune vis-a-vis Neo4j

Let us look at some of the key comparative view b/w AWS Neptune vis-a-vis Neo4j

***
2 Data Domains for GraphDB -
- **PG Model/Tinkerpop Gremlin or CQL**
- **RDF Model / SPARQL**

Customers in domains using 
	- **triple entities** with **subject-predicate-object** such as **knowledge graphs** or **clinical data** stores prefer **RDF Model**,
	- while customers from **variably structured data sources** such as **social media** prefer **PG Model**
	
{Property Graph (PG) model:Apache TinkerPop Gremlin,or, Cypher Query Language (CQL) }
{Resource Description Framework (RDF) model: SAPRQL}
***


|**AWS Neptune** | **Neo4j** | 
| :--: | :--: |
|Amazon Neptune is a **fully-managed cloud-based** high-performance graph database that is generally available on AWS. You can use open and popular graph query languages such as **Gremlin and SPARQL** to query connected data.|Neo4j is the world's leading native graph database platform. It is written in Java and Scala and is accessible with the **Cypher Query Language (CQL)** developed internally at Neo4j and later opened sourced through the openCypher project.Neo4j has been working exclusively with graph technology since 2007 and it boasts the *world's largest ecosystem for Graph DBMS*.|
|AWS handles **provisioning, patching, backup, recovery, failure detection and repair** for you.|One has to leverage Dockerization & K8S to manage those NFRs |
|Amazon Neptune is closed source.|Neo4j is currently available in a GPL3-licensed open source community edition with online backup and high availability extensions licenced under the Affero GPL.|
|Supports both -  the **Property Graph (PG) model** and its open source query language - **Apache TinkerPop Gremlin** ,OR, the W3C standard **Resource Description Framework (RDF) model** and its standard query language, **SPARQL**.{**PG Model / Tinkerpop Gremlin** and  **RDF Model / SPARQL**}. Once you declare which choice to use, the two *models are not interoperable*. This does not come as a suprise as bridging the two models is not trivial. |Supports only **PG Model**. **PG Model/ Cyper QL** (Neo4j own custom query language - Cypher).OpenCypher has some industry support, most prominently by **SAP HANA Graph, Redis and AgensGraph**. Neo4j also added support for **Cypher on Spark** and ** Cypher for Gremlin**. {Cypher on Spark is just a wrapper around GraphFrames}. |
|Amazon Neptune **conspicously lacks** graph data **visualization**.|The default Neo4j server comes with a **powerful customizable graph visualization (in-browser) tool**. The Neo4j browser is based on the **built-in D3.js** library. This web interface can be used for **querying, adding data and creating relationships** amongst other things.|
|Amazon Neptune does not support advanced data analytics with solutions such as Spark and GraphX|Neo4j allows specific delegation for ad-hoc reporting and analytics instances. |
|SECURITY - Amazon Neptune isolates your Graph Data in **Virtual Private Clouds** . There are also firewall settings and network access controls to database instances.Permission are managed with **standard AWS IAM roles**. Amazon Neptune instances can be **encrypted with AWS KMS**. P.S.: Encrypting an existing unencrypted Neptune instance is not supported, you have to migrate your data to a new encrypted instance to achieve this.As a managed service, AWS keeps your Amazon Neptune instances up-to-date with the latest patches (you can control when patches are applied).|**Native user role management is only available with Neo4j Enterprise Edition**. Neo4j supports **pluggable authentication with the LDAP protocol** which allows integration with ***other LDAP-compatible authentication services*** such as **Active Directory, OpenLDAP**, and  **Kerberos**.Neo4j supports **subgraph access control making** it possible to restrict a user's access to specified portions of a graph.|

***
- AWS chose not to include **RDF inference** in Amazon Neptune citing it's impact on scalability. If you want support for these, you have to use a **reasoner engine** *in addition to* Neptune.

- Inference provides the ability to process **RDFS or OWL rules** *used to declare schema when adding data*. Schema declared often includes **classes, inheritances, types, restrictions for nodes, edges and properties**.
***

- Unlike some other Tinkerpop-enabled graph databases, Neptune allows you to attach multiple labels to a vertex
- The schema-free nature of Neptune: no two vertices, even those sharing the same label, need have the exact same set of properties.

