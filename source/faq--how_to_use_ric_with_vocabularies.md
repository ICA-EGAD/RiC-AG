

## What is this FAQ about?

In this FAQ, we [begin](#vocabularies-as-solutions-to-assigning-values-to-several-ric-cm-attributes) by giving a brief introduction to how vocabularies can be used in combination with RiC-CM-compliant entity descriptions; RiC-CM includes a significant number of attributes that serve as connection points between the two.

We [then](#using-skos-vocabularies-to-populate-classes-in-ric-o-datasets) provide a brief overview of how RDF vocabularies can be used in a RiC-O dataset. Properties (relations) and classes allowing for this are available in RiC-O in greater numbers than in RiC-CM, with possibilities for extension.

We highlight some points of note in both situations.

## Vocabularies as solutions to assigning values to several RiC-CM attributes

RiC-CM 1.0 defines 42 attributes, a quite significant number of which have the value schema 'controlled value'. The table below provides an overview of the specifications of these attributes in RiC-CM (excluding their detailed definition, application notes, and examples).

<table id="LA">
    <tbody>
        <tr class="header">
            <td>Attribute name</td>
            <td>Attribute definition</td>
            <td>Attribute domain (expanded)</td>
            <td>Repeatable</td>
            <td>Extensible</td>
            <td>Note</td>
        </tr>
        <tr>
            <td>Activity Type</td>
            <td>Categorization of an activity</td>
            <td>Activity</td>
            <td/>
            <td>x</td>
            <td/>
        </tr>
        <tr>
            <td>Carrier Type</td>
            <td>Categorization of physical material on which information is represented.</td>
            <td>Instantiation</td>
            <td>x</td>
            <td>x</td>
            <td/>
        </tr>
        <tr>
            <td>Classification</td>
            <td>A term, number or alphanumeric string that is usually taken from an external
                classification vocabulary or scheme that qualifies a record resource.</td>
            <td>Record Resource (thus also Record, Record Part, Record Set)</td>
            <td>x</td>
            <td>x</td>
            <td>May be used in a Record Set description when the attribute value is shared by some
                or all members of the Record Set.</td>
        </tr>
        <tr>
            <td>Content Type</td>
            <td>The fundamental form of communication in which a record resource is expressed.</td>
            <td>Record Resource (thus also Record, Record Part, Record Set)</td>
            <td>x</td>
            <td>x</td>
            <td>May be used in a Record Set description when the attribute value is shared by some
                or all members of the Record Set.</td>
        </tr>
        <tr>
            <td>Corporate Body Type</td>
            <td>Categorization of a corporate body.</td>
            <td>Corporate Body</td>
            <td>x</td>
            <td>x</td>
            <td/>
        </tr>
        <tr>
            <td>Date Qualifier</td>
            <td>A human readable qualification of a date to indicate the level of precision or
                certainty.</td>
            <td>Date</td>
            <td/>
            <td>x</td>
            <td/>
        </tr>
        <tr>
            <td>
                <p>Date Type</p>
           </td>
            <td>Categorization of a date.</td>
            <td>Date</td>
            <td/>
            <td>x</td>
            <td/>
        </tr>
        <tr>
            <td>Demographic Group</td>
            <td>Categorization of a person or group based on shared characteristics</td>
            <td>Group (thus also Corporate Body and Family), Person</td>
            <td>x</td>
            <td>x\*</td>
            <td>\* Needs to be differentiated into specific attributes in order to be useful.</td>
        </tr>
        <tr>
            <td>Documentary Form Type</td>
            <td>Categorization of a record set, record, or record part with respect to its extrinsic
                and intrinsic elements that together communicate its content, administrative and
                documentary context, and authority</td>
            <td>Record Set, Record, Record Part</td>
            <td>x\*</td>
            <td>x</td>
            <td>\* Not repeatable on Record or Record Part, or on Record Set when describing all
                members of the Record Set. Repeatable on Record Set when describing some members of
                the Record Set.</td>
        </tr>
        <tr>
            <td>Event Type</td>
            <td>Categorization of an event.</td>
            <td>Event (thus also Activity)</td>
            <td/>
            <td>x</td>
            <td/>
        </tr>
        <tr>
            <td>Family Type</td>
            <td>Categorization of a family.</td>
            <td>Family</td>
            <td/>
            <td/>
            <td/>
        </tr>
        <tr>
            <td>Language</td>
            <td>A spoken or written human language represented in a record resource or used by an
                agent.</td>
            <td>Agent (thus also Person, Group, Corporate Body, Family, Position, Mechanism);
                Record Resource (thus also Record, Record Part, Record Set)</td>
            <td>x</td>
            <td>x</td>
            <td>May be used in a Record Set description when the attribute value is shared by
                    some or all members of the Record Set.</td>
        </tr>
        <tr>
            <td>
                <p>Legal Status</p>
           </td>
            <td>A status defined by law.</td>
            <td>Agent (thus also Person, Group, Corporate Body, Family, Position, Mechanism);
                Record Resource (thus also Record, Record Part, Record Set)</td>
            <td>x\*</td>
            <td/>
            <td>\* Not repeatable on Record or Record Part, Agent, or on Record Set when describing
                all members of the Record Set. Repeatable on Record Set when describing some members
                of the Record Set.</td>
        </tr>
        <tr>
            <td>Mandate Type</td>
            <td>Categorization of a mandate.</td>
            <td>Mandate</td>
            <td/>
            <td>x</td>
            <td/>
        </tr>
        <tr>
            <td>Occupation Type</td>
            <td>Categorization of a profession, trade, or craft pursued by a person in fulfilment
                of an activity.</td>
            <td>Përson</td>
            <td>x</td>
            <td>x</td>
            <td/>
        </tr>
        <tr>
            <td>Place Type</td>
            <td>Categorization of a place.</td>
            <td>Place</td>
            <td/>
            <td>x</td>
            <td/>
        </tr>
        <tr>
            <td>Production Technique</td>
            <td>The method used in the representation of information on an instantiation.</td>
            <td>Instantiation</td>
            <td>x</td>
            <td>x</td>
            <td/>
        </tr>
        <tr>
            <td>Record Set Type</td>
            <td>A broad categorization of the type of record set.</td>
            <td>Record Set</td>
            <td/>
            <td>x</td>
            <td/>
        </tr>
        <tr>
            <td>Representation Type</td>
            <td>Method of recording the content type of an instantiation</td>
            <td>Instantiation</td>
            <td/>
            <td>x</td>
            <td/>
        </tr>
        <tr>
            <td>Rule Type</td>
            <td>Categorization of a rule</td>
            <td>Rule (thus also Mandate)</td>
            <td/>
            <td>x</td>
            <td/>
        </tr>
        <tr>
            <td>State</td>
            <td>Description of the production or reproduction status of a record resource</td>
            <td>Record Resource (thus also Record, Record Part, Record Set)</td>
            <td>x\*</td>
            <td>x</td>
            <td>\* Not repeatable on Record or Record Part, or on Record Set when describing all
                members of the Record Set. Repeatable on Record Set when describing some members of
                the Record Set.</td>
        </tr>
    </tbody>
</table>


Most of these attributes are used, as their name indicates, to assign a type to the entities described, i.e. categorize them. The other attributes are of a different nature, but all have one thing in common: as section 3.5 of RiC-CM specifies, their value should not be freely chosen, but

> should be selected from controlled lists of authorized (or authoritative) terms.

That is to say, from a controlled vocabulary as defined by the ISO 25964 standard, specifically [ISO 25964-1:2011](https://www.iso.org/standard/53657.html), item 2.12, pg.3:

> Prescribed list of terms, headings or codes, each representing a concept.
>
> Controlled vocabularies are designed for applications in which it is useful to identify each concept with one consistent label, for example when classifying documents, indexing them and/or searching them. Thesauri, subject heading schemes and name authority lists are examples of controlled vocabularies.

Concretely, even if none of our suggestions here are to be regarded as obligatory, it is preferable, when you wish to use attributes to describe an entity, to proceed as follows:

- Identify controlled vocabularies that can be used to assign values to these attributes in your institution, work community, country, or elsewhere. If your institution does not have a vocabulary available, aim for public, well-known, widely-used, and good quality vocabularies.

    If you cannot find an appropriate vocabulary from which to assign values to certain attributes, try to create one. This kind of work is never done in isolation, and takes time, but even if it isn't complete or perfect, if your information system is able to offer you the list of declared values and force you to use only these values, your metadata will always gain in consistency and quality.

- In the appropriate way depending upon the technical architecture of your software and its functionalities, ensure that you record, in the description of an entity, either the name, the identifier, or both of the term in your vocabulary or list which seems most relevant to you.

    Ideally, both a name and an identifier should be recorded. Typically the most important would be the identifier, usually defined to be unique and persistent, as it allows retrieval and access even if the concept changes name or position in your vocabulary. Such identifiers are not mentioned in RiC-CM as they are not of primary importance conceptually, but when you implement RiC-CM and need to define a logical and then physical model for your metadata, they will almost be essential.

Here we are only stating good practices which are already well-established within many institutions, and which are often followed when indexing the description of archival resources within finding aids conforming to ISAD(G); possibly accompanied by descriptions of persons, corporate bodies and families conforming to ISAAR(CPF).

An example is provided by the Society of American Archivists' Encoded Archival Standards: Best Practices Guide. The [EAC-CPF examples page of this guide](https://saa-sdt.github.io/EAS-Best-Practices/docs/examples/eaccpf-examples.html) provides a link to [an XML file](https://raw.githubusercontent.com/SAA-SDT/EAS-Best-Practices/refs/heads/main/_examples/eaccpf-matturbancenter.xml) that describes a corporate body, the Lt. Col. Matt Urban Human Services Center of Western New York, in which the following XML/EAC-CPF code block is to be found:

```
<function valueURI="http://vocab.getty.edu/page/aat/300055433" vocabularySource="aat"
  vocabularySourceURI="https://www.getty.edu/research/tools/vocabularies/aat/">
    <term>community development</term>
    <placeName target="IDPlaceName1">East Side (Buffalo, N.Y.)</placeName>
    <descriptiveNote>
        <p>The organization’s mission is to create programs to improve the
           quality of residential housing and develop projects to improve the
           East Side of Buffalo and Western New York.
        </p>
    </descriptiveNote>
</function>
<places>
    <place>
        <placeName vocabularySource="local" id="IDPlaceName1">
            East Side (Buffalo, N.Y.)
        </placeName>
        <geographicCoordinates coordinateSystem="WGS84">
            N 42°53´48" W 78°50´2"
        </geographicCoordinates>
    </place>
</places>
```

The activity of this corporate body is briefly described, and linked to the activity of [community development](http://vocab.getty.edu/page/aat/300055433) in the [Getty Center's Art and Architecture Thesaurus (AAT)](https://www.getty.edu/research/tools/vocabularies/aat/), the URI of the activity being provided in the valueURI attribute of the `function` element, and that of the thesaurus itself being given by the vocabularySourceURI attribute of `function`. In addition to the HTML view, the AAT thesaurus is available formally in RDF and other formats. As well as the URI, the preferred term 'community development' is encoded in the `term` subelement of `function`. We will return to this example later.

Regardless of the technical architecture and storage formats you work with constructing descriptions, such good practices should ideally be applied to all RiC-CM entities you include, no matter whether Record Resources or contextual entities. This will provide your end users with precise and functional search criteria. If your vocabularies are generic, possibly multilingual, ones in widespread use, federated search across institutions will be possible.

### Some additional observations

RiC-CM is more precise than traditional description standards when it comes to categorizing record resources. In particular, three attributes, Record Set Type, Documentary Form Type, and State, are proposed to categorize these resources, whilst a single vocabulary might well define concepts falling under all three of these categories.

Even though, as discussed in [int-ref](int-ref:faq--record_or_record_set), it is not always easy to decide whether what is being described is a Record Set or a Record, since the conceptual model distinguishes between these two entities, it is logical to distinguish between types of Record Set and types of Record, and therefore between the attributes that allow these types to be specified; thus between Record Set Type and the other two. State refers to the state of production or dissemination of a Record or Record Part, such as 'original' or 'authentic copy', which is quite different from its form — such as 'register' or 'papal bull' — or the type of legal action it sanctions, such as 'sale', 'document of legal proceedings', or 'plan'. These last two are not always easy to distinguish between, and today in RiC-CM they both fall under Documentary Type.

Conversely, the very generic Demographic Group attribute must normally be extended in order to be useful; see [int-ref](int-ref:faq--how_to_extend_ric) for more on this subject. The Occupation Type attribute, being defined as a sub-attribute of Demographic Group, is an extension already integrated into RiC.

It is also possible to use authority lists or classification schemes to fill in attributes other than those listed in the table above. A typical case would for the Name attribute when it is associated with an Agent or Place entity.

Be sure to comply with the specification of the attributes in RiC-CM. In particular, you should only use a given attribute to categorize an entity that is indicated as being in the domain of that attribute; an attribute is by definition a characteristic inherent to an entity.

The attributes Content Type, Documentary Form Type, Language, Legal Status, and State have the special aspect, explained in section 3.4 of RiC-CM, that although a priori attributes of a Record or Record Part, RiC-CM allows them to be used as attributes of any Record Resource; when used to describe a Record Set, this is to be understood to mean that the Record Set includes Records having the specified attribute. Such a possibility can greatly facilitate the migration of ISAD(G)-style archival descriptions to RiC-CM, where sets of records are quite often indexed with several genre or form terms.

If an attribute is specified as non-repeatable, this means that in principle you cannot assign more than one value to this attribute for the same entity. As an example, the repeatable Language attribute can be used to express that a given Record has content in several different languages, but since Documentary Form Type and State are non-repeatable, it is to be assigned a single legal status or state. If there seem to be several possibilities, the narrowest, most precise term should be chosen — in a well-designed, comprehensive vocabulary, there should exist such a choice.

## Using SKOS vocabularies to populate classes in RiC-O datasets


Moving from RiC-CM to RiC-O, each of the attributes in the table apart from Classification for now, but along with Name, is formalised as a class; see the [RiC-O documentation](https://www.ica.org/standards/RiC/RiC-O_1-1.html#fromRiCCM-to-RiCO) for more on this. This enables us to assign a URI, labels and other relevant properties to each of the values used.

There are few slight differences in nomenclature: Production Technique corresponds to [rico:ProductionTechniqueType](https://www.ica.org/standards/RiC/ontology#ProductionTechniqueType), whilst State corresponds to [rico:RecordState](https://www.ica.org/standards/RiC/ontology#RecordState). Reflecting the fact discussed above that Occupation Type is a specialization of Demographic Group, the [rico:OccupationType](https://www.ica.org/standards/RiC/ontology#OccupationType) class is defined as a subclass of [rico:DemographicGroup](https://www.ica.org/standards/RiC/ontology#DemographicGroup). All of these classes coming from RiC-CM attributes, and others, have been grouped under a [rico:Concept](https://www.ica.org/standards/RiC/ontology#Concept) class.

Let's revisit the XML/EAC-CPF code block presented above. To represent this data in accordance with RiC-CM, we would need to distinguish multiple entities more clearly, and link them together, as follows for instance.

[![Categorizing an Activity using RiC-CM](../diagrams/activityType_ric-cm.svg)](../diagrams/activityType_ric-cm.svg)


In this diagram, the activity described by the `function` element of the code block becomes an entity of its own, linked to the Corporate Body in question by the *performs or performed* relation in the manner discussed elsewhere in the Application Guidelines, such as in [int-ref](int-ref:faq--sequences). This Activity has been equipped with an Activity Type attribute, and is also described by a General Description attribute. Finally, it is linked to a Place entity, which has a name (used as a label for the entity in the diagram) and geographical coordinates, the latter recorded using the Coordinates attribute.

If we used RiC-O, we would instead end up with a graph like the following one. We might have modeled the Place entity differently, producing a more detailed description - but that is not the subject that concerns us here.


[![Categorizing an Activity using RiC-O](../diagrams/activityType_ric-o.svg)](../diagrams/activityType_ric-o.svg)


In this RDF graph, the Activity Type attribute has become an instance of the [skos:Concept](http://www.w3.org/2004/02/skos/core#Concept) class: 'Community development' is indeed a concept that categorizes the activity described; and to define this concept, we have chosen to use a data model that the W3C has developed and which is widely used to formalize concepts and vocabularies: [Simple Knowledge Organization System (SKOS)](https://www.w3.org/2004/02/skos/). As with (almost) everything in RDF, the 'Community development' Activity Type implicitly has an URI, and we have equipped it with a label, but SKOS also facilitates assigning other properties to it, though we omit this in the diagram: a definition, scope notes, examples, change notes, relations to broader or narrower concepts, and so on. It is a concept that we could define in a [skos:ConceptScheme](http://www.w3.org/2004/02/skos/core#ConceptScheme) developed by our institution or project, and is declared as equivalent to the concept with the same name in the Getty Center's AAT thesaurus (which is itself expressed in RDF, in accordance with SKOS and an ontology developed by the Getty Center), using the [skos:exactMatch](http://www.w3.org/2004/02/skos/core#exactMatch) relation.

We could alternatively choose not to create and manage the description of this concept ourselves, and instead link the Activity directly to the AAT concept as follows (using Turtle syntax, and supposing that the activity described has

```
https://www.ica.org/standards/RiC/examples#AG_section_06_faq_vocabs_Activity
```

as URI):

```
@prefix rico: <https://www.ica/org/standards/RiC/ontology#> .
@prefix ric-ex: <https://www.ica.org/standards/RiC/examples#> .

<ric-ex:AG_section_06_faq_vocabs_Activity> rico:hasActivityType
    <http://vocab.getty.edu/page/aat/300055433> .
```

Choosing between these two options depends upon our modelling strategy, which may depend upon available human and technical resources; the lists or vocabularies we already have and our plans concerning them; the existence or not of external vocabularies that are truly suited to our needs; and so on. Whatever our decision, the vocabulary we wish to use with RiC-O data should be expressed in RDF; and the [rico:hasActivityType](https://www.ica.org/standards/RiC/ontology#hasActivityType) object property should be used to link the 'Community development' Activity to the concept that categorizes it. An analogous object property, and an inverse for it, exists for all of the attributes which we are discussing here.

If we were to apply a reasoner to the above RDF snippet, it would infer, and add to the existing graph, that the concept with URI `http://vocab.getty.edu/page/aat/300055433` is an instance of the [rico:ActivityType](https://www.ica.org/standards/RiC/ontology#ActivityType) class, because the [rico:hasActivityType](https://www.ica.org/standards/RiC/ontology#hasActivityType) property is formally defined in RiC-O as having as range [rico:ActivityType](https://www.ica.org/standards/RiC/ontology#ActivityType). See [RDFS entailment rules](https://www.w3.org/TR/rdf-mt/#RDFSRules]) for more on this.

On the other hand, it is permitted to explicitly specify that the concepts you use to categorize Activities are both an instance of skos:Concept and of the [rico:ActivityType](https://www.ica.org/standards/RiC/ontology#ActivityType) RiC-O class; the same is true in all analogous cases, and is the approach taken by, for instance, the Archives nationales de France. This makes it possible to immediately have vocabularies and concepts whose formal specification is complete, and which are therefore ready to be used in RiC-O datasets, without having to rely on a reasoner. Later, it may also enable, depending upon time and means, moving beyond terminology, using RiC-O properties to assign say temporal or spatial dimensions to the concepts described; to connect them to Rules when appropriate (decrees, legal texts, policies...); to express that they have successor concepts, and so on; in other words to contextualize concepts. Particularly interesting might be the contextualization of Activity Types, Documentary Form Types, or Corporate Body Types.

If you do not have, or cannot find, any appropriate vocabulary for populating RiC-O classes, the [rico:type](https://www.ica.org/standards/RiC/ontology#type) datatype property to store, as a string, the term you wish to use. If you need to define another category than those in RiC-O today, you can easily extend RiC-O, creating in your own ontology a subclass of [rico:Concept](https://www.ica.org/standards/RiC/ontology#Concept) or [rico:Type](https://www.ica.org/standards/RiC/ontology#Type), and defining the properties you needed to connect the relevant entities to your new concept. See [int-ref](int-ref:faq--how_to_extend_ric) for more on this.

Finally, note that RiC-O defines various 'Type' classes: [rico:ExtentType](https://www.ica.org/standards/RiC/ontology#ExtentType), [rico:IdentifierType](https://www.ica.org/standards/RiC/ontology#IdentifierType), [rico:RoleType](https://www.ica.org/standards/RiC/ontology#RoleType) and [rico:TitleType](https://www.ica.org/standards/RiC/ontology#TitleType). The same considerations as we have brought up apply to these.

### Some additional observations


As explained [above](#some-additional-observations), RiC-CM allows the use of Content Type, Documentary Form Type, Language, Legal Status, and State attributes to categorize a Record Set, even though actually means that all or part of the members of the Record Set have this attribute. RiC-O, as is often the case (see [int-ref](int-ref:faq--general_questions_and_smaller_modelling_questions:what-is-the-relationship-between-ric-o-and-ric-cm), is more precise than RiC-CM in this regard, and defines a larger number of relations (object properties), each having a very specific meaning. For example, the domain of the [rico:hasDocumentaryFormType](https://www.ica.org/standards/RiC/ontology#hasDocumentaryFormType) property is reduced to the union of [rico:Record](https://www.ica.org/standards/RiC/ontology#Record) and [rico:RecordPart](https://www.ica.org/standards/RiC/ontology#RecordPart), so that you cannot use this property with a Record Set. If you want to link a Record Set to a [rico:DocumentaryFormType](https://www.ica.org/standards/RiC/ontology#DocumentaryFormType), you will need to use either the [rico:hasOrHadSomeMembersWithDocumentaryFormType](https://www.ica.org/standards/RiC/ontology#hasOrHadSomeMembersWithDocumentaryFormType) property or the [rico:hasOrHadAllembersWithDocumentaryFormType](https://www.ica.org/standards/RiC/ontology#hasOrHadAllMembersWithDocumentaryFormType) property.

To transform legacy metadata into RiC-O data, to choose the right property, you may in some cases need to comprehensively analyze your data. The presence of several index terms designating document types for the same Record Set will for instance allow you to deduce that the correct property is [rico:hasOrHadSomeMembersWithDocumentaryFormType](https://www.ica.org/standards/RiC/ontology#hasOrHadSomeMembersWithDocumentaryFormType). In the absence of index terms, an analysis of the title of the Record Set, for instance mentions in plural of different document types, might lead you to the same conclusion. If the Record Set described is a series designated by a single plural document type, such as 'Photographs', you can probably deduce that you can use [rico:hasOrHadAllembersWithDocumentaryFormType](https://www.ica.org/standards/RiC/ontology#hasOrHadAllMembersWithDocumentaryFormType).

Note that if you have asserted that all the members of a Record Set have documentary form type 'photograph' for example, you might consider inferring that each Record included in the Record Set has documentary form type ([rico:hasDocumentaryFormType](https://www.ica.org/standards/RiC/ontology#hasDocumentaryFormType)) 'photograph'. Future versions of RiC-O may allow for a greater degree of automation in this regard.


### A more complex use case

RiC-O provides a technical method for dating and, more generally speaking, contextualizing the relation between an entity and the category it may belong to. This is touched upon at the end of [int-ref](int-ref:extended_example--cervantes_and_the_printing_of_don_quixote:records-of-the-council-of-castile-i), but let us give another example.

The Archives nationales de France, which was created in 1790, only received its current status as a 'service à compétence nationale' (service with national competence; a status authorizing them to carry out missions halfway between those of central administration and territorial administration) in December 2006. To model this in RiC-O, we might use the [rico:TypeRelation](https://www.ica.org/standards/RiC/ontology#TypeRelation) in the following way.

[![using a rico:TypeRelation](../diagrams/corporateBodyType_withDate_ric-o.svg)](../diagrams/corporateBodyType_withDate_ric-o.svg)



## Conclusion

Many institutions, consortia, and national projects have developed vocabularies that now make it possible to index, in traditional archival descriptions, the subjects or themes of archival resources and, more broadly, cultural objects. There also are more specialized vocabularies such as those used to indicate what is represented by a visual document. As touched upon in [int-ref](int-ref:faq--general_questions_and_smaller_modelling_questions:is-describing-the-content-of-a-record-within-rics-domain), the concepts defined in these vocabularies can be used to specify the subjects of the records described, using the *has or had subject* or *has or had main subject* relations and their corresponding properties in RiC-O, which also include more specific properties such as [rico:hasContentWhichRepresents](https://www.ica.org/standards/RiC/ontology#hasContentWhichRepresents). More generally, since anything can be the subject of a Record Resource, these relations can target any type of RiC-CM entity. For example, the file of a civil servant, included in a series created by a ministry's Human Resources department, has the civil servant as its main subject.

We have also emphasized in this FAQ that, even if you do not use RiC-O to describe records, only RiC-CM, you can still make use of the many vocabularies or lists published on the web as RDF datasets, after having verified their quality and relevance for your needs, and having ensured that their governance guarantees their long-term maintenance. The notions defined in these RDF vocabularies always have a unique identifier, and they should, as RDF data, remain accessible online. SKOS, as the main technical standard used to structure these vocabularies, and being defined by the W3C, is widely used today and not likely to lose its popularity or become obsolete.

As a final remark, to help improve the quality of archival and records management metadata, increasing the chances of linking RiC metadata sets together, and facilitating federated or large-scale user searches, it is important that the community equips itself with vocabularies capable of covering its own needs, maintained by itself. These may be fairly generic and include terms in several languages. To this end, the EGAD group has so far defined two vocabularies and, within them, created seven concepts in total; see [the section on individuals](https://www.ica.org/standards/RiC/RiC-O_1-1.html#individuals) in the HTML view of RiC-O. If you wish to download these vocabularies as separate files, [the modularized version of RiC-O](https://github.com/ICA-EGAD/RiC-O/tree/master/ontology/current-version/modularized-version) may be convenient.

In its program of work, EGAD plans to construct more vocabularies. In addition to the two already started, which will need to be enriched, it plans to work on vocabularies for Rule Types and Activity Types, to initially cover at least terms of importance in records management and the curation of records.

