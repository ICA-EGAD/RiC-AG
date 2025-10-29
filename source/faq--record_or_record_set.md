What is this FAQ about?
----------------------

Sooner or later, having worked with RiC for a while, one will almost certainly find oneself needing to make a judgement as to whether one has a Record or a Record Set. Whilst the situation is rarely black-and-white, our aim here is to provide some guidance upon this question. We shall explore the matter quite thoroughly, as it gets to the heart of several aspects of RiC.

All of the sections of this FAQ, given the subtleties involved and the novelty of the way in which RiC embraces them, are likely most appropriate for an intermediate or advanced user of RiC, or a beginner working towards becoming such a user. The modelling diagrams included along the way are quite rich; aspects of them may be of independent interest.

We [begin](#import-data) with an example of data upon imports to the UK, discussing it from both a Record and a Record Set perspective, as well as reflecting briefly upon the fact that a judgement one way or another might be time-dependent: for instance, what is deemed a Record Set at a certain point in time might later be judged to be a Record in a particular context. We illustrate how Record Part might be brought into this example; discuss how a Record can be regarded as part of another Record and how this might be useful in this example; suggest how multiple Instantiations of the table of import data might arise; and conclude our exploration of this example with a few remarks about the Record Resource entity.

We then [turn](#parish-registers) to a complementary example, of parish registers. Again, we discuss them from both a Record and a Record Set perspective, elaborating more fully than in the import data example on a Records-within-a-Record point of view. We conclude with a discussion of how the distinction between a civil and a church marriage in different countries might be handled in RiC.

[Next](#minute-books) we give a third example, of several kinds of minute books, focusing upon where we might consider the boundary between a Record and a Record Set to be. We first consider minutes which arise from sittings of the House of the Commons in the UK, before turning our attention to the minutes of the council of state in Norway at the time of its invasion in 1940.

Finally, we [return](#databases) to the import data example, but with a different theme: generation of Records via interaction with a database which is regarded as an Instantiation of a Record Set. This section may be of particular interest for its treatment of core elements of modern software — API calls and database queries.

Don't be put off by the subtleties of the exposition we will give! One might think of RiC as providing a language to express the nuanced judgement and experience which you as an archivist or records manager already possess; there is no definitive right or wrong approach. The semantics of RiC are 'open-world': judgements can always be changed, elaborated upon, or clarified further.

Moreover, even though, as we shall explore, the distinction between whether one has a Record Set or Record is regarded as meaningful and significant in RiC, the attributes and relations available for each are not all that different, so that in practice choosing one or the other is unlikely to impose severe constraints — if you do find yourself needing an attribute or relation which is only available for one of them, that may be a good indication as to what you have.

Import data
-----------

### As Record

Each half-year, HM Revenue & Customs in the UK [publishes](http://web.archive.org/web/20251003101852/https://www.uktradeinfo.com/trade-data/latest-bulk-data-sets/#imports-(bds-imp-yymm)) data on goods imported into the UK. The [data](miscellaneous/uk_import_data_july_2025.txt) can be thought of as a table — though a text file in a custom [format](http://web.archive.org/web/20251026122409/https://www.uktradeinfo.com/media/ih3eqsz3/bds_technical_specification.xlsx) is actually used — in which each row corresponds to a single import, with the columns recording the commodity that was imported, the country of despatch, the mode of transport, the port of arrival, the value of the import, and so on.

This table might be viewed either as a Record or as a Record Set. As RiC-CM puts it:

> The most prominent difference in the description of Record Set and Record is that the identity of the Record is directly derived from the Record itself.

If we view the table as documenting the activity as whole of importing goods to the UK, then we might regard it as having this aspect of self-sufficiency, i.e. as being a Record. The rows of the table, i.e. individual imports, would then primarily be viewed via as a contribution to an overall picture: as one import amongst many despatched from a certain country, or with a particular mode of transport, etc. This perspective might fit into a model as follows, where we include the aspect that the half-year records assemble into a sequence — see [int-ref](int-ref:faq--sequences) for more on sequences in RiC — and the distinction between the creation of the table of import data and its publication.

[![Import data as record](../diagrams/import_data_as_record.svg)](../diagrams/import_data_as_record.svg)

### As Record Set

Let us turn to how we might view the table of import data as a Record Set. The key aspect of this is that we would regard each row primarily as documenting an import, i.e. as a Record. The table itself would be seen only as a collection/aggregation of such import documentation; by contrast with when we view it as documenting import activity as a whole, we could have restricted to a subset of the imports, or changed the criteria for aggregation in some other way, without the nature and role of the table being significantly different.

To elaborate a little, individual imports might originate with an online submission to the [Customs Declaration Service](https://www.gov.uk/government/collections/customs-declaration-service) —  in the past, paper forms would have served this purpose. We might model this as follows; the way in which the Mechanism entity is used to express provenance in a software application may be of particular interest.

[![Import as record](../diagrams/import_as_record.svg)](../diagrams/import_as_record.svg)

Once an import has been completed, suppose that the data sent in upon declaration of it, along with data gathered subsequently, is entered as a new row into the table of import data; this row becoming HR Revenue & Customs' primary record of the import. A model of all of this in the end might look as follows.

[![Import data as record set](../diagrams/import_data_as_record_set.svg)](../diagrams/import_data_as_record_set.svg)

As an aside, it is not impossible that both the declaration record and the import record have one and the same Instantiation (see [int-ref](int-ref:faq--the_instantiation_entity)) within HM Revenue & Customs' software — as a row in a database table, or across several tables related by foreign keys, say (see [below](#databases) for more on this). The distinction between the two records at an intellectual level nevertheless allows us to distinguish their different functions and creators, as well as to express other differences in their provenance — that, for instance, a user ID protected by various authentication mechanisms is required to create an import declaration (giving a reasonable degree of assurance as to the identity of its creator).

The difference between viewing the table of import data as a Record Set or as a Record also manifests itself in the degree of significance we attach to the syntactical form/tabular structure of the data. When regarding the table as a Record, the fact that the rows have a common syntax/the same columnar divisons is important; each row is one more contribution to the scope of documentation defined by the overall table structure. Whereas when we see the table as a Record Set, the fact that the rows share a common syntax/structure is of secondary importance; each row could have a different syntax, and indeed include different data, without changing the perspective that what we have is a collection/aggregation of import records.

### Time-dependence

HM Revenue & Customs may not actually create a new table of import data for each half-year period; they might have a single large table with years worth of data, extracted from to create the published half-yearly data. Internally at HM Revenue & Customs, the large table may primarily be viewed as documenting individual imports, i.e. the Record Set perspective may be the default one; but the table of half-yearly data extracted from it may principally be regarded as enabling transparency and insight into import activity during that half-year, i.e. the Record perspective may be dominant.

In particular, the judgement as to whether we have a Record Set or a Record can change in time. This view of context as dynamic is an important aspect of RiC.

The change from a Record Set to a Record perspective following extraction of the half-yearly data might reflect archival/records management realities: HM Revenue & Customs might not regard the table of half-yearly data as needing to archived and managed in the same way as its large table of import data does, but a statistics bureau which analyses the half-year period, or a governmental department which takes the half-yearly data into account in its decision making, might well do.

### Record Part

When we regard the table of import data as a Record, we might find it useful to view each row as a Record Part, enabling us to formulate as follows an analogue of the previous diagram (only part of which we include below).

[![Import as record part](../diagrams/import_as_record_part.svg)](../diagrams/import_as_record_part.svg)

We might make use of Record Part at finer levels of granularity too, corresponding to components of the rows of the table, say with the intention of expressing the content of those components — countries, modes of transport, and so on — in a structured way. This stretches beyond the domain of RiC, but other standards could be brought to bear; this would take us too far afield here, but it is touched upon in [int-ref](int-ref:extended_example--cervantes_and_the_printing_of_don_quixote:broader-cultural-heritage-aspects), and a brief discussion of complementary standards can be found in [int-ref](int-ref:combining_ric_with_other_standards). The following diagram indicates how the the modelling might look as far as RiC goes.

[![Import data record parts](../diagrams/import_data_record_parts.svg)](../diagrams/import_data_record_parts.svg)

Geography frequently has something to say for the provenance of a Record — there are several examples of this in [int-ref](int-ref:extended_example--cervantes_and_the_printing_of_don_quixote), for instance — or other archival/records management matters; designating Costa Rica a Place, as we do in the diagram, opens the door for this. Suppose for instance that HM Revenue & Customs had an agreement to pass on all data on imports from Costa Rica to the Costa Rican embassy in London; we might bring this into our modelling, as follows for instance. The use of _affects or affected_ and _results or resulted in_ is a common pattern; we shall see it again in [int-ref](int-ref:faq--how_to_describe_activities_such_as_digitization_appraisal_or_disposition:digitization), for instance.

[![Use of place with record part](../diagrams/use_of_place_with_record_part.svg)](../diagrams/use_of_place_with_record_part.svg)

A different example of the use of Record Part is discussed in [int-ref](int-ref:faq--general_questions_and_smaller_modelling_questions:my-archival-institution-holds-fragments-of-medieval-documents-how-might-ric-model-this).

### Record within a Record

A Record in RiC can be considered to be part of another Record, and thus it would be possible to adopt both of the perspectives we have discussed at the same time: the table of import data as a whole could be considered as a Record, documenting import activity as a whole in a half-year period, whilst each row too could be considered a Record, documenting a single import. This perspective might be appropriate, for instance, if HM Revenue & Customs does not simply extract the half-yearly data and pass it on to a statistics bureau or governmental department in the manner suggested [above](#time-dependence), but makes use of the table of half-yearly data directly themselves in a context in which import activity as a whole is relevant. We shall discuss another example of this [later](#parish-registers).


### Two instantiations

As we mentioned at the [beginning](#as-record) of our exposition, the half-yearly import data is not actually published in a tabular format as usually understood, but as a text file whose rows have a certain custom format. We might well run a script to parse the text file and create say a spreadsheet from it. In RiC we might regard a single Record as being involved — import data for half a year — having two Instantiations, text file and spreadsheet, the latter derived from the former; the following diagram illustrates this.

[![Two instantiations of import data](../diagrams/import_data_two_instantiations.svg)](../diagrams/import_data_two_instantiations.svg)

A few notes on the diagram:

* We might often think of multiple Instantiations of a Record or Record Set as being inscribed upon different media, but, as this example illustrates, this need not be the case.
* One could further elaborate upon the diagram to detail who carried out the parsing of text file, using _is or was performed by_; when it was carried out, using _occurred at date_; and so on.
* Expressing in a structured way — not only in free-text description — that an Instantiation is a text file or a spreadsheet goes beyond the domain of RiC. As discussed [above](#record-part), it would be appropriate to introduce other standards into the diagram than RiC to this end, for instance one or more of those touched upon in [int-ref](int-ref:combining_ric_with_other_standards).

### Where does Record Resource enter the picture?

The Record Resource entity serves primarily a placeholder for an entity that might be a Record Set, Record, or Record Part. At a meta-level, it is convenient when one wishes to allow a property to allow any of these three entities in its domain or range, and it is frequently used in this way in both RiC-CM and RiC-O. When employing RiC in practice, the Record Resource entity can also be useful when one does not wish to, or is unable to, make a judgement as to which of a Record Set, Record, or Record Part one has. This might be for any number of reasons, not least lack of time and/or resources — for instance when working to migrate legacy metadata to RiC. This has practical consequences, though: for instance, some relations and attributes are only available for specific kinds of Record Resources, even if many are shared.


Parish registers
---------------

### As Record

Let us turn to a different example, of a parish register for Bratsberg church in Norway, specifically to its [documentation of marriages in 1944](https://media.digitalarkivet.no/view/39552/44). We shall further explore the parish registers for this church in [int-ref](int-ref:faq--how_to_describe_activities_such_as_digitization_appraisal_or_disposition:digitization).

From an archival point of view, this register might primarily be viewed as documentation of the church's activity in the period of time it covers: as a Record. The diagram below expresses this.

[![Parish register as record](../diagrams/parish_register_as_record.svg)](../diagrams/parish_register_as_record.svg)

The entries for marriages are made into a pre-defined table. As discussed [above](#as-record-set) (the final paragraph) in the case of regarding a table of import data, this fact that there is a common format for the marriage registrations lends weight to the idea of considering the parish register a Record.

### As Record Set

On the other hand, in 1944, the entry of a marriage into the parish register was likely the primary documentation of it; for somebody concerned with proof that a marriage took place, simply the existence of an entry for that marriage in a parish register might be enough — the format of the entry, or the full details, or what the parish register includes beyond this single entry, might be of little consequence. Just as [for imports](#as-record-set), we might in this context consider a single marriage registration to be a Record, and the parish register to be a Record Set; the following diagram illustrates such a perspective.

[![Parish register as record set](../diagrams/parish_register_as_record_set.svg)](../diagrams/parish_register_as_record_set.svg)

The difference in formulation of the Activity in the two diagrams in this section is intended to highlight that in the first context, the emphasis is upon documentation of Bratsberg church as an entity, regardless of the precise nature of its activity; whereas it is specifically the fact that marriages took place at Bratsberg church that is relevant in the second context.

Even following the introduction of a national register for marriages, an entry into which would today be regarded as the primary documentation of a marriage from the point of view of the Norwegian state, a marriage entry in a parish register could still be viewed as a Record of that marriage — the fact that the marriage took place at a church might be of significance for the bridal pair. In RiC, the judgement of whether one has a Record Set, Record, or Record Part made in any context is a valid as one made in an official administrative setting.

### As Records within a Record

It is intriguing to ponder which point of view might have been primary for the deacon or deacons of Bratsberg church, the records managers of their day, at the time the parish register was created. Perhaps both perspectives equally, in which case a judgement that we have a case of Records within a Record — as discussed [above](#record-within-a-record) — might be natural. We illustrate one way to express this in RiC in the following diagram; note the slight readjustment of the formulation of the Activity once again.

[![Parish register as record containing records](../diagrams/parish_register_as_record_containing_records.svg)](../diagrams/parish_register_as_record_containing_records.svg)

### Further considerations

Today, in some countries, a marriage ceremony in a church will be legally binding; an entry will be made into a national civil register of marriages afterwards, in addition to into a parish register during the ceremony. This is for instance the case in Norway for weddings performed in a state church. One might in this case see the entries into the national and parish registers as two Records deriving from the same Event; we illustrate this below, including the fact that all marriages in Norway after 1970 are required to be entered into the national register.

[![State and parish registers as two records](../diagrams/state_and_parish_registers_as_two_records.svg)](../diagrams/state_and_parish_registers_as_two_records.svg)

As an aside, the use of _has beginning date_ above reflects the fact that the law on entry into a national civil marriage register came into force in 1970, but does not imply that the first Record of either of either of the Record Sets in the diagram necessarily was created in 1970. See the discussion of technical points in [int-ref](int-ref:extended_example--cervantes_and_the_printing_of_don_quixote:records-of-the-council-of-castile-i) for more on this.

In other countries, France for instance, a religious marriage is an entirely separate event from a civil marriage. We might then illustrate the situation as follows instead.

[![Civil and church marriage as two events](../diagrams/civil_and_church_marriage_as_two_events.svg)](../diagrams/civil_and_church_marriage_as_two_events.svg)


Minute books
------------

### Journal of the House of Commons and Hansard

Minute books are, from their inception, more self-consciously archival in nature than parish registers. They can vary widely in particulars:  for a single sitting of the House of Commons in the UK, for instance, two quite dissimilar kinds of minutes are taken. The first, the Journal of the House of Commons, is a recording of the proceedings, formal and concise; the second, Hansard, is a verbatim transcript of the entire sitting (lightly polished and edited according to certain conventions).

As an extreme example of the difference between the two, at the end of the sitting of the 22nd of November 1965, a brief debate was held, [recorded](https://hansard.parliament.uk/Commons/1965-11-22/debates/3121057b-e85f-4a19-9173-011d3ce1561c/SlumClearance%28Manchester%29) in Volume 721 of Hansard, which is historically valuable for its insights into what were termed the slum clearances in Manchester and Liverpool. In the Journal of the House of Commons' [record](http://assets.parliament.uk/Journals/HCJ_volume_221.pdf) of the day, there is not a glimpse of this; only that there was a debate upon the motion "That this House do now adjourn" (a [standard mechanism](https://en.wikipedia.org/wiki/Adjournment_debate)) is recorded.

As an aside, there are subtleties here. Both the Journal of the House of Commons and Hansard are published, so that the distinction between the original manuscripts of each and their published copies — more the domain of libraries — is relevant; whilst both are assembled from raw notes which themselves are of archival importance. One might also quibble over terminology, objecting say to referring to the content of Hansard as minutes. Such matters are not very important for our present discussion, and for simplicity we shall ignore them; we shall treat both the Journal of the House of Commons and Hansard as if they themselves are archival material.

Recall again the following, from RiC-CM:

> The most prominent difference in the description of Record Set and Record is that the identity of the Record is directly derived from the Record itself.

The minutes (of either kind) of a single sitting of the House of Commons would certainly have the requisite aspect of completeness or wholeness to be considered a Record. But sometimes a sitting is adjourned and an item taken up again the following day, so that the minutes flow into another to some extent; the minutes also have a certain degree of structure in their layout that to some extent binds them together. Could then other periods of time than a single sitting also be regarded as delimiting the boundaries of a Record?

Periods of time that the House of Commons itself orients itself around to are candidates. An entire parliament (the period of time that the UK's legislative body is in situ between two elections) for instance, or what are known as sessions of parliament (perhaps a year long).

On the other hand, RiC-CM emphasises that the notions of Record and Instantiation inform one another. Because the actual division into volumes of the Journal of the House of Commons was and is constrained by manuscript size — as well as by the feasibility of indexing for instance — where one volume ends is in practice often somewhat arbitrary. In particular, the volumes are not necessarily divided by session or parliament; the same goes for Hansard.

Moreover, with regard to structure, if we compare to a [parish register](#as-record-1), when entering a marriage into the latter, it is fundamental to know which two people were married; the existence of a column or pair of columns for this purpose is important — before 1812, parish registers in Norway did not have such a  structure, and significantly more context is needed to find and read a marriage entry. Compared to this, the structures reflected in the minutes might be regarded as being of secondary significance, perhaps reflecting the mechanisms of the activity of the House of Commons more than being intrinsic to that activity itself.

Putting all this together, it would seem natural to restrict to regarding a single sitting of the House of Cmmons as giving rise to a Record, and rather regard the volumes of the Journal of the House of Commons and Hansard as Record Sets, that is to say, characterise them primarily as aggregations of minutes. We illustrate how this might be modelled below.

[![House of commons records](../diagrams/house_of_commons.svg)](../diagrams/house_of_commons.svg)

### Invasion of Norway in 1940

The point of view that the Journal of the House of Commons and Hansard are Records Sets whose delineations are shaped to a significant extent by external factors is supported by a different example: a [volume](https://media.digitalarkivet.no/view/153656/1) of minutes from the meetings of the council of state (statsråd) in Norway in 1940. Such minutes are known as a protokoll, distinguished from more informal minutes (a referat) by carrying legal weight and by various matters of form, including the requirement that they be signed in order to be considered authoritative. The council of state was and is responsible for the enacting of law (kongelige resolusjoner — royal decrees) upon authorisation by the king.

The minutes for each meeting are pasted in as they usually would be from January until March, but the volume [ends](https://media.digitalarkivet.no/view/153656/138) suddenly with only informal minutes from the 5th of April 1940. As an archivist's prologue to the latter states:

> The protokoll for the council of states which was held on the 5th of April 1940 was not written up because of the German invasion of Norway on the 9th of April of the same month.

The Norwegian royal family and government fled north and then to England. The council of state continued to be held both on the run and then abroad, but the very different circumstances are reflected in the aggregating of the minutes from these meetings into a new [volume](https://media.digitalarkivet.no/view/39875/6).

The latter begins dramatically with a council of state held on the 9th of April in Hamar whose minutes consists of a single royal decree announcing the temporary movement of the capital of Norway to Hamar. This is followed the day after by a council of state held at Trysil, whose minutes too consists of a single paragraph expressing a famous refusal (known colloquially as "Kongens nei") to capitulate to the invading army.

We illustrate this situation of a compelled 'splitting' into two Record Sets in the following diagram.

[![Norwegian royal decrees](../diagrams/norwegian_royal_decrees.svg)](../diagrams/norwegian_royal_decrees.svg)

Some notes:

1. This is a case where the structured inclusion of locations via the Place entity is very useful, these being a key aspect of the archival context — telling much of the story, indeed. They would be one of the likely means of discovering this material.
2. The invasion of Norway is modelled as an Event rather than an Activity because, within the archival context we have sketched, its performance and purpose are not in scope: it is seen through a historical lens, i.e. passively, simply as something that occurred which had archival consequences. See [int-ref](int-ref:faq--general_questions_and_smaller_modelling_questions:can-you-elaborate-upon-the-difference-between-activity-and-event) for further discussion of this.


Databases
--------

Finally, let us return to our import data [example](#import-data). HM Revenue & Customs' software might actually involve a database with a table of imports within it, the latter having foreign keys pointing to other tables of importers, currencies, modes of transport, and so on. This does not really affect the analysis we carried out earlier; whether an Instantiation of what we referred to earlier as a row of a table in fact in involves several tables via foreign keys makes no significant conceptual difference to the discussion.

That an Instantiation of the import data is a database might be important in other ways, though. A database is dynamic: it can be queried (and updated) programmatically, generating Records — the instantiations of which might be quite different from tabular data. Below we model how the Office of National Statistics in the UK might query the import data in the course of generating its [statistics](https://www.ons.gov.uk/economy/nationalaccounts/balanceofpayments/bulletins/uktrade/july2025) for July 2025.

[![Database](../diagrams/database.svg)](../diagrams/database.svg)

Here 'UK import data' Record Set belongs to what is sometimes known as the 'data layer' of an application; the SQL query and API call belong to the 'business layer' (several such calls might well be involved, but we have included only one for simplicity); and the webpage of statistics for July 2025 to the 'presentation layer'.


A couple of notes on the diagram:

1. We draw particular attention to the distinction between the creation of the statistics for July 2025, namely the Office of National Statistics' calling of an API, and the triggering and execution of business logic within HM Revenue & Customs' software which results from that API call. In particular, HM Revenue & Customs' software is not regarded as creating the statistics Record.
2. The records pertaining to the SQL query and API call are here taken to be the specific ones for the July 2025 data; they might be instantiated as software logs, for instance. They are a form of meta-metadata or 'paradata': rather than simply documenting that the Office of National Statistics made use of HM Revenue & Customs' data, we are documenting how this was done. Further meta-metadata could have been included: the precise timestamp of the API call and SQL query, for instance, by means of the _has creation date_ relation. See [int-ref](int-ref:faq--general_questions_and_smaller_modelling_questions:do-you-have-examples-illustrating-chapter-6-of-ric-cm) for more on interpolating with Activity and Record entities in this way to express meta-metadata/paradata.

    A different kind of meta-metadata would be documentation of the business logic itself, rather than of executions of it: a template of an API call and SQL query, say, without populating the template with specific values (July 2025, etc).
