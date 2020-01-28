# Synopsis #
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

# Ontology in METAGENOTE #
The NCBI SRA (Sequence Read Archive) promises great biological insight if one could analyze the data in the aggregate. 
However, the metadata submitted to the SRA remain largely underutilized because of the poor structure of the data associated
with each sample. The SRA generally does not define a standardized set of terms that should be used to describe the
biological samples. As a consequence, the metadata include many synonyms, spelling variants and references to outside
sources of information. As a consequence, it has been difficult to perform large-scale analyses that study the relationships
between molecular processes and phenotype across diverse diseases, tissues and cell types present in the SRA. A major
component of biological metadata is the sample attributes. Sample attributes define the material under investigation and can
include sample characteristics such as cell type, collection site and phenotypic information like disease state. Since a
single sample can be used in multiple experiments and be subjected to different technologies and treatments, information
regarding such methodology aspects generally appears on the experimental metadata.

Standardized descriptions for metadata, such as <q>Minimum Information about a (Meta)Genome Sequence (MIGS/MIMS/MIMARKS)</q>,
was first developed by the [Genomic Standards Consortium (GSC)](https://press3.mcs.anl.gov/gensc/). The goal of GSC standard
is to promote mechanisms for standardization of description for (meta)genomes, including the exchange and integration of
(meta)genomic data. As an example, attributes that describe human diseases require the
[Human Disease Ontology (DO)](http://www.disease-ontology.org). The DO database includes specific formal semantic rules
to express meaningful disease models. To achieve the standardization of metadata, METAGENOTE offers features such as ontology
search that enable users to describe their samples more precisely with standardized vocabulary. Metadata is validated
according to the guidelines from the Genomics Standard Consortium (GSC), European Bioinformatics Institute (EBI), Earth
Microbiome Project, and NCBI SRA. The following lists the sources and ontologies used in METAGENOTE for sample attributes.

# Source of Ontologies #
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

# Comments and Suggestions #
If you have any comments or suggestions, please [email us](mailto:metagenote@nih.gov).

Bioinformatics and Computational Biosciences Branch (BCBB)<br>
Office of Cyber Infrastructure and Computational Biology (OCICB)<br>
National Institute of Allergy and Infectious Diseases (NIAID)<br>
National Institutes of Health (NIH)<br>
Rockville, MD 20852

*Last updated on January 31, 2020*.
