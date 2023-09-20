# commonX properties
openwemi's `commonX` properties are intended to allow modelers to relate resources described using vocabularies that may
 or may not fit nicely into the FRBR entity model to other resources describing the same creative endeavor. The terms do
 not entail any definition upon the subject or object, it simply establishes a way to denote that they share a common
 work, expression, manifestation, or item and allows connections between datasets that might express the resource for 
 different communities.

Some examples:

To relate the Tom Stoppard work "Rosencrantz & Guildenstern are Dead" between the Wikidata entry, an OCLC WorldCat 
 bibliographic record, the Library of Congress, Open Library, IMDB, and the Internet Archive.

 <http://www.wikidata.org/entity/Q2517513> <openwemi:commonWork> <https://worldcat.org/title/365199> .
 <https://worldcat.org/title/365199> <openwemi:commonManifestation> <https://id.loc.gov/resources/instances/283701> .
 <https://id.loc.gov/resources/instances/283701> <openwemi:commonExpression> <https://www.imdb.com/title/tt0100519/> .
 <https://www.imdb.com/title/tt0100519/> <openwemi:commonExpression> <https://archive.org/details/randg2019> .

Wikidata is a tremendous resource, but its data model and schema would be challenging to fit cleanly into a FRBR model.
  Here it is related by `commonWork` to the WorldCat record. WorldCat is using schema.org via json-ld to represent the 
  original MARC record. It is modeled as a [schema.org Book](https://schema.org/Book) which (like MARC) combines 
  properties from the Work, Expression, and Manifestation into one graph. We then link the WorldCat graph to a Library
  of Congress BIBFRAME Instance. BIBFRAME's model is complex and, while not strictly constrained, does distinguish 
  between resources that would be different FRBR entities. `commonX` allows us to sidestep any semantic contradictions
  between models and ontologies: we can simply declare that the WorldCat schema.org/Book and the Library of Congress 
  BIBFRAME Instance are both describing the same FRBR Manifestation.