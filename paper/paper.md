---
title: 'Synergising ELIXIR resources for training in systems biology'
title_short: 'ELIXIR resources for training in systems biology'
date: "7 April 2024"
output:
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
biohackathon_name: "BioHackathon Europe 2023"
biohackathon_url:   "https://biohackathon-europe.org/"
biohackathon_location: "Barcelona, Spain, 2023"
group: Project 32 - Synergising ELIXIR resources for training in systems biology
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
  orcid: "XXXX-XXXX-XXXX-XXXX"
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

Systems biology (SB) is a new ELIXIR Community, utilising different ELIXIR resources, such as the Training eSupport System (TeSS) and bio.tools, a registry of software tools and data resources for life sciences. One of the main initial objectives of the SB Community is to create a SB-themed domain hosted by TeSS, encompassing SB-related ELIXIR services and events, in a fully automated way.

Most content in TeSS is sourced through automated aggregation ("scraping") of external sources containing resources marked up with semantic metadata, like Bioschemas. Currently, TeSS cannot recognize references to bio.tools identifiers from a Bioschemas-annotated resource, so the number of resources linked to bio.tools is relatively low.

In this project, we will focus on selected SB disciplines from the priority areas of the SB Community to integrate and cross-link related ELIXIR products - training events, training materials, computational and bioinformatics tools, databases and services from the bio.tools registry.

This will be achieved using suitable ontologies identified by the SB community and by careful curation of SB-related materials. We aim to extend this work to other ELIXIR products such as lists of trainers, related ELIXIR Innovation and Industry events and publications. This will serve as a pilot project leading to broader integration with other SB disciplines, and will be of interest to several other ELIXIR Communities.

### Keywords {#keywords}

Systems biology, Bio-ontologies, FAIR science


## Introduction {#introduction}

### Background {#background}

The Systems Biology Community is one of the most recently-created ELIXIR Community [@citesAsRelated:Beard_2020], with the aim of answering several infrastructure needs identified by the community. Owing to its very nature, the field of systems biology (SB) relies not only on the development and use of modelling tools, but also on data storage solutions and community standards. For these reasons,  the SB community set some of its main focuses on the interoperability of systems biology resources and the coordination of capacity building and training resources.

These objectives align within the scope of the ELIXIR Programme and ecosystem, and more specifically with the Training eSupport System (TeSS) [@citesAsAuthority:Beard_2020] and the bio.tools registry [@citesAsAuthority:Ison_2019]. TeSS provides a platform for all sorts of life science-related training events and materials, mostly by aggregating data and metadata from identified content providers by means of HTML scraping, application programming interface (API) integration, and structured-data formats parsing [schema.org](https://schema.org/) [@usesMethodIn:Guha_2016]. Besides, the project is highly involved in [Bioschemas](https://bioschemas.org/) [@citesAsAuthority:Gray_2017] development, an initiative that aims at building upon Schema.org specifications, while providing better-tailored specification profiles for life sciences at large. The bio.tools platform is a community effort of curation of computational biology tools, answering the need for a consistent and up-to-date registry of existing tools and algorithms across all fields of life sciences. The project, also supported by ELIXIR, currently amounts to almost 30,000 tools, annotated by topics, operations, data formats, and many more criteria, allowing users to navigate it rather straightforwardly.

The adequate annotation of both tools and training materials available in TeSS and bio.tools is permitted and facilitated by using the EDAM ontology [@citesAsAuthority:Black_2021]. EDAM is precisely aimed at standardizing terms and definitions for data analysis and management in the context of life sciences. Its goal is to define a controlled vocabulary to be used for several purposes such as the classification of concepts and the semantic annotation of relevant resources. 

### Problematics {#problematics}

While the wealth of available systems biology resources takes into account concerns for interoperability and findability, it still suffers a frequent lack of standard annotations and uneven metadata coverage. A second potential bottleneck is the absence of adequately fine-tuned EDAM concepts and terms, due to the uneven coverage of certain subdisciplines of biology, as well as the constant evolution of bioinformatics methods and topics deriving from advanced biotechnologies. In particular, the domain of systems biology in EDAM has previously not been populated extensively (beyond data formats and a few main concepts), partly due to a lack of demand and appropriate expertise (i.e. experts interested in contributing).

### Objectives {#objectives}

The overall vision of this project is to better synergize the ELIXIR ecosystem by working towards the integration of finer-grained SB concepts and their use for the annotation of software and training contents relevant to the field, and thus improve their findability and navigability.
The long-term goal is to extend the automated framework to other SB-related ELIXIR domains and services by (1) adapting ontologies and exploring ontology mappings (e.g. between EDAM and SBO), to annotate SB-related products by a set of controlled and relational vocabularies; (2) using selected SB disciplines and related TeSS and bio.tools products (training events, training materials, computational, bioinformatics tools, databases, services), to integrate TeSS and bio.tools by extending TeSS’ Bioschemas parser; (3) comply with FAIR principles; (4) explore a possible extension to other ELIXIR resources. To facilitate this, the project conducted during this Biohackathon focused on a pilot study, to assess more precisely the feasibility of this goal.

### Strategy {#strategy}

In developing this project and evaluating its feasibility, we undertook a step-by-step approach involving several key tasks needed to design the foreseen product.
We initiated the process by identifying specific use cases, spanning various systems biology courses, relevant topics, tools, and search terms. This user-centred design approach provided insights into the requirements needed to refine our method and align it with our objectives.
Simultaneously, we implemented a data model utilising resources like EDAM, TeSS, and bio.tools. This allowed us to assess the availability and adequacy of metadata for representing and connecting different elements within the domain, such as events, materials, and software.
Furthermore, we focused on identifying ontologies needed to properly describe SB resources, particularly refining the EDAM ontology and other specialised ontologies like the Systems Biology Ontology (SBO). This ensured the provision of an accurate and consistent representation of available information, thus strengthening the effectiveness of our approach.
Additionally, we conducted a thorough analysis to identify any existing gaps in platforms like TeSS and bio.tools. This analysis served to guide improvements to these platforms, enhancing their usability and relevance for users in the field of systems biology.


## Biohackathon results {#biohackathon-results}

### 1. Semantic model

Most of the ELIXIR resources that serve the contents we aim to connect provide interoperable metadata using schema.org, Bioschemas, and EDAM. We surveyed here how these metadata standards can enable the representation of the information necessary to describe different resources (e.g. software, training materials) so that they can be searched and connected. 
In order to facilitate the findability of SB resources of interest, as well as to ease the navigation between those, the first step was to find a way to connect TeSS and bio.tools entries via markup annotations based on schema.org and, and identify a semantic model to make them interoperable (Figure 1). 


![A. Events and tools from TeSS and bio.tools could be connected through the implementation of Bioschemas markup and the use of the EDAM ontology, however the process is currently not straightforward. B. This data model represents the data objects and links linking training and software tools as well as EDAM with Bioschemas links. It summarises information that can be linked in an interoperable way between bio.tools and TeSS, using EDAM and BioSchemas/schema.org.](./Figures_report/Figure1AB.png){width=80%}


Although the connection is functionally feasible, in practice it relies on the proper use of markup annotations, as recommended in FAIR guidelines [@citesAsRecommendedReading:Wilkinson_2016]. In particular, on one hand, it requires a constant effort to use, develop and maintain an vocabulary specific to Systems Biology in the EDAM ontology (developer-dependent), and on the other hand, an effort to make the best use of markup annotations provided by Bioschemas (content maker-dependent).


### 2. Definition of use cases

#### Courses {#courses}

Systems biology target events or courses (Table 1).

| Type of event | Event name                                                 | Original course url | TeSS url | … |
| - | ----- | - | - | - |
| Course        | Systems biology: from large datasets to biological insight | [link](https://www.ebi.ac.uk/training/events/systems-biology-large-datasets-biological-insight-2/) | [link](https://tess.elixir-europe.org/events/systems-biology-from-large-datasets-to-biological-insight-a32ab30e-f479-4d14-9a12-20000161d99f) | … |
| Course        | Integrative analysis of multi-omics data                   | [link](https://www.embl.org/about/info/course-and-conference-office/events/mmd24-01/)              | none                                                                                                                                         | … |

**Table 1.** 

#### Keywords {#keywords-sb}

List of potentially relevant keywords (specific to the field or not) for a user to search for courses or training materials in systems biology (Table 2).

| | | | |
| ------------------------ | ------------------ | ---------------- | ----------------- |
| machine learning         | network analysis   | data management  | logic modelling   |
| deep learning            | open science       | data integration | single cell omics |
| dimensionality reduction | data heterogeneity | multi omics      | Cytoscape         |
| MOFA2                    | Seurat             | mixOmics         | cosmosR           |
| CellNOptR                | MuVi               | CytoCopteR       | …                 |

**Table 2. ** List of keywords a user may use in order to search for target courses. 

### 3. Knowledge gap: immediate improvements

Following our curation of existing ontologies and keywords list, we were able to make immediate improvements to our main issue: the accessibility of training resources for systems biology. It involved 3 components: the EDAM ontology, the bio.tools registry, and finally the TeSS platform.


#### EDAM {#edam}

First, we identified concepts from our keywords list that were already available in EDAM for the annotation of resources, and when relevant, added or edited relevant attributes. Then we identified terms to be added to the ontology, whether they’re topics, operations, or data types, and their parents in the ontology, concise definition, URL, common synonyms, etc (Table 3).  

    
| Label                    | in EDAM                                                                                    | Sub-ontology in EDAM | Parent<br>in EDAM                                           | Def                    | Attributes                                    |
| -- | - | - | -- | -- | --- |
| machine learning         | [yes](https://edamontology.github.io/edam-browser/#http://edamontology.org/topic_3474)     | Topic                |                                                             |                        |                                               |
| deep learning            | no                                                                                         | Topic                | [Machine learning](http://edamontology.org/topic_3474)      | (from EDAM-BioImaging) |                                               |
| dimensionality reduction | [yes](https://edamontology.github.io/edam-browser/#http://edamontology.org/operation_3935) | Operation            |                                                             |                        | hasTopic Machine Learning                     |
| logic modelling          | no                                                                                         | Data                 | [Mathematical modelling](http://edamontology.org/data_0950) | (from MAMO)            | hasSynonym algebraic logic model, logic model |
| single-cell omics        | no                                                                                         | Topic                | [Omics](http://edamontology.org/topic_3391)                 | (new)                  | hasSynonym Single-cell multi-omics            |

**Table 3. ** Selection of keywords that may be used for a user to search for SB courses or training materials in TeSS, and their attributes. Those terms were added and/or annotated appropriately following our objectives and semantics model.


#### bio.tools {#bio-tools}

Tools that were already available in the bio.tools registry were edited to include more accurate annotations of their related EDAM topics, operations, as well as data types when needed. Plus, a few tools were added to the registry (Table 4).

| Tool      | In BT                              | Topic (EDAM) ; applicationSubCategory (BT) | Operation (EDAM) ; featureList (BT)         | Data (EDAM) ; input/output (BT)                 | URL                                           |
| - | - | -- | -- | -- | - |
| Cytoscape | [Yes](https://bio.tools/cytoscape) | Systems Biology,<br>(Bioinformatics)        | Network analysis,<br>(Network visualisation) | ...                                            | …                                             |
| Seurat    | [Yes](https://bio.tools/seurat)    | Transcriptomics,<br>(Single-cell omics)     | Data integration                             | RNA sequence,<br>Clustered expression profiles | …                                             |
| MOFA2     | No                                 | Multi-omics                                 | Data integration                             | ...                                            | [link](https://biofam.github.io/MOFA2/) |

**Table 4.** A selection of tools that were added or further annotated in bio.tools.

#### TeSS {#tess}

Finally, we added (number?) new event entries in TeSS for SB-related courses, past or future (or recurring events). However, the existing entries could not be edited, though they lacked a number of annotations, such as EDAM terms or tools used/taught in those courses (Table 5).  

| Type   | Event name                                                 | URL in TeSS | Terms                | Tools                    |
| ------ | ---------------------------------------------------------- | ----------- | -------------------- | ------------------------ |
| Course | Systems biology: from large datasets to biological insight | …           | …                    | …                        |
| Course | Integrative analysis of multi-omics data                   | link        | (EDAM tags) | (biotools tags) |

**Table 5.** (from use cases) A new course was added to TeSS’ catalogue and properly annotated using relevant keywords and following the semantics model (see Figure 1B).


The addition of these terms and annotations across the EDAM-bio.tools-TeSS ecosystem allows us to connect tools and courses through our semantic model, thus facilitating users’ search for appropriate courses and training material in the field of systems biology (Figure 2).


![The addition and/or update of terms and tools in the ecosystem allows the connection of events and tools through markup annotations.](./Figures_report/Figure2.png){width=80%}

In a wider fashion, the adoption of detailed markup annotation as recommended guidelines will contribute to a mutual enrichment among ELIXIR platforms as well as their content providers,  through bidirectional metadata scraping.


## Discussion {#discussion}


### Content annotation  {#content-annotation}

* Ontology terms suggestions should be extracted from abstract or other descriptive text about tools (bio.tools) or materials (TeSS).
* Suggested terms should be manually confirmed/validated/corrected by the curator.
* Additional terms can be provided manually by the curator.
* Allow users to edit entries in TeSS ? (many events lack annotations)


### Content search {#content-search}

* Ontology term(s) can be selected from different ontologies (autocomplete …). Multiple terms can be connected with Boolean operators. Boolean expressions are used for search.
* Can Regular expressions be used too?
* Used search expressions can be saved or edited for more advanced searches.

### Navigation across platforms  {#navigation-across-platforms}

#### From bio.tools to TeSS {#from-bio-tools-to-tess}

Enable browsing on found tools in bio.tools and provide links that will search with the same terms on TeSS (Figure 3A).

#### From TeSS to bio.tools {#from-tess-to-bio-tools}

Enable browsing on found materials in TeSS and provide links that will search with the same terms on bio.tools (Figure 3B).


#### To other ontologies {#to-other-ontologies}

Search linking to ontologies or semi-refill search to nearest terms (?)

![A. From bio.tools to TeSS. B. From TeSS to bio.tools.](./Figures_report/Figure3AB.png){width=80%}




## Acknowledgements {#acknowledgements}

This work was performed during the ELIXIR BioHackathon Europe 2023 organised by ELIXIR in November 2023. CR is part of the *Institut Français de Bioinformatique* (IFB, UAR 3601), funded by the *Programme d'Investissements d'Avenir* subsidised by the *Agence Nationale de la Recherche*, number ANR-11-INBS-0013.


## References {#references}
