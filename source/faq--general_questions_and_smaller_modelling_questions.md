What is this part about?
--------------------------

This part of the Application Guidelines has several sub-parts. We begin in [int-ref](int-ref:faq--general_questions_and_smaller_modelling_questions) on this page with some frequently asked questions about RiC in general, before turning to some smaller modelling questions concerning RiC. In the following sub-parts, [int-ref](int-ref:faq--record_or_record_set), [int-ref](int-ref:faq--the_instantiation_entity), [int-ref](int-ref:faq--how_to_describe_activities_such_as_digitization_appraisal_or_disposition), and [int-ref](int-ref:faq--sequences), we discuss further modelling questions in quite some detail. The final two sub-parts give an introduction to using vocabularies with RiC ([int-ref](int-ref:faq--how_to_use_ric_with_vocabularies)) and extending RiC ([int-ref](int-ref:faq--how_to_extend_ric)).

An introduction to concepts in RiC was given in [int-ref](int-ref:getting_started_with_ric); the answers given here are intended to complement this and RiC-CM, offering further guidance. We bring up subtleties and nuances which often arise upon taking RiC into use in earnest. All of the entities in RiC-CM, and a large percentage of the attributes and relations, are covered either on one of the pages of the FAQ or in [int-ref](int-ref:extended_example--cervantes_and_the_printing_of_don_quixote).

We encourage the modelling examples to be explored in a spirit of reflection, to be dipped in and out of: more important than the concrete details is the philosophy of the modelling, how the examples are approached. How might you approach your own examples in a similar way?

If at any point you feel overwhelmed, don't forget that although the aim in some of these FAQs, as well as in [int-ref](int-ref:case_study--how_might_ric_be_of_use_to_indigenous_communities_and_other_minority_groups) and in [int-ref](int-ref:extended_example--cervantes_and_the_printing_of_don_quixote), is to really get to the heart of what RiC can do, RiC fully allows for more traditional methodologies to be translated into it, as discussed in [int-ref](int-ref:getting_started_with_ric) and comprehensively described in [int-ref](int-ref:mappings).


General questions
-----------------

### Is RiC an officially recommended standard?

Yes, the International Council on Archives has officially recommended RiC as a replacement for ISAD(G), ISAAR(CPF), ISDF, and ISDIAH since the release of v1 in 2023. See [int-ref](int-ref:combining_ric_with_other_standards:the-ica-standards-ric-replaces) for a discussion of the relationship between these four standards and RiC.

### What is the relationship between RiC-O and RiC-CM?

[RiC-CM](https://www.ica.org/resource/records-in-contexts-conceptual-model/) is the primary definition of Records in Contexts. It is itself what one might call semi-formal: some further choices are necessary to arrive at something fully formal, for instance something which a machine can understand and which software applications can be built upon. [RiC-O](https://www.ica.org/resource/records-in-contexts-ontology/) is such a formalisation. It is an [ontology](https://www.ica.org/standards/RiC/RiC-O_1-1.html): a formal definition of semantics, in a language, [OWL](https://en.wikipedia.org/wiki/Web_Ontology_Language), made for this purpose.

In addition, whilst formally transposing the entities, relations, and attributes of RiC-CM to OWL classes, object properties, and datatype properties, RiC-O expands RiC by adding more of these, allowing for greater nuance, and the precise expression of aspects of archival and records management practice which have not yet made it into RiC-CM. See the [introduction to RiC-O](https://www.ica.org/standards/RiC/RiC-O_1-1.html#understanding-RiCO) for a detailed overview. New versions of RiC-O are released fairly frequently, driven by the suggestions and requests of users. Innovations in RiC-O will likely be incorporated into future versions of RiC-CM.

One can certainly, though, take RiC into use without RiC-O. On the one hand, RiC-CM can be useful as a tool for an archivist/records manager even without supporting software — stimulating reflection upon internal practices, for instance. On the other, as touched upon in [int-ref](int-ref:implementation_strategies:introduce-ric-in-your-software) and [int-ref](int-ref:combining_ric_with_other_standards:ric-o-versus-eadeac-cpf), other formalisations of RiC-CM than RiC-O should be possible.

### Is it correct to describe RiC as a standard for the description of records?

RiC can definitely be regarded as a standard for the description of records. However, it might be most accurate to say that RiC provides a semantics — semi-formal in the case of RiC-CM, formal in the case of RiC-O —  for archival and records management practice. It is reflecting upon, and seeking to represent the needs and nuances of, this practice that has driven the development of RiC. RiC's semantics might inform and find use in diverse aspects of archival and records management, not only description. In addition, the fact, touched upon in [int-ref](int-ref:implementation_strategies:other-kinds-of-cultural-heritage-objects) and [int-ref](int-ref:faq--record_or_record_set:record-part), that RiC allows for and encourages bridges to other domains   — examples are given in [int-ref](int-ref:extended_example--cervantes_and_the_printing_of_don_quixote:broader-cultural-heritage-aspects) and [int-ref](int-ref:extended_example--cervantes_and_the_printing_of_don_quixote:beyond-the-traditional-archival-context) — may open the door to other kinds of utilization than description as conventionally understood.

### Is RiC intended for records managers as well as archivists?

Yes! RiC is Record-centric, and is intended to provide a semantics for the entire life of a Record. As discussed in [int-ref](int-ref:combining_ric_with_other_standards:records-management), the standard ISO 23081 is the canonical reference for records management, but RiC is much closer to it than earlier standards, and a revision of ISO 23081 is planned which will take RiC into account. By embracing use of RiC's Activity entity, one should be able to model most aspects of records management; see [below](#are-activity-and-event-central-entities-in-ric-how-about-rule-and-place) and [int-ref](int-ref:faq--how_to_describe_activities_such_as_digitization_appraisal_or_disposition) for more on this, and [int-ref](int-ref:faq--sequences) for a particularly relevant part of the Application Guidelines. Specific semantics are available for many aspects of records management, all the more so in RiC-O. EGAD is is open to adding more in future versions of RiC, according to the needs and requests of users.

### Will an analogue of the tool Atom be developed for RiC?

The development of software to support working with RiC is beyond the direct scope of EGAD itself, though we are actively working to support initiatives in this direction. Atom too was developed outside of the committee responsible for ISAD(G) and its companion standards. It takes time for the influence of new standards to be felt, and EGAD has a firm belief that software with comprehensive support for RiC will arrive in due course — some already exists commercially, whilst freely available tools are beginning to be developed. Keep an eye on the RiC [Resource List](https://ica-egad.github.io/RiC-ResourceList/), which is intended, amongst other things, to serve as a hub for developments in this area.

 A technical barrier — not necessarily insurmountable — to simply further developing Atom to support RiC is that natural data formats for RiC, such as RDF, OWL and variants, are not necessarily immediately well-suited to the relational database infrastructure underlying Atom; see [int-ref](int-ref:implementation_strategies:map-your-legacy-data-to-ric) and [int-ref](int-ref:implementation_strategies:introduce-ric-in-your-software) for a little more on this. There are also funding obstacles.

Modern software usually is built around APIs for programmatic handling of data. It is possible that providing such APIs for use with RiC might be more appropriate and fruitful in today's open-source ecosystem than development of a full-scale application akin to Atom. At minimum, though, it will be necessary construct tools for translating data in Atom databases to RiC.


Smaller modelling questions
---------------------------

### Is describing the content of a Record within RiC's domain?

The tasks of archivists and records managers might be said to primarily concern the handling of records — with its many facets — rather than detailed interaction with the contents of those records, this being carried out by users of records. Nevertheless, there is far from a complete divide.

Firstly, modelling content in a structured way enriches the description of a record, placing it into a richer context, this facilitating its discovery; broadening the understanding of its provenance; and opening the door to any number of connections between fields, serendipitous or sought after. RiC-CM includes various attributes and relations to this end, the Scope and content attribute and _has or had subject_ relation, for instance; whilst RiC-O also includes for example [rico:hasContentWhichRepresents](https://www.ica.org/standards/RiC/RiC-O_1-1.html#hasContentWhichRepresents) and [rico:sentimentOrEmotionExpressed](https://www.ica.org/standards/RiC/RiC-O_1-1.html#sentimentOrEmotionExpressed), with further developments likely. In addition, RiC fully allows for other standards to take over at the boundaries of RiC, as we discussed [above](is-it-correct-to-describe-ric-as-a-standard-for-the-description-of-records).

Secondly, certain aspects of a record's content can be of importance for the handling of a record. If, for instance, a record's content is deemed sensitive, offensive, or inappropriate in any other way, one might make use of a Rule to express this as suggested below; the releavant content of the Record is not modelled explicitly, only referred to in free-text, although one could certainly do this using Record Part.

[![Record with sensitive content](../diagrams/record_with_sensitive_content.svg)](../diagrams/record_with_sensitive_content.svg)

As an aside, whilst the History attribute is used in the modelling above for simplicity, one might model this kind of meta-metadata, i.e. the reason something appears in a description, using — as suggested in Chapter 6 of RiC-CM and discussed in more detail [below](do-you-have-examples-illustrating-chapter-6-of-ric-cm) — a Record, the content of which might be along the lines of the History attribute above, but which would in addition facilitate expressing in a structured way who made the judgement of offensiveness, when it was made, and so on.

[![Record with sensitive content, more structured](../diagrams/record_with_sensitive_content_more_structured.svg)](../diagrams/record_with_sensitive_content_more_structured.svg)


### Are Activity and Event central entities in RiC? How about Rule and Place?

In short: yes, they are all regarded as central entities! Earlier standards including entities somewhat akin Activity, such as ISDF, have not been broadly adopted, although activities themselves are implicit all function-based classification schemes, which are widespread. The scope of Activity is much broader in RiC than in these previous standards, though: it may be used to refer to archival practices and processes; it may be used to indicate functional provenance; or it may be used to refer to external happenings of relevance to the archival context. See the introduction to [int-ref](int-ref:faq--how_to_describe_activities_such_as_digitization_appraisal_or_disposition) for links to examples of all of these kinds of usage in the Application Guidelines. In many ways, Activity and Event might be said to be the glue that makes RiC what it is, when it is fully embraced.

This is of course not to say that you cannot express what you want in RiC without Activity or Event; you certainly can! See [int-ref](int-ref:getting_started_with_ric) for a typical example in which Activity or Event are hardly present; migrations from ISAD(G) or other earlier standards along the lines suggested in [int-ref](int-ref:mappings) may well not use Activity or Event to begin with. It is more when the philosophy of RiC has begun to impress itself upon one that Activity or Event will likely enter the stage!

The Rule and Mandate entities, if perhaps not quite as widely applicable as Activity or Event, can also be made use of in all kinds of archival and records management settings, those pertaining to conditions of access for instance. In addition, of course, external laws, regulations, and societal mores frequently are important aspects of the context of a Record Resource. See [int-ref](int-ref:faq--how_to_describe_activities_such_as_digitization_appraisal_or_disposition:appraisal-and-disposition) for an example where the Rule and Mandate entities are fundamental to the context.

The Place entity often plays an important role in binding together aspects of context: see [int-ref](int-ref:record_or_record_set:invasion-of-norway-in-1940) and [int-ref](int-ref:extended_example--cervantes_and_the_printing_of_don_quixote) for example. RiC sees Places as having a dynamic, geopolitical character; their changes through time can be a significant and enlightenting, if non-traditional, perspective from which to approach records.

### Can you elaborate upon the difference between Activity and Event?

In RiC, an Activity is a special case of an Event. As an initial guide, it is quite likely that you have an Activity, and that this should be used. It is easy to be a little tricked by ordinary language, coming to a quick conclusion that something might be more of a one-off event than an activity, but RiC-CM stresses that an Event might very well be a continuous endeavour that lasts a period of time. The key sentence in RiC-CM, in §2.2.4, is that an Activity is:

> an agent-designed and performed event that has an intended purpose or purposes.

Almost any aspect of archival and records management practice — digitization, accrual, appraisal, description, curation, and so on — will likely fall under this.

A typical use of an Event which is not an Activity would be in connection with _is associated with event_, _has or had subject_, or _has or had main subject_, namely relating a Record or Record Set to a certain moment of history, seen in our context as an abstract point of reference, i.e. we disregard its performance and purpose; [Lord Halifax's diaries](https://discover.york.ac.uk/collections/halifax-diaries/?m=2&cv=42) might be said relate to the Event of the Second World War, without being regarded as documenting it as such — an Activity which they document is Lord Halifax's carrying out of his governmental and private duties. Such Events are very useful for placing a Record Resource in a rich thematic context, facilitating for instance their discovery. Further examples of the Event vs Activity distinction are given in [int-ref](int-ref:case_study--how_might_ric_be_of_use_to_indigenous_communities_and_other_minority_groups:incorporating-map-data-into-a-sámi-context) and [int-ref](int-ref:faq--record_or_record_set:minute-books).


### Do you have examples illustrating Chapter 6 of RiC-CM?

The focus of Chapter 6 in RiC-CM is upon meta-metadata, the principal theme being that RiC has a certain self-reflexivity: it can be used to speak about itself — to elaborate upon modelling choices in a structured way. To achieve this, one approach, where a single relation or attribute has been chosen, might be to interpolate with Activity, Event, and Record entities and relations. An example of this approach is given above [int-ref](int-ref:faq--general_questions_and_smaller_modelling_questions:is-describing-the-content-of-a-record-within-rics-domain); see also [int-ref](int-ref:faq--record_or_record_set:databases).

One also has the attributes of relations in §5.5 of RiC-CM, implemented as sub-classes of the [rico:Relation](https://www.ica.org/standards/RiC/RiC-O_1-1.html#Relation) class in RiC-O. Although it may at first seem a distinct mechanism, use of these attributes is in fact very similar to the interpolation approach, albeit that the latter is more general, and typically more flexible. In future, the two techniques may be formally unified.

Recording of meta-metadata is important in settings where artifical intelligence is used; it is sometimes referred to as paradata in this context. The diagram below indicates how this might be modelled in the case of transcription of handwritten parish register using AI. Instead of the single _has or had derived instantiation_ relation, a number of Activity and other entities are involved. More could of course be included. Standards developed specifically for the purpose might be used to form the content of the Records documenting the two Activities in the modelling.

[![Transcription using artificial intelligence](../diagrams/artificial_intelligence_transcription.svg)](../diagrams/artifical_intelligence_transcription.svg)

As a second example, a generative AI chatbot might be used to create an overview of the contents of a Record, to be used as part of a description of that Record. This might be modelled as follows, the prompt given to the chatbot being an important piece of meta-metadata/paradata in such cases. Again, more could be included.

[![Archival description using generative chatbot](../diagrams/generative_chatbot.svg)](../diagrams/generative_chatbot.svg)


### My archival institution holds fragments of medieval documents, how might RiC model this?

An example are fragments at the Norwegian National Archives of a manuscript containing [Frostatingsloven](https://en.wikipedia.org/wiki/Frostating_Law), pictured [here](https://www.arkivverket.no/utforsk-arkivene/skole/historiske-kilder/middelalder-i-norge/frostatingsloven). In RiC, a Record (RiC-E04) is not required to have an extant Instantiation (RiC-E06), only to have once had one. Thus each fragment can be modelled as a Record Part (RiC-E05) with a still-extant Instantiation, components of a now-lost Instantiation of a Record.

A somewhat tricky aspect is how exactly to define this Record: what does it document? Why are the fragments held in an archival institution? There exist discussions of these matters in the literature, which it would take us too far afield to enter into; as ever, the context in which one approaches the questions is crucial. For simplicity, let us regard the original manuscript as a Record of propagation of Frostatingsloven in the 1300s.

There do exist (complete) transcriptions of Frostatingsloven from the 1600s. We include one of these in the modelling too, viewing it as an Instantiation of a copy of the Record in question; given that we taking the Record to be documenting the propagating of Frostatingsloven, rather than Frostatingsloven itself as an abstract, non-written conception, it would not be correct to regard it as an Instantiation of the original Record itself — as discussed in [int-ref](int-ref:faq--the_instantiation_entity:when-does-a-derived-instantiation-represent-a-new-record), one might regard it as representing a Record in its own right, but we omit to take this into consideration here.

[![Frostatingsloven](../diagrams/frostatingsloven.svg)](../diagrams/frostatingsloven.svg)



