What is this FAQ about?
----------------------

We [begin](#records-in-order) by discussing sequences of records and how they might be modelled in RiC. We explore a simple example, indicating along the way how correspondence might be modelled in RiC. This section is appropriate for a beginner in RiC.

We then [turn](#beyond-sequence-numbers) to a different example, of documentation of activity in a hospital ward. We show how the relational approach to sequences which RiC takes is flexible, allowing for the solving of concrete problems in records management. This section is appropriate for an intermediate to advanced user of RiC. The use of RiC's Activity entity (see [int-ref](int-ref:faq--general_questions_and_smaller_modelling_questions:are-activity-and-event-central-entities-in-ric-how-about-rule-and-place)) to express functional provenance is also illustrated.

The short [third section](#not-only-chains), building upon the same example, discusses the assembly of sequences into patterns other than chains, and how RiC can handle this. It would be appropriate for an intermediate user of RiC, or a curious beginner.

The [final section](#different-points-of-view), again quite short, is a further elaboration upon the same example, delving a little more deeply into what is possible in RiC. It is most appropriate for an advanced user of RiC, or an intermediate user reasonably comfortable with some of [int-ref](int-ref:faq--record_or_record_set).


Records in order
----------------

It frequently happens that records form a sequence, the order of which it is important to preserve. Database migrations, for example, might be stored in a directory of a digital file system, its contents being sorted by file name; one would typically prefix these by a date, or by increasing numbers, to ensure that the order is retained.

```
001--first-migration.sql 002--second-migration.sql 003--third-migration.sql
```

In a finding aid, a sequence of series might correspond to a sequence of paragraphs within a free-text section for description of these series. The paragraphs might be numbered — but neither this numbering or the division of the paragraphs into a sequence are part of the documentary structure of the finding aid.

This mixing of semantics might be regarded as less than ideal: should a name not simply be a name, and a description a description?! We might hope for specific metadata/structure for expressing that we have a sequence.

Let us now focus upon correspondence between a citizen and an official body: an initial inquiry sent by the citizen, a reply by the official body, a response to this reply by the citizen, and so on. The order of the copies of these records kept by the official body might be able to be gleaned from inspection of their contents, or even just from their form: the iterative usage in the subject line of 'Re:', 'Re: Re:', 'Re: Re: Re:' and so on would have been enough in the early days of email, for instance!

So that we do not need to explore these records to ascertain their order, a sequence number might be assigned to each of them. However, for reasons we shall discuss [below](#beyond-sequence-numbers), RiC instead takes the point of view that a sequence is more robustly expressed by relations _between_ records: that one record _precedes or preceded_ another (or, inversely, _follows or followed_ another). In this way, our example might be modelled as follows — the relation _precedes in time_ could have been used in place of _precedes or preceded_.

[![Correspondence sequence](../diagrams/correspondence_sequence.svg)](../diagrams/correspondence_sequence.svg)

RiC goes beyond older standards in its possibilities for modelling correspondence; we might make use of this to incorporate more of the context of the example. The fact that the sequence is defined by replies to correspondence can be expressed using the relation _is reply to_ (or its inverse _has reply_), whilst the _has addressee_ and _has author_ relations and their inverses allow for further precision; this is illustrated below. Such an approach would allow for searching in a precise way for a reply to a given inquiry, or for all replies to a particular person, and so on; dates, and more, could be included to expand the possibilities.

[![Correspondence sequence context](../diagrams/correspondence_sequence_context.svg)](../diagrams/correspondence_sequence_context.svg)


Beyond sequence numbers
-----------------------

Let us turn to a different example. In a hospital ward, at the end of a shift, a nurse typically writes a report on each of their patients. The collection of end-of-shift reports for a particular patient forms a sequence of records; including some context, we might model it in RiC as follows.

[![End-of-shift reports](../diagrams/end-of-shift_reports.svg)](../diagrams/end-of-shift_reports.svg)

During their shift, a nurse might in addition write progress notes for a patient; the progress notes and end-of-shift notes together also form a sequence. If the hospital's records managers wish to keep track of both sequences using sequence numbers, either each end-of-shift report must be equipped with two of them — one for the sequence consisting only end-of-shift reports, and one for the sequence involving both kinds of reports. Alternatively, some workaround is needed, say an indexing syntax which takes the form S1-1, S1-2, S1-3, ... and S2-1, S2-2, S2-3, ... for progress notes written during the nurse's first and second shifts respectively, and S1-R and S2-R for the first and second end-of-shift reports respectively. Either way, this is quite complex, and management of the sequences of records would be a little fragile.

Progress notes for a patient written by doctors might also need to be managed, both as a sequence on their own, and as part of a sequence including the nurses' progress notes and shift reports. Chaos!

By contrast, when expressing sequences in the way RiC does, one can simply add extra _precedes or preceded_ or _precedes in time_ relations to handle all of this, as illustrated in the following diagram. If one is only interested in the patient's progress notes, one can simply ignore the end-of-shift reports and the arrows to and from them, and vice versa.

[![Progress notes and end-of-shift reports](../diagrams/progress_notes_and_end-of-shift_reports.svg)](../diagrams/progress_notes_and_end-of-shift_reports.svg)

In particular, RiC can, without trouble, handle multiple, parallel sequences involving the same record resources. This is a significant departure from older standards, where writing a finding aid would likely necessitate choosing one sequence as primary; another sequence might well involve the creation of a second finding aid for almost the same record resources — this redundancy having costs both for the institution holding the records and its users.

RiC's approach also allows for flexibility in the construction of sequences. It might be, for instance, that the nurses use an app to log their progress notes and end-of-shift reports, but that the end-of-shift reports are not regarded as part of a sequence within the app itself, because they are primarily viewed by the incoming nurse immediately after a change of shift. In other words, the situation might be as follows in the internals of the app, with the end-of-shift reports not related by _precedes or preceded_ or _precedes in time_.

[![Progress notes and isolated end-of-shift reports](../diagrams/progress_notes_and_isolated_end-of-shift_reports.svg)](../diagrams/progress_notes_and_isolated_end-of-shift_reports.svg)

It might be only later that extra _precedes or preceded_ relations are added, say upon discharge of the patient and an archiving of the documentation of their stay, ending up with a diagram akin to the following.

[![Joined progress notes and end-of-shift reports](../diagrams/joined_progress_notes_and_end-of-shift_reports.svg)](../diagrams/joined_progress_notes_and_end-of-shift_reports.svg)

By contrast, if one relies upon sequence numbers, any change in a sequence — an addition or removal somewhere — would necessitate recomputing all sequence numbers after where the change was made. This would be the case even if one's sequence is only a simple chain.

Not only chains
---------------

Sequences of records can assemble into other shapes too; RiC can express these equally well. Suppose, for instance, that in the time between a nurse writing a first progress note and a later one, two different doctors — with different fields of expertises, say — visit a patient, and themselves each write progress notes. We might model this as follows; in different contexts, any or all of the paths through the diamond might be relevant.

[![Diamond of progress notes](../diagrams/diamond_of_progress_notes.svg)](../diagrams/diamond_of_progress_notes.svg)

For a different example, a patient, following discharge, might — in the case of recovery from a heart attack, for instance — continue to visit a hospital periodically for physiotherapy, and separately for clinical follow-up. These two sequences of visits might be modelled as a bifurcation of the chain of documentation created during the patient's hospital stay, as in the following diagram.

[![Bifurcation following discharge](../diagrams/bifurcation_following_discharge.svg)](../diagrams/bifurcation_following_discharge.svg)


Different points of view
------------------------

Thus far we have discussed sequences of records involving a single patient, but per-nurse sequences of records might be equally important to manage. A nurse's end-of-shift report encompasses all of their patients; as discussed in [int-ref](int-ref:faq--record_or_record_set:record-within-a-record), RiC allows a Record to be included in other Records, and we might make use of this to describe how the per-nurse and per-patient sequences interact. The diagram below suggests one way to do it; a sequence of records authored by Nurse 1 lies horizontally in the middle of the diagram, whilst sequences of records for two patients, A and B, lie above and below it.


[![Nurse point of view](../diagrams/nurse_point_of_view.svg)](../diagrams/nurse_point_of_view.svg)
