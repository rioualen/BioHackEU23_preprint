---
title: 'BioHackEU23: Synergising ELIXIR Resources for Training in Systems Biology '
title_short: 'BioHackEU23 #32: Synergising ELIXIR Resources for Training in Systems
  Biology'
tags:
- Systems Biology
- Ontologies
- ELIXIR
- EDAM
- Bioschemas
- (other...)
output: pdf_document
affiliations:
- name: Institut Français de Bioinformatique, CNRS UAR 3601, Évry, France.
  index: 1
- name: University of  Manchester.
  index: 2
- name: Laboratory of Systems and Synthetic Biology, Wageningen University and Research,
    Wageningen, Netherlands.
  index: 3
- name: University of Bergen, 5020 Bergen, Norway.
  index: 4
- name: "University of Ljubljana, Faculty of Medicine, IBMI, Centre ELIXIR-SI, Slovenia."
  index: 5
- name: Institut Pasteur, Université Paris Cité, Bioinformatics and Biostatistics
    Hub, 75015, Paris, France.
  index: 6
- name: Division of Infection and Immunity & Systems Immunity Research Institute,
    Cardiff University School of Medicine, United Kingdom.
  index: 7
date: "7 April 2024"
cito-bibliography: paper.bib
event: BH23EU
biohackathon_name: BioHackathon Europe 2023
biohackathon_url: "https://biohackathon-europe.org/"
biohackathon_location: Barcelona, Spain, 2023
group: Project 32
git_url: "https://github.com/biohackrxiv/publication-template"
authors_short: Rioualen \emph{et al.}
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
Most content in TeSS is sourced through automated aggregation (“scraping”) of external sources containing resources marked up with semantic metadata, like Bioschemas. Currently, TeSS cannot recognize references to bio.tools identifiers from a Bioschemas-annotated resource, so the number of resources linked to bio.tools is relatively low.
In this project, we will focus on selected SB disciplines from the priority areas of the SB Community to integrate and cross-link related ELIXIR products - training events, training materials, computational and bioinformatics tools, databases and services from the bio.tools registry.
This will be achieved using suitable ontologies identified by the SB community and by careful curation of SB-related materials. We aim to extend this work to other ELIXIR products such as lists of trainers, related ELIXIR Innovation and Industry events and publications. This will serve as a pilot project leading to broader integration with other SB disciplines, and will be of interest to several other ELIXIR Communities.

### Keywords {#keywords}

Systems biology, Bio-ontologies, FAIR science


## Introduction {#introduction}

### Background {#background}

The Systems Biology Community is one of the most recently-created ELIXIR Community (Santos et al., 2022), with the aim of answering several infrastructure needs identified by the community. Owing to its very nature, the field of systems biology (SB) relies not only on the development and use of modelling tools, but also on data storage solutions and community standards. For these reasons,  the SB community set some of its main focuses on the interoperability of systems biology resources and the coordination of capacity building and training resources.

These objectives align within the scope of the ELIXIR Programme and ecosystem, and more specifically with the Training eSupport System (TeSS; Beard et al., 2020) and the bio.tools registry [@citesAsAuthority:Ison2019]. TeSS provides a platform for all sorts of life science-related training events and materials, mostly by aggregating data and metadata from identified content providers by means of HTML scraping, application programming interface (API) integration, and structured-data formats parsing (schema.org, Guha et al., 2016). Besides, the project is highly involved in Bioschemas development, an initiative that aims at building upon Schema.org specifications, while providing better-tailored specification profiles for life sciences at large (Gray et al., 2017). The bio.tools platform is a community effort of curation of computational biology tools, answering the need for a consistent and up-to-date registry of existing tools and algorithms across all fields of life sciences. The project, also supported by ELIXIR, currently amounts to almost 30,000 tools, annotated by topics, operations, data formats, and many more criteria, allowing users to navigate it rather straightforwardly.

The adequate annotation of both tools and training materials available in TeSS and bio.tools is permitted and facilitated by using the EDAM ontology [@citesAsAuthority:edam]. EDAM is precisely aimed at standardizing terms and definitions for data analysis and management in the context of life sciences. Its goal is to define a controlled vocabulary to be used for several purposes such as the classification of concepts and the semantic annotation of relevant resources. 

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


![Figure 1. A.](./Figures_report/Figure1A.png){width=50%}

![Figure 1. B.](./Figures_report/Figure1B_Semantics-model-Herve.png){width=70%}

**Figure 1.** A. Events and tools from TeSS and bio.tools could be connected through the implementation of Bioschemas markup and the use of the EDAM ontology, however the process is currently not straightforward. B. This data model represents the data objects and links linking training and software tools as well as EDAM with Bioschemas links. It summarises information that can be linked in an interoperable way between bio.tools and TeSS, using EDAM and BioSchemas/schema.org.

Colours on right part of the figure represent the following: navy blue=EDAM vocabulary terms, orange=software as bio.tools contents represented with schema.org/BioSchemas, forest green=trainings and training materials as TeSS contents  represented with schema.org/BioSchemas, light pink=connections between bio.tools and TeSS represented with schema.org/BioSchemas. 

Although the connection is functionally feasible, in practice it relies on the proper use of markup annotations, as recommended in FAIR guidelines (Wilkinson et al., 2016). In particular, on one hand, it requires a constant effort to use, develop and maintain an vocabulary specific to Systems Biology in the EDAM ontology (developer-dependent), and on the other hand, an effort to make the best use of markup annotations provided by Bioschemas (content maker-dependent).


### 2. Definition of use cases

#### Courses {#courses}

Systems biology target events or courses (Table 1).

| Type of event | Event name                                                 | Original course url | TeSS url | … |
| - | ----- | - | - | - |
| Course        | Systems biology: from large datasets to biological insight | [link](https://www.ebi.ac.uk/training/events/systems-biology-large-datasets-biological-insight-2/) | [link](https://tess.elixir-europe.org/events/systems-biology-from-large-datasets-to-biological-insight-a32ab30e-f479-4d14-9a12-20000161d99f) | … |
| Course        | Integrative analysis of multi-omics data                   | [link](https://www.embl.org/about/info/course-and-conference-office/events/mmd24-01/)              | none                                                                                                                                         | … |

**Table 1.** 

#### Keywords {#keywords}

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


![Figure 2.](./Figures_report/Figure2.png){width=80%}

**Figure 2.** The addition and/or update of terms and tools in the ecosystem allows the connection of events and tools through markup annotations.


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

![Figure 3. A.](./Figures_report/Figure3A.png){width=80%}

![Figure 3. B.](./Figures_report/Figure3B.png){width=80%}

**Figure 3.** A. From bio.tools to TeSS. B. From TeSS to bio.tools.



## Acknowledgements {#acknowledgements}

This work was performed during the ELIXIR BioHackathon Europe 2023 organised by ELIXIR in November 2023. CR is part of the *Institut Français de Bioinformatique* (IFB, UAR 3601), funded by the *Programme d'Investissements d'Avenir* subsidised by the *Agence Nationale de la Recherche*, number ANR-11-INBS-0013.


## References {#references}

Beard, N., Bacall, F., Nenadic, A., Thurston, M., Goble, C. A., Sansone, S.-A., & Attwood, T. K. (2020). TeSS: A platform for discovering life-science training opportunities. Bioinformatics, 36(10), 3290–3291. https://doi.org/10.1093/bioinformatics/btaa047 
Gray, A.J.G, Goble, C.A. and Jimenez, R., 2017. Bioschemas: From Potato Salad to Protein Annotation. In International Semantic Web Conference (Posters, Demos & Industry Tracks).
Guha, R. V., Brickley, D., & Macbeth, S. (2016). Schema.org: Evolution of structured data on the web. Communications of the ACM. https://doi.org/10.1145/2844544
[cito:usesMethodIn]

Ison, J., Kalaš, M., Jonassen, I., Bolser, D., Uludag, M., McWilliam, H., Malone, J., Lopez, R., Pettifer, S., & Rice, P. (2013). EDAM: An ontology of bioinformatics operations, types of data and identifiers, topics and formats. Bioinformatics, 29(10), 1325–1332. https://doi.org/10.1093/bioinformatics/btt113 
Ison, J., Rapacki, K., Ménager, H., Kalaš, M., Rydza, E., Chmura, P., Anthon, C., Beard, N., Berka, K., Bolser, D., Booth, T., Bretaudeau, A., Brezovsky, J., Casadio, R., Cesareni, G., Coppens, F., Cornell, M., Cuccuru, G., Davidsen, K., … Brunak, S. (2016). Tools and data services registry: A community effort to document bioinformatics resources. Nucleic Acids Research, 44(D1), D38–D47. https://doi.org/10.1093/nar/gkv1116 
Ison, J., Ienasescu, H., Chmura, P., Rydza, E., Ménager, H., Kalaš, M., Schwämmle, V., Grüning, B., Beard, N., Lopez, R., Duvaud, S., Stockinger, H., Persson, B., Vařeková, R. S., Raček, T., Vondrášek, J., Peterson, H., Salumets, A., Jonassen, I., … Brunak, S. (2019). The bio.tools registry of software tools and data resources for the life sciences. Genome Biology, 20(1), 164. https://doi.org/10.1186/s13059-019-1772-6

Santos, V. M. dos, Anton, M., Szomolay, B., Ostaszewski, M., Arts, I., Benfeitas, R., Angel, V. D. D., Ferk, P., Fey, D., Goble, C., Golebiewski, M., Gruden, K., Heil, K. F., Hermjakob, H., Kahlem, P., Klapa, M. I., Koehorst, J., Kolodkin, A., Kutmon, M., … Hancock, J. M. (2022). Systems Biology in ELIXIR: Modelling in the spotlight (11:1265). F1000Research. https://doi.org/10.12688/f1000research.126734.1 
Wilkinson, M., Dumontier, M., Aalbersberg, I. et al. The FAIR Guiding Principles for scientific data management and stewardship. Sci Data 3, 160018 (2016). https://doi.org/10.1038/sdata.2016.18


#### Citation Typing Ontology annotation

You can use [CiTO](http://purl.org/spar/cito/2018-02-12) annotations, as explained in [this BioHackathon Europe 2021 write up](https://raw.githubusercontent.com/biohackrxiv/bhxiv-metadata/main/doc/elixir_biohackathon2021/paper.md) and [this CiTO Pilot](https://www.biomedcentral.com/collections/cito).
Using this template, you can cite an article and indicate _why_ you cite that article, for instance DisGeNET-RDF [@citesAsAuthority:Queralt2016].

The syntax in Markdown is as follows: a single intention annotation looks like
`[@usesMethodIn:Krewinkel2017]`; two or more intentions are separated
with colons, like `[@extends:discusses:Nielsen2017Scholia]`. When you cite two
different articles, you use this syntax: `[@citesAsDataSource:Ammar2022ETL; @citesAsDataSource:Arend2022BioHackEU22]`.

Possible CiTO typing annotation include:

* citesAsDataSource: when you point the reader to a source of data which may explain a claim
* usesDataFrom: when you reuse somehow (and elaborate on) the data in the cited entity
* usesMethodIn
* citesAsAuthority
* citesAsEvidence
* citesAsPotentialSolution
* citesAsRecommendedReading
* citesAsRelated
* citesAsSourceDocument
* citesForInformation
* confirms
* documents
* providesDataFor
* obtainsSupportFrom
* discusses
* extends
* agreesWith
* disagreesWith
* updates
* citation: generic citation
