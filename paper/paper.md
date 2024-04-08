---
title: "Synergising ELIXIR resources for training in systems biology"
title_short: ELIXIR resources for training in systems biology
date: "7 April 2024"
output:
  pdf_document: default
  html_document:
    df_print: paged
affiliations:
- name: Institut Français de Bioinformatique, CNRS UAR 3601, Évry, France
  index: 1
- name: University of Manchester, United Kingdom
  index: 2
- name: Laboratory of Systems and Synthetic Biology, Wageningen University and Research,
    Wageningen, Netherlands
  index: 3
- name: ELIXIR Norway, and Department of Informatics, University of Bergen, Norway
  index: 4
- name: University of Ljubljana, Faculty of Medicine, IBMI, Centre ELIXIR-SI, Slovenia
  index: 5
- name: Institut Pasteur, Université Paris Cité, Bioinformatics and Biostatistics
    Hub, 75015, Paris, France
  index: 6
- name: Division of Infection and Immunity & Systems Immunity Research Institute,
    Cardiff University School of Medicine, United Kingdom
  index: 7
tags:
- Systems biology
- Training
- Ontologies
- ELIXIR
- EDAM
- Bioschemas
cito-bibliography: paper.bib
event: BH23EU
biohackathon_name: BioHackathon Europe 2023
biohackathon_url: "https://biohackathon-europe.org/"
biohackathon_location: Barcelona, Spain, 2023
group: "Project 32 - Synergising ELIXIR resources for training in systems biology"
git_url: https://github.com/rioualen/BioHackEU23_preprint
authors_short: Claire Rioualen \emph{et al.}
authors:
- name: Claire Rioualen
  orcid: "0000-0002-7684-8679"
  affiliation: 1
- name: Finn Bacall
  orcid: "0000-0002-0048-3300"
  affiliation: 2
- name: Cristina Furlan
  orcid: "0000-0003-1416-3647"
  affiliation: 3
- name: Matúš Kalaš
  orcid: "0000-0002-1509-4981"
  affiliation: 4
- name: Brane Leskošek
  orcid: "0000-0001-5202-2349"
  affiliation: 5
- name: Hervé Ménager
  orcid: "0000-0002-7552-1009"
  affiliation: 1,6
- name: Barbara Szomolay
  orcid: "0000-0002-5375-5533"
  affiliation: 7
---

## Project abstract {#project-abstract}

Systems biology (SB) is a new ELIXIR community, that aims to utilise the ELIXIR ecosystem, such as the Training eSupport System (TeSS) and bio.tools, a registry of software tools and data resources for life sciences. One of the main initial objectives of the SB community is to create an SB-themed domain hosted by TeSS, encompassing SB-related ELIXIR services and events, in a fully automated way.

Most content in TeSS is sourced through automated aggregation ("scraping") of external sources containing resources marked up with semantic metadata, like Bioschemas. Currently, TeSS cannot recognize references to bio.tools identifiers from a Bioschemas-annotated resource, so the number of resources linked to bio.tools is relatively low.

In this project, we will focus on selected SB disciplines from the priority areas of the ELXIR SB community to integrate and cross-link related ELIXIR products - training events, training materials, computational and bioinformatics tools, databases and services from the bio.tools registry.

This will be achieved using suitable ontologies identified by the SB community and by careful curation of SB-related materials. We aim to extend this work to other ELIXIR products such as lists of trainers, related ELIXIR Innovation and Industry events and publications. This will serve as a pilot project leading to broader integration with other SB disciplines, and will be of interest to several other ELIXIR communities.


## Introduction {#introduction}

### Background {#background}

The systems biology community [@citesAsRelated:Santos_2022] is one of the most recently-created ELIXIR community, with the aim of answering several infrastructure needs identified by the community. Owing to its very nature, the field of systems biology relies not only on the development and use of modelling tools, but also on data storage solutions and community standards. For these reasons, the SB community set some of its main focuses on the interoperability of systems biology resources and the coordination of capacity building and training resources.

These objectives align within the scope of the ELIXIR Programme and ecosystem, and more specifically with the Training eSupport System (TeSS) [@citesAsAuthority:Beard_2020] and the bio.tools registry [@citesAsAuthority:Ison_2019]. TeSS provides a platform for all sorts of life science-related training events and materials, mostly by aggregating data and metadata from identified content providers by means of HTML scraping, application programming interface (API) integration, and structured-data formats parsing ([Schema.org](https://schema.org/)) [@usesMethodIn:Guha_2016]. Besides, TeSS is highly involved with [Bioschemas](https://bioschemas.org/) [@citesAsAuthority:Gray_2017] development, an initiative that aims at building upon Schema.org specifications, while providing better-tailored specification profiles for life sciences at large. The bio.tools platform is a community effort of curation of computational biology tools, answering the need for a consistent and up-to-date registry of existing tools and algorithms across all fields of life sciences. The bio.tools registry, also supported by ELIXIR, currently amounts to almost 30,000 tools, annotated by topics, operations, data formats, and many additional criteria, allowing users to navigate it rather straightforwardly.

The adequate annotation of both tools and training materials available in TeSS and bio.tools is granted and facilitated by using the EDAM ontology [@citesAsAuthority:Black_2022]. EDAM is precisely aimed at standardising terms and definitions for data analysis and management in the context of life sciences and beyond. Its goal is to define a controlled vocabulary to be used for several purposes such as the the semantic annotation and classification of relevant resources. 

### Problem {#problematics}

While the wealth of systems biology resources address interoperability and findability concerns, they often lack standard annotations and consistent metadata coverage. A second potential bottleneck is the absence of adequately fine-tuned EDAM concepts and terms, due to the uneven coverage of certain subdisciplines of biology, as well as the constant evolution of bioinformatics methods and topics deriving from advanced biotechnologies. In particular, the domain of systems biology in EDAM has not been populated extensively yet (beyond data formats and a few main concepts [@citesAsRelated:biosimulators]), partly due to a lack of demand and appropriate expertise (_i.e._ experts interested in contributing).

### Objective {#objectives}

The overall vision of this project is to better synergise the ELIXIR ecosystem by working towards the integration of finer-grained SB concepts and their use for the annotation of software and training materials relevant to the field, and thus improve their findability and navigability.

### Strategy {#strategy}

In developing this project and evaluating its feasibility, we undertook a step-by-step approach involving several key tasks needed to design the foreseen product.
We initiated the process by identifying specific use cases, spanning various systems biology courses, relevant topics, tools, and search terms. This user-centred design approach provided insights into the requirements needed to refine our method and align it with our objectives.

Simultaneously, we implemented a data model utilising resources like EDAM, TeSS, and bio.tools. This allowed us to assess the availability and adequacy of metadata for representing and connecting different elements within the domain, such as events, materials, and software.

Furthermore, we focused on identifying ontologies needed to properly describe SB resources, particularly refining the EDAM ontology and other specialised ontologies like the Systems Biology Ontology (SBO; http://biomodels.net/SBO/) and the The Mathematical Modelling Ontology (MAMO; http://identifiers.org/mamo). This ensured the provision of an accurate and consistent representation of the available information, thus strengthening the effectiveness of our approach.

Additionally, we conducted a thorough analysis to identify any existing gaps in platforms like TeSS and bio.tools. This analysis served to guide improvements to these platforms, enhancing their usability and relevance for users in the field of systems biology.


## BioHackathon results {#biohackathon-results}



### 1. Definition of use cases


**Table 1.** List of systems biology target events or courses.

| Type | Name                                                 | URL |
| - | --- | ----- |
| Course        | Systems biology: from large datasets to biological insight | [https://www.ebi.ac.uk/training/events/systems-biology-large-datasets-biological-insight-2/](https://www.ebi.ac.uk/training/events/systems-biology-large-datasets-biological-insight-2/) |
| Course        | Integrative analysis of multi-omics data                   | [https://www.embl.org/about/info/course-and-conference-office/events/mmd24-01/](https://www.embl.org/about/info/course-and-conference-office/events/mmd24-01/)              |



**Table 2.** List of systems biology software tools.

| Software link |
| -- |
| https://biofam.github.io/MOFA2/ |
| https://bio.tools/cytoscape |
| https://bio.tools/cellnoptr |
| https://apps.cytoscape.org/apps/cytocopter |
| https://bio.tools/cosmos-omics |
| https://bio.tools/seurat |
| https://github.com/MLO-lab/MuVI |
| https://bio.tools/mixomics |

**Table 3.** List of keywords used in order to search for target courses. 

| Keyword |
| ---------------- | 
| machine learning |
| network analysis |
| data management  |
| logic modelling  |
| data integration |
| single cell omics |
| deep learning     |
| open science      |
| data heterogeneity |
| dimensionality reduction |
|  multi omics.     |

The different resources, to facilitate their access, should be properly searchable (using e.g. the keywords mentioned above), and linked in the ELIXIR resources (e.g. Training eSupport System (TeSS) [@citesAsAuthority:Beard_2020], the bio.tools registry [@citesAsAuthority:Ison_2019], EDAM Browser [@citesAsAuthority:brancotte2018reusable]). Figure 2 illustrates a proposition for these use cases, backed  by the data model described in the next section.

### 2. Data model

Most of the ELIXIR resources that serve the contents we aim to connect provide interoperable metadata using Schema.org, Bioschemas, and EDAM. We surveyed here how these metadata standards can enable the representation of the information necessary to describe different resources (_e.g._ software, training materials) so that they can be searched and connected. 

To enhance the findability and navigation of SB resources, the first step was to connect TeSS and bio.tools entries using schema.org markup annotations and establish a semantic model for interoperability (Figure 1). 


![A. Connecting events and tools from TeSS and bio.tools via Bioschemas markup and the EDAM ontology implementation is feasible, but currently not straightforward. B. This data model represents the data objects and links linking training and software tools as well as EDAM with Bioschemas links. It summarises information that can be linked in an interoperable way between bio.tools and TeSS, using EDAM and Bioschemas/Schema.org.](./Figures_report/Figure1AB.png){width=100%}


Although the connection is functionally feasible, in practice it relies on the proper use of markup annotations, as recommended by the FAIR guiding principles. Specifically, it demands ongoing efforts to utilise, develop, and sustain a systems biology vocabulary within the EDAM ontology (developer-dependent), while also necessitating efforts to maximise the utilisation of markup annotations offered by Bioschemas (content maker-dependent).


### 3. Knowledge gap: immediate improvements

Following our curation of existing ontologies and keywords list, we were able to make immediate improvements to our main issue: the accessibility of training resources for systems biology. It involved 3 components: the EDAM ontology, the bio.tools registry, and finally the TeSS platform.


#### EDAM {#edam}

First, we identified concepts from our keywords list that were already available in EDAM for the annotation of resources, and when relevant, added or edited relevant attributes. Then we identified terms to be added to the ontology, whether they are topics, operations, or data types, and their parents in the ontology, concise definition, URL, common synonyms, _etc._ (Table 4).

**Table 4. ** Selection of terms that may be used for a user to search for SB courses or training materials in TeSS. Some of those terms are already available in EDAM and can be further annotated with relevant synonyms, some terms are available in specialised ontologies (SBO, MAMO), and finally some terms are yet to be added to and defined in EDAM. More detail can be found in the supplementary table S1.

| Label                    | Ontology term                                                                                    | Sub-ontology in EDAM |
| -- | ---- | - |
| machine learning         | [http://edamontology.org/topic_3474](http://edamontology.org/topic_3474)     | Topic                |                                                             |                        |
| deep learning            | [EDAM-BioImaging](https://bioportal.bioontology.org/ontologies/EDAM-BIOIMAGING/?p=classes&conceptid=http%3A%2F%2Fedamontology.org%2Ftopic______Deep_learning)                                                                                         | Topic                |
| dimensionality reduction | [http://edamontology.org/operation_3935](http://edamontology.org/operation_3935) | Operation            |                                                             |
| logic modelling          | http://identifiers.org/mamo/MAMO_0000030                                                   | Data                 |
| single-cell omics        |  [http://edamontology.org/topic_4028](http://edamontology.org/topic_4028) (dev. version)                                                                                       | Topic                |




#### bio.tools {#bio-tools}

Tools that were already available in the bio.tools registry were edited to include more accurate annotations of their related EDAM topics, operations, as well as data types when needed. Plus, a few tools were added to the registry (Table 5).

**Table 5.** Selection of tools commonly used for SB analyses. Some tools are referenced in bio.tools but not necessarily thoroughly annotated, while others are yet to be added. More detail can be found in the supplementary table S2. 

| Name      | bio.tools ID                              | Topic | Operation         |
| - | --- | --- | --- |
| Cytoscape | [https://bio.tools/cytoscape](https://bio.tools/cytoscape) | Systems biology        | Network analysis |
| Seurat    | [https://bio.tools/seurat](https://bio.tools/seurat)    | Transcriptomics     | Data integration                             |
| MOFA2     | -                                 | Multi-omics                                 |


#### TeSS {#tess}

Courses that are in the TeSS catalogue cannot currently be edited by users to add markup annotations. New entries can however be annotated with EDAM topics and operations using an integrated drop-down menu (Table 6).  

**Table 6.** Selection of events or courses related to systems biology. More detail can be found in the supplementary table S3. 

| Type   | Name                                                 | Topics                | Operations                    |  Tools                    |
| - | ---- | --| -- |  - |
| Course | Systems biology: from large datasets to biological insight | Systems biology, <br> Multi-omics |  Data integration                   | Cytoscape                       |
| Course | Integrative analysis of multi-omics data                   | Multi-omics |  Dimensionality reduction | MOFA2, <br> Seurat |




The addition of these terms and annotations across the EDAM-bio.tools-TeSS ecosystem allows us to connect tools and courses through our semantic model, thus facilitating users’ search for appropriate courses and training material in the field of systems biology. As shown in Figure 2, the connection of events and tools.

![The update of existing terms and tools in the ecosystem (dark-coloured tags) and the addition of new terms and tools (pale-coloured tags) allow the connection of events and tools through Bioschemas markup annotations, specifically, by using (1) the "ComputationalTool" profile (Group Tools), (2) the "Course", "CourseInstance" and "TrainingMaterial" profiles (Group Training) and (3) the EDAM ontology (controlled vocabulary). ](./Figures_report/Figure2.png){width=100%}

In a wider fashion, the adoption of detailed markup annotation as recommended guidelines will contribute to a mutual enrichment among ELIXIR platforms as well as their content providers,  through bidirectional metadata scraping.


## Discussion {#discussion}

The general goal of the project presented here was to synchronise systems biology resources with the ELIXIR ecosystem. The work conducted during the 2023 Biohackathon Europe event focused on a pilot study, to assess more precisely the feasibility of our goal. 

In addition to the various specific editions and additions listed above, a number of evolutions or new features could potentially facilitate the maintenance and curation of bioinformatics resources listed and described with systems and references such as bio.tools, TeSS, or EDAM. In particular, a concrete and rather easy-to-implement feature would to enable a direct navigation from tools referenced in the bio.tools registry to courses or training materials that feature them (Figure 3A), and conversely,  from courses or events referenced in TeSS to bio.tools entries relevant to those (Figure 3B).

![ A. From bio.tools to TeSS: enable browsing on found tools in bio.tools and provide links that will search with the same terms on TeSS. B. From TeSS to bio.tools: enable browsing on found materials in TeSS and provide links that will search with the same terms on bio.tools.](./Figures_report/Figure3AB.png){width=100%}

Long-term goals include the extension the automated framework to other SB-related ELIXIR domains and services by adapting ontologies and exploring ontology mappings (e.g. between EDAM and SBO or MAMO), the annotation of SB-related products by a set of controlled and relational vocabularies, by using selected SB disciplines and related TeSS and bio.tools products (training events, training materials, computational, bioinformatics tools, databases, services), the integration of TeSS and bio.tools by extending TeSS’ Bioschemas parser, and finally, the exploration of a possible extension to other ELIXIR resources.

## Acknowledgements {#acknowledgements}

This work was performed during the ELIXIR BioHackathon Europe 2023 organised by ELIXIR in November 2023. This work was supported by [ELIXIR](https://elixir-europe.org), the research infrastructure for life science data. CR is part of the *Institut Français de Bioinformatique* (IFB, UAR 3601), funded by the *Programme d'Investissements d'Avenir* subsidised by the *Agence Nationale de la Recherche*, number ANR-11-INBS-0013.


## References {#references}
