---
author: "Kyle Jones"
date_published: "March 27, 2024"
date_exported_from_medium: "November 10, 2025"
canonical_link: "https://medium.com/@kyle-t-jones/4-myths-about-graph-databases-for-analytics-2eec7219a6d8"
---

# 4 myths about Graph databases for analytics Graph databases are incredible. They can connect data in ways that
traditional relational databases cannot. This creates opportunities to...

### 4 myths about Graph Databases for analytics
Graph databases are incredible. They can connect data in ways that traditional relational databases cannot. This creates opportunities to change how companies use their data to make decisions.



But, in my experience, using Graph DB is always more difficult than customers expect. This was largely due to customers' limited experienced with Graph DB and its special query language.

**Myths about using Graph DBs**

As part of introducing any new technology, the project sponsor will start learning about the solution and share the benefits of Graph DB with leadership across the organization. Unintentionally, these educational presentations can cause hype and set expectations that Graph DB can do much more than it was actually capable of doing.

In my experience, four key myths surround Graph DB technology that both lead to the technologies adoption and positioned it to fail.

- "The Graph creates relationships." No. The Graph uses declared relationships. Once a graph is highlight populated, it may be possible to infer relationships between nodes but the graph doesn't magically connect one dataset to another.
- "All data should be stored in the Graph DB." No. The Graph should index all relationships but it is not an efficient database for a number of formats such as time series.
- "Building the Graph is just like drawing a network diagram on a whiteboard." No. Business users are accustomed to drawing relationships on a whiteboard but translating those to graph requires much more precision than they have used in the past.
- "Graph DB can identify data quality issues." Sort of. Data quality is comprised on six parts: Completeness, Consistency, Conformity, Accuracy, Integrity, and Timeliness. The Graph can apply standards for consistency and conformity but that is not unique to Graph DB. Business users associated data quality with accuracy --- and Graph DB does not resolve data accuracy problems.

**Graph DB Use Cases**

**Linked Data:** Customers often seek a nirvana state in which all their data connects across business lines. While similar systems may be used by different business units, transactional data is rarely interchangeable to the degree people need for analytics.

**Schema on read flexibility:** Traditional applications define the schema for their data which restricts the variety of questions which can be posed to the data. ERPs often have dedicated staffs to build views on behalf of business customers. This means the speed of answering business questions is dependent on actions from an IT-team with no direct connection to the business problem. A predefined schema also leads to "functional fixedness" where users struggle to identify new use cases because they perspective is limited but the standard presentation of the data.

Questions Linked Data could answer:

- *How many compressors do we have? Are those compressors operated different by different parts of the business? Do different operating conditions lead to more/less maintenance?*
- *Which pieces of equipment are associated with process safety incidents? Are machines by a specific manufacturer more/less likely to be associated with safety incidents?*

**AI/ML:** Customers consider Graph DBs when they want to be able to conduct ML using graph patterns and also to deploy ML by using algorithms as nodes. Graph DBs can support traditional ML and also graph-specific algorithms.

**Challenges with implementing Graph DB**

In my experience, there are two key challenges limited the effectiveness of Graph DBs. Working though these took time and resources away from producing value and contributed to a general feeling that the project was unsuccessful.

- No standard Ontology: Graph DBs link data based on shared features. Since the data throughout the system is defined differently, there is not an obvious ontology that links all the data. This can be overcome but requires rethinking data and applying abstract classes to data --- a process that is foreign to most business users. For example, "Address", "Functional Location", and "Facility" could all be classified under "Location" even though these operate at very different scales. "Phone Number" and "Email" could also be classified as "Locations". Abstracting away from the specifics of the business use case is needed to create an ontology that can apply across disparate business lines. "Payer ID", "SKU", and "Customer ID" collapse into a single class of "ID". Applications must be refactored to take advantage of the new ontology.
- Incompatible with Popular BI Tools: Common BI tools like Tableau, Power BI, and Spotfire cannot connect directly to a Graph DB. Customers handle this by using the graph to create and curate relationships and then creating virtualized tables for common workloads. However, creating these tables imposes a schema, which contravenes one of the benefits of using Graph DB.

**Background: Knowledge Graph and Property Graph**

- Knowledge graph is governed by the Relational Data Framework standard (RDF) and uses a triple as the atomic data unit. This leads to a more verbose structure than a columnar or key value store but adds directional relationships into the atomic unit, making it easier to create meaningful connections between data points. Data stored in triples can be converted to RDBMS, columnar, or key value stores. In converting a spreadsheet to a triple, each cell becomes a unique triple.
- Property graph build upon edge-lists of nodes (nouns) and edges (verbs). Both can have additional properties storied as key value pairs.

**Reference**

Graph Databases (O'Reilly) available for [free from Neo4J](https://neo4j.com/graph-databases-book/)

### Related Stories
- [[Data Science is still relevant and can unlock value in many ways](https://medium.com/@kylejones_47003/data-science-is-still-relevant-and-can-unlock-value-in-many-ways-dc8235e31acf)]
- [[3 ways Generative AI can help assess trends in Environmental Change](https://medium.com/@kylejones_47003/3-ways-generative-ai-can-help-assess-trends-in-environmental-change-e230f82aaaf9)]
- [[Generative Artificial intelligence And the Climate: Can technology help save the Planet?](https://medium.com/@kylejones_47003/generative-artificial-intelligence-and-the-climate-can-technology-help-save-the-planet-a3357df11a34)]
