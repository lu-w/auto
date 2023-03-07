# The Automotive Urban Traffic Ontology

This is the Automotive Urban Traffic Ontology (A.U.T.O.). 
It describes phenomena and artifacts of the traffic world that relevant for the verification and validation of automated driving systems in urban contexts. 
The goal is to build a formal, digital model of urban traffic that includes safety-relevant entities and categories, their properties and important relations between them.

## Structural overview

### Traffic Entity (`traffic_entity`)

Artefacts semantically mainly belonging to the urban traffic domain (e.g. cars, pedestrians) are categorized into the traffic entity. 
This taxonomy builds on the [work of Scholtes et al.](https://ieeexplore.ieee.org/document/9400833/) by using the 6-Layer Model for a traffic entity description. 

### Traffic Related (`traffic_related`)

The broad spectrum of urban road traffic covers many concepts that are related to traffic, but not a primary part of it (i.e. not categorizable in the 6-Layer Model): the so-called traffic related concepts. 
They include (but are not limited to) perception, communication, policies, physics, and temporal aspects. 
These concepts, which naturally interact with traffic, are used within the formalized 6-Layer Model.

### A.U.T.O.

On the top level, we define three ontologies:

- `automotive_urban_traffic_ontology.owl`: imports all ontologies mentioned above into a coherent, single ontology.
- `criticality_phenomena.owl`: contains the 'vocabulary' of criticality phenomena and an initial, expert-based set of inter-relations between them (such as the subsumption relation)
- `criticality_phenomena_formalization.owl`: adds DL axioms and SWRL rules for the definition of criticality phenomena that in turn are based on the semantics of A.U.T.O.
