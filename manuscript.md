---
author-meta:
- "Jo\xE3o Vitor Ferreira Cavalcante"
- Tiago Lubiana
bibliography:
- content/manual-references.json
date-meta: '2020-09-23'
header-includes: "<!--\nManubot generated metadata rendered from header-includes-template.html.\nSuggest improvements at https://github.com/manubot/manubot/blob/master/manubot/process/header-includes-template.html\n-->\n<meta name=\"dc.format\" content=\"text/html\" />\n<meta name=\"dc.title\" content=\"Analysing the extent of cell type information present in Wikidata: A case study on PanglaoDB\" />\n<meta name=\"citation_title\" content=\"Analysing the extent of cell type information present in Wikidata: A case study on PanglaoDB\" />\n<meta property=\"og:title\" content=\"Analysing the extent of cell type information present in Wikidata: A case study on PanglaoDB\" />\n<meta property=\"twitter:title\" content=\"Analysing the extent of cell type information present in Wikidata: A case study on PanglaoDB\" />\n<meta name=\"dc.date\" content=\"2020-09-23\" />\n<meta name=\"citation_publication_date\" content=\"2020-09-23\" />\n<meta name=\"dc.language\" content=\"en-US\" />\n<meta name=\"citation_language\" content=\"en-US\" />\n<meta name=\"dc.relation.ispartof\" content=\"Manubot\" />\n<meta name=\"dc.publisher\" content=\"Manubot\" />\n<meta name=\"citation_journal_title\" content=\"Manubot\" />\n<meta name=\"citation_technical_report_institution\" content=\"Manubot\" />\n<meta name=\"citation_author\" content=\"Jo\xE3o Vitor Ferreira Cavalcante\" />\n<meta name=\"citation_author_institution\" content=\"Bioinformatics Multidisciplinary Environment, Federal University of Rio Grande do Norte\" />\n<meta name=\"citation_author_orcid\" content=\"0000-0001-7513-7376\" />\n<meta name=\"citation_author\" content=\"Tiago Lubiana\" />\n<meta name=\"citation_author_institution\" content=\"Computational Systems Biology Laboratory, University of S\xE3o Paulo\" />\n<meta name=\"citation_author_orcid\" content=\"0000-0003-2473-2313\" />\n<link rel=\"canonical\" href=\"https://jvfe.github.io/paper_wdt_panglao/\" />\n<meta property=\"og:url\" content=\"https://jvfe.github.io/paper_wdt_panglao/\" />\n<meta property=\"twitter:url\" content=\"https://jvfe.github.io/paper_wdt_panglao/\" />\n<meta name=\"citation_fulltext_html_url\" content=\"https://jvfe.github.io/paper_wdt_panglao/\" />\n<meta name=\"citation_pdf_url\" content=\"https://jvfe.github.io/paper_wdt_panglao/manuscript.pdf\" />\n<link rel=\"alternate\" type=\"application/pdf\" href=\"https://jvfe.github.io/paper_wdt_panglao/manuscript.pdf\" />\n<link rel=\"alternate\" type=\"text/html\" href=\"https://jvfe.github.io/paper_wdt_panglao/v/8cec85600211ab88982b558b7ce88dcbda439473/\" />\n<meta name=\"manubot_html_url_versioned\" content=\"https://jvfe.github.io/paper_wdt_panglao/v/8cec85600211ab88982b558b7ce88dcbda439473/\" />\n<meta name=\"manubot_pdf_url_versioned\" content=\"https://jvfe.github.io/paper_wdt_panglao/v/8cec85600211ab88982b558b7ce88dcbda439473/manuscript.pdf\" />\n<meta property=\"og:type\" content=\"article\" />\n<meta property=\"twitter:card\" content=\"summary_large_image\" />\n<link rel=\"icon\" type=\"image/png\" sizes=\"192x192\" href=\"https://manubot.org/favicon-192x192.png\" />\n<link rel=\"mask-icon\" href=\"https://manubot.org/safari-pinned-tab.svg\" color=\"#ad1457\" />\n<meta name=\"theme-color\" content=\"#ad1457\" />\n<!-- end Manubot generated metadata -->"
keywords:
- markdown
- publishing
- manubot
lang: en-US
manubot-clear-requests-cache: false
manubot-output-bibliography: output/references.json
manubot-output-citekeys: output/citations.tsv
manubot-requests-cache-path: ci/cache/requests-cache
title: 'Analysing the extent of cell type information present in Wikidata: A case study on PanglaoDB'
...






<small><em>
This manuscript
([permalink](https://jvfe.github.io/paper_wdt_panglao/v/8cec85600211ab88982b558b7ce88dcbda439473/))
was automatically generated
from [jvfe/paper_wdt_panglao@8cec856](https://github.com/jvfe/paper_wdt_panglao/tree/8cec85600211ab88982b558b7ce88dcbda439473)
on September 23, 2020.
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

[Wikidata](https://www.wikidata.org/wiki/Wikidata:Main_Page), a freely editable knowledge graph database, presents a great opportunity for the integration of biomedical knowledge, its well thought
linked data model can improve significantly the handling and distribution of scientific information. On the other hand, Wikidata is still lacking
in various aspects, in particular to what pertains to cell type information. This study aims to analyse how cell type knowledge is currently modelled 
in Wikidata and how it differs from other types of biological information, using, as a reference point, metadata from the well known single cell RNA sequencing database, [PanglaoDB](https://panglaodb.se/index.html).

**Keywords**: wikidata, knowledge graph, cell type, ontology.


## Introduction

### Wikidata

Wikidata [@https://www.wikidata.org/wiki/Wikidata:Main_Page] is an open, freely editable, knowledge graph database within the semantic web [@https://www.w3.org/standards/semanticweb/] that stores knowledge across a multitude of domains,
such as arts, history, chemistry and biology, using an item-property-value linked data model (Figure @fig:wdt-hep). It is easy to use and edit, by both humans and machines, with a rich web user interface and wrapper packages available
in common programming languages such as R and Python. All the data within Wikidata is linked and inherently public domain, thus, it presents a great opportunity to make scientific data more FAIR (Findable, accessible, interoperable and reusable), as well as provides the necessary tools to curate and develop ontologies. 

![
Wikidata item example, showing item hepatocyte (Q827450), the labels change according to the user's language, but each item has a universal identifier, called QID.
](images/wdt_hepatocyte.png){#fig:wdt-hep}

Several advances towards biological data integration and biological data analysis in Wikidata have been made before, yielding positive
results [@doi:10.1101/031971] [@doi:10.7554/eLife.52614] and showcasing it's potential for bioinformatics-related analyses, such as drug repurposing and ID conversion [@doi:10.7554/eLife.52614]. Wikidata has been proposed as a unified base to gather and distribute biomedical knowledge, with more than 50 000 human gene items indexed and hundreds of biomedical-related properties [@doi:10.1016/j.jbi.2019.103292]. However, as of August 2020, cell type information is still very scarse, with only 264 items being categorized as "instances of cell types (Q189118)" (<https://w.wiki/b2w>), of those, only nine have a "Cell Ontology ID"[@pmid:27377652] (P7963) associated, and most have a varying amount of statements (Table @tbl:cell-counts). As an additional problem, there are also 23 items being categorized as "instances of cell (Q7868)" (<https://w.wiki/b2x>), illustrating the absence of any formal data model.

| Cell type Item | Number of statements |
|:-------------:|:---------------:|
| red blood cell (Q37187) | 48 |
| myocyte (Q428914) | 18 |
| mesenchymal cell (Q66568500) | 2 |
Table: As of August 2020, Wikidata items regarding cell types have a varying amount of information, with most having very few statements.
{#tbl:cell-counts}


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


## Methodology

### Data acquisition

Data from Wikidata will be acquired using the Wikidata Query Service [@https://query.wikidata.org/] and associated wrapper packages in Python, 
such as WikidataIntegrator[@https://pypi.org/project/wikidataintegrator/] and wikidata2df [@https://pypi.org/project/wikidata2df/].

Data from PanglaoDB will be acquired through their [web interface](https://panglaodb.se/index.html) and [metadata database dump repository](https://github.com/oscar-franzen/PanglaoDB).

All data used will be handled with commonly used Python data science packages, such as Pandas[@doi:10.5281/zenodo.3630805], Seaborn[@doi:10.5281/zenodo.3767070] and Jupyter[@doi:10.1109/MCSE.2007.53].

### Reconciliation

The metadata from PanglaoDB on cell types, genes, tissues (including germ layers) and organs will be matched to Wikidata items using the reconciler[@https://pypi.org/project/reconciler/] Python package, which is itself a wrapper around the well known OpenRefine[@https://openrefine.org/]
reconciliation service, as well as manual intersections of both data sources. 
Data from the reconciliation service will be considered a match if the service returns a value of "match" equals to "True". 

### Item quality assessment

Wikidata items will be assessed for their quality by their number of statements, which can be acquired via both the MediaWiki API [@https://www.mediawiki.org/wiki/API:REST_API] and Wikidata's own query service. And also by the presence of external identifiers, such as Ensembl Gene[@doi:10.1093/nar/gkz966] and Entrez Gene[@doi:10.1093/nar/gks1189] IDs for genes, Cell Ontology[@pmid:27377652] IDs for cell types and Uberon[@pmid:22293552] IDs for organs and tissues. 


# Results

Histological entities from PanglaoDB, that is, cell types, tissue types and organs, were reconciled with Wikidata items using the reconciler[@https://pypi.org/project/reconciler/]
python package and an associated Python stemming function from NLTK [@isbn:9780596516499] for string matching.  

After reconciliation, items were manually checked for false matches - items with the same name but that don‘t represent the same concept. Finally, we obtained the reconciled csv data, and it‘s summary can be seen on Table @tbl:reconcilesummary. 

Depicted in Table @tbl:reconcilesummary are also matches for gene data, which were acquired using manual intersection of both sources, via a Pandas inner merge. This data didn't go through reconciliation because of it's size, but since both ends are dealing with identifiers (Gene Symbol), the item matching should work much better than with histological entities, which are described in natural language.

|         |   # of unique matches  |   # of matched items |   % of total items that were matched |   % of matches that were perfect |   % of matches that don‘t have P31 |
|:--------|-------------------:|-----------------:|---------------:|---------------------------:|------------------:|
| Cells   |                 81 |               85 |        37.6744 |                    38.8235 |           55.2941 |
| Tissues |                 79 |               87 |        32.1138 |                    62.069  |           37.931  |
| Organs  |                 22 |               30 |        75.8621 |                    53.3333 |           46.6667 |
| Human Genes |                 35423 |               35427 |        60.847533 |                    NA      |           NA      |
| Mouse Genes  |                 25124 |               25127 |        46.704962 |                    NA      |           NA      |
Table: Summary of the matched entities from PanglaoDB.
{#tbl:reconcilesummary}

Afterwards, we analysed which types these reconciled items belonged to in Wikidata, which is indicated by their “instance of” (P31) property. 
Most items were missing this information (Figure @fig:reconciledbar).

![
Percentage of reconciled entities, divided by which item type they belong to. Most reconciled items don‘t count with a “instance of” property.
](images/reconciled_item_types.png){#fig:reconciledbar}



# General Ideas

Temporary file containing ideas for the project. Interesting references and concepts.

med2rdf[@http://med2rdf.org/] is a project to migrate biomedical knowledge bases to RDF format,
facilitating integration with the semantic web.

15 years ago, in the original Cell Ontology paper, they mention the idea to integrate their knowledge with gene expression databases, 
something not done as far as we know [@doi:10.1186/gb-2005-6-2-r21]


## References {.page_break_before}

<!-- Explicitly insert bibliography here -->
<div id="refs"></div>
