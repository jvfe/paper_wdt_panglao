---
title: 'Wikidata to build 5-star Linked Open biological databases: A case study of PanglaoDB'
keywords:
- markdown
- publishing
- manubot
lang: en-US
date-meta: '2020-12-25'
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
  <meta name="dc.date" content="2020-12-25" />
  <meta name="citation_publication_date" content="2020-12-25" />
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
  <link rel="alternate" type="text/html" href="https://jvfe.github.io/paper_wdt_panglao/v/785bd546f8fd2e2feec198b3fcd065f0404cdf64/" />
  <meta name="manubot_html_url_versioned" content="https://jvfe.github.io/paper_wdt_panglao/v/785bd546f8fd2e2feec198b3fcd065f0404cdf64/" />
  <meta name="manubot_pdf_url_versioned" content="https://jvfe.github.io/paper_wdt_panglao/v/785bd546f8fd2e2feec198b3fcd065f0404cdf64/manuscript.pdf" />
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
([permalink](https://jvfe.github.io/paper_wdt_panglao/v/785bd546f8fd2e2feec198b3fcd065f0404cdf64/))
was automatically generated
from [jvfe/paper_wdt_panglao@785bd54](https://github.com/jvfe/paper_wdt_panglao/tree/785bd546f8fd2e2feec198b3fcd065f0404cdf64)
on December 25, 2020.
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

[PanglaoDB](https://panglaodb.se/index.html) is a database of cell type markers widely used for single cell RNA sequencing data analysis. The genes, tissues, organs and cell types mentioned in the database, however, are described by free text and lack identifiers. [Wikidata](https://www.wikidata.org/wiki/Wikidata:Main_Page), is a freely editable knowledge graph database useful for the integration of biomedical knowledge. Its linked data model can improve significantly the handling and distribution of scientific information. 

In this study we explore the feasibility of enriching PanglaoDB with Wikidata identifiers. We accessed the state of reconciliation at the beginning of the project, comparing the modelling of genes, tissues, organs and cell types on Wikidata. Taking advantage of the openess of Wikidata, we leveraged our initial analysis to contribute towards Wikidata completeness and enable full reconciliation. As a final product, we released the first SPARQL endpoint for cell marker information, in a 5-star open linked data format. We hope that this study encourages further reconciliations of databases to Wikidata. 

**Keywords**: wikidata, knowledge graph, cell type, ontology.


## Introduction

### PanglaoDB

PanglaoDB [@https://panglaodb.se/index.html] [@doi:10.1093/database/baz046] is a public database that contains data and metadata on hundreds of single-cell RNA sequencing experiments, providing extensive information on cell types, genes and tissues, as well as manually and community curated cell type markers (Tables @tbl:panglao and @tbl:panglao2). It also provides a rich web user interface for easy data acquisition, including database dumps for bulk downloads.

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

Despite its usefulness for the community, the database is on a 3-star category for Linked Open Data [@url:https://www.w3.org/DesignIssues/LinkedData.html] as it does not use open standards from W3C (RDF and SPARQL). To make it 5-star, it needs to be also linked to external data via common identifiers. 

The OBO Foundry provides a rich collection of linked biological identifiers [@url:http://www.obofoundry.org/]. However, reconciliation to OBO is challenging, as there are many ontologies, each with slightly different contribution guidelines. For that reason, we decided to reconcile PanglaoDB to Wikidata, which allows simple creation of new terms, provided they follow Wikidata`s notability criteria[@url:https://www.wikidata.org/wiki/Wikidata:Notability]. 

### Wikidata

Wikidata [@https://www.wikidata.org/wiki/Wikidata:Main_Page] is an open, freely editable, knowledge graph database within the semantic web [@https://www.w3.org/standards/semanticweb/] that stores knowledge across a multitude of domains,
such as arts, history, chemistry and biology, using an item-property-value linked data model (Figure @fig:wdt-hep). It is easy to use and edit, by both humans and machines, with a rich web user interface and wrapper packages available
in common programming languages such as R and Python. All the data within Wikidata is linked and inherently public domain, thus, it presents a great opportunity to make scientific data more FAIR (Findable, accessible, interoperable and reusable), as well as provides the necessary tools to curate and develop ontologies. 

![
Wikidata item example, showing item hepatocyte (Q827450), the labels change according to the user's language, but each item has a universal identifier, called QID.
](images/wdt_hepatocyte.png){#fig:wdt-hep}

Several advances towards biological data integration and biological data analysis in Wikidata have been made before, yielding positive
results [@doi:10.1101/031971] [@doi:10.7554/eLife.52614] and showcasing it's potential for bioinformatics-related analyses, such as drug repurposing and ID conversion [@doi:10.7554/eLife.52614]. Wikidata has been proposed as a unified base to gather and distribute biomedical knowledge, with more than 50 000 human gene items indexed and hundreds of biomedical-related properties [@doi:10.1016/j.jbi.2019.103292].


 Wikidata, however, is a work in progress, and might need extensive improvement. For example, as of August 2020, cell type information is still very scarse, with only 264 items being categorized as "instances of cell types (Q189118)" (<https://w.wiki/b2w>). Of those, only nine have a "Cell Ontology ID"[@pmid:27377652] (P7963) associated, and most have a varying amount of statements (Table @tbl:cell-counts). As an additional problem, there are also 23 items being categorized as "instances of cell (Q7868)" (<https://w.wiki/b2x>), illustrating the absence of any formal data model.

| Cell type Item | Number of statements |
|:-------------:|:---------------:|
| red blood cell (Q37187) | 48 |
| myocyte (Q428914) | 18 |
| mesenchymal cell (Q66568500) | 2 |
Table: As of August 2020, Wikidata items regarding cell types have a varying amount of information, with most having very few statements.
{#tbl:cell-counts}


This work has the dual goal of re-releasing PandlaoDB in a 5-star Linked Open Data Format and improving the modelling of the necessary concepts on Wikidata.



## Methodology

### Data acquisition

Gene data from Wikidata was acquired using the Wikidata Query Service [@https://query.wikidata.org/]
    - <https://w.wiki/bWc> for *Homo sapiens* genes and <https://w.wiki/bWe> for *Mus musculus* genes.

Data from PanglaoDB was acquired through their metadata database dump repository[@https://github.com/oscar-franzen/PanglaoDB].

All data used was handled using the Pandas[@doi:10.5281/zenodo.3630805] library, 
with the Seaborn[@doi:10.5281/zenodo.4019146] and Matplotlib[@doi:10.5281/zenodo.4030140] libraries being used for plotting. 

### Reconciliation and matching

The metadata from PanglaoDB on cell types, tissues (including germ layers) and organs was matched to Wikidata items using the reconciler[@https://pypi.org/project/reconciler/] library, 
further matching was done using a custom stemming function on the item labels, via PorterStemmer from the NLTK library [@isbn:9780596516499]. 
Matches were considered perfect if the reconciliation service or the stemming function returned a value of "match" equals to "True". 
Matches were manually analysed for false matches, such as items with same labels but used for different concepts.

Gene data was matched manually using a Pandas [@doi:10.5281/zenodo.3630805] inner merge, since both data sources contained identifiers, which should be the same.

### Item quality assessment

Wikidata items were assessed for their quality by their number of statements, 
which were acquired using a custom wrapper on the MediaWiki API [@https://www.mediawiki.org/wiki/API:REST_API] and, 
in the case of gene data, via Wikidata's own query service, as stated in the Data acquisition section.

Furthermore, items were also assessed by the presence of external identifiers - all of which are Wikidata properties: 
Ensembl Gene[@doi:10.1093/nar/gkz966] ([P594](https://www.wikidata.org/wiki/Property:P594)) 
and Entrez Gene[@doi:10.1093/nar/gks1189] ([P351](https://www.wikidata.org/wiki/Property:P351)) IDs for genes, 
Cell Ontology[@pmid:27377652] ([P7963](https://www.wikidata.org/wiki/Property:P7963)) IDs for cell types 
and Uberon[@pmid:22293552] ([P1554](https://www.wikidata.org/wiki/Property:P1554)) IDs for organs and tissues. 


# Results

## Wikidata reconciliation - initial look

Entities from PanglaoDB, that is, cell types, genes, tissue types and organs, were matched with Wikidata items, 
matching summary can be seen on Table @tbl:reconcilesummary. 



|         | # of total items |   # of unique matches  |  % of total items that were matched |
|:--------|---------:|-------------------:|---------------:|
| Cells   |      215 |                 81 |        37.67% |
| Tissues |      246 |                 85 |        34.55% |
| Organs  |       29 |                 22 |        75.86% |
| Human Genes |    58216 |                 35423 |        60.84% |
| Mouse Genes  |    53793 |                 25124 |        46.70% |
Table: Summary of the matched entities from PanglaoDB.
{#tbl:reconcilesummary}

## Analysis of item quality - initial look

Only *Homo sapiens* genes and Organs reconciled more than 50%.
In the case of genes, this is probably due to the Gene Wiki initiative [@doi:10.1093/database/baw015], 
a long-running project to improve biological information in Wikipedia and its sister-projects, including Wikidata. 

This is further illustrated by Figure @fig:gene_alt_ids, in which we can see that all *Mus musculus* gene items - 
and nearly all *Homo sapiens* items - 
analysed had the Entrez ID alternative identifier present - 
Most of the data from the Gene Wiki project came from NCBI, creator and maintainer of Entrez. 
Nevertheless, there are still many gene items without an "Ensembl Gene ID" property, 
showcasing the need for further work in migrating this important source of information.   
In the case of Organ data, there was a high number of matches both due to the fact that there were only a few number of items, but also
since most Organ entities have Wikipedia pages, that are, therefore, cross-linked using Wikidata, requiring the creation of these items. 

Regarding alternative identifiers, what was observed for genes cannot be said for histological entities, 
while there is significant progress in integrating UBERON IDs, there is near to no items with a Cell Ontology ID property (Figure @fig:histo_alt_ids).

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

![
The distribution of the number of statements of the matched histological entities. 
Cell types performed the lowest.
](images/histo_boxplots.png){#fig:histo_boxplot}

![
The distribution of the number of statements for matched gene items, divided by species.
](images/gene_violin.png){#fig:gene_violin}

## Improving Wikidata
- TBD

### Adding missing items
- TBD

### Improving interoperability
- TBD

## Wikidata reconciliation - final look

After the aforementioned improvements were made, 
data from PanglaoDB was reconciled once again, 
now most cell types had appropriate matches (Table
@tbl:finallook_summary).

||  # of total items |# of unique matches  |   % of total items that were matched |
|:-|--------------:|-------------------:|---------------:|
| Cells     | 215 | 173 |80.4651 |
| Tissues   |  246 |63 | 25.6097 |
| Organs    | 29 |18 | 62.0689 |
| Human Genes | 58216 |35423 | 60.8475 |
| Mouse Genes |  53793 |25124 |  46.705|
Table: Summary of matched PanglaoDB entities after improvements were made.
{#tbl:finallook_summary}

While it may seem that the information for other entity types may have decreased, such as tissues and organs, this is difficult to ascertain, as different items could have been merged for clarity or
were reclassified as belonging to different types not covered by this study. 

## Analysis of item quality - final look

As can be gathered from Figure @fig:finallook_reconciledbar, nearly all cell type items have the appropriate "instance of cell type" statement, with only 4 items still missing said statement and one item being classified as an "instance of gland". 

This is a considerable advance in improving the quality of cell type data in Wikidata, as having this simple statement will make these items easier to find and be expanded upon.

![
Percentage of reconciled entities gathered during the second and final reconciliation, divided by which item type they belong to.
](images/final_look_reconciled_types.png){#fig:finallook_reconciledbar}

## SPARQL endpoint
- TBD


# General Ideas

Temporary file containing ideas for the project. Interesting references and concepts.

med2rdf[@http://med2rdf.org/] is a project to migrate biomedical knowledge bases to RDF format,
facilitating integration with the semantic web.

15 years ago, in the original Cell Ontology paper, they mention the idea to integrate their knowledge with gene expression databases, 
something not done as far as we know [@doi:10.1186/gb-2005-6-2-r21]


## References {.page_break_before}

<!-- Explicitly insert bibliography here -->
<div id="refs"></div>
