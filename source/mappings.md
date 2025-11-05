## What is this part about?

With the release of these Application Guidelines, we make available:

- a crosswalk between the four earlier ICA standards
[ISAD(G)](https://www.ica.org/resource/isadg-general-international-standard-archival-description-second-edition/),
[ISAAR(CPF)](https://www.ica.org/resource/isaar-cpf-international-standard-archival-authority-record-for-corporate-bodies-persons-and-families-2nd-edition/),
[ISDF](https://www.ica.org/resource/isdf-international-standard-for-describing-functions/),
and
[ISDIAH](https://www.ica.org/resource/isdiah-international-standard-for-describing-institutions-with-archival-holdings/),
comprehensively mapping them to RiC-CM. It is in spreadsheet format:
[crosswalk--ica_standards_to_ric-cm.xlsx](mappings/crosswalk--ica_standards_to_ric-cm.xlsx).

- a crosswalk between the EAD 2002 DTD and RiC-O 1.1. Again, it is in spreadsheet format: [crosswalk--EAD2002_to_ric-o-1-1.xlsx](mappings/crosswalk--EAD2002_to_ric-o-1-1.xlsx).

The [first](#how-to-read-the-crosswalk-from-the-ica-standards-to-ric) section of
this part of the Application Guidelines explains the structure of the
spreadsheet, and suggests how to read it. The
[second](#annotations-on-the-crosswalk-from-the-ica-standards-to-ric) section provides annotations on this
crosswalk, elaborating upon particular points, including where there is more
than one possible mapping.

The relation of the four earlier ICA standards to RiC was discussed in broad
terms in
[int-ref](int-ref:combining_ric_with_other_standards:the-ica-standards-ric-replaces).
A detailed example of how the crosswalk might be applied in practice is given in
[int-ref](int-ref:getting_started_with_ric).

The [third](#annotations-on-the-crosswalk-from-EAD-2002-to-RiC-O-1-1) section provides annotations on the crosswalk between EAD 2002 and RiC-O 1.1. We plan to release a mapping from EAC-CPF to RiC-O 1.1 as soon as possible.


## How to read the crosswalk from the ICA standards to RiC

There are four tabs/sheets in the crosswalk spreadsheet, one each for the
mappings of ISAD(G), ISAAR(CPF), ISDF, and ISDIAH to RiC. Within each tab, the
mapping should be read from left to right. The elements of the ICA standards are
furthest to the left. These typically map in RiC to either an attribute of a
certain entities, or to a relation having certain entities as its domain. In all
cases, the entities come next after the ICA standard elements, followed by an
attribute if applicable (left blank if not), and then by a relation if
applicable (left blank if not). Sometimes one maps not only to a relation, but
to an attribute of an entity in the range of the relation; in these cases, the
relevant entities are given in the columns following the relation, and their
attribute given in the columns following these again.

If an element from a former ICA standard maps to multiple possible entities,
attributes, or relations in RiC, the alternatives are listed. Which to use will
depend will upon your specific case in hand.

The mapping reflects the most evident and commonly applicable usages. You
should, though, feel free to map ICA elements to RiC in other ways, where this
makes sense in the setting in which you are example. The ISAD(G) element 3.1.3
*Dates* for instance might certainly be interpreted in different ways.

## Annotations on the crosswalk from the ICA standards to RiC

### ISAD(G) 3.1.4: Level of Description

ISAD(G) does not have equivalents for the RiC-CM entities Record Resource,
Record Part, and RiC-E06 Instantiation. These entities are not therefore
included in the mapping of ISAD(G) element 3.1.4 *Level of Description* to
RiC-CM.

The *file* level of description is typically mapped to Record Set, as a file
often contains multiple documents or consists of several items. However,
depending on the archival traditions and descriptive practices of your country
or cultural context, *file* level may also have been used in such a way that
mapping to Record is more appropriate — particularly in situations where *file*
is the smallest archival unit commonly used.

### ISAD(G) 3.2.3: Archival history

Archival history may be described using free narrative text, and hence the
History attribute in RiC is used in the crosswalk.  However, whenever possible,
activities such as appraisal, destruction, and scheduling should be represented
in a more structured way in RiC, e.g. using the Activity entity in the manner
discussed in [int-ref](int-ref:faq--how_to_describe_activities_such_as_digitization_appraisal_or_disposition).

### ISAD(G) 3.6.1: Note

RiC-CM does not have a direct equivalent to the ISAD(G) element *Note*, being
primarily designed to accommodate all information relevant to archival
description through the entities, attributes, and relations which it defines.
Nevertheless, the attribute General Description serves as a generic text field,
and might be used to record one or more characteristics that are not otherwise
captured by more specific RiC attributes or relations.

### ISDF & ISAAR(CPF) 5.4 and ISDIAH 5.6: Control Area

The *control area* in these three standards is intended for information about an
archival description itself — that is to say, meta-metadata. How to handle this
in RiC is the topic of §6.4 in RiC-CM, and is elaborated upon in
[int-ref](int-ref:faq--general_questions_and_smaller_modelling_questions:do-you-have-examples-illustrating-chapter-6-of-ric-cm).
In short, one might map to a Record holding the meta-metadata, often via the
Activity of describing the Record Resource in question. The attributes and
relations of the mapped-to enable description of an archival description as a
Record Resource in its own right.

## Annotations on the crosswalk from EAD 2002 and RiC-O 1.1.

The crosswalk is not at all a complete specification, that would be ready to use; it is just a generic mapping between the EAD 2002 DTD and [RiC-O 1.1](https://www.ica.org/standards/RiC/ontology), the former currently remaining the most widely-used of the EAD versions. The Tag Library of EAD 2002 DTD can be accessed [here](https://www.loc.gov/ead/tglib); a few EAD elements are still missing from the crosswalk.

The content of the spreadsheet can be discussed or even contradicted, but we hope that it might be useful, at least as far as initiating reflection. It should be modified or refined according to the rules by which EAD is applied within your institution, in your specific project, or in national or supranational recommendations.

EAD 2002 is very flexible, and includes many mixed content elements. Indeed, when EAD is implemented in a given context, most usually a specific, more constraining profile is used. Therefore, a local mapping will probably far exceed what is proposed below.

An example of such a detailed specification for converting EAD 2002 documents to a RiC-O 1.1 dataset is provided by the [documentation](https://archivesnationalesfr.github.io/rico-converter/en/Mappings.html) and [unit tests](https://archivesnationalesfr.github.io/rico-converter/en/UnitTests.html) of the open source software [RiC-O Converter](https://github.com/ArchivesNationalesFR/rico-converter), developed for and with the Archives nationales de France. Its version 3.0.0 enables the production of a consistent RiC-O 1.1 dataset from a collection of more than 30,000 archival finding aids written in EAD 2002, conforming to a more restrictive DTD. We have drawn inspiration from this experience in developing the crosswalk.

The mapping is intended for a human reader. To take full advantage of the provided mapping, you should be familiar with EAD 2002 and RiC-O, understand an XPath expression, and be able to read RDF expressed in Turtle syntax. In the spreadsheet we have used EAD c elements; the same mapping can be provided for numbered c elements (c01, c02, etc.).

Before embarking on a project to convert finding aids to XML/EAD 2002, you should also define a strategy (see [int-ref](int-ref:implementation_strategies:map-your-legacy-data-to-ric) for more) for assigning IRIs to the instances of the RiC-O classes — at least rico:RecordResource and its subclasses, as well as rico:Agent and its sub-classes — you will make use of, and for maintaining these IRIs. If the archdesc and c (or numbered c) elements of your finding aids all have an id attribute, and the values of this attribute are unique and persistent in your information system, this can constitute a good starting point. Having authority records on the agents and/or places mentioned in the finding aids, and controlled vocabularies (see [int-ref](int-ref:faq--how_to_use_ric_with_vocabularies)) whose entries are also mentioned in your finding aids, constitutes a favorable situation.

It may also be important to establish whether the same archival materials are described more than once in your collection of finding aids. If that is the case, you might try to reconcile these descriptions into a single one for the archival resource described, or link them ogether.

Finally, the mapping does not take into account formatting elements present in EAD, such as titlepage, runner, or table. Nor does it mention the audience attribute. If your goal is to publish the RDF dataset you produce as open-access, it's worth checking whether you're using the audience attribute, and in particular making sure you do not take into account, when processing the EAD files, c, numbered c, or scopecontent elements that have an audience attribute with the value 'internal'.

Remember that it is possible to store an XML structure as the value of a RDF datatype property (see [https://www.w3.org/TR/rdf-syntax-grammar/#section-Syntax-XML-literals](https://www.w3.org/TR/rdf-syntax-grammar/#section-Syntax-XML-literals)). This may be very helpful if you wish to convert the text content of EAD elements like bioghist, custodhist or scopecontent, that might include a series of p or list elements. Converting them to a XHTML structure included in a html:div wrapper element, as the RiC-O converter does, is often helpful.

Of course, if you can pre-process the content of your finding aids to improve their quality, and/or produce structures from your text elements, recognizing named entities using AI for example, the result will be much better. But this is not always possible. Even in cases where it is not, it is possible to produce RiC-O compliant RDF from EAD files.
