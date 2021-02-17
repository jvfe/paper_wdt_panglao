---
title: 'Wikidata to build 5-star Linked Open biological databases: A case study of PanglaoDB'
keywords:
- markdown
- publishing
- manubot
lang: en-US
date-meta: '2021-02-17'
author-meta:
- João Vitor Ferreira Cavalcante
- Tiago Lubiana
header-includes: |-
  <!--
  Manubot generated metadata rendered from header-includes-template.html.
  Suggest improvements at https://github.com/manubot/manubot/blob/main/manubot/process/header-includes-template.html
  -->
  <meta name="dc.format" content="text/html" />
  <meta name="dc.title" content="Wikidata to build 5-star Linked Open biological databases: A case study of PanglaoDB" />
  <meta name="citation_title" content="Wikidata to build 5-star Linked Open biological databases: A case study of PanglaoDB" />
  <meta property="og:title" content="Wikidata to build 5-star Linked Open biological databases: A case study of PanglaoDB" />
  <meta property="twitter:title" content="Wikidata to build 5-star Linked Open biological databases: A case study of PanglaoDB" />
  <meta name="dc.date" content="2021-02-17" />
  <meta name="citation_publication_date" content="2021-02-17" />
  <meta name="dc.language" content="en-US" />
  <meta name="citation_language" content="en-US" />
  <meta name="dc.relation.ispartof" content="Manubot" />
  <meta name="dc.publisher" content="Manubot" />
  <meta name="citation_journal_title" content="Manubot" />
  <meta name="citation_technical_report_institution" content="Manubot" />
  <meta name="citation_author" content="João Vitor Ferreira Cavalcante" />
  <meta name="citation_author_institution" content="Bioinformatics Multidisciplinary Environment, Federal University of Rio Grande do Norte" />
  <meta name="citation_author_orcid" content="0000-0001-7513-7376" />
  <meta name="citation_author" content="Tiago Lubiana" />
  <meta name="citation_author_institution" content="Computational Systems Biology Laboratory, University of São Paulo" />
  <meta name="citation_author_orcid" content="0000-0003-2473-2313" />
  <link rel="canonical" href="https://jvfe.github.io/paper_wdt_panglao/" />
  <meta property="og:url" content="https://jvfe.github.io/paper_wdt_panglao/" />
  <meta property="twitter:url" content="https://jvfe.github.io/paper_wdt_panglao/" />
  <meta name="citation_fulltext_html_url" content="https://jvfe.github.io/paper_wdt_panglao/" />
  <meta name="citation_pdf_url" content="https://jvfe.github.io/paper_wdt_panglao/manuscript.pdf" />
  <link rel="alternate" type="application/pdf" href="https://jvfe.github.io/paper_wdt_panglao/manuscript.pdf" />
  <link rel="alternate" type="text/html" href="https://jvfe.github.io/paper_wdt_panglao/v/9735f017bbd54b8e7ccd94158f2f9f8e9cb9b1e4/" />
  <meta name="manubot_html_url_versioned" content="https://jvfe.github.io/paper_wdt_panglao/v/9735f017bbd54b8e7ccd94158f2f9f8e9cb9b1e4/" />
  <meta name="manubot_pdf_url_versioned" content="https://jvfe.github.io/paper_wdt_panglao/v/9735f017bbd54b8e7ccd94158f2f9f8e9cb9b1e4/manuscript.pdf" />
  <meta property="og:type" content="article" />
  <meta property="twitter:card" content="summary_large_image" />
  <link rel="icon" type="image/png" sizes="192x192" href="https://manubot.org/favicon-192x192.png" />
  <link rel="mask-icon" href="https://manubot.org/safari-pinned-tab.svg" color="#ad1457" />
  <meta name="theme-color" content="#ad1457" />
  <!-- end Manubot generated metadata -->
bibliography:
- content/manual-references.json
manubot-output-bibliography: output/references.json
manubot-output-citekeys: output/citations.tsv
manubot-requests-cache-path: ci/cache/requests-cache
manubot-clear-requests-cache: false
...






<small><em>
This manuscript
([permalink](https://jvfe.github.io/paper_wdt_panglao/v/9735f017bbd54b8e7ccd94158f2f9f8e9cb9b1e4/))
was automatically generated
from [jvfe/paper_wdt_panglao@9735f01](https://github.com/jvfe/paper_wdt_panglao/tree/9735f017bbd54b8e7ccd94158f2f9f8e9cb9b1e4)
on February 17, 2021.
</em></small>

## Authors



+ **João Vitor Ferreira Cavalcante**<br>
    ![ORCID icon](images/orcid.svg){.inline_icon}
    [0000-0001-7513-7376](https://orcid.org/0000-0001-7513-7376)
    · ![GitHub icon](images/github.svg){.inline_icon}
    [jvfe](https://github.com/jvfe)<br>
  <small>
     Bioinformatics Multidisciplinary Environment, Federal University of Rio Grande do Norte
  </small>

+ **Tiago Lubiana**<br>
    ![ORCID icon](images/orcid.svg){.inline_icon}
    [0000-0003-2473-2313](https://orcid.org/0000-0003-2473-2313)
    · ![GitHub icon](images/github.svg){.inline_icon}
    [lubianat](https://github.com/lubianat)<br>
  <small>
     Computational Systems Biology Laboratory, University of São Paulo
  </small>



## Abstract {.page_break_before}

[PanglaoDB](https://panglaodb.se/index.html) is a database of cell type markers widely used for single-cell RNA sequencing data analysis. 
However, genes, tissues, organs, and cell types in the database are encoded by free text and lack identifiers. 
[Wikidata](https://www.wikidata.org/wiki/Wikidata:Main_Page), is a freely editable knowledge graph database useful for integrating biomedical knowledge. 
Its linked data model can massively improve the handling and distribution of scientific information. 

In this study, we explore the feasibility of enriching PanglaoDB with Wikidata identifiers. 
We accessed the state of reconciliation at the beginning of the project, comparing the modeling of genes, tissues, organs, and cell types on Wikidata. 
Taking advantage of the openness of Wikidata, we leveraged our initial analysis to contribute towards Wikidata completeness and enable full reconciliation. 
As a final product, we released the first SPARQL endpoint for cell marker information directly in Wikidata, in a 5-star open-linked data format. 
We hope that this study encourages further reconciliations of databases to Wikidata. 


**Keywords**: wikidata, knowledge graph, cell type, ontology.


## Introduction

### PanglaoDB

PanglaoDB [@https://panglaodb.se/index.html] [@doi:10.1093/database/baz046] is a publically-available database that contains data and metadata on hundreds of single-cell RNA sequencing experiments. 
It provides extensive information on cell types, genes, and tissues and manually and community curated cell type markers (Tables @tbl:panglao and @tbl:panglao2).
It also displays a rich web user interface for easy data acquisition, including database dumps for bulk downloads.

|	|Mus musculus 	| Homo sapiens|
|:--:|:-------------:|:---------------:|
|Samples |	1063 | 305 |
|Tissues |	184  |74 |
|Cells 	| 4,459,768 | 1,126,580 |
|Cell Clusters| 8,651 | 1,748 |
Table: Database statistics for each species in PanglaoDB, as of 31st of August, 2020.
{#tbl:panglao}

|        |  Number |
|:----------:|:-------:|
| Cell types |	215 (uniquely named)   | 
|  Tissues   |	 240 (+6 germ layers)   |
|  Organs    | 29  | 
|  Species   | 2 (Homo sapiens and Mus musculus)  |
|  Genes     | 110292 |
Table: Metadata statistics for PanglaoDB, gathered from their [last update on August, 2019](https://github.com/oscar-franzen/PanglaoDB/tree/master/data).
{#tbl:panglao2}

As of 30 December 2020, the article describing PanglaoDB has been cited 88 times. 
Despite its use by the community, the database is on a 3-star category for Linked Open Data [@url:https://www.w3.org/DesignIssues/LinkedData.html] as it does not use the open semantic standards from W3C (RDF and SPARQL) needed for a 4-star rank, neither the links to external data via standard identifiers that make datasets 5-star. 
Improving the data format toward W3C's gold standards is a valuable step in making biological knowledge FAIR (Findable, Accessible, Interoperable, and Reusable).


The OBO Foundry provides a rich collection of linked biological identifiers [@url:http://www.obofoundry.org/]. 
However, reconciliation to OBO is challenging, as there are many ontologies, each with slightly different contribution guidelines. 
For that reason, we decided to reconcile PanglaoDB to Wikidata, which allows the simple creation of new terms, provided they follow Wikidata's notability criteria [@url:https://www.wikidata.org/wiki/Wikidata:Notability]. 

### Wikidata

Wikidata [@https://www.wikidata.org/wiki/Wikidata:Main_Page] is an open, freely editable, knowledge graph database within the semantic web [@https://www.w3.org/standards/semanticweb/] that stores knowledge across a multitude of domains, such as arts, history, chemistry, and biology, using an item-property-value linked data model (Figure @fig:wdt-hep). 
It is easy to use and edit, by both humans and machines, with a rich web user interface and wrapper packages available in common programming languages such as R and Python. 
All the data within Wikidata is linked and inherently public domain. 

![
Wikidata item example, showing item hepatocyte (Q827450), the labels change according to the user's language, but each item has a universal identifier, called QID.
](images/wdt_hepatocyte.png){#fig:wdt-hep}


Several advances towards biological data integration and biological data analysis in Wikidata have been made before, yielding positive results [@doi:10.1101/031971] [@wikidata:Q87830400] and showcasing its potential for bioinformatics-related analyses, such as drug repurposing and ID conversion [@doi:10.7554/eLife.52614]. 
Wikidata has been proposed as a unified base to gather and distribute biomedical knowledge, with more than 50 000 human gene items indexed and hundreds of biomedical-related properties [@doi:10.1016/j.jbi.2019.103292].


 Wikidata is  a collaborative database, and content is available on different levels of quality. 
 For example, as of August 2020, cell type information was still deficient, with only 264 items being categorized as "instances of cell types (Q189118)" (for current status, see <https://w.wiki/b2w>), while similar projects describe over two thousand cell types [@wikidata:Q28660708; @wikidata:Q36067763].
Of those 264 items on Wikidata, only 9 had a "Cell Ontology ID"[@pmid:27377652] (P7963) associated, and most have a varying amount of statements (Table @tbl:cell-counts). 
As an additional problem, there were also 23 items categorized as "instances of cell (Q7868)" (for current status, see <https://w.wiki/b2x>). This classification is imprecise, as an instance of cell would be an individual named cell from a single named individual.

| Cell type Item | Number of statements |
|:-------------:|:---------------:|
| red blood cell (Q37187) | 48 |
| myocyte (Q428914) | 18 |
| mesenchymal cell (Q66568500) | 2 |
Table: As of August 2020, Wikidata items regarding cell types have a varying amount of information, with most having very few statements.
{#tbl:cell-counts}


This study was motivated by the increasing importance of cell-type concepts in light of the Human Cell Atlas [@wikidata:Q46368626], and the utter need for improved interoperability of biological data. 
Thus, we aimed to provide a case study of making the core information of PandlaoDB available in a 5-star Linked Open Data Format while improving the modeling of the necessary concepts on Wikidata.


## Methodology

### Data acquisition

Gene data from Wikidata was acquired using the Wikidata Query Service for *Homo sapiens* genes and *Mus musculus* genes, as well as their HGNC names.  

The markers dataset was downloaded manually from PanglaoDB's website (<https://panglaodb.se/markers/PanglaoDB_markers_27_Mar_2020.tsv.gz>). It contains 15 columns and 8256 rows. Only the columns `species`, `official gene symbol`, and  `cell type` were used for the reconciliation. 

All data used was handled using the Pandas [@doi:10.5281/zenodo.3630805] library.

### Class creation on Wikidata

Classes corresponding to species-neutral classes were retrieved from Wikidata manually using Wikidata's Graphic User Interface. 
The dictionary matching terms in PanglaoDB to Wikidata identifiers were stored in a [reference CSV table](https://github.com/jvfe/wikidata_panglaodb/blob/master/improvements/results/cell_type_reference_from_panglao_to_wikidata_31_10_2020.csv). 


Cell types that were not represented on Wikidata were added to the database via the graphical user interface (<https://www.wikidata.org/wiki/Special:NewItem>) and logged in the reference table.


Species-specific cell types for human and mouse cell types were created for every entry in the reference table and connected to the species-neutral concept via a "[subclass of](http://www.wikidata.org/entity/P279)" property (e.g. every single "[human neutrophil](http://www.wikidata.org/entity/Q101405102)" is a also "[neutrophil](http://www.wikidata.org/entity/Q188417)"). 
Our approach was analogous to the one taken by the CELDA ontology to create species-specific cell-types, with the difference that they used `rdfs:subClassOf` to denote the subclass relationship [@wikidata:Q21284308].


Each item was labeled "human" + the label for the neutral cell type, described as "cell type found in Homo sapiens" and tagged with the statement "[found in taxon](http://www.wikidata.org/entity/P703)" [_Homo sapiens_](https://www.wikidata.org/wiki/Q15978631). 
An analogous framework was used for mouse cell types, assuming that "mouse" in PanglaoDB meant [_Mus musculus_](http://www.wikidata.org/entity/Q83310). 
Batch creations were added to Wikidata via the tool Quickstatements (<https://quickstatements.toolforge.org/#/>).

All genes in PanglaoDB either were already present on Wikidata or resolved to multiple entities and thus were excluded. 

### Property creation on Wikidata

Properties on Wikidata need to be supported by the users in a public forum before creation. 
We proposed a property called `has marker` to the Wikidata community to represent the cell-type marker relation.  
We posted a message in the 17th of November presenting the property, domain, range constraints, and additional comments.

The following motivation statement accompanied the proposal: 

    "Even though the concept of a marker gene/protein is not clear cut, it is very important, and widely used in databases and scientific articles.

    This property will help us to represent that a gene/protein has been reported as a marker by a credible source, and should always contain a reference.

    Some markers are reported as proteins and some as genes. Some genes don't encode proteins, and some protein markers are actually protein complexes.

    The property would be inclusive to these slightly different markers.
    Some cell types are marked by absence of expression of genes/proteins/protein expression. As these seem to be less common than positive markers (no organized databases, for example) they are left outside the value range for this property"


The proposal contained specifications of the property such as:

- Description:
  - "a gene or a protein published as a marker of a species-specific cell type"
- Data type:
  - [Item](https://www.wikidata.org/wiki/Help:Data_type#wikibase-item) (internal entities in Wikidata)
- Domain:
  - ?subject [instance of (P31)](http://www.wikidata.org/entity/P31) [cell type (Q189118)](http://www.wikidata.org/entity/Q189118)
- Allowed values:
  - {?object [instance of (P31)](http://www.wikidata.org/entity/P31)  [protein (Q8054)](http://www.wikidata.org/entity/Q8054) .}
  - UNION {?object [instance of (P31)](http://www.wikidata.org/entity/P31)  [gene (Q7187)](http://www.wikidata.org/entity/Q7187) .}
  - UNION {?object [instance of (P31)](http://www.wikidata.org/entity/P31)  [macromolecular complex (Q22325163)](http://www.wikidata.org/entity/Q22325163) .}
- Planned use:
  - Reconcile knowledge from the PanglaoDB marker database to Wikidata. In the future, expand to other trusted sources of cell type marker information.

More details can be found in the archived Wikidata:Property proposal page (<https://www.wikidata.org/wiki/Wikidata:Property_proposal/has_positive_marker>).

### Integration to Wikidata 

The reconciled dataset was uploaded to Wikidata via the WikidataIntegrator python package [@https://github.com/SuLab/WikidataIntegrator], a wrapper for the Wikidata Application Programming Interface. 
The integration details can be seen in the Jupyter notebooks at the GitHub repository (https://github.com/jvfe/wikidata_panglaodb).

## Access to reconciled data
### Wikidata dumps

Wikidata provides regular dumps in a variety of formats, including RDF dumps: <https://www.wikidata.org/wiki/Wikidata:Database_download>. 
It is possible to also download partial dumps of the database with reduced size (ex: <https://wdumps.toolforge.org/dump/987> for all cell types with the `has_marker` property).   

### SPARQL queries

Besides the Wikidata Dumps, Wikidata provides an SPARQL endpoint with a Graphical User Interface (<https://query.wikidata.org/>). 
Updated data was immediately accessible via this endpoint, enabling integrative queries integrated with other database statements.

## Source code and data availability

<!-- this can be improved -->
All source code used for the study and data created during the study are available in a GitHub repository, 
<https://github.com/jvfe/wikidata_panglaodb>,
as well as archived in a zenodo repository, <https://doi.org/10.5281/zenodo.4438614>.


 # Cell types on Wikidata

As of August 2020, Wikidata had 264 items being categorized as a "cell type" (Wikidata ID Q189118), considerably less than in specialized cell catalogs, which count over two thousand cell types [@wikidata:Q28660708; @wikidata:Q36067763].
Strikingly, there were also 23 items categorized as "instances of cell (Q7868)" . This classification is imprecise, as an instance of cell would be an individual named cell from a single named individual.

Wikidata editors often mix first-order classes such as "cells" and "organs" with second-order classes like "cell types" and "organ types" (Supplementary Information). First-order classes point to real-world individuals, like the "Dolly sheep zygote" (a real-world "cell") and the "brain of Albert Einstein" (a real-world "organ"). Second-order classes point to classes, like "zygote" (a conceptual "cell type") and "brain" (a conceptual "organ type").

We diligently fixed and improved information on cell types on Wikidata. As of February 2021, the Wikidata database contained 1828 instances of "cell type" (see current status at <https://w.wiki/b2t>) and 0 instances of "cell" (<https://w.wiki/b2q>) highlighting the improvements in both quantity and quality. 



# Results

## Cell Marker information on Wikidata

Adding marker information on Wikidata was not possible before this study and became possible after community approval of the property "has marker" (P8872) (see Methods).
Figure @fig:chat_marker shows 2 of the current markers of "human colinergic neuron"([Q101405051](http://www.wikidata.org/entity/Q101405051)), [CHAT](http://www.wikidata.org/entity/Q14863671) and [ACHE](http://www.wikidata.org/entity/Q407983), as they seen on Wikidata.
The PanglaoDB is referenced both via URL to the website (<https://panglaodb.se/markers.html>) and a pointer to the PanglaoDB item on Wikidata, [Q99936939](http://www.wikidata.org/entity/Q99936939).

![
Subset of the marker genes for item Q101405051 (human cholinergic neuron )
](images/chat_marker.png){#fig:chat_marker}


Since Wikidata is an open system, information about markers will be complemented by user contributions.
To date, no other project has systematically integrated cell type markers to Wikidata, and, thus, most information shown here comes from PanglaoDB. The tables show the marker count for the five cell types of humans and mice with most markers on Wikidata, for both species around two hundred marker genes.

| celltypeLabel                                                       |   marker_count |
|:--------------------------------------------------------------------|---------------:|
| [human interneuron ](http://www.wikidata.org/entity/Q101405035)     |            216 |
| [human neuron](http://www.wikidata.org/entity/Q101405104)           |            203 |
| [human endothelial cell](http://www.wikidata.org/entity/Q68621315)  |            187 |
| [human fibroblast](http://www.wikidata.org/entity/Q101404861)       |            170 |
| [human hepatocyte](http://www.wikidata.org/entity/Q101405101)       |            149 |

Table: Top 5 _Homo sapiens_ cell types with most markers on Wikidata (15/02/2020, full query on <https://w.wiki/zoQ>).
{#tbl:hs_markers}

| celltypeLabel                                                              |   marker_count |
|:---------------------------------------------------------------------------|---------------:|
| [mouse neocortical interneuron](http://www.wikidata.org/entity/Q102426621) |            219 |
| [mouse interneuron](http://www.wikidata.org/entity/Q104416243)             |            219 |
| [mouse neuron](http://www.wikidata.org/entity/Q104416303)                  |            210 |
| [mouse endothelial cell](http://www.wikidata.org/entity/Q104416178)        |            188 |
| [mouse fibroblast](http://www.wikidata.org/entity/Q104416140)              |            176 |

Table:  Top 5 _Mus musculus_ cell types with most markers on Wikidata (15/02/2020, full query on <https://w.wiki/zoN>).
{#tbl:mm_markers}

# Wikidata SPARQL queries enabled by the integration

Now that we re-formatted the markers on PanglaoDB as Linked Open Data, we can make queries that were not possible before, including
federated queries with other biological databases, such as Uniprot [@https://sparql.uniprot.org/sparql]
and Wikipathways [@https://www.wikipathways.org/index.php/Portal:Semantic_Web].
Due to previous similar reconciliation projects, Wikidata already contains information about genes, including their relations to Gene Ontology (GO) terms.

PanglaoDB's integration to the Wikidata ecosystem allows us to ask a variety of questions (figure @fig:chat_marker). The next section headers exemplify such questions.

![
Wikidata SPARQL queries bring to light hidden biomedical knowledge
](images/query_figures.png){#fig:queries}

### "Which human cell types are related to neurogenesis via their markers?"

As expected, the query below retrieved a series of neuron types, such as "[human purkinje neuron](https://www.wikidata.org/wiki/Q101404913)" and "[human cajal-retzius cell](https://www.wikidata.org/wiki/Q101405091)." It also retrieved non-neural cell types such as the "[human loop of henle cell](https://www.wikidata.org/wiki/Q101405109), a kidney cell type, and "[human osteoclast](https://www.wikidata.org/wiki/Q101404928). These seemingly unrelated cell types markedly express genes involved in neurogenesis, but that does not mean that they are involved with this process. The seemingly confusing results reinforce the idea that one needs to be careful when using curated pathways to enrich one's analysis, as false positives abound.

The molecular process that gene products take part depends on the cell type. SPARQL allows us to seamlessly compare Gene Ontology processes with cell marker data, providing a sandbox to generate hypotheses and explore the biomedical knowledge landscape.

| geneLabel   | cellTypeLabel                   |
|:------------|:--------------------------------|
| OMP         | human purkinje neuron           |
| OMP         | human olfactory epithelial cell |
| OMP         | human neuron                    |
| EPHB1       | human oligodendrocyte           |
| EPHB1       | human osteoclast                |
| PCSK9       | human delta cell                |
| PCSK9       | human loop of Henle cell        |
| CXCR4       | human b cell                    |
| CXCR4       | human T cell                    |
| CXCR4       | human nk cell                   |

Table: Top 10 cell types related to neurogenesis via markers (07/02/2020, full query on <https://w.wiki/yQ6>).
{#tbl:neuro}

### "Which cell types express markers associated with Parkinson's disease?"

Besides integration with Gene Ontology, Wikidata reconciliation makes it possible to complement the marker gene info on PanglaoDB with information about diseases. This integration is of biomedical interest, as there is a quest to detail mechanisms that link genetic associations and the diseases themselves.

"Disease genes" are often compiled from Genomic Wide Association Studies, which look for sequence variation in the DNA. These studies are commonly blind to the cell types related to the pathophysiology of the disease. In the query below, we can see cell types marked by genes genetically associated with Parkinson's disease. Even considering the false positives, the overview can aid domain experts in coming up with novel hypotheses.

| geneLabel   | diseaseLabel        | cellTypeLabel    |
|:------------|:--------------------|:-----------------|
| BST1        | Parkinson's disease | human b cell     |
| BST1        | Parkinson's disease | human neutrophil |
| RIT2        | Parkinson's disease | human neuron     |
| SH3GL2      | Parkinson's disease | human alpha cell |
| SH3GL2      | Parkinson's disease | human beta cell  |

Table: Top 5 cell types related to Parkinson's disease via markers (07/02/2020, full query on <https://w.wiki/yQD>).
{#tbl:parkinson}


### Which diseases are associated with the markers of pancreatic beta cells?

We can check the cell-type to disease relation in both ways. Scientists that study specific cell types (and not necessarily specific diseases) might be interested in knowing which diseases are related to their cell type of interest.  We looked for the diseases linked on Wikidata to the [human pancreatic beta cells](https://www.wikidata.org/wiki/Q101405087), which play an important role in controlling blood sugar levels. Reassuringly, top hits associated with markers included
[obesity](https://www.wikidata.org/wiki/Q12174) and [type-2 diabetes](https://www.wikidata.org/wiki/Q3025883). Other diseases retrieved, such as [aniridia](https://www.wikidata.org/wiki/Q548719) - a disturb of the iris of the eye - do not bear a clear link with classic pancreatic functions and might provide novel insights on disease pathophysiology

| diseaseLabel        | genes                   |   count | cellTypeLabel   |
|:--------------------|:------------------------|--------:|:----------------|
| obesity             | PCSK2, ADCYAP1, SLC30A8 |       3 | human beta cell |
| type 2 diabetes     | SLC30A8, TGFBR3         |       2 | human beta cell |
| Parkinson's disease | SH3GL2                  |       1 | human beta cell |
| asthma              | SLC30A8                 |       1 | human beta cell |
| aniridia            | PAX6                    |       1 | human beta cell |
Table: Top 5 cell types related to Parkinson's disease via markers (07/02/2020, full query on <https://w.wiki/yQD>).
{#tbl:beta}

# Discussion

In this work, we re-released the knowledge curated in PanglaoDB on Wikidata, connecting it to the semantic web.
Each cell-type/marker statement was added to Wikidata with a pointer to PanglaoDB and a citation of the article, providing proper provenance.
At the same time, we documented the process of database integration to Wikidata, providing a blueprint for future efforts.

It is important to note that not all data on PanglaoDB was added to Wikidata.
Fine-grained, database-specific details were too granular for a general-purpose database like Wikidata (e.g. the sensitivity and specificity attached to each marker-cell type pair).
As Wikidata license is very permissive (CC0), content in PanglaoDB that could be protected by copyright (for example, narrative descriptions of cell types) is not suitable for integration.
In either case, depending on the goals, these data could be released in RDF format and be connected to independent SPARQL endpoints (as done in the Bio2RDF effort [@wikidata:Q56989268]).
In this work, we focused on integration to Wikidata to take advantage of the built-in integration with various types of knowledge, as well as the tooling developed by the Wikidata community.

As described in the methods session, we added species-specific terms to Wikidata for cell types of _Homo sapiens_ and _Mus musculus_ described in the PanglaoDB database.
The use of species-specific cell-types is necessary because genes in Wikidata are also species-specific, connected to their taxon by the "[found in taxon](http://www.wikidata.org/entity/P703)" properties.
In the biomedical literature, however, genes and cell types are sometimes referred to broadly, in a multi-species or species-neutral way.
The fuzzy, humane meanings are not always compatible with formalized data models.
Thus, the reconciliation endeavor is not merely finding the right match on Wikidata, but largely of crafting coherent interpretations of data.

The complexity of biomedical communication adds to the argument pro-Wikidata.
Sometimes, as happened for us, it is just impossible to find a suitable term in an existing ontology.
OBO Foundry ontologies are open to contribution, but require a large investment.
For starters, one must learn a lot about description logic, a field that is often exotic for biologists and software developers alike.
Moreover, to contribute, one needs to acquire the tooling.
That includes learning to use GitHub (<https://github.com/>) and Protegé (<https://protege.stanford.edu/>), but also learning community conventions and social norms that are slightly different for every single ontology.
Wikidata bypasses this steep learning curve by providing a web interface which requires little to no previous experience with ontologies and programming.
The reconciliation process becomes smoother, as if a concept is not previously catalogued, we can add a new one on the fly.

Additionally, knowledge added to Wikidata is not locked in the ivory tower of academia.
Data on Wikidata can be easily reused on Wikipedia, a major source of information for scientists and lay people alike.
Wikipedia's thriving mutualism with academia is well documented. [@wikidata:Q42013239; @wikidata:Q21629969; @wikidata:Q21145331]
Wikidata information can enhance the quality of articles about life-science subjects in semi-automated ways (as has been done before [@wikidata:Q21503276]).
Thus, Wikidata is  directly connected to the well-established science education platform of Wikipedia, a feature unrivaled by any other structured knowledge system.

Of course, Wikidata has its limitations.
Concerns with the reliability of Wikipedia are as old as the encyclopedia itself (for a discussion, see <https://en.wikipedia.org/wiki/Reliability_of_Wikipedia>) and Wikidata likely shares many of such concerns.
The ontological modelling on Wikidata is often far from perfect, and inconsistencies and logical mistakes abound. [@wikidata:Q27037396].
It has been argued, though, that bio-ontologies generally lack "strict, explicit and well defined semantics" (at least in 2008 [@wikidata:Q21093639]).
While a comprehensive analysis of pros and cons of scientific Wikidata is not available, we extend Don Fallis' view on Wikipedia and argue that Wikidata  has a number of "epistemic virtues (e.g., power, speed, and fecundity) that arguably outweigh any deficiency in terms of reliability." [@wikidata:Q101955295]

This work exemplifies the power of releasing Linked Open Data via Wikidata, and provides the biomedical community with the first semantically accessible, 5-star LOD dataset of cell markers, easily reachable from Wikidata's SPARQL Query Service (<https://query.wikidata.org/>).
It is not first case study of biomedical data integration to Wikidata (see [@wikidata:Q105037759] for example.
Nevertheless, the differences among the articles in style and scope contribute to a richer ecosystem for possible contributor.
])
The work also paves the way for Wikidata reconciling of other databases for cell-type markers, such as CellMarker [@wikidata:Q56984510], labome [@doi:10.13070/mm.en.3.183], CellFinder [@wikidata:Q28660708] and SHOGoiN/CELLPEDIA [@https://stemcellinformatics.org/]).
The approach we took here can in essence be applied to any knowledge set of public interest, providing a low-cost and low-barrier platform for sharing biocurated knowledge in gold standard format.

We hope that the community will keep improving marker and overall biological content on Wikidata, and that the interlinked marker information will be helpful. We invite the reader to improve information on Wikidata for their favorite cell types, adding markers and a link to the reference works, and make ourselves available for aiding anyone interested in using or editing marker information on Wikidata.


## References {.page_break_before}

<!-- Explicitly insert bibliography here -->
<div id="refs"></div>


# Supplementary text and figures


Only *Homo sapiens* genes and Organs reconciled more than 50%.
In the case of genes, this is probably due to the Gene Wiki initiative [@doi:10.1093/database/baw015], a long-running project to improve biological information in Wikipedia and its sister-projects, including Wikidata. 

This is further illustrated by Figure @fig:gene_alt_ids, in which we can see that all *Mus musculus* gene items - and nearly all *Homo sapiens* items - analysed had the Entrez ID alternative identifier present.
Most of the data from the Gene Wiki project came from NCBI, creator and maintainer of Entrez. 
Nevertheless, there are still many gene items without an "Ensembl Gene ID" property, 
showcasing the need for further work in migrating this important source of information.   
In the case of Organ data, there was a high number of matches both due to the fact that there were only a few number of items, but also since most Organ entities have Wikipedia pages, that are, therefore, cross-linked using Wikidata, requiring the creation of these items. 

Regarding alternative identifiers, what was observed for genes cannot be said for histological entities. While there is significant progress in integrating UBERON IDs, there is near to no items with a Cell Ontology ID property (Figure @fig:histo_alt_ids).


![
Percentage of matched histological items that had alternative identifiers,
UBERON IDs for Tissues and Organs, Cell Ontology IDs for Cell types. 
](images/histo_alt_ids.png){#fig:histo_alt_ids}


![
Percentage of matched gene items that had alternative identifiers, Entrez ID and Ensembl Gene ID, divided by species. 
](images/gene_alt_ids.png){#fig:gene_alt_ids}


![
Percentage of reconciled entities, divided by which item type they belong to. Most reconciled items don‘t count with the P31 property.
](images/reconciled_item_types.png){#fig:reconciledbar}


A significant proportion of the matches we could acquire for histological data didn't contain in their data model an "instance of" (P31) property, 
this illustrates an extremely concerning fact: Although we could still match around 30 percent of the data - 
in the case of Cell types and Tissues - 
this data was probably "low-quality", that is, hard to find and even harder to obtain insights from, 
we can affirm this since the P31 property is the basis for most items in Wikidata, 
it's the most intuitive way to perform queries against their database and to annotate their items. 


Furthermore, there is a significant disparity between histological data and gene data: 
while we could only match around 37% of Cell types from PanglaoDB, and of those 55% didn't have P31, 
we matched 60% of *Homo sapiens* genes, and all of them had P31. 
This disparity is not clearly shown when looking exclusively at the number of statements for these items 
(Figures @fig:histo_boxplot and @fig:gene_violin), but it shows there is still a great amount of missing information
for biological data, in particular in regards to cell types.


| Cell type Item | Number of statements |
|:-------------:|:---------------:|
| red blood cell (Q37187) | 48 |
| myocyte (Q428914) | 18 |
| mesenchymal cell (Q66568500) | 2 |
Table: As of August 2020, Wikidata items regarding cell types have a varying amount of information, with most having very few statements.
{#tbl:cell-counts}

![
The distribution of the number of statements of the matched histological entities. 
Cell types performed the lowest.
](images/histo_boxplots.png){#fig:histo_boxplot}

![
The distribution of the number of statements for matched gene items, divided by species.
](images/gene_violin.png){#fig:gene_violin}



## Analysis of item quality - final look

As can be gathered from Figure @fig:finallook_reconciledbar, nearly all cell type items have the appropriate "instance of cell type" statement, with only 4 items still missing said statement and one item being classified as an "instance of gland".

This is a considerable advance in improving the quality of cell type data in Wikidata, as having this simple statement will make these items easier to find and be expanded upon.

![
Percentage of reconciled entities gathered during the second and final reconciliation, divided by which item type they belong to.
](images/final_look_reconciled_types.png){#fig:finallook_reconciledbar}

## Improvement of Wikidata data on cell types

To reconcile a database to Wikidata, we need to match names on the databases, often in natural language, to the unique identifiers on Wikidata. We first employed an automatic approach based on Entities from PanglaoDB, that is, cell types, tissue types and organ types, were matched with Wikidata items, matching summary can be seen on Table @tbl:reconcilesummary.

|         | PanglaoDB (count) |   Automatic matches (count)   |
|:--------|---------:|-------------------:|
| Cell types   |      215 |                 81 (37.67 %) |
| Tissue types |      246 |                 85 (34.55 %) |
| Organ types  |       29 |                 22 (75.86%) |
Table: Summary of the matched entities from PanglaoDB (August 2020).
{#tbl:reconcilesummary}


After marker data from PanglaoDB was added to Wikidata, we tested the automatic classification method was able to detect most cell types matches for most cell types on PanglaoDB matches (Table
@tbl:finallook_summary). The improvement of 38% to 80% of automatically matched types is evidence that our work improved cell type content on Wikidata, and will arguably facilitate the reconciliation of other cell-type related resources.

||  PanglaoDB (count) | Automatic matches (count)  |
|:-|--------------:|-------------------:|
| Cell types  |  215 | 173 (80.46 %) |
| Tissue types   |  246 |  63  (25.60 %) |
| Organ types    |   29 |  18 (62.06 %) |
Table: Summary of matched PanglaoDB entities after improvements were made (December 2020).
{#tbl:finallook_summary}

Noticeably, the proportion of automatic matches for other entity types (tissues and organs) seems reduced in relation to the first assessment (35% to 25% and 76 to 62%). These entities were not targeted by our work, but as Wikidata is a living resource, modifications in the database, such as reclassification of entities or adding of other similar concepts, may have reduced the performance of our simple reconciler.
