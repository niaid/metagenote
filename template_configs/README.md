# Template Configuration Files



METAGENOTE uses Excel configuration files to compile BioSample attribute definitions used by users in the sample group editor. This allows flexible and reusable attribute characterizations. Each attribute configuration file corresponds to a parent package.



## Packages

| Package                   | Configuration File     |
| ------------------------- | ---------------------- |
| Survey                    | survey.attributes.xlsx |
| Metagenomes               | mims.attributes.xlsx   |
| Specimen                  | specimen.xlsx          |
| Bacteria/Archaea Genome   | ba.attributes.xlsx     |
| Assembled Genome          | mimag.genome.xlsx      |
| Amplified Genome          | misag.genome.xlsx      |
| Viral Genome              | vi.attributes.xlsx     |
| Uncultivated viral genome | miuvig.genome.xlsx     |
| Model Organism            | model.xlsx             |
| Eukaryote                 | eu.attributes.xlsx     |
| Human                     | human.xlsx             |



## Content



### Attributes

A listing of all BioSample attributes with definitions, input format, and appropriate ontology source when applicable.

### Anatomy

Defines anatomy tool resources to use if appropriate.

### Use

Specifies attributes for each specific package and usage, e.g. required.

| Code | Description                                                  |
| ---- | ------------------------------------------------------------ |
| 0    | Not applicable                                               |
| 1    | Optional                                                     |
| 2    | Recommended                                                  |
| 3    | At least one attribute from a group is required to have a user value |
| 102  | Attribute is hidden from users; usually set to a constant value that should not be modifiable by users |

### Terms

Sets the choices displayed as drop-downs in the sample group editor

### Defaults

If appropriate, sets a default value for an attribute

### Packages

Package descriptions

### Vocabulary

Cross package attribute definitions

