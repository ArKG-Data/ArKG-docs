# ArKG data documentation

On this site, you can download the latest version of the ArKG dataset and find some preliminary documentation (under development). At the bottom, you can find and download the different versions of the dataset. Next, we briefly present some technical details of the graph representation. 

The ArKG knowledge graph is modeled as an RDF graph, a format for describing graph data. Data is stored as triples:

> (subject, predicate, object)

where *subject* and *object* are nodes in the graph data, and *predicate* is a label that gives a meaning to the connection between both. In ArKG, each date data item is a node, connected to other data items (such as locations, dates, materials, etc.) through triples. Therefore, the predicates state the *type* of the connection between different data items. 

The following table describes each predicate currently supported/used in ArKG: 

| Predicate | Description |
| :------- | :------- |
  **`rdf:type`** | Class or category to which the resource belongs. |
| **`rdfs:label`** | Readable label associated with the resource's URI. |
| **`wdt:P186`** *(made from material)* | The type of sample analyzed (e.g, bone, wood, shell,etc.)|
| **`wdt:P9047`** *(archaeological site of)* | Name of the archaeological site where the archaeological date was discovered. |
| **`wdt:P1343`** *(described by source)* | Bibliographic source or publication where the archaeological date is reported.|
| **`wdt:P276`** *(location)* | More specific place regarding the archaeological date's location, of which there is a record in Wikidata.  |
| **`wdt:P585`** *(point in time)* | Date when the analysis of the archaeological date was performed.|
| **`:14C_age`** | Radiocarbon age of the archaeological date.|
| **`:14C_age_einfo`** | Additional information about the radiocarbon age.|
| **`:14C_type`** | Type of radiocarbon measurement, can be "Conventional" or "AMS".|
| **`:TL_Age_AC_DC`** | Age obtained through **Thermoluminescence** (**TL**), expressed in BC/AD years.|
| **`:dating_method`** | Dating method used, can be **wd:Q173412** (radiocarbon dating), **wd:Q2727388** (thermoluminescence dating), or unknown.|
| **`:location`** | Text description of the location of the archaeological date.|
| **`:x`** , **`:y`** | Geographic coordinates of the site in decimal degrees (longitude and latitude, respectively).|
| **`:sd`** | Standard deviation associated with the radiocarbon measurement.|
| **`:delta13C`** | Measure of the proportion of stable carbon isotopes.|
| **`:material_einfo`** | Additional information about the type of sample analyzed.|


