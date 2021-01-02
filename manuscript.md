---
title: 'Wikidata to build 5-star Linked Open biological databases: A case study of PanglaoDB'
keywords:
- markdown
- publishing
- manubot
lang: en-US
date-meta: '2021-01-02'
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
  <meta name="dc.date" content="2021-01-02" />
  <meta name="citation_publication_date" content="2021-01-02" />
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
  <link rel="alternate" type="text/html" href="https://jvfe.github.io/paper_wdt_panglao/v/c264a3af04aea766a506f04f04d6bc2a332e64f3/" />
  <meta name="manubot_html_url_versioned" content="https://jvfe.github.io/paper_wdt_panglao/v/c264a3af04aea766a506f04f04d6bc2a332e64f3/" />
  <meta name="manubot_pdf_url_versioned" content="https://jvfe.github.io/paper_wdt_panglao/v/c264a3af04aea766a506f04f04d6bc2a332e64f3/manuscript.pdf" />
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
([permalink](https://jvfe.github.io/paper_wdt_panglao/v/c264a3af04aea766a506f04f04d6bc2a332e64f3/))
was automatically generated
from [jvfe/paper_wdt_panglao@c264a3a](https://github.com/jvfe/paper_wdt_panglao/tree/c264a3af04aea766a506f04f04d6bc2a332e64f3)
on January 2, 2021.
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

PanglaoDB [@https://panglaodb.se/index.html] [@doi:10.1093/database/baz046] is a publically-available database that contains data and metadata on hundreds of single-cell RNA sequencing experiments, providing extensive information on cell types, genes and tissues, as well as manually and community curated cell type markers (Tables @tbl:panglao and @tbl:panglao2). It also provides a rich web user interface for easy data acquisition, including database dumps for bulk downloads.

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

As of 30 December 2020, the article describing PanglaoDB has been cited 88 times. Despite its use by the  the community, the database is on a 3-star category for Linked Open Data [@url:https://www.w3.org/DesignIssues/LinkedData.html] as it does not use the semantic open standards from W3C (RDF and SPARQL) needed for a 4-star rank, neither the links to external data via common identifiers that makes datasets 5-star. Improving the data format toward W3C's gold standards is a valuable step in making biological knowlegde FAIR (Findable, Acessible, Interoperable and Reusable).


The OBO Foundry provides a rich collection of linked biological identifiers [@url:http://www.obofoundry.org/]. However, reconciliation to OBO is challenging, as there are many ontologies, each with slightly different contribution guidelines. For that reason, we decided to reconcile PanglaoDB to Wikidata, which allows simple creation of new terms, provided they follow Wikidata`s notability criteria [@url:https://www.wikidata.org/wiki/Wikidata:Notability]. 

### Wikidata

Wikidata [@https://www.wikidata.org/wiki/Wikidata:Main_Page] is an open, freely editable, knowledge graph database within the semantic web [@https://www.w3.org/standards/semanticweb/] that stores knowledge across a multitude of domains,
such as arts, history, chemistry and biology, using an item-property-value linked data model (Figure @fig:wdt-hep). It is easy to use and edit, by both humans and machines, with a rich web user interface and wrapper packages available
in common programming languages such as R and Python. All the data within Wikidata is linked and inherently public domain, thus, it presents a great opportunity to make scientific data more FAIR (Findable, accessible, interoperable and reusable), as well as provides the necessary tools to curate and develop ontologies. 

![
Wikidata item example, showing item hepatocyte (Q827450), the labels change according to the user's language, but each item has a universal identifier, called QID.
](images/wdt_hepatocyte.png){#fig:wdt-hep}

Several advances towards biological data integration and biological data analysis in Wikidata have been made before, yielding positive
results [@doi:10.1101/031971] [@wikidata:Q87830400] and showcasing it's potential for bioinformatics-related analyses, such as drug repurposing and ID conversion [@doi:10.7554/eLife.52614]. Wikidata has been proposed as a unified base to gather and distribute biomedical knowledge, with more than 50 000 human gene items indexed and hundreds of biomedical-related properties [@doi:10.1016/j.jbi.2019.103292].


 Wikidata is nevertheless a collaborative database, and content is available on different levels of quality. For example, as of August 2020, cell type information was still very lacking, with only 264 items being categorized as "instances of cell types (Q189118)" (<https://w.wiki/b2w>), while other projects describe over 2.000 cell types [@wikidata:Q28660708][@wikidata:Q36067763]. Of those, only nine have a "Cell Ontology ID"[@pmid:27377652] (P7963) associated, and most have a varying amount of statements (Table @tbl:cell-counts). As an additional problem, there are also 23 items being categorized as "instances of cell (Q7868)" (<https://w.wiki/b2x>), illustrating the absence of any formal data model.

| Cell type Item | Number of statements |
|:-------------:|:---------------:|
| red blood cell (Q37187) | 48 |
| myocyte (Q428914) | 18 |
| mesenchymal cell (Q66568500) | 2 |
Table: As of August 2020, Wikidata items regarding cell types have a varying amount of information, with most having very few statements.
{#tbl:cell-counts}


This study was motivated by the increasing importance of cell-type concepts in light of the Human Cell Atlas [@wikidata:Q46368626], and the utter need for improved inteoperability of biological data. We aimed, thus, at providing a case study of the  re-release PandlaoDB in a 5-star Linked Open Data Format while improving the modelling of the necessary concepts on Wikidata.



## Methodology

### Data acquisition

Gene data from Wikidata was acquired using the Wikidata Query Service [@https://query.wikidata.org/]
    - <https://w.wiki/bWc> for *Homo sapiens* genes and <https://w.wiki/bWe> for *Mus musculus* genes.

Data for quality acessment from PanglaoDB was acquired through their metadata database dump repository[@https://github.com/oscar-franzen/PanglaoDB].

The markers dataset was dowloaded manually from PanglaoDB's website (https://panglaodb.se/markers/PanglaoDB_markers_27_Mar_2020.tsv.gz). It contains 15 columns and 8256 rows. 

For the reconciliation, only the columns `species`, `official gene symbol` and 	`cell type` were used. 

All data used was handled using the Pandas[@doi:10.5281/zenodo.3630805] library, 
with the Seaborn[@doi:10.5281/zenodo.4019146] and Matplotlib[@doi:10.5281/zenodo.4030140] libraries being used for plotting. 



### Automated matching

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

### Class creation on Wikidata

Classes corresponding to species-neutral classes were retrieved from Wikidata manually using Wikidata's Graphic User Interface. The dictionay matching terms in PanglaoDB to Wikidata identifiers were stored in a [reference csv table](https://github.com/jvfe/wikidata_panglaodb/blob/master/improvements/results/cell_type_reference_from_panglao_to_wikidata_31_10_2020.csv). 

Cell types which were not represented on Wikidata were added to the database via the graphical user interface (https://www.wikidata.org/wiki/Special:NewItem) and logged in the reference table.

Species-specific cell types for human and mouse cell types were created for every entry in the reference table, connected to the species-neutral concept via a "[subclass of](http://www.wikidata.org/entity/P279)" property (e.g. every single "[human neutrophil](http://www.wikidata.org/entity/Q101405102)" is a also "[neutrophil](http://www.wikidata.org/entity/Q188417)" ).


The reference sheet for species-neutral concepts was used to obtain the "subclass of" for every newly created item. Each item was labeled either "human " + the label for the neutral cell type, described as "cell type found in Homo sapiens" and tagged with the statement "[found in taxon](http://www.wikidata.org/entity/P703)" [_Homo sapiens_](https://www.wikidata.org/wiki/Q15978631). An analogous framework was used for mouse cell types, assuming that mouse in PanglaoDB meant [_Mus musculus_](http://www.wikidata.org/entity/Q83310). Batch creations were added to Wikidata via the tool Quickstatements (<https://quickstatements.toolforge.org/#/>).

All genes in PanglaoDB either were already present on Wikidata or resolved to multiple entities and thus were excluded. 

### Property creation on Wikidata





### Integration to Wikidata 

The reconciled dataset was uploaded to Wikidata via the Wikidata Integrator python package (<https://github.com/SuLab/WikidataIntegrator>), a wrapper for the Wikidata Application Programming Interface. The details of the integration can be seen in the accompanying Jupyter notebook. 

## Access to reconciled data
### Wikidata dumps

Wikidata provides regular dumps in a variety of formats, including RDF dumps: <https://www.wikidata.org/wiki/Wikidata:Database_download>. It is possible to also download partial dumps of the database with reduced size (ex: <https://wdumps.toolforge.org/dump/987> for all cell types with the `has_marker` property).   

### SPARQL queries

Besides the Wikidata Dumps, Wikidata provides an SPARQL endpoint with a Graphical User Interface (<https://query.wikidata.org/>). Updated data was immediately accessible via this endpoint, enabling integrative queries integrated with other database statements.

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

- Adding species specific terms

### Adding a new property
### Adding missing items
- TBD

### Improving interoperability
- TBD

## Wikidata reconciliation - final look

After the aforementioned improvements were made, 
data from PanglaoDB was reconciled once again, 
the automatic classification method was able to detect most cell types matches for most cell types on PanglaoDB matches (Table
@tbl:finallook_summary). The non-unique matches are likely due to synonym or very similar aliases used for different cell type concepts. Nevertheless, it is an evidence that our work improved cell type content on Wikidata, and will arguably facilitate the reconciliation of other cell-type related resources.

||  # of total items |# of unique matches  |   % of total items that were matched |
|:-|--------------:|-------------------:|---------------:|
| Cells     | 215 | 173 |80.4651 |
| Tissues   |  246 |63 | 25.6097 |
| Organs    | 29 |18 | 62.0689 |
| Human Genes | 58216 |35423 | 60.8475 |
| Mouse Genes |  53793 |25124 |  46.705|
Table: Summary of matched PanglaoDB entities after improvements were made.
{#tbl:finallook_summary}

Noticeably, the proportion of automatic matches for other entity types (tissues and organs) seems reduced in relation to the first assessment (35% to 25% and 76 to 62%). These entities were not targeted by our work, but as Wikidata is a living resource, modifications in the database, such as reclassification of entities or adding of other similar concepts, may have reduced the performance of our simple reconciler.

## Analysis of item quality - final look

As can be gathered from Figure @fig:finallook_reconciledbar, nearly all cell type items have the appropriate "instance of cell type" statement, with only 4 items still missing said statement and one item being classified as an "instance of gland". 

This is a considerable advance in improving the quality of cell type data in Wikidata, as having this simple statement will make these items easier to find and be expanded upon.

![
Percentage of reconciled entities gathered during the second and final reconciliation, divided by which item type they belong to.
](images/final_look_reconciled_types.png){#fig:finallook_reconciledbar}


## Wikidata SPARQL queries enabled by the integration

Now that the PanglaoDB is released as Linked Open Data, we can make queries that were not possible before, including
federated queries with other biological databases, such as Uniprot [@https://sparql.uniprot.org/sparql]
and Wikipathways [@https://www.wikipathways.org/index.php/Portal:Semantic_Web].
Due to previous similar reconciliation projects, Wikidata already contains information about genes, including their relations to Gene Ontology (GO) terms,
<!-- você decide se quer manter essa parte ou acha que fica muita coisa -->
something that led to the development of an R package, go2cell [@https://github.com/jvfe/go2cell],
that facilitates interconnection between cell types and GO terms via their markers.
<!--  -->

PanglaoDB's integration to the Wikidata ecosystem allows us to ask a variety of questions. The next section headers exemplify such questions.

### "Which human cell types are related to neurogenesis via their markers?"

As expected, the query below retrieved a series of neuron types, such as "[human purkinje neuron](https://www.wikidata.org/wiki/Q101404913)" and "[human cajal-retzius cell](https://www.wikidata.org/wiki/Q101405091)." It did, however, also retrieved non-neural cell types such as the "[human loop of henle cell](https://www.wikidata.org/wiki/Q101405109), a kidney cell type, and "[human osteoblast](https://www.wikidata.org/wiki/Q101405044). These seemingly unrelated cell types markedly express genes that are involved in neurogenesis, but that does not mean that they are involved with this process. This reinforces the idea that one needs to be careful when using curated pathways to enrich one's analysis, as false positives abound. 

The molecular process that gene products take part depends on the cell type. The SPARQL query below enables us to seamlessly compare  Gene Ontology processes with cell marker data, providing a fruitful sandbox for generation of hypothesis and exploration of the biomedical knowledge landscape.

<div class="is-hidden" id="three-tab-content">
<h5 class="title is-5" style="text-align:center;"> Query for cell types related to neurogenesis </h5>
<div class="columns is-centered">
<p style="text-align: center">
<iframe width=92% height="500" src="https://query.wikidata.org/embed.html#SELECT%20%3FgeneLabel%20%3FcellTypeLabel%0AWHERE%20%0A%7B%0A%20%20%3Fprotein%20wdt%3AP682%20wd%3AQ1456827.%20%23%20protein%20molecular%20process%20neurogenesis%0A%20%20%3Fprotein%20wdt%3AP702%20%3Fgene.%20%20%20%20%20%20%20%23%20protein%20encoded%20by%20gene%0A%20%20%0A%20%20%7B%3Fgene%20wdt%3AP31%20wd%3AQ277338.%7D%20%20%20%20%23%20gene%20is%20an%20instance%20of%20a%20pseudogene%20%0A%20%20UNION%20%20%20%20%20%20%20%20%20%20%20%20%20%20%20%20%20%20%20%20%20%20%20%20%20%20%23%20or%0A%20%20%7B%3Fgene%20wdt%3AP31%20wd%3AQ7187.%7D%20%20%20%20%20%20%23%20gene%20is%20an%20instance%20of%20a%20gene%0A%20%20%3Fgene%20wdt%3AP703%20wd%3AQ15978631.%20%20%20%23%20gene%20is%20found%20in%20taxon%20Homo%20sapiens%0A%20%20%0A%20%20%3FcellType%20wdt%3AP8872%20%3Fgene.%20%20%20%20%20%23%20cell%20type%20has%20marker%20gene%0A%20%20%0A%20%20%3FcellType%20rdfs%3Alabel%20%3FcellTypeLabel.%0A%20%20%3Fgene%20%20%20rdfs%3Alabel%20%3FgeneLabel.%0A%0A%0A%20%20FILTER%28LANG%28%3FcellTypeLabel%29%20%3D%20%22en%22%29%0A%20%20FILTER%28LANG%28%3FgeneLabel%29%20%3D%20%22en%22%29%0A%0A%7D"></iframe>
</p>
</div>
</div>

### "Which cell types express markers associated to Parkinson`s disease?"

Besides integration with Gene Ontology, Wikidata reconciliation makes it possible to complement the marker gene info on PanglaoDB with information about diseases. This integration is of biomedical interest, as there is a quest for detailing of mechanisms that link genetic associations and the diseases themselves. 

"Disease genes" are often compiled from Genomic Wide Association Studies, which look for sequence variation in the DNA. These studies are commonly blind to the cell types related to the pathophysiology of the disease. In the query below, we can see cell types that are marked by genes genetically associated with Parkinson's disease. Even considering the false positives (as per the previously mentioned multifunctional nature of genes) this kind of overlook can aid domain experts to come up with novel hypothesis. 

<div class="is-hidden" id="three-tab-content">
<h5 class="title is-5" style="text-align:center;"> Query for cell types related to Parkinson's disease </h5>
<div class="columns is-centered">
<p style="text-align: center">
<iframe width=92% height="500" src="https://query.wikidata.org/embed.html#SELECT%20%3FcellTypeLabel%20%3FgeneLabel%20%3FdiseaseLabel%20%0AWHERE%20%0A%7B%0A%20%20wd%3AQ11085%20wdt%3AP2293%20%3FdiseaseGene.%20%20%23%20Parkinson%27s%20disease%20--%3E%20genetic%20association%20--%3E%20gene%0A%20%20%3FcellType%20wdt%3AP8872%20%3FdiseaseGene.%20%23%20Cell%20type%20--%3E%20has%20marker%20--%3E%20gene%0A%20%20%0A%20%20%3FcellType%20rdfs%3Alabel%20%3FcellTypeLabel.%0A%20%20wd%3AQ11085%20rdfs%3Alabel%20%3FdiseaseLabel.%0A%20%20%3FdiseaseGene%20%20%20rdfs%3Alabel%20%3FgeneLabel.%0A%0A%20%20FILTER%28LANG%28%3FcellTypeLabel%29%20%3D%20%22en%22%29%0A%20%20FILTER%28LANG%28%3FdiseaseLabel%29%20%3D%20%22en%22%29%0A%20%20FILTER%28LANG%28%3FgeneLabel%29%20%3D%20%22en%22%29%0A%7D"></iframe>
</p>
</div>
</div>

### Which diseases are associated with the markers of pancreatic beta cells?

We can check the cell-type to disease relation in both ways. Scientists that study specific cell types (and not necessarily specific diseases) might be interested in knowing which diseases are related to their cell type of interest. In the sample query below, I looked for the diseases linked to the [human pancreatic beta cells](https://www.wikidata.org/wiki/Q101405087), which play an important role in controlling blood sugar levels. Reassuringly, top hits associated with markers included
[obesity](https://www.wikidata.org/wiki/Q12174) and [type-2 diabetes](https://www.wikidata.org/wiki/Q3025883). Other diseases retrieved, such as [Huntington disease-like 2](https://www.wikidata.org/wiki/Q30990046) don't bear a clear link with sugar function, and might merit a further look by a domain expert to see if there are any hypothesis worth pursuing.

<div class="is-hidden" id="three-tab-content">
<h5 class="title is-5" style="text-align:center;"> Query for cell types related to Parkinson's disease </h5>
<div class="columns is-centered">
<p style="text-align: center">
<iframe width=92% height="500" src="https://query.wikidata.org/embed.html#SELECT%20%3FcellTypeLabel%20%3FdiseaseLabel%20%0A%28COUNT%28DISTINCT%20%3FdiseaseGene%29%20AS%20%3Fcount%29%20%0A%28GROUP_CONCAT%28DISTINCT%20%3FgeneLabel%3B%20SEPARATOR%3D%22%2C%20%22%29%20AS%20%3Fgenes%29%0AWHERE%20%0A%7B%0A%20%20wd%3AQ101405087%20wdt%3AP8872%20%3FdiseaseGene%20.%20%20%20%20%23%20human%20pancreatic%20beta%20cell%20--%3E%20%20has%20marker%20--%3E%20%20gene%0A%20%20%3Fdisease%20wdt%3AP2293%20%3FdiseaseGene%20.%20%20%20%20%20%20%20%20%20%23%20disease%20--%3E%20genetic%20association%20--%3E%20gene%0A%20%20%0A%20%20wd%3AQ101405087%20rdfs%3Alabel%20%3FcellTypeLabel%20.%0A%20%20%3Fdisease%20rdfs%3Alabel%20%3FdiseaseLabel%20.%0A%20%20%3FdiseaseGene%20%20%20rdfs%3Alabel%20%3FgeneLabel%20.%0A%0A%20%20FILTER%28LANG%28%3FcellTypeLabel%29%20%3D%20%22en%22%29%0A%20%20FILTER%28LANG%28%3FdiseaseLabel%29%20%3D%20%22en%22%29%0A%20%20FILTER%28LANG%28%3FgeneLabel%29%20%3D%20%22en%22%29%0A%20%20%0A%20%7D%0A%0AGROUP%20BY%20%3FdiseaseLabel%20%3FcellTypeLabel%20ORDER%20BY%20DESC%28%3Fcount%29%0A%0A"></iframe>
</p>
</div>
</div>


In this work, we re-released the knowledge curated in PanglaoDB on Wikidata, connecting it to the semantic web. Each cell-type/marker statement was added to Wikidata with a pointer to PanglaoDB and a citation of the article, providing proper provenance. At the same time, we documented the process of database integration to Wikidata, providing a blueprint for future efforts. 

It is important to note that not all data on PanglaoDB was added to Wikidata. Fine-grained, database-specific details were too granular for a general-purpose database like Wikidata (e.g. the sensitivity and specificity attached to each marker-cell type pair). Eventhough, these data could be released in RDF format and be connected to independent SPARQL endpoints (as done in the Bio2RDF effort [@wikidata:Q56989268]), we focused on integration to Wikidata to take advantage of the built-in integration with various types of knowledge, as well as the tooling developed by the Wikidata community.  

Linking biological with Wikidata allows out-of-the-box integrative SPARQL queries, as many biomedical ontologies and datasets have been already integrated to Wikidata, and are available in Wikidata's graph. Besides the well-known advantages of having data linked to the Linked Open Data cloud, the Wikidata integration provides user-friendly interfaces for the data. That includes both navigable html pages of classes and properties (e.g. <https://www.wikidata.org/wiki/Q67801129>) as well as an SPARQL Query Service with user-friendly modifications to ease queries for beginners (<https://query.wikidata.org/>) with helper pages for learning SPARQL (<https://www.wikidata.org/wiki/Wikidata:SPARQL_tutorial>) or even requesting queries (<https://www.wikidata.org/wiki/Wikidata:Request_a_query>).   


Wikidata also makes it easy for users to contribute. Wikidata allows editions directly in the Graphical User Interface, acessible for domain experts without programming or ontology training. In fact,  Wikidata may be the solution for an (at least) 7 year-old gap of an "community-based crowd-sourcing approach" for representing knowlegde about cell types. [@wikidata:Q34026802] For those interest in continuous integration, the Python module Wikidata Integrator facilitates for python users to reconcile databases to Wikidata, and it has been used to build bots for several different biological databases [@wikidata:Q87830400].


This work exemplifies the power of releasing Linked Open Data via Wikidata, and provides the biomedical community with the first semantically accessible, 5-star LOD dataset of cell markers. It also paves the way for Wikidata reconciling of other databases for cell-type markers, such as CellMarker [@wikidata:Q56984510], labome [@doi:10.13070/mm.en.3.183], CellFinder [@wikidata:Q28660708] and SHOGoiN/CELLPEDIA [@https://stemcellinformatics.org/]). The approach can in essence be applied to any knowledge set of public interest, providing a low-cost and low-barrier platform for sharing biocurated knowledge in gold standard format.  We hope that community will keep improving marker and overall biological content on Wikidata, and that the interlinked marker information will be useful for researchers all over the world.  

# General Ideas

Temporary file containing ideas for the project. Interesting references and concepts.

med2rdf[@http://med2rdf.org/] is a project to migrate biomedical knowledge bases to RDF format,
facilitating integration with the semantic web.

15 years ago, in the original Cell Ontology paper, they mention the idea to integrate their knowledge with gene expression databases, 
something not done as far as we know [@doi:10.1186/gb-2005-6-2-r21]


## References {.page_break_before}

<!-- Explicitly insert bibliography here -->
<div id="refs"></div>
