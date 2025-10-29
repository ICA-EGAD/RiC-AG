## What is this part about?

As discussed in the introduction to
[RiC-CM](https://www.ica.org/resource/records-in-contexts-conceptual-model/),
Records in Contexts is designed for working intellectually with records and
contexts of records. Its main focus is not upon other aspects of records —
their storage, materiality, or preservation, for instance; upon other types of
cultural heritage material such as books or artworks; or upon detailed
description of people, places, and other entities. Nevertheless, RiC can be
combined with standards for these domains and others. Introducing this topic
will be the focus of the second half of this part of the Application Guidelines.

In addition, RiC relates to other standards for archival description and records
management. We will begin here, touching upon both standards of a more
conceptual nature and technical standards which can complement the structured,
machine-readable descriptions that are possible with RiC-O.

## The ICA standards RiC replaces

As touched upon in the earlier parts of the Application Guidelines, RiC
replaces ISAD(G), ISAAR(CPF), ISDF and ISDIAH, combining and significantly
extending the ability to describe archival resources, actors, functions and
archival institutions that using these earlier standards gave. Though RiC
differs significantly from these standards both concretely and conceptually, it
is backwards compatible with them. In
[int-ref](int-ref:getting_started_with_ric), we explored in detail an example
of moving from a description made in accordance with these earlier standards to
a RiC description. A full crosswalk is presented in
[int-ref](int-ref:mappings). There is not always a unique way to adapt a
description based upon these standards to RiC, but there is always some way to
do it.


## Records management

Records in Contexts is greatly inspired by, and closely related to, the standard
[ISO 23081](https://www.iso.org/standard/73172.html) (Information and
documentation – Records management processes – Metadata for records) for
describing and managing records. The relation between the two is described in
section 1.6.3 of RiC-CM. It states that the difference is that RiC-CM defines
how to capture

> the metadata used to describe, control, and enable access to records of
enduring value that are identified for ongoing preservation by an archival
program

whilst the focus of ISO 23081 is upon

> the metadata that is needed to protect, understand, and enable the usability
of records as evidence from the point of creation by records creators and for
as long as the records need to be retained.

Records in Contexts can be helpful in implementing the ISO 23081 standard. It is
a significant step forward in this respect from ISAD(G) and its accompanying
standards, closing the gap between 'old' and 'new' archives.  The three entities
of people, records and mandates in ISO 23081 are included in RiC, enabling both
archivists and records managers to use the same general framework.

RiC, though, introduces further entities, enabling more precise description of
records than is possible in ISO 23081, in particular additional metadata
concerning the provenance and history of records and their descriptions. The
standardizing committee of ISO 23081 and EGAD intends to iron out the (subtle,
where the two overlap) differences between the two standards in future versions
of them.

## RiC-O versus EAD/EAC-CPF

In RiC, we distinguish between a conceptual model and the way metadata is stored
or disseminated. For the latter purpose, we provide the ontology
[RiC-O](https://www.ica.org/standards/RiC/ontology) to allow for expressing RiC
metadata in [RDF](https://en.wikipedia.org/wiki/Resource_Description_Framework)
triples — we feel this fits the networked, open-ended nature of RiC particularly
well. As discussed in
[int-ref](int-ref:implementation_strategies:introduce-ric-in-your-software),
though, it should also be possible to make use of a relational or NoSQL database
instead.

Over the past few decades, many people have made use of the Encoded Archival
Description (EAD) XML standard for descriptive data, in conjunction with the
Encoded Archival Context for Corporate Bodies, Persons and Families (EAC-CPF)
XML standard. RiC-O serves the purpose of both standards, namely the capturing
of data about Record Resources and Agents respectively.

New versions, EAD4 and EAC-CPF, of the two Encoded Archival Standards are
expected to be released in the summer of 2026, along with a new XML schema,
EAC-F, for functions. They will place greater emphasis upon rich, detailed
descriptions of entities such as record resources, instantiations, agents, and
functions/activities. Relations between these entities will be represented more
comprehensively, both structurally and semantically.

The design and naming of relations in these new versions is inspired by RiC-O,
ensuring conceptual alignment. Looking beyond their release, the plan is to
focus development upon deeper integration and harmonization with related
standards such as RiC, to foster a more consistent and interoperable metadata
ecosystem.

A mapping between RiC and EAD is provided in [int-ref](int-ref:mappings).

The nature of the EAD XML schema is such that if you use it to represent
RiC-CM-based metadata, you may feel a need to duplicate some parts of a
description.  We suggest you try to avoid this as far as possible, or at least
to create links with locally unique identifiers between EAD components
describing the same record resource.

Whatever technology you choose, we recommend that, in line with RiC-CM, you
create separate descriptions for agents, events, activities, rules and places,
pointing to them from your record resource descriptions. This might be by means
of authority records; by using separate tables within a relational database; by
using unique identifiers in EAD/EAC-CPF; or by using Uniform Resource
Identifiers (URIs) in RiC-O.

## Digital preservation

For digital storage in the long-term, specific, mostly technical, metadata is
needed. Attributes and relations to this end are intentionally not provided in
RiC, but are well defined in [PREMIS](https://www.loc.gov/standards/premis/),
which provides a standard for

> metadata to support the preservation of digital objects and ensure their
long-term usability.

Alignment between PREMIS and RiC-CM, and between RiC-O and the PREMIS ontology,
is planned as part of EGAD's future work.

## Specific aspects of context entities

Many record resources relate to persons, places, subject matter, events and the
like. Sometimes your local culture will necessitate specific metadata structures
to sufficiently capture these. In the Netherlands and Germany, for instance, a
family name could consist of a prefix ('von') that must be separable from the
rest of the family name. Addresses might have a particular structure in your
country. RiC is extensible: it should be possible to apply an appropriate
standard for your use case on top of RiC. In particular, controlled
vocabularies, often expressed using [SKOS](https://www.w3.org/2004/02/skos/),
can be used alongside RiC. We refer to
[int-ref](int-ref:faq--how_to_use_ric_with_vocabularies) for more on this.

## Datasets

The concept of a 'dataset' can be useful, whether to refer to the
content of a Record Resource — data collected by an organisation or
for an academic project, say; or to metadata offering access points into a
set of records; or to a selection of metadata describing records themselves
which is organised into a single entity. Depending on the nature of the data and
the context in which they are described, datasets can be considered a Record or
a Record Set. See [int-ref](int-ref:faq--record_or_record_set) for a discussion
of this kind of judgement.

Certain kinds of metadata might be appropriate for datasets, and collections of
them, specifically. Two standards for this are the Data Catalog Vocabulary
([DCAT](https://www.w3.org/TR/vocab-dcat/)) and the Vocabulary of Interlinked
Datasets ([VoID](https://www.w3.org/TR/void/)). They are used to describe the
origin, contexts, accessibility and usability of in this case digital and
structured data. According to its documentation, DCAT

> enables a publisher to describe datasets and data services in a catalog using a
standard model and vocabulary that facilitates the consumption and aggregation
of metadata from multiple catalogs.

Whilst VOID is aimed towards RDF datasets:

> It is an RDF Schema vocabulary that provides terms and patterns for
describing RDF datasets, and is intended as a bridge between the publishers and
users of RDF data.

We suggest to investigate whether these standards might be applicable to your
use case alongside RiC. When viewing a dataset as a Record Resource, RiC can be
used for archival and records management aspects, whilst a dataset standard can
be used for dataset-specific aspects of content, provenance, or aggregation.

## Other kinds of cultural heritage objects

Archives are considered cultural heritage, as are — in some contexts — books,
artworks, archeological findings, site, and built monuments. The concepts of RiC
are approached from the point of view of description of records; other domains
have their own conceptualizations, also of records in some cases, appropriate to
the specificities of their own domains. If you wish to relate your records to
other kinds of cultural heritage material or perspectives, standards exist which
can be used along with RiC. We cannot give a complete overview, but will give
brief descriptions of a few in the following paragraphs.

The library community is organized by the International Federation of Library
Associations (IFLA). They have set up a committee that standardized the [Library
Reference Model](https://repository.ifla.org/handle/20.500.14598/40.2) (LRM), a

> model that covers all aspects of bibliographic data.

Also relevant is the [Resource Description and
Access](https://www.rdatoolkit.org/about) (RDA) standard, a

> package of data elements, guidelines, and instructions for creating library and
cultural heritage resource metadata that are well-formed according to
international models for user-focused linked data applications.

In the museum community, the *Comité International pour la Documentation*
(CIDOC), part of the International Council of Museums (ICOM), has developed the
[Conceptual Reference Model](https://cidoc-crm.org/) (CRM), mostly known as
CIDOC-CRM. It contains

> definitions and a formal structure for describing the implicit and explicit
concepts and relationships used in cultural heritage documentation.

Whilst a careful relating of RiC and CIDOC-CRM remains for the future,
experience suggests that descriptions expressed in RiC can be mapped to
CIDOC-CRM, but with considerable loss of specificity: RiC is a domain standard,
whilst CIDOC-CRM is a general cultural heritage/human knowledge framework at
quite a high level of abstraction. The [Linked Art](https://linked.art/)
community has followed this template, building upon CIDOC-CRM to create a

> shared model ... to describe cultural heritage, with a focus on artwork but
also including archives and bibliographic material.

At the data level, in line with the Linked Data philosophy, RDF enables you to
link, by means of its URI, a description in RiC-O to the description of a
cultural heritage object described in another formalised conceptual model. This
might for instance be useful when an artwork or book is part of an archive, but
needs to be described in an artistic or bibliographic context; or to describe
the content of an artwork or publication held as a Record. It is possible to
combine the classes and properties of RiC-O and those of RDA or CIDOC-CRM to
describe a cultural object as, say, being both a LRM Expression and a RiC
Record.

We give a couple of examples of this kind of interaction in
[int-ref](int-ref:extended_example--cervantes_and_the_printing_of_don_quixote:broader-cultural-heritage-aspects)
and
[int-ref](int-ref:extended_example--cervantes_and_the_printing_of_don_quixote:beyond-the-traditional-archival-context).


## Simplification

In some cases, it might be necessary or useful to provide less complex metadata
than RiC allows for, using a more general standard, such as [Dublin
Core](https://www.dublincore.org/specifications/dublin-core/dcmi-terms/),
[Schema.org](https://schema.org/docs/schemas.html), or the [Europeana Data
Model](https://pro.europeana.eu/page/edm-documentation) (EDM). Mapping between
RiC and these standards has not yet been carried out, but it is possible in
practice, at least in specific cases. Whilst such standards cannot play the role
RiC does, transforming your RiC metadata to them and publishing it as an extra
service might facilitate interoperability.
