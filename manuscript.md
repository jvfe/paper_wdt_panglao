---
author-meta:
- "Jo\xE3o Vitor Ferreira Cavalcante"
- Tiago Lubiana
bibliography:
- content/manual-references.json
date-meta: '2020-09-15'
header-includes: "<!--\nManubot generated metadata rendered from header-includes-template.html.\nSuggest improvements at https://github.com/manubot/manubot/blob/master/manubot/process/header-includes-template.html\n-->\n<meta name=\"dc.format\" content=\"text/html\" />\n<meta name=\"dc.title\" content=\"Analysing the extent of cell type information present in Wikidata: A case study on PanglaoDB\" />\n<meta name=\"citation_title\" content=\"Analysing the extent of cell type information present in Wikidata: A case study on PanglaoDB\" />\n<meta property=\"og:title\" content=\"Analysing the extent of cell type information present in Wikidata: A case study on PanglaoDB\" />\n<meta property=\"twitter:title\" content=\"Analysing the extent of cell type information present in Wikidata: A case study on PanglaoDB\" />\n<meta name=\"dc.date\" content=\"2020-09-15\" />\n<meta name=\"citation_publication_date\" content=\"2020-09-15\" />\n<meta name=\"dc.language\" content=\"en-US\" />\n<meta name=\"citation_language\" content=\"en-US\" />\n<meta name=\"dc.relation.ispartof\" content=\"Manubot\" />\n<meta name=\"dc.publisher\" content=\"Manubot\" />\n<meta name=\"citation_journal_title\" content=\"Manubot\" />\n<meta name=\"citation_technical_report_institution\" content=\"Manubot\" />\n<meta name=\"citation_author\" content=\"Jo\xE3o Vitor Ferreira Cavalcante\" />\n<meta name=\"citation_author_institution\" content=\"Bioinformatics Multidisciplinary Environment, Federal University of Rio Grande do Norte\" />\n<meta name=\"citation_author_orcid\" content=\"0000-0001-7513-7376\" />\n<meta name=\"citation_author\" content=\"Tiago Lubiana\" />\n<meta name=\"citation_author_institution\" content=\"Computational Systems Biology Laboratory, University of S\xE3o Paulo\" />\n<meta name=\"citation_author_orcid\" content=\"0000-0003-2473-2313\" />\n<link rel=\"canonical\" href=\"https://jvfe.github.io/paper_wdt_panglao/\" />\n<meta property=\"og:url\" content=\"https://jvfe.github.io/paper_wdt_panglao/\" />\n<meta property=\"twitter:url\" content=\"https://jvfe.github.io/paper_wdt_panglao/\" />\n<meta name=\"citation_fulltext_html_url\" content=\"https://jvfe.github.io/paper_wdt_panglao/\" />\n<meta name=\"citation_pdf_url\" content=\"https://jvfe.github.io/paper_wdt_panglao/manuscript.pdf\" />\n<link rel=\"alternate\" type=\"application/pdf\" href=\"https://jvfe.github.io/paper_wdt_panglao/manuscript.pdf\" />\n<link rel=\"alternate\" type=\"text/html\" href=\"https://jvfe.github.io/paper_wdt_panglao/v/87bf6aca1adac5e6186a08a6b9901711368797a2/\" />\n<meta name=\"manubot_html_url_versioned\" content=\"https://jvfe.github.io/paper_wdt_panglao/v/87bf6aca1adac5e6186a08a6b9901711368797a2/\" />\n<meta name=\"manubot_pdf_url_versioned\" content=\"https://jvfe.github.io/paper_wdt_panglao/v/87bf6aca1adac5e6186a08a6b9901711368797a2/manuscript.pdf\" />\n<meta property=\"og:type\" content=\"article\" />\n<meta property=\"twitter:card\" content=\"summary_large_image\" />\n<link rel=\"icon\" type=\"image/png\" sizes=\"192x192\" href=\"https://manubot.org/favicon-192x192.png\" />\n<link rel=\"mask-icon\" href=\"https://manubot.org/safari-pinned-tab.svg\" color=\"#ad1457\" />\n<meta name=\"theme-color\" content=\"#ad1457\" />\n<!-- end Manubot generated metadata -->"
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
([permalink](https://jvfe.github.io/paper_wdt_panglao/v/87bf6aca1adac5e6186a08a6b9901711368797a2/))
was automatically generated
from [jvfe/paper_wdt_panglao@87bf6ac](https://github.com/jvfe/paper_wdt_panglao/tree/87bf6aca1adac5e6186a08a6b9901711368797a2)
on September 15, 2020.
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




# Methods

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
