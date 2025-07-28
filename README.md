<!-- markdownlint-disable MD033 -->

[![DOI](https://zenodo.org/badge/570454941.svg)](https://zenodo.org/badge/latestdoi/570454941)


# Solid Oxide Fuel Cell Domain Ontology

<!-- [![CI tests](https://github.com/emmo-repo/domain-sofc/workflows/CI%20tests/badge.svg)](https://github.com/emmo-repo/domain-sofc/actions/) -->

The Solid Oxide Fuel Cell (SOFC) Domain Ontology is a specialized domain within the Elementary Multiperspective Materials Ontology [(EMMO)][1], that encompasses essential terms and relationships for systems, materials, methods, and data reletad to solid oxide fuel cells (SOFCs). It is a specialisation ontology of electrochemistry. Its primary objective is to enable the creation of linked and FAIR (Findable, Accessible, Interoperable, and Reusable) data, thereby fostering advancements in research and innovation within the realm of SOFCs. This ontology serves as a foundational resource for harmonizing SOFC knowledge representation, enhancing data interoperability, and accelerating progress in SOFC related research and development.

* IRI: https://w3id.org/emmo/domain/sofc
* Asserted ontology: [sofc.ttl](https://emmo-repo.github.io/domain-sofc/sofc.ttl)
* Inferred ontology: [sofc-inferred.ttl](https://emmo-repo.github.io/domain-sofc/sofc-inferred.ttl)
* [Reference documentation](https://emmo-repo.github.io/domain-sofc/sofc.html)


## Solid Oxide Electrolysis Cell Domain Ontology

A SOFC is a special case of a solid oxide electrochemical cell that utilises a solid oxide material as an electrolyte to facilitate electrochemical reactions to produce electric energy. A Solid Oxide Electrolysis Cell (SOEC) produces a chemical from a electric energy.

The SOEC domain ontology in this repository focuses on hydrogen production.

* IRI: https://w3id.org/emmo/domain/sofc/soec
* Asserted ontology: [soec.ttl](https://emmo-repo.github.io/domain-sofc/soec.ttl)
* Inferred ontology: [soec-inferred.ttl](https://emmo-repo.github.io/domain-sofc/soec-inferred.ttl)
* [Reference documentation](https://emmo-repo.github.io/domain-sofc/soec.html)


## Key Features

- Seamless integration with the EMMO ontology, and the EMMO-based domain ontologies for electrochemistry and batteries.
- Provides persistent machine-readable identifiers for systems, devices, methods, datasets, and quantities for SOFCs.
- Standardized nomenclature for SOFC/SOEC entities.
- Facilitates data exchange and interoperability within the EMMO ecosystem.


### Persistent Identifiers

This ontology assigns persistent machine-readable identifiers to concepts from the electrochemistry domain. These identifiers facilitate data exchange and interoperability among various tools and systems. It includes annotations to other sources of information including [DBPedia](https://www.dbpedia.org/) and [Wikidata](https://www.wikidata.org/).

### Standardized Nomenclature

The ontology builds on standardized nomenclature for solid oxide fuel cells, relying on recognized authorities including the [IEC](https://www.electropedia.org/). IEC is the the world's leading organization that prepares and publishes International Standards for all electrical, electronic and related technologies. This consistency in naming conventions enhances collaboration and data sharing.


## Usage

Researchers, domain experts, and developers within the SOFC communities can utilize the ontology for various purposes, including:

- Incorporating consistent and standardized information into their modeling and simulation activities.
- Enhancing data interoperability between modeling tools, databases, and platforms.
- Supporting research projects that require precise and standardized knowledge representation.
- Building applications, databases, or knowledge graphs that leverage EMMO and require SOFC information.
- Generating linked data in the semantic web.
- Complying with FAIR data mandates (FAIR Guidelines available [here](FAIR.md))


## Structure and Integration with EMMO

The SOFC and SOEC Domain Ontologies are official EMMO domain ontologies.

Their import structure for different versions of SOFC and SOEC are summarised in the following table:

| Version | [EMMO]      | [ECHO]      | [CHEMS]     | [Battery]   |
|---------|-------------|-------------|-------------|-------------|
| 0.0.1   | 1.0.0-beta7 | 0.7.0-alpha | -           | 0.7.2-alpha |
| 0.0.2   | 1.0.0       | 0.30.0-beta | 0.12.2-beta | 0.18.5-beta |

Squashed and inferred versions of the SOFC and SOEC domain ontologies are published on [GitHub Pages](https://emmo-repo.github.io/domain-sofc).


## Getting Started

### Prerequisites

Before you begin, we recommend that you install the following tools. They are not all required, but greatly simplify the process of working with ontologies:

- [Protégé](https://protege.stanford.edu/) (a graphical ontology editor)
  - Installation instructions are available [here](https://protege.stanford.edu/software.php#desktop-protege).

- [EMMOntoPy](https://github.com/emmo-repo/EMMOntoPy) (python package for working with EMMO ontologies)
  - Installation instructions are available [here](https://github.com/emmo-repo/EMMOntoPy#installation).

- [RDFLib](https://rdflib.readthedocs.io/en/stable/) (optional, python package for working with RDF graphs)
  - Installation instructions are available [here](https://rdflib.readthedocs.io/en/stable/gettingstarted.html).

- [VS Studio Code](https://code.visualstudio.com/) (optional, a code editor with extensions for RDF formats like TTL and JSON-LD)
  - Installation instructions are available [here](https://code.visualstudio.com/download).

### Quick Start

To quickly explore and make use of the ontology, first download the pre-inferred version [pre-inferred ontology](inferred_version/sofc-inferred.ttl). You can then simply open the file in Protégé and explore its content or load the ontology into python using EMMOntoPy.

In [EMMOntoPy](https://github.com/emmo-repo/EMMOntoPy), you can choose to import the ontology from your local downloaded copy or directly from the web. Commands for both options are given below:

```python
from ontopy import get_ontology

# Loading from local repository
electrochemistry = get_ontology('/path/to/domain-electrochemistry/sofc-inferred.ttl').load()

# Loading from web
electrochemistry = get_ontology('https://raw.githubusercontent.com/emmo-repo/domain-sofc/master/inferred_version/sofc-inferred.ttl').load()
```

## Contributing

We welcome contributions from the community to enhance and expand the ontology. If you have suggestions, improvements, or additional chemical substance information to contribute, please refer to our [Contribution Guidelines](CONTRIBUTING.md).

### Acknowledgements

<img src="docs/assets/images/flag_of_europe.png" alt="EU-Flag" width="100">

This project has received support from European Union research and innovation programs, under grant agreement numbers:

* Mediate - how to acknowledge?
* 101091687 - [MatCHMaker](http://www.he-matchmaker.eu/)


## License

The SOFC Domain Ontology is released under the [Creative Commons Attribution 4.0 International](https://creativecommons.org/licenses/by/4.0/legalcode) license (CC BY 4.0).



[EMMO]: https://github.com/emmo-repo/EMMO
[ECHO]: https://github.com/emmo-repo/domain-electrochemistry
[CHEMS]: https://github.com/emmo-repo/domain-chemical-substance
[Battery]: https://github.com/emmo-repo/domain-battery
[CHAMEO]: https://github.com/emmo-repo/domain-characterisation-methodology
