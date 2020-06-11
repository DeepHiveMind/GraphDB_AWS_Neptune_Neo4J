# GraphDB_AWS_Neptune_Neo4J

We live in a connected world! There are no isolated pieces of information, but rich, connected domains all around us.

*Welcome to the Real world of System-Of-Engagements*

<img src="img/graph_data_modeling.jpg" width="500" height="200" border="10">

**Welcome to world of GraphDB!!**


- Graph databases **natively embraces relationships**. 
- While other databases compute **relationships at query time** through **expensive JOIN operations**, a Graph database stores **connections alongside the data** in the model.
- The Property Graph Model: A *Node-Edges-Properties model* to *organize Domain Data and their inherent relationships*. A quick glimpse of Property Graph Model- 
  
|Relational Model | Graph Model|
| :--: | :--: |
|<img src="img/relational_org_chart.jpg" width="500" height="200" border="10">|<img src="img/graph_org_chart.jpg" width="500" height="200" border="10">|
|Please click on the above image to expand|Please click on the above image to expand|   

- Independent of the total size of your dataset, graph databases excel at managing highly-connected data and complex queries.
- Graph DB is used for very many types of Use Cases (*not* just for *Social Graph* or *Recommendation engine*), such as 
	- **MASTER DATA MANAGEMENT**
	- **GRAPH BASED SEARCH**
	- **REAL TIME RECOMMENDATIONS**
	- **SOCIAL NETWORK**
	- **FRAUD DETECTION**
	- **Google Maps and Routes APIs**
	- **NETWORK & IT-OPERATIONS**
	- **IDENTITY & ACCESS MANAGEMENT**
	- **System-Of-Engagements**

- Graph DB Offers over other RDMBS as well as NOSQL DBs
	- Intuitiveness
	- Speed
	- Agility
**graphs are the most natural way to model data in the real world.**

Please relish [Video](https://www.youtube.com/watch?v=JaATpaGDNh4) to understand the aforementioned high level concepts in a better way.

***
CONNECTED DATA

Many of the most important questions we want to ask of our data today from our **Data Platform (System-of-engagement)** require us to understand **how things are connected – in what ways, and with what strength, weight or quality**. Such as:

- Which applications and services in my network will be affected if a particular network element—a router or switch, for example—fails?
     - Do we have redundancy throughout the network for our most important customers?
- What's the quickest route between two stations on the underground?
- Which friends and colleagues do we have in common?
- What do you recommend this customer should buy, view, or listen to next?
- Which products, services and subscriptions does a user have permission to access and modify?
- What's the cheapest or fastest means of delivering this parcel from A to B?
- Which parties are likely working together to defraud their bank or insurer?
- Which institutions are most at risk of poisoning the financial markets?

This needs a Data Platform which can manage and make sense of 
     - **large volumes of variably-structured**, 
     - **densely-connected data**. 
     - what depends on what; how things flow;  analysing the impact of events on deep dependency chains;  identifying and assessing risk; (**All connected data problems**) :simley: .
     
These are the kinds of problems for which GrphDB like Amazon Neptune is ideally suited. 

P.S.: I am still a big proponent of **POLYGLOT DB/ FEDERATED DATA LAKE**.
***

#### The Quick rundown of this repo

*Please note:* 

 	- ***This page serve as the Index page.***
	- Please click on hyperlinks of the respective items to delve deep into it.
	- Please keep checking your **compass (this index page)** for to seamlessly steer your way to the next mile of this wonderful journey.

 
- [Tranformation from RDBMS Model Schema to Graph Data Model](README%20-Data%20Model%20Transformation.md)
- [AWS Neptune vis-a-vis Neo4j](README%20-AWS%20Neptune%20%26%20Neo4j.md)
- [Polymorphysm in AWS Neptune](README%20-Polymorphysm%20in%20AWS%20Neptune.md)
- [Deep dive into AWS Neptune Property Graph DB](README.md)
	- [AWS Neptune Cluster Setup]()
	- [AWS Neptune Property Graph DataModel UNDERSTANDING](/notebook/02-Labelled-Property-Graph.ipynb)
	- [AWS Neptune Property Graph DataModel CREATE & QUERY 1 Using Gremlin Notebook](/notebook/PG-Data-model-Query-1.ipynb)
	- [AWS Neptune Property Graph DataModel CREATE & QUERY 2 Using Gremlin Notebook](/notebook/PG-Data-model-Query-2.ipynb)

	- [Bulk Loading Data into AWS Neptune]()
	- [CREATE, VISUALIZE & PERDICTIVE QUERY play on SOCIAL NETWORK PG Datamodel Using Gremlin Notebook](/notebook/03-CREATE-QUERY-VISUALIZE-Social-Network-Recommendations.ipynb)
	- [Writing to Amazon Neptune from Amazon Kinesis Data Streams]()
	- [Production garde Data pipeline with Neptune as Data Sink]()
	- [Visualize data in Amazon Neptune using VIS.js](https://github.com/DeepHiveMind/AWS_GraphDB_AWS-API-GW_AWS-Lambda_Visualization_Pipeline)


## AWS Neptune Property GraphDB Codesets
Following folders carry **Jupyter notebook (interactive python notebook/ .ipynb)** || **Python Codeset as well as pseudocode** ||  **refernce blogs** et al.

- **[Social-Network-Recommendations](/notebook/03-CREATE-QUERY-VISUALIZE-Social-Network-Recommendations.ipynb)**
  

- **[Visualize data in Amazon Neptune using VIS.js](https://github.com/DeepHiveMind/AWS_GraphDB_AWS-API-GW_AWS-Lambda_Visualization_Pipeline)**

- **[AWS Neptune Cluster setup](neptune)** 
