# ArKG data documentation

On this site, you can download the latest version of the ArKG dataset and find some preliminary documentation (under development). At the bottom, you can find and download the different versions of the dataset. Next, we briefly present some technical details of the graph representation. 

The ArKG knowledge graph is modeled as an RDF graph, a format for describing graph data. Data is stored as triples:

> (subject, predicate, object)

where *subject* and *object* are nodes in the graph data, and *predicate* is a label that gives a meaning to the connection between both. In ArKG, each date data item is a node, connected to other data items (such as locations, dates, materials, etc.) through triples. Therefore, the predicates state the *type* of the connection between different data items. 

The following namespaces and prefixes are used in ArKG:
| Prefix | Namespace URI | Description |
| :------- | :------- | :------- |
| **`rdf:`** | <http://www.w3.org/1999/02/22-rdf-syntax-ns#> | RDF syntax vocabulary. |
| **`rdfs:`** | <http://www.w3.org/2000/01/rdf-schema#> | RDF Schema vocabulary. |
| **`wd:`** | <http://www.wikidata.org/entity/> | Wikidata entities. |
| **`wdt:`** | <http://www.wikidata.org/prop/direct/> | Wikidata direct properties. |
| **`:`** | <https://arkg.cl/> | ArKG custom vocabulary. |

The following table describes each predicate currently supported/used in ArKG: 

| Predicate | Description |
| :------- | :------- |
| **`rdf:type`** | Class or category to which the resource belongs. |
| **`rdfs:label`** | Readable label associated with the resource's URI. |
| **`wdt:P186`** *(made from material)* | The type of sample analyzed (e.g, bone, wood, shell,etc.)|
| **`wdt:P9047`** *(archaeological site of)* | Name of the archaeological site where the archaeological date was discovered. |
| **`wdt:P1343`** *(described by source)* | Bibliographic source or publication where the archaeological date is reported.|
| **`wdt:P585`** *(point in time)* | Date when the analysis of the archaeological date was performed.|
| **`wdt:P131`** *(is located in)* | The item is located on the territory of the following administrative entity.|
| **`wdt:P17`** *(country)* | Sovereign state that this item is in.|
| **`:14C_age`** | Uncalibrated radiocarbon age expressed in years BP.|
| **`:14C_type`** | Type of radiocarbon measurement, can be "Conventional" or "AMS".|
| **`:TL_age`** | Thermoluminescence age expressed in years BP.|
| **`:TL_reference_year`** | Baseline year used for age calculation.|
| **`:TL_Age_AC_DC`** | Age obtained through **Thermoluminescence** (**TL**), expressed in BC/AD years.|
| **`:dating_method`** | Dating method used, can be **wd:Q173412** (radiocarbon dating), **wd:Q2727388** (thermoluminescence dating), or unknown.|
| **`:x`** , **`:y`** | Geographic coordinates of the site in decimal degrees (longitude and latitude, respectively).|
| **`:sd`** | Standard deviation associated with the radiocarbon measurement.|
| **`:delta13C`** | Measure of the proportion of stable carbon isotopes.|
| **`:biomolecule`** | Targeted molecular fraction analyzed.|
| **`:unit`** | Excavation unit.|
| **`:level`** | Stratigraphic or arbitrary excavation level.|
| **`:sample_type_info`** | Information about the type of sample analyzed.|
| **`:age_einfo`** | Additional information about the archaeological age.|
| **`:data_compilation`** | Source or compiler of the dataset.|


