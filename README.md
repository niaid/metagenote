# METAGENOTE

## Synopsis

METAGENOTE (https://metagenote.niaid.nih.gov) is a project from the National Institutes of Health (NIH). The objective of
this project is to streamline the submission process of biological samples and metadata to the National Center for
Biotechnology Information (NCBI) Sequence Read Archive (SRA) repository for public access. METAGENOTE compiles and manages
the submission process on user’s behalf with an easy-to-use web interface. The platform offers a wide selection of templates
for different types of biological and experimental studies with a special emphasis on the standardization of metadata
reporting. Importantly, the standardization of metadata reporting permits consistent and reproducible downstream analysis
across different studies. Metadata is documentation that describes data. Properly described and documented data allows the
scientific community to understand and disseminate important details of the work. As sequencing projects become more
commonplace, it is critically important that all biological samples should be made publicly available with standardized
metadata reporting so that these samples can be reanalyzed to independently assess the veracity of the conclusions.

## METAGENOTE User Workflow

### User Types

#### Registered Users

Registered users are able to store their work in METAGENOTE. Additionally, the registration form allows users to identify themselves as members of a particular lab. METAGENOTE offers the ability to view work being done by their peers. Currently, this feature is only available to NIH affiliated users.

##### SSO

METAGENOTE allows single-sign-on authentication to an IDP using SAML. Currently, METAGENOTE is configured to authenticate against NIH CIT.

##### Workspace

The METAGENOTE workspace is the primary work management area for registered users. The “My Workspace” page allows registered users to view the status and continue wok on previous sample groups, view sample groups previously submitted to SRA, and provides a read-only view to sample groups by lab member peers.

######  WIP

The Work-In-Progress (WIP) section of the workspace displays sample groups that have not been submitted to SRA. Sample groups in this section are labeled as one of three status – Incomplete, Publish, or Pending.

Incomplete - indicates that the sample group is missing data required by NCBI on at least one sample

 Publish - when all required fields have been entered the status field of the sample group becomes a clickable button labeled Publish. This indicates the user’s samples are in a complete state ready to be accepted by SRA. The user may initiate the submission process by clicking the Publish button for the indicated sample group.

Pending – the submission process may potentially take several hours to be analyzed and processed by NCBI’s servers. While waiting for this processing to complete, the sample group is marked as Pending. This indicates that METAGENOTE is still waiting for a conclusive acceptance status from NCBI. Once the METAGENOTE system receives an indication that the users sample group has been posted as a public BioProject, the sample group is no longer considered as a work-in-progress and is marked as Published.

###### Published

The Published section in the My Workspace area lists sample groups accepted and published on SRA. The table listing these samples contains the SRA assigned BioProject Id along with a direct link to NCBI’s site with the published information for these annotations. 

###### Lab

Lab sample groups are those that have been entered by members of the same lab. These sample annotations are displayed in a read-only and non-editable mode.

### Non-Registered Users

Non-registered users submit their sample annotations directly to SRA without the storage and management features available to registered users.

### Select Template

METAGENOTE provides a wizard style selection to guide users when choosing the appropriate BioSample Package for their samples. Selection is done in two general stages, select data source then package selection, to help the user target narrow and target the appropriate choice.

![img](../assets/data_src_packages.png?raw=true)

#### Descriptions

##### Metagenomics
Study of genetic material recovered directly from environmental samples

###### Survey (16S, 18S, ITS, other)
Sequences (e.g. 16S, 18S, 23S, 28S rRNA, ITS, COI) from samples obtained directly from the environment, without culturing or identification of the organisms. Example: 16S reads from mouse skin microbiome.
* Air
Survey of microbiome typically sampled from residential and hospital indoor ventilation system. Example: https://www.ncbi.nlm.nih.gov/Traces/study/?acc=SRX749901 (Berkeley Air System)
* Host Associated
Survey of microbiome with the emphasis on the ecological and physiological interactions between hosts and environment. Typical samples sources include skin or stool from mouse. Example: https://www.ncbi.nlm.nih.gov/Traces/study/?acc=SRX2887740 (Mouse Skin)
* Human Associated
Survey of human associated microbiome sampled from the body sites such as anterior nares, retro auricular crease, saliva and nares. Example: https://www.ncbi.nlm.nih.gov/Traces/study/?acc=SRX3744458 (Human Saliva)
* Human Gut
Survey of microbiome in human gastrointestinal track typically with samples from stool. Example: https://www.ncbi.nlm.nih.gov/Traces/study/?acc=SRX3877179 (Human Colon)
* Human Oral
Survey of oral microbiome sampled habitats such as teeth, gingival sulcus, tongue, cheeks, hard and soft palates, and tonsils. Example: https://www.ncbi.nlm.nih.gov/Traces/study/?acc=SRX3347299 (Gingival Groove)
* Human Skin
Survey of microbiome on human skin such as nare, external auditory canal, occiput, retroauricular crease, and volar forearm. Example: https://www.ncbi.nlm.nih.gov/Traces/study/?acc=ERX1953742 (Children Forearm)
* Human Vaginal
Survey of vaginal microbiome sampled from locations such as poster fornix, mid vagina, and introitus. Example: https://www.ncbi.nlm.nih.gov/Traces/study/?acc=SRX3099510 (Human Vaginal Swab)
* Microbial
Survey of microbiome without specific categories, such as ant fungus, beach sand, dust, fermentation, and compost. Example: https://www.ncbi.nlm.nih.gov/Traces/study/?acc=SRX3743992 (Fermentation)
* Miscellaneous
Survey of microbiome generally not classified in any particular categories, such as samples collected from debris after natural disaster and echinoderm. Example: https://www.ncbi.nlm.nih.gov/Traces/study/?acc=SRX2827072 (Manure)
* Plant Associated
Survey of microbiome in plants typically as a response to changes in environment with samples from, as an example, the roots. Example: https://www.ncbi.nlm.nih.gov/Traces/study/?acc=SRX3884967 (Leaf)
* Sediment
Survey of microbiome sampled from the locations such as estuaries, wetland, and river bed. Example: https://www.ncbi.nlm.nih.gov/Traces/study/?acc=SRX3948228 (Beach Sediment)
* Soil
Survey of microbiome in soil sampled from the locations such forest, glaciers, and permafrost. Example: https://www.ncbi.nlm.nih.gov/Traces/study/?acc=ERX1298469 (Canada Soil)
* Wastewater
Survey of microbiome typically sampled from sewage and sludge. Example: https://www.ncbi.nlm.nih.gov/Traces/study/?acc=SRX3387942 (Municipal Wastewater)
* Water
Survey of microbiome sampled from, for example, tap/drinking water, swimming pool, river, and ocean. Example: https://www.ncbi.nlm.nih.gov/Traces/study/?acc=SRX1078403 (Freshwater)

###### Metagenomes
Sequences obtained using whole genome sequencing on samples obtained directly from the environment, without culturing or identification of the organisms.
* Air
Metagenomic survey of microbiome typically sampled from residential and hospital indoor ventilation system. Example: https://www.ncbi.nlm.nih.gov/Traces/study/?acc=SRX749901 (Berkeley Air System)
* Host Associated
Metagenomic survey of microbiome with the emphasis on the ecological and physiological interactions between hosts and environment. Typical samples sources include skin or stool from mouse. Example: https://www.ncbi.nlm.nih.gov/Traces/study/?acc=SRX2887740 (Mouse Skin)
* Human Associated
Metagenomic survey of human associated microbiome sampled from the body sites such as anterior nares, retro auricular crease, saliva and nares. Example: https://www.ncbi.nlm.nih.gov/Traces/study/?acc=SRX3744458 (Human Saliva)
* Human Gut
Metagenomic survey of microbiome in human gastrointestinal track typically with samples from stool. Example: https://www.ncbi.nlm.nih.gov/Traces/study/?acc=SRX3877179 (Human Colon)
* Human Oral
Metagenomic survey of oral microbiome sampled habitats such as teeth, gingival sulcus, tongue, cheeks, hard and soft palates, and tonsils. Example: https://www.ncbi.nlm.nih.gov/Traces/study/?acc=SRX3347299 (Gingival Groove)
* Human Skin
Metagenomic survey of microbiome on human skin such as nare, external auditory canal, occiput, retroauricular crease, and volar forearm. Example: https://www.ncbi.nlm.nih.gov/Traces/study/?acc=ERX1953742 (Children Forearm)
* Human Vaginal
Metagenomic survey of vaginal microbiome sampled from locations such as poster fornix, mid vagina, and introitus. Example: https://www.ncbi.nlm.nih.gov/Traces/study/?acc=SRX3099510 (Human Vaginal Swab)
* Microbial
Metagenomic survey of microbiome without specific categories, such as ant fungus, beach sand, dust, fermentation, and compost. Example: https://www.ncbi.nlm.nih.gov/Traces/study/?acc=SRX3743992 (Fermentation)
* Miscellaneous
Metagenomic survey of microbiome generally not classified in any particular categories, such as samples collected from debris after natural disaster and echinoderm. Example: https://www.ncbi.nlm.nih.gov/Traces/study/?acc=SRX2827072 (Manure)
* Plant Associated
Metagenomic survey of microbiome in plants typically as a response to changes in environment with samples from, as an example, the roots. Example: https://www.ncbi.nlm.nih.gov/Traces/study/?acc=SRX3884967 (Leaf)
* Sediment
Metagenomic survey of microbiome sampled from the locations such as estuaries, wetland, and river bed. Example: https://www.ncbi.nlm.nih.gov/Traces/study/?acc=SRX3948228 (Beach Sediment)
* Soil
Metagenomic survey of microbiome in soil sampled from the locations such forest, glaciers, and permafrost. Example: https://www.ncbi.nlm.nih.gov/Traces/study/?acc=ERX1298469 (Canada Soil)
* Wastewater
Metagenomic survey of microbiome typically sampled from sewage and sludge. Example: https://www.ncbi.nlm.nih.gov/Traces/study/?acc=SRX3387942 (Municipal Wastewater)
* Water
Metagenomic survey of microbiome sampled from, for example, tap/drinking water, swimming pool, river, and ocean. Example: https://www.ncbi.nlm.nih.gov/Traces/study/?acc=SRX1078403 (Freshwater)

###### Specimen
Marker gene sequences obtained from any material identifiable by means of specimens.
* Air
Metagenomic survey of microbiome typically sampled from residential and hospital indoor ventilation system
* Host Associated
Metagenomic survey of microbiome with the emphasis on the ecological and physiological interactions between hosts and environment. Typical samples sources include skin or stool from mouse.
* Human Associated
Metagenomic survey of human associated microbiome sampled from the body sites such as anterior nares, retro auricular crease, saliva and nares
* Human Gut
Metagenomic survey of microbiome in human gastrointestinal track typically with samples from stool
* Human Oral
Metagenomic survey of oral microbiome sampled habitats such as teeth, gingival sulcus, tongue, cheeks, hard and soft palates, and tonsils
* Human Skin
Metagenomic survey of microbiome on human skin such as nare, external auditory canal, occiput, retroauricular crease, and volar forearm
* Human Vaginal
Metagenomic survey of vaginal microbiome sampled from locations such as poster fornix, mid vagina, and introitus
* Microbial
Metagenomic survey of microbiome without specific categories, such as ant fungus, beach sand, dust, fermentation, and compost
* Miscellaneous
Metagenomic survey of microbiome generally not classified in any particular categories, such as samples collected from debris after natural disaster and echinoderm
* Plant Associated
Metagenomic survey of microbiome in plants typically as a response to changes in environment with samples from, as an example, the roots
* Sediment
Metagenomic survey of microbiome sampled from the locations such as estuaries, wetland, and river bed
* Soil
Metagenomic survey of microbiome in soil sampled from the locations such forest, glaciers, and permafrost
* Wastewater
Metagenomic survey of microbiome typically sampled from sewage and sludge
* Water
Metagenomic survey of microbiome sampled from, for example, tap/drinking water, swimming pool, river, and ocean

##### Single microbial genomes
Study of complete DNA sequence of an organism's genome

###### Bacteria/Archaea Genome
Cultured bacterial/archaeal sample
* Air
Cultured bacterial/archaeal libraries typically sampled from residential and hospital indoor ventilation system. Example: https://www.ncbi.nlm.nih.gov/Traces/study/?acc=SRX749901 (Berkeley Air System)
* Host Associated
Cultured bacterial/archaeal libraries with the emphasis on the ecological and physiological interactions between hosts and environment. Typical samples sources include skin or stool from mouse. Example: https://www.ncbi.nlm.nih.gov/Traces/study/?acc=SRX2887740 (Mouse Skin)
* Human Associated
Cultured bacterial/archaeal libraries from the body sites such as anterior nares, retro auricular crease, saliva and nares. Example: https://www.ncbi.nlm.nih.gov/Traces/study/?acc=SRX3744458 (Human Saliva)
* Human Gut
Cultured bacterial/archaeal libraries in human gastrointestinal track typically with samples from stool. Example: https://www.ncbi.nlm.nih.gov/Traces/study/?acc=SRX3877179 (Human Colon)
* Human Oral
Cultured bacterial/archaeal libraries sampled habitats such as teeth, gingival sulcus, tongue, cheeks, hard and soft palates, and tonsils. Example: https://www.ncbi.nlm.nih.gov/Traces/study/?acc=SRX3347299 (Gingival Groove)
* Human Skin
Cultured bacterial/archaeal libraries on human skin such as nare, external auditory canal, occiput, retroauricular crease, and volar forearm. Example: https://www.ncbi.nlm.nih.gov/Traces/study/?acc=ERX1953742 (Children Forearm)
* Human Vaginal
Cultured bacterial/archaeal libraries of vaginal microbiome sampled from locations such as poster fornix, mid vagina, and introitus. Example: https://www.ncbi.nlm.nih.gov/Traces/study/?acc=SRX3099510 (Human Vaginal Swab)
* Microbial
Cultured bacterial/archaeal libraries without specific categories, such as ant fungus, beach sand, dust, fermentation, and compost. Example: https://www.ncbi.nlm.nih.gov/Traces/study/?acc=SRX3743992 (Fermentation)
* Miscellaneous
Cultured bacterial/archaeal libraries generally not classified in any particular categories, such as samples collected from debris after natural disaster and echinoderm. Example: https://www.ncbi.nlm.nih.gov/Traces/study/?acc=SRX2827072 (Manure)
* Plant Associated
Cultured bacterial/archaeal libraries in plants typically as a response to changes in environment with samples from, as an example, the roots. Example: https://www.ncbi.nlm.nih.gov/Traces/study/?acc=SRX3884967 (Leaf)
* Sediment
Cultured bacterial/archaeal libraries sampled from the locations such as estuaries, wetland, and river bed. Example: https://www.ncbi.nlm.nih.gov/Traces/study/?acc=SRX3948228 (Beach Sediment)
* Soil
Cultured bacterial/archaeal libraries in soil sampled from the locations such forest, glaciers, and permafrost. Example: https://www.ncbi.nlm.nih.gov/Traces/study/?acc=ERX1298469 (Canada Soil)
* Wastewater
Cultured bacterial/archaeal libraries typically sampled from sewage and sludge. Example: https://www.ncbi.nlm.nih.gov/Traces/study/?acc=SRX3387942 (Municipal Wastewater)
* Water
Cultured bacterial/archaeal libraries sampled from, for example, tap/drinking water, swimming pool, river, and ocean. Example: https://www.ncbi.nlm.nih.gov/Traces/study/?acc=SRX1078403 (Freshwater)

###### Assembled genome
Metagenome assembled genome
* Air
Metagenomic survey of microbiome typically sampled from residential and hospital indoor ventilation system. Example: https://www.ncbi.nlm.nih.gov/Traces/study/?acc=SRX749901 (Berkeley Air System)
* Host Associated
Metagenomic survey of microbiome with the emphasis on the ecological and physiological interactions between hosts and environment. Typical samples sources include skin or stool from mouse. Example: https://www.ncbi.nlm.nih.gov/Traces/study/?acc=SRX2887740 (Mouse Skin)
* Human Associated
Metagenomic survey of human associated microbiome sampled from the body sites such as anterior nares, retro auricular crease, saliva and nares. Example: https://www.ncbi.nlm.nih.gov/Traces/study/?acc=SRX3744458 (Human Saliva)
* Human Gut
Metagenomic survey of microbiome in human gastrointestinal track typically with samples from stool. Example: https://www.ncbi.nlm.nih.gov/Traces/study/?acc=SRX3877179 (Human Colon)
* Human Oral
Metagenomic survey of oral microbiome sampled habitats such as teeth, gingival sulcus, tongue, cheeks, hard and soft palates, and tonsils. Example: https://www.ncbi.nlm.nih.gov/Traces/study/?acc=SRX3347299 (Gingival Groove)
* Human Skin
Metagenomic survey of microbiome on human skin such as nare, external auditory canal, occiput, retroauricular crease, and volar forearm. Example: https://www.ncbi.nlm.nih.gov/Traces/study/?acc=ERX1953742 (Children Forearm)
* Human Vaginal
Metagenomic survey of vaginal microbiome sampled from locations such as poster fornix, mid vagina, and introitus. Example: https://www.ncbi.nlm.nih.gov/Traces/study/?acc=SRX3099510 (Human Vaginal Swab)
* Microbial
Metagenomic survey of microbiome without specific categories, such as ant fungus, beach sand, dust, fermentation, and compost. Example: https://www.ncbi.nlm.nih.gov/Traces/study/?acc=SRX3743992 (Fermentation)
* Miscellaneous
Metagenomic survey of microbiome generally not classified in any particular categories, such as samples collected from debris after natural disaster and echinoderm. Example: https://www.ncbi.nlm.nih.gov/Traces/study/?acc=SRX2827072 (Manure)
* Plant Associated
Metagenomic survey of microbiome in plants typically as a response to changes in environment with samples from, as an example, the roots. Example: https://www.ncbi.nlm.nih.gov/Traces/study/?acc=SRX3884967 (Leaf)
* Sediment
Metagenomic survey of microbiome sampled from the locations such as estuaries, wetland, and river bed. Example: https://www.ncbi.nlm.nih.gov/Traces/study/?acc=SRX3948228 (Beach Sediment)
* Soil
Metagenomic survey of microbiome in soil sampled from the locations such forest, glaciers, and permafrost. Example: https://www.ncbi.nlm.nih.gov/Traces/study/?acc=ERX1298469 (Canada Soil)
* Wastewater
Metagenomic survey of microbiome typically sampled from sewage and sludge. Example: https://www.ncbi.nlm.nih.gov/Traces/study/?acc=SRX3387942 (Municipal Wastewater)
* Water
Metagenomic survey of microbiome sampled from, for example, tap/drinking water, swimming pool, river, and ocean. Example: https://www.ncbi.nlm.nih.gov/Traces/study/?acc=SRX1078403 (Freshwater)

###### Amplified genome
Single amplified genome
* Air
Single amplified genome typically sampled from residential and hospital indoor ventilation system
* Host Associated
Single amplified genome with the emphasis on the ecological and physiological interactions between hosts and environment. Typical samples sources include skin or stool from mouse.
* Human Associated
Single amplified genome from the body sites such as anterior nares, retro auricular crease, saliva and nares
* Human Gut
Single amplified genome in human gastrointestinal track typically with samples from stool
* Human Oral
Single amplified genome sampled habitats such as teeth, gingival sulcus, tongue, cheeks, hard and soft palates, and tonsils
* Human Skin
Single amplified genome on human skin such as nare, external auditory canal, occiput, retroauricular crease, and volar forearm
* Human Vaginal
Single amplified genome of vaginal microbiome sampled from locations such as poster fornix, mid vagina, and introitus
* Microbial
Single amplified genome without specific categories, such as ant fungus, beach sand, dust, fermentation, and compost
* Miscellaneous
Single amplified genome generally not classified in any particular categories, such as samples collected from debris after natural disaster and echinoderm
* Plant Associated
Single amplified genome in plants typically as a response to changes in environment with samples from, as an example, the roots
* Sediment
Single amplified genome sampled from the locations such as estuaries, wetland, and river bed
* Soil
Single amplified genome in soil sampled from the locations such forest, glaciers, and permafrost
* Wastewater
Single amplified genome typically sampled from sewage and sludge
* Water
Single amplified genome sampled from, for example, tap/drinking water, swimming pool, river, and ocean

###### Viral genome
Viral samples
* Air
Viral libraries typically sampled from residential and hospital indoor ventilation system
* Host Associated
Viral libraries with the emphasis on the ecological and physiological interactions between hosts and environment. Typical samples sources include skin or stool from mouse.
* Human Associated
Viral libraries sampled from the body sites such as anterior nares, retro auricular crease, saliva and nares
* Human Gut
Viral libraries in human gastrointestinal track typically with samples from stool
* Human Oral
Viral libraries sampled habitats such as teeth, gingival sulcus, tongue, cheeks, hard and soft palates, and tonsils
* Human Skin
Viral libraries on human skin such as nare, external auditory canal, occiput, retroauricular crease, and volar forearm
* Human Vaginal
Viral libraries sampled from locations such as poster fornix, mid vagina, and introitus
* Microbial
Viral libraries without specific categories, such as ant fungus, beach sand, dust, fermentation, and compost
* Miscellaneous
Viral libraries generally not classified in any particular categories, such as samples collected from debris after natural disaster and echinoderm
* Plant Associated
Viral libraries in plants typically as a response to changes in environment with samples from, as an example, the roots
* Sediment
Viral libraries sampled from the locations such as estuaries, wetland, and river bed
* Soil
Viral libraries in soil sampled from the locations such forest, glaciers, and permafrost
* Wastewater
Viral libraries typically sampled from sewage and sludge
* Water
Viral libraries sampled from, for example, tap/drinking water, swimming pool, river, and ocean

###### Uncultivated viral genome
Uncultivated viral genome
* Air
Uncultivated Virus Genome, Air; Version 5.0
* Host Associated
Uncultivated Virus Genome, Host-Associated; Version 5.0
* Human Associated
Uncultivated Virus Genome, Human-Associated; Version 5.0
* Human Gut
Uncultivated Virus Genome, Human-Gut; Version 5.0
* Human Oral
Uncultivated Virus Genome, Human-Oral; Version 5.0
* Human Skin
Uncultivated Virus Genome, Human-Skin; Version 5.0
* Human Vaginal
Uncultivated Virus Genome, Human-Vaginal; Version 5.0
* Microbial
Uncultivated Virus Genome, Microbial; Version 5.0
* Miscellaneous
Uncultivated Virus Genome, Miscellaneous; Version 5.0
* Plant Associated
Uncultivated Virus Genome, Plant-Associated; Version 5.0
* Sediment
Uncultivated Virus Genome, Sediment; Version 5.0
* Soil
Uncultivated Virus Genome, Soil; Version 5.0
* Wastewater
Uncultivated Virus Genome, Wastewater; Version 5.0
* Water
Uncultivated Virus Genome, Water; Version 5.0

##### Eukaryote/Model organism
Eukaryotic or multicellular samples

###### Model organism
Multicellular samples or cell lines derived from common laboratory model organisms, e.g., mouse, rat, Drosophila, worm, fish, frog, or large mammals including zoo and farm animals.

###### Eukaryote
Eukaryotic samples
* Air
Eukaryotic libraries typically sampled from residential and hospital indoor ventilation system. Example: https://www.ncbi.nlm.nih.gov/Traces/study/?acc=SRX749901 (Berkeley Air System)
* Host Associated
Eukaryotic libraries with the emphasis on the ecological and physiological interactions between hosts and environment. Typical samples sources include skin or stool from mouse. Example: https://www.ncbi.nlm.nih.gov/Traces/study/?acc=SRX2887740 (Mouse Skin)
* Human Associated
Eukaryotic libraries sampled from the body sites such as anterior nares, retro auricular crease, saliva and nares. Example: https://www.ncbi.nlm.nih.gov/Traces/study/?acc=SRX3744458 (Human Saliva)
* Human Gut
Eukaryotic libraries in human gastrointestinal track typically with samples from stool. Example: https://www.ncbi.nlm.nih.gov/Traces/study/?acc=SRX3877179 (Human Colon)
* Human Oral
Eukaryotic libraries sampled habitats such as teeth, gingival sulcus, tongue, cheeks, hard and soft palates, and tonsils. Example: https://www.ncbi.nlm.nih.gov/Traces/study/?acc=SRX3347299 (Gingival Groove)
* Human Skin
Eukaryotic libraries on human skin such as nare, external auditory canal, occiput, retroauricular crease, and volar forearm. Example: https://www.ncbi.nlm.nih.gov/Traces/study/?acc=ERX1953742 (Children Forearm)
* Human Vaginal
Eukaryotic libraries of vaginal microbiome sampled from locations such as poster fornix, mid vagina, and introitus. Example: https://www.ncbi.nlm.nih.gov/Traces/study/?acc=SRX3099510 (Human Vaginal Swab)
* Microbial
Eukaryotic libraries without specific categories, such as ant fungus, beach sand, dust, fermentation, and compost. Example: https://www.ncbi.nlm.nih.gov/Traces/study/?acc=SRX3743992 (Fermentation)
* Miscellaneous
Eukaryotic libraries generally not classified in any particular categories, such as samples collected from debris after natural disaster and echinoderm. Example: https://www.ncbi.nlm.nih.gov/Traces/study/?acc=SRX2827072 (Manure)
* Plant Associated
Eukaryotic libraries in plants typically as a response to changes in environment with samples from, as an example, the roots. Example: https://www.ncbi.nlm.nih.gov/Traces/study/?acc=SRX3884967 (Leaf)
* Sediment
Eukaryotic libraries sampled from the locations such as estuaries, wetland, and river bed. Example: https://www.ncbi.nlm.nih.gov/Traces/study/?acc=SRX3948228 (Beach Sediment)
* Soil
Eukaryotic libraries in soil sampled from the locations such forest, glaciers, and permafrost. Example: https://www.ncbi.nlm.nih.gov/Traces/study/?acc=ERX1298469 (Canada Soil)
* Wastewater
Eukaryotic libraries typically sampled from sewage and sludge. Example: https://www.ncbi.nlm.nih.gov/Traces/study/?acc=SRX3387942 (Municipal Wastewater)
* Water
Eukaryotic libraries sampled from, for example, tap/drinking water, swimming pool, river, and ocean. Example: https://www.ncbi.nlm.nih.gov/Traces/study/?acc=SRX1078403 (Freshwater)

##### Human-derived cell lines
For samples isolated from humans use the Pathogen, Microbe or appropriate MIxS package. Only use for human-derived cell line samples that have no privacy concerns.

### Describe Samples: Sample Group Editor

The Sample Group editor provides a tool with a familiar "Excel-like" experience that allows users to efficiently annotate their samples.

* Required Attributes - indicates sample atributes required by NCBI. These attributes must be filled to be accepted to the SRA.

* Recommended Attributes - attributes recommended by METAGENOTE. While these values are not marked required by NCBI. These annotations are recommended by groups within the NIH.

* Anatomy Tool - METAGENOTE features a graphical interface to aid users when annotating attributes requiring an anatomical location. Users indicate the site by clicking on a graphical depiction of the general anatomical area. METAGENOTE fills the attribute with a value from a standardized ontology value set such as the Foundational Model of Anatomy (FMA).

* Ontology Lookup - context menus are available in the editor using a mouse right-click. A searchable set of ontology values may be used to help users quickly fill fields with standardized values.

* Attribute Descriptions - every attribute in the editor is accompanied with a description to provide context, commonly used values, and expected formatting of input.

* Export - the sample group editor allows users to export their work locally to their comoputer as an Excel formatted file

* Import - METAGENOTE features an import tool for existing sample annotations. The import may be CSV formatted or an Excel binary file. The import process will automatically map column headers to the selected package 

  

### Submit to SRA

#### Upload Sequence Files

Recognized Sequence File Types

#### Map Samples to Sequence Files

Auto Sequence Filename Grouping

#### Describe Project

- Project Name

- Project Title

- Sequencing Platform

- Sequencing Instrument

  The choice of sequencing instrument is dependent on the Sequencing Platform specified.

  * _LS454
    * 454 GS
    * 454 GS 20
    * 454 GS FLX
    * 454 GS FLX+
    * 454 GS FLX Titanium
    * 454 GS Junior
  * ABI_SOLID
    * AB 5500 Genetic Analyzer
    * AB 5500xl Genetic Analyzer
    * AB 5500x-Wl Genetic Analyzer
    * AB SOLiD 3 Plus System
    * AB SOLiD 4 System
    * AB SOLiD 4hq System
    * AB SOLiD PI System
    * AB SOLiD System
    * AB SOLiD System 2.0
    * AB SOLiD System 3.0
  * BGISEQ
    * BGISEQ-500
  * CAPILLARY
    * AB 310 Genetic Analyzer
    * AB 3130 Genetic Analyzer
    * AB 3130xL Genetic Analyzer
    * AB 3500 Genetic Analyzer
    * AB 3500xL Genetic Analyzer
    * AB 3730 Genetic Analyzer
    * AB 3730xL Genetic Analyzer
  * COMPLETE_GENOMIC
    * Complete Genomics
  * HELICOS
    * Helicos HeliScope
  * ILLUMINA
    * HiSeq X Five
    * HiSeq X Ten
    * Illumina Genome Analyzer
    * Illumina Genome Analyzer II
      Illumina Genome Analyzer IIx
    * Illumina HiScanSQ
    * Illumina HiSeq 1000
    * Illumina HiSeq 1500
    * Illumina HiSeq 2000
    * Illumina HiSeq 2500
    * Illumina HiSeq 3000
    * Illumina HiSeq 4000
    * Illumina iSeq 100
    * Illumina NovaSeq 6000
    * Illumina MiniSeq
    * Illumina MiSeq
    * NextSeq 500
    * NextSeq 550
  * ION_TORRENT
    * Ion Torrent PGM
    * Ion Torrent Proton
    * Ion Torrent S5 XL
    * Ion Torrent S5
  * OXFORD_NANOPORE
    * GridION
    * MinION
    * PromethION
    * PACBIO_SMRT
    * PacBio RS
    * PacBio RS II
    * PacBio Sequel

- Read Orientation

- Library Strategy

- Data Type

- Library Source

- Library Selection

- Description

- Corresponding Email

- Contact Person or PI

- Hold Release Date

## Metadata Standardization in METAGENOTE
The SRA promises great biological insight if metadata can be analyzed in aggregate. However, the metadata submitted to the
SRA remain underutilized because of the poor structure of the data associated with each sample. The SRA generally does not
enforce a standardized set of terms that should be used to describe the biological samples. As a consequence, the metadata
include many synonyms, spelling variants and references to outside sources of information. It has been difficult to perform
large-scale analyses that identify the relationships between molecular processes and phenotype across diverse diseases,
tissues and cell types present in the SRA. A major component of biological metadata is the sample attributes. Sample
attributes define the material under investigation and can include sample characteristics such as cell type, collection site
and phenotypic information like disease state. Since a single sample can be used in multiple experiments and be subjected to
different technologies and treatments, information regarding such methodology aspects generally appears on the experimental
metadata.

Standardized descriptions for metadata, such as <q>Minimum Information about a (Meta)Genome Sequence (MIGS/MIMS/MIMARKS)</q>,
was first developed by the [Genomic Standards Consortium (GSC)](https://press3.mcs.anl.gov/gensc/). The goal of GSC standard
is to promote mechanisms for standardization of description for (meta)genomes, including the exchange and integration of
(meta)genomic data. As an example, attributes that describe human diseases require the
[Human Disease Ontology (DO)](http://www.disease-ontology.org). The DO database includes specific formal semantic rules
to express meaningful disease models. To achieve the standardization of metadata, METAGENOTE offers features such as ontology
search that enable users to describe their samples more precisely with standardized vocabulary. Metadata is validated
according to the guidelines from the Genomics Standard Consortium (GSC), European Bioinformatics Institute (EBI), Earth
Microbiome Project, and NCBI SRA. The following lists the sources and ontologies used in METAGENOTE for sample attributes.

## Source of Ontologies
* [Disease Ontology](http://disease-ontology.org/): The Disease Ontology has been developed as a standardized ontology for
human disease with the purpose of providing the biomedical community with consistent, reusable and sustainable descriptions
of human disease terms, phenotype characteristics and related medical vocabulary disease concepts.
* [BioPortal Metadata Ontology](http://purl.bioontology.org/ontology/BP-METADATA): This ontology represents the structure
that BioPortal uses to represent all of its metadata (ontology details, mappings, notes, reviews, views).
* [Human Disease Ontology](http://purl.bioontology.org/ontology/DOID): The Disease Ontology has been developed as a
standardized ontology for human disease with the purpose of providing the biomedical community with consistent, reusable and
sustainable descriptions of human disease terms, phenotype characteristics and related medical vocabulary disease concepts.
* [Experimental Factor Ontology](http://purl.bioontology.org/ontology/EFO): The Experimental Factor Ontology (EFO) is an
application focused ontology modelling the experimental variables in multiple resources at the EBI and the Centre for
Therapeutic Target Validation.
* [Environment Ontology](http://purl.bioontology.org/ontology/ENVO): The Experimental Factor Ontology (EFO) provides a
systematic description of many experimental variables available in EBI databases. It combines parts of several biological
ontologies, such as UBERON anatomy, ChEBI chemical compounds, and Cell Ontology.
* [Foundational Model of Anatomy](http://purl.bioontology.org/ontology/FMA): The Foundational Model of Anatomy Ontology
(FMA) is concerned with the representation of classes or types and relationships necessary for the symbolic representation
of the phenotypic structure of the human body in a form that is understandable to humans and is also navigable, parseable
and interpretable by machine-based systems.
* [NGS Ontology](http://purl.bioontology.org/ontology/NGSONTO): The NGSOnto ontology aims at capturing the workflow of all
the processes involved in a Next Generation Sequencing, in order to ensure the reproducibility of a controlled and specific
vocabulary.
* [Ontology for Biomedical Investigations](http://purl.bioontology.org/ontology/OBI): The Ontology for Biomedical
Investigations (OBI) is an ontology that provides terms with precisely defined meanings to describe all aspects of how
investigations in the biological and medical domains are conducted.
* [Phenotypic Quality Ontology](http://purl.bioontology.org/ontology/PATO): Phenotypic qualities (properties). This ontology
can be used in conjunction with other ontologies such as GO or anatomical ontologies to refer to phenotypes. Examples of
qualities are red, ectopic, high temperature, fused, small, edematous and arrested.
* [Plant Ontology](http://purl.bioontology.org/ontology/PO): The Plant Ontology is a structured vocabulary and database
resource that links plant anatomy, morphology and growth and development to plant genomics data.
* [Uber Anatomy Ontology](http://purl.bioontology.org/ontology/UBERON): Uberon is an integrated cross-species anatomy
ontology representing a variety of entities classified according to traditional anatomical criteria such as structure,
function and developmental lineage. The ontology includes comprehensive relationships to taxon-specific anatomical
ontologies, allowing integration of functional, phenotype and expression data.
* [Food and Agriculture Organization](http://www.fao.org/soils-portal/soil-survey/soil-classification/universal-soil-classification/en/):
FAO provides soil information and knowledge on the different components and aspects of soils.
* [Country](http://www.insdc.org/country.html): The names of countries or areas refer to their short form used in
day-to-day operations of the United Nations and not necessarily to their official name as used in formal documents.
* [Chemical Entities of Biological Interest](https://www.ebi.ac.uk/chebi/): Chemical Entities of Biological Interest (ChEBI)
is a freely available dictionary of molecular entities focused on small chemical compounds.
* [Omics Observation](https://github.com/GLOMICON/omicon): OMICON is an emerging ontology which links interoperating
semantic solutions for omic observation. This will federate existing ontologies which provide semantics for field sampling,
wet lab work, sequencing, and *in silico* analysis.

## Comments and Suggestions
If you have any comments or suggestions, please [email us](mailto:metagenote@nih.gov).

Bioinformatics and Computational Biosciences Branch (BCBB)<br>
Office of Cyber Infrastructure and Computational Biology (OCICB)<br>
National Institute of Allergy and Infectious Diseases (NIAID)<br>
National Institutes of Health (NIH)<br>
Rockville, MD 20852

*Last updated on January 31, 2020*.
