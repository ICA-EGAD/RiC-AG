

## What is this FAQ about?

This FAQ offers some food for thought and advice for people who would like to extend RiC — whether RiC-CM or RiC-O. That is to say, to add components to RiC that you need for your descriptions.

## Why extend RiC?

RiC is a generic, international, standard; it might be necessary to extend it to meet local requirements. In addition, RiC-CM is a reference framework, without the level of granularity that might be necessary to, say, precisely describe special collections — sets of medieval charters, postcards, or notarial acts, for instance —  precisely, or to meet the very specific needs of researchers. As the introduction to RiC-CM puts it in 1.2 Purpose and Scope:

> As a high-level model, RiC-CM is a broad conceptual framework. It does not address the full range of activities needed to manage records, nor does it address the full detail that may be required in any possible context in which it may be applied.

RiC-O offers a richer arsenal than RiC-CM; it currently has 107 classes, 75 datatype properties, and 480 object properties, as presented in its [history note](https://www.ica.org/standards/RiC/RiC-O_1-1.html#history-note). Nevertheless, the ontology cannot anticipate all use cases and all current and future needs, though suggestions for additions are always welcome.

Furthermore, RiC is a recent standard. Version 1.0 of RiC-CM and version 1.1 of RiC-O are themselves the result of enhancements to previous versions. Though they constitute a coherent whole, at this stage of its history, RiC is not as complete as one might hope in an ideal world, or as it will be in the future.


## Is your journey necessary?

Developing an extension to RiC involves defining additional entities, attributes, or relations — or, in the case of RiC-O, additional classes or properties — to complete the model. This requires thought, testing, formalization, and time. Once the extension is developed, it must be implemented in practice; in some cases, albeit somewhat unlikely today, there not yet being a profusion of software for RiC, this may involve adapting a pre-existing, RiC-compliant, tool. The extension must then be maintained, and if RiC evolves, you may need to update it accordingly.

Thus, before embarking upon such an initiative, it's a good idea to verify that your extension really is necessary in your institution or for your project!

If RiC-CM doesn't include the additional entity, attribute, or relation you would like, check to see if RiC-O offers it. Here are some examples of RiC-O components that currently don't appear in any form in RiC-CM, and which concern Record Resources or Instantiations:

- the classes [rico:Title](https://www.ica.org/standards/RiC/ontology#Title), [rico:IdentifierType](https://www.ica.org/standards/RiC/ontology#IdentifierType), [rico:TitleType](https://www.ica.org/standards/RiC/ontology#TitleType); the properties [rico:title](https://www.ica.org/standards/RiC/ontology#title), [rico:hasIdentifierType](https://www.ica.org/standards/RiC/ontology#hasIdentifierType), [rico:hasTitleType](https://www.ica.org/standards/RiC/ontology#hasTitleType), and their inverse properties;

- several object properties which are sub-properties of [rico:includesOrIncluded](https://www.ica.org/standards/RiC/ontology#includesOrIncluded), like [rico:included](https://www.ica.org/standards/RiC/ontology#included);

- several object properties which have domain [rico:Date](https://www.ica.org/standards/RiC/ontology#Date), e.g. [rico:isDerivationDateOf](https://www.ica.org/standards/RiC/ontology#isDerivationDateOf),  [rico:isMigrationDateOf](https://www.ica.org/standards/RiC/ontology#isMigrationDateOf), [rico:isAccumulationDateOf](https://www.ica.org/standards/RiC/ontology#isAccumulationDateOf), [rico:isDestructionDateOf](https://www.ica.org/standards/RiC/ontology#isDestructionDateOf), [rico:isPublicationDateOf](https://www.ica.org/standards/RiC/ontology#isPublicationDateOf), and their inverse properties;

- several object properties and datatype useful to represent sequences (see [int-ref](int-ref:faq--sequences) for more on these) and hierarchies of record resources, such as the ones defined as sub-properties of [rico:precedesOrPreceded](https://www.ica.org/standards/RiC/ontology#precedesOrPreceded), and also [rico:wasMergedInto](https://www.ica.org/standards/RiC/RiC-O_1-1.html#wasMergedInto) and [rico:wasSplitInto](https://www.ica.org/standards/RiC/RiC-O_1-1.html#wasSplitInto), as well as the inverse properties of all of these;

- several object properties which are subproperties of [rico:hasOrHadSubject](https://www.ica.org/standards/RiC/ontology#hasOrHadSubject), such as [rico:hasContentWhichRepresents](https://www.ica.org/standards/RiC/ontology#hasContentWhichRepresents);

- the [rico:recordResourceHasSourceOfInformation](https://www.ica.org/standards/RiC/ontology#recordResourceHasSourceOfInformation) object property;

- datatype properties related to the dimensions of things, such as [rico:width](https://www.ica.org/standards/RiC/ontology#width) or [rico:height](https://www.ica.org/standards/RiC/ontology#height).

If you find any of these RiC-O components useful, then when developing an extension for RiC-CM, you can draw inspiration from them and, whenever possible, explicitly establish a correspondence in your extension between components you add and existing components in RiC-O.

Check toothat there are no other models that meet your needs, whose scope would be complementary to that of RiC, and that you could use in combination with RiC. For more on this, see [int-ref](int-ref:combining_ric_with_other_standards) and [int-ref](int-ref:faq--how_to_use_ric_with_vocabularies:skos-vocabularies-to-populate-classes-in-ric-o-datasets).

Here are two examples of existing projects that have combined RiC and other models:

- The [FranceArchives (FA) portal](https://francearchives.gouv.fr/) team has semanticized, in accordance with RiC-O 0.2, all the archival metadata that this portal aggregates; see [this page](https://francearchives.gouv.fr/fr/article/756183859) (in French). Since FranceArchives also manages specific data, such as opening hours and contact details, on French archival institutions that provide finding aids to the portal, the FA team had to find a solution to structuring this data, since RiC-O does not provide properties for this. It was decided to use a few properties defined in [Schema.org](https://schema.org/), including [schema:openingHours](https://schema.org/openingHours) and [schema:telephone](https://schema.org//openingHours), as well as the class [schema:PostalAddress](https://schema.org/PostalAddress). See for example [this description](https://francearchives.gouv.fr/service/33862) of a French territorial archives service, the 'Archives départementales de la Mayenne'.

    Note that this implies that such an archival service, initially defined as an instance of the [rico:CorporateBody](https://www.ica.org/standards/RiC/ontology#CorporateBody) class, also can be considered an instance of the Schema.org [Local Business](https://schema.org/LocalBusiness) or [Civic Structure](https://schema.org/CivicStructure) class, since the union of these two is the domain of [schema:openingHours](https://schema.org/openingHours) and [schema:telephone](https://schema.org//openingHours).

- The [Memobase portal](https://memoriav.ch/fr/memobase), which aggregates data about audiovisual cultural heritage in Switzerland, uses RiC-O 0.2 as its main reference ontology, completed by properties defined by [the RDA registry](https://www.rdaregistry.info/), and by properties defined by [EBUCore](https://tech.ebu.ch/metadata/ebucore), an ontology developed by The European Broadcasting Union, an alliance of public service media. See the [documentation](https://ub-basel.atlassian.net/wiki/spaces/MD/pages/336855177/Memobase+RDF)of the Memobase data model, particularly the list of properties for digital instantiations, such as ebucore:duration or ebucore:mediaResourceDescription.


## Is your need really specific to your project?

If your needs seem to be of quite general interest and might be shared by others, you are very welcome to contact EGAD; we would be happy to discuss them with you. You might contact EGAD in one of the ways indicated below, explaining what you would need; and then EGAD will see if RiC can be enriched so that your need is addressed.

This is how, alongside other processes, RiC-O has evolved over the past few years. Here are two examples, among several others, of developments requested by users, and publicly discussed:

- A [discussion](https://groups.google.com/g/Records_in_Contexts_users/c/yYQFdlDcPBQ) on the RiC users list in August 2024 resulted in the creation of several properties, used to link a [rico:Record](https://www.ica.org/standards/RiC/ontology#Record) or a [rico:RecordPart](https://www.ica.org/standards/RiC/ontology#RecordPart) to a thing it represents or an emotion expressed — see [the pull request](https://github.com/ICA-EGAD/RiC-O/pull/138);

- an issue created on GitHub in November 2024 about adding a property to link a student and the organization at which they studied, resulted in the creation of two properties and one class — see [the issue](https://github.com/ICA-EGAD/RiC-O/issues/125) and the [resulting pull request](https://github.com/ICA-EGAD/RiC-O/pull/129).


Do not hesitate to create issues on GitHub, comment on issues, and make pull requests. EGAD may need time to think about your problems and proposals, make a decision and carry out the necessary work, so it is possible that you will have to extend RiC-CM or RiC-O in the meantime. But taking the step of contacting EGAD might benefit both your organization and the the whole community, either immediately or over time!

## If you decide to develop an extension: a few recommendations

As the additional components you need are not included in RiC, they should be clearly declared as such: create your own list of additional entities, attributes and relations (or classes and properties), in a distinct model (resp. or ontology) which would have its own identifier and name (resp. URI and namespace prefix). Equip each component which you add with its own name and identifier too (resp. its own URI).

Given that you are constructing an extension of RiC, the next step would be to define your new components as sub-entities, sub-attributes, sub-relations, of an entity, an attribute or a relation of RiC-CM (resp. sub-classes or sub-properties of an existing component of RiC-O). It is worth taking the time to ask yourself and reflect upon precisely which existing component in RiC could be this attachment point; the extension must be consistent with the semantics and hierarchies provided by RiC.

Let us consider a very simple example. Suppose you are describing a set of notarial records, including many wills, and that you need to record the relations that exist between these Records and People or Corporate bodies very accurately. In particular, you wish to record that a given person is the testator of a given will, so that later, end users can query the data, asking say: "give me the names of the testators of the wills that are dated within some given date range and/or held by some institution".

Neither RiC-CM nor RiC-O provides a relation or property to record such a fact, or address this specific need, nor is likely to do so soon. For RiC is not a model about wills, nor about the roles of the individuals involved, it is about records in general and their context entities. If you need to express the situation, and if RiC is your main reference model, this is a good reason to extend RiC.

Start by looking amongst the RiC relations for one that you are confident is broader than your 'has testator' relation. There is, for instance, a *has author* relation in RiC-CM, and a corresponding property in RiC-O, [rico:hasAuthor](https://www.ica.org/standards/RiC/ontology#hasAuthor). This relation is defined as follows in RiC-O, and it's just the same in RiC-CM.

> Label(s): a pour responsable intellectuel (fr) | has author (en) | tiene como autor a (es)
>
> Definition: Connects a Record to the Group, Person or Position that is responsible for conceiving and formulating the information contained in the Record.
>
> Scope note: To be used for a Person, Group or Position that makes any contribution to the content of a record. Includes the Person, Group or Position in whose name or by whose command the content may have been formulated and first instantiated (for example the Person who signed the Record).
>
> Has super-properties: rico:hasCreator
>
> Has domain: rico:Record
>
> Has range: rico:Group or rico:Person or rico:Position
>
> Has inverse: rico:isAuthorOf

The definition and scope note here encompass, broadly speaking, 'has testator'. Whether the will was created by the testator's hand then deposited within the records of a notary, or by a third party (for example a notary), its content is defined by the testator and the testator's signature attests to this, i.e. is a kind of authorship.

The 'has testator' relation you want to create could therefore be declared as a sub-relation or sub-property *has author*. It would always have a Person as its source, this being consistent with the domain of *has author* relation, which is a union of Group, Person, and Position. The relation would have a will as its target, which can be considered a kind of Record, and thus everything is fine — there is no logical inconsistency between RiC and your proposal. You've found a good solution!

If you decide to define a conceptual model for your project, you will define the *has testator* relation there, giving it a clear textual definition, maybe a scope note. You would specify that this relation has domain RiC-CM Person, and target RiC-CM Record.

If you decide to define an ontology for your project, named say "An ontology for notarial records held by my institution", you will need to assign a URI to it, e.g. 'http://myinstitution.org/projects/notarialRecords/ontology', as well, possibly, as a preferred namespace prefix, such as 'my-onto'. You would define the *has testator* relation in the ontology, giving it a URI derived from the one for the ontology, say 'http://myinstitution.org/projects/notarialRecords/ontology#hasTestator'), and then, again, a clear textual definition and a scope note. You would specify that this relation has domain rico:Person and range rico:Record. All this might result in the following lines (in Turtle syntax):
```
@prefix owl: <http://www.w3.org/2002/07/owl#> .
@prefix vann: <http://purl.org/vocab/vann/> .
@prefix rdfs: <http://www.w3.org/2000/01/rdf-schema#> .
@prefix dc: <http://purl.org/dc/elements/1.1/> .
@prefix my-onto: <http://myinstitution.org/projects/notarialRecords/ontology#> .


<http://myinstitution.org/projects/notarialRecords/ontology>
  a owl:Ontology ;
# This ontology imports RiC-O 1.1; this is not absolutely necessary to do so when developing an extension, but throughout the development of the extension it may be very helpful.
  owl:imports <https://www.ica.org/standards/RiC/ontology/1.1> ;
  dc:title """An ontology for notarial records in my
            institution"""@en ;
# It's good to declare a license, the contributors, and other metadata about the ontology here; we will skip this.
  vann:preferredNamespacePrefix "my-onto" ;
  vann:preferredNamespaceUri "http://myinstitution.org/projects/notarialRecords/ontology#" .

dc:title
  a owl:AnnotationProperty ;
  rdfs:isDefinedBy <http://purl.org/dc/elements/1.1/> .

vann:preferredNamespacePrefix
  a owl:AnnotationProperty ;
  rdfs:isDefinedBy <http://purl.org/vocab/vann/>.

vann:preferredNamespaceUri
  a owl:AnnotationProperty ;
  rdfs:isDefinedBy <http://purl.org/vocab/vann/>.

<http://myinstitution.org/projects/notarialRecords/ontology#hasTestator>
  a owl:ObjectProperty ;
  rdfs:subPropertyOf <https://www.ica.org/standards/RiC/ontology#hasAuthor> ;
  owl:inverseOf <http://myinstitution.org/projects/notarialRecords/ontology#isTestatorOf> ;
# we will also declare the inverse property below.
  rdfs:domain <https://www.ica.org/standards/RiC/ontology#Person> ;
  rdfs:range <https://www.ica.org/standards/RiC/ontology#Record> ;
  rdfs:isDefinedBy <http://myinstitution.org/projects/notarialRecords/ontology> ;
  rdfs:label "has testator"@en .
# Here it is recommended to add a textual definition of the property, using e.g. rdfs:comment, and if necessary a scope note,
# using e.g. skos:scopeNote; we will skip this.

<http://myinstitution.org/projects/notarialRecords/ontology#isTestatorOf>
  a owl:ObjectProperty ;
  rdfs:subPropertyOf <https://www.ica.org/standards/RiC/ontology#isAuthorOf> ;
  owl:inverseOf <http://myinstitution.org/projects/notarialRecords/ontology#hasTestator> ;
  rdfs:domain <https://www.ica.org/standards/RiC/ontology#Record> ;
  rdfs:range <https://www.ica.org/standards/RiC/ontology#Person> ;
  rdfs:isDefinedBy <https://rdf.archives-nationales.culture.gouv.fr/ontology> ;
  rdfs:label "is testator of"@en .
```


If you use this extension, and thus create triples in your dataset whose predicate is 'my-onto:hasTestator', a reasoner will be able to infer from each such triple one where the 'my-onto:hasTestator' predicate is replaced by [rico:hasAuthor](https://www.ica.org/standards/RiC/ontology#hasAuthor); and that the target of the triple is a [rico:Record](https://www.ica.org/standards/RiC/ontology#Record), its source a [rico:Person](https://www.ica.org/standards/RiC/ontology#Person).

We recommend that you use an OWL 2 ontology editor, it will likely be very useful to you. The open source [Protégé Desktop software](https://protege.stanford.edu/software.php#desktop-protege), for example, can display your extension and the original model extended in the same window (if you have imported the latter), so that you can see where the components are declared in the RiC-O hierarchy. Such tools typically embed reasoners which can check that there is no logical inconsistency in what you have asserted, as well as infer triples.

If you clearly document the extension you have defined, and publish it under a permissive licence along with the data using the components you have added, this will enable others to reuse your data, understanding its semantics. They will also enable the production from your dataset of one which is strictly compliant to RiC-O, i.e. not an extension, since the components you have defined are sub-properties or sub-classes of RiC-O. Portals or aggregators might for instance wish to gather datasets using RiC-O only, not taking into account extensions; or they might also be interested in your extension, and reuse it.

In the end, all of this might influence the development of RiC itself.


## Conclusion

It may be important in the future to maintain a registry of RiC-CM and RiC-O extensions. For now, we invite you to add an entry for your work to the [RiC resource list](https://ica-egad.github.io/RiC-ResourceList/).
