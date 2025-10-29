What is this FAQ about?
-----------------------

As touched upon in [int-ref](int-ref:faq--general_questions_and_smaller_modelling_questions:are-activity-and-event-central-entities-in-ric-how-about-rule-and-place), the Activity entity is important in RiC. It is very flexible: it might be used when describing functional provenance — there are several examples of this in, for instance, [int-ref](int-ref:faq--record_or_record_set) and [int-ref](int-ref:faq--sequences); or for incorporating context which bears upon a Record Resource in less direct ways, as for instance in some of the examples in [int-ref](int-ref:case_study--how_might_ric_be_of_use_to_indigenous_communities_and_other_minority_groups) and [int-ref](int-ref:extended_example--cervantes_and_the_printing_of_don_quixote); or for expressing meta-metadata, as discussed in [int-ref](int-ref:faq--general_questions_and_smaller_modelling_questions:do-you-have-examples-illustrating-chapter-6-of-ric-cm).

Here, though, we will focus upon using Activity to describe archival and records management processes. [First](#digitization) we will discuss digitization, and [then](#appraisal-and-disposition) appraisal and disposition. When it comes to the use of the Activity entity, the same modelling pattern will be used in both cases; it generalizes to many other kinds of processes. Other aspects of the modelling may be of independent interest.

Much of the discussion, especially the core aspect of how the Activity entity is used, is appropriate for a beginner in RiC who has acquired a little experience. Certain aspects are a little more advanced.


Digitization
------------

As we did in [int-ref](int-ref:faq--record_or_record_set:parish-registers), let us consider a parish register for Bratsberg Church between 1938 and 1952. For an example of how it looks, see for instance the [page for deaths in 1939 and 1940](https://media.digitalarkivet.no/view/39552/50).

This parish register was scanned in 2005 by the Regional State Archives in Trondheim, a sub-entity within the National Archives of Norway. We might model this as follows, incorporating some context. At its heart is the way in which the Activity entity and the relations _affects or affected_, _results or resulted in_, _occurred at date_, and _is or was performed by_ are used.

[![Digitization](../diagrams/digitization.svg)](../diagrams/digitization.svg)

Some notes on the modelling:

1. As discussed [int-ref](int-ref:faq--record_or_record_set:parish-registers), we might model the parish register as a Record or a Record Set depending on the context; we have chosen Record here.
2. The Rule brought into the modelling concerning blocking of pages has been applied to all pages to do with births in the digitization, as can be [seen](https://media.digitalarkivet.no/view/39552/6) in the early parts of the parish register.
3. For why digitization is regarded as an Activity pertaining to an Instantiation as oppposed to a Record Resource, see the discussion in [int-ref](int-ref:faq--the_instantiation_entity:do-i-have-an-instantiation-or-a-record-resource): the intellectual aspect of the Record Resource — the information it holds — is essentially unaltered; digitization takes one inscription of that information to another. From a more functional point of view, a digitization may make a Record Resource more widely available — online, or via another electronic channel — or it may contribute to more robust preservation of it; but, in the first instance at least, this again has to do with how concrete inscriptions of the information held in a Record Resource are used, without affecting that information itself.
4. We refer to [int-ref](int-ref:faq--general_questions_and_smaller_modelling_questions:can-you-elaborate-upon-the-difference-between-activity-and-event) for more on why Activity and not Event is used in all three cases in the modelling, including the one-off Activity of the digitization of this particular parish register: the degree of time that an Activity lasts is not so important in this regard, rather...

    > An Activity is an agent designed and performed event that has an intended purpose or purposes.

    ...which applies here.
5. In RiC-O, one has [rico:hasOrHadAnalogueInstantiation](https://www.ica.org/standards/RiC/RiC-O_1-1.html#hasOrHadAnalogueInstantiation) and [rico:hasOrHadDigitalInstantiation](https://www.ica.org/standards/RiC/RiC-O_1-1.html#hasOrHadDigitalInstantiation) available as refinements of [rico:hasOrHadInstantiation](https://www.ica.org/standards/RiC/RiC-O_1-1.html#hasOrHadInstantiation); these would complement nicely the use of the Representation Type attribute in the modelling.
6. Digitization could of course also apply e.g. to audio material; the noting of the Carrier Type and Representation Type of an Instantation as in the modelling, in addition to the inclusion of scanning as a specific form of digitization, allows for deducing which kind of digitization is meant in this case — even by a machine.
7. The 'Digitization' and 'Scanning' Activities serve a slightly different purpose to the 'Scanning' Activity Type in the model. As is discussed in more depth in [int-ref](int-ref:faq--how_to_use_ric_with_vocabularies), a primary purpose of Activity Type and similar attributes in RiC is categorization — this facilitating simple querying, for instance — often making use of a standardized vocabulary. To this end, as in the other cases, Activity Type is defined in RiC-CM to be non-repeatable, with the expectation that the narrowest available categorization is used, as in the diagram.

    The inclusion of the 'Digitization' and the 'Scanning' Activities, on the other hand, permits us to express the nuance that the one is a special case of the other, but more significantly allows us to connect the digitization of the parish register to a much broader context: all kinds of relations and attributes might have their source in either the Digitization or the Scanning Activity.

If the digitized instantiation in this example were, say, in such a format as to allow for annotating, and if it were indeed to be annotated, it might in the end, as per the discussion in [int-ref](int-ref:faq--the_instantiation_entity:when-does-a-derived-instantiation-represent-a-new-record), be judged an Instantiation of a new Record. We might model this as follows.

[![Digitization resulting in new record](../diagrams/digitization--new_record.svg)](../diagrams/digitization--new_record.svg)

On a different note, as it happens, all of the parish registers for Bratsberg Church up to 1961 have been digitized. We could model this as follows, regarding all of these parish registers as aggregating into a Record Set. The only change from the case of a single register is that the Date Entity is now a period of time (one could make use of the Date Type attribute to emphasize this if one wished).

[![Digitization record set](../diagrams/digitization--record_set.svg)](../diagrams/digitization--record_set.svg)

The modelling of the single parish register with which we began fits into the above as follows.

[![Digitization record set including record](../diagrams/digitization--record_set--including_record.svg)](../diagrams/digitization--record_set--including_record.svg)


Appraisal and disposition
-------------------------

We turn to an [example](https://groups.google.com/g/records_in_contexts_users/c/X9KYzx45kZE/m/_Nx6CpsuBQAJ) from the RiC mailing list, discussing appraisal by a records management organization in Flanders of a series which we denote by R. One outcome of the appraisal is the decision to destroy, ten years later (say), a file within the series, which we denote by F. R has an entry in a government register, and the outcomes of the appraisal of R, including the disposition of F, are required by law to be logged in this register.

The register log indicating that F is to be destroyed can be regarded as providing a mandate for that destruction. It so happens in this case that the same records management organization that conducted the appraisal is also likely to carry out the disposition when the time comes. A description in RiC of all of this might look as follows.

[![Appraisal](../diagrams/appraisal.svg)](../diagrams/appraisal.svg)

Some notes on the modelling:

1. The key aspect is the way in which appraisal of R is formulated as an Activity in conjunction with the relations _is or was affected by_, _results or resulted in_, and _performs or performed_, entirely analogously to in the approach to digitization above.
2. We have chosen to model the government register as a Record Set, and the entry for R in the register as a Record. This is because, in the context we are exploring, the emphasis is upon R rather than upon the register as a record of appraisals in Flanders; see [int-ref](int-ref:faq--record_or_record_set) for detailed discussion of this kind of judgement.
3. RiC-O includes the object property [rico:hasDestructionDate](https://www.ica.org/standards/RiC/RiC-O_1-1.html#hasDestructionDate); if one is using RiC-O, this would be a bit more precise than _is date associated with_.
4. There is nothing in RiC that prevents referring to dates in the future, despite the verb tense of some relations. These may be changed in future versions of RiC, with steps towards this having already been taken in the latest version (1.1) of RiC-O.
5. Similarly to in the digitization example, we might have asserted that the Activity 'Appraisal of R' has Activity Type 'Appraisal'; but viewing it as a sub-event of 'Appraisal' as a general Activity is useful here, allowing for a bridge to be built via a Rule to the logging of the outcomes of the appraisal in the government register.
