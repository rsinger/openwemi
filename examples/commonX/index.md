# commonX properties
openwemi's `commonX` properties are intended to allow modelers to relate resources described using vocabularies that may
 or may not fit nicely into the FRBR entity model to other resources describing the same creative endeavor. The terms do
 not entail any definition upon the subject or object, it simply establishes a way to denote that they share a common
 work, expression, manifestation, or item and allows connections between datasets that might express the resource for 
 different communities.

Some examples:

To relate the Tom Stoppard work "Rosencrantz & Guildenstern are Dead" between the Wikidata entry, OCLC WorldCat 
 bibliographic record (in Schema.org), the Library of Congress (BIBFRAME), and IMDB (Schema.org, again).

 <http://www.wikidata.org/entity/Q2517513> <openwemi:commonWork> <https://worldcat.org/title/365199> .
 <https://worldcat.org/title/365199> <openwemi:commonManifestation> <https://id.loc.gov/resources/instances/283701> .
 <https://id.loc.gov/resources/instances/283701> <openwemi:commonExpression> <https://www.imdb.com/title/tt0100519/> .
 <https://www.imdb.com/title/tt0100519/> <openwemi:commonExpression> <https://archive.org/details/randg2019> .