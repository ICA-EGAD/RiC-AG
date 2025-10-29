What is this FAQ about?
-----------------------

The introduction of the Instantiation entity, and the distinction between an Instantiation and a Record Resource, is one of the novelties of RiC. We [begin](#do-i-have-an-instantiation-or-a-record-resource) by offering some guidance, including several simple examples, upon how to tell whether one is describing an Instantiation or a Record Resource. This section is appropriate for a beginner in RiC.

An important aspect of the Record Resource versus Instantiation distinction in RiC is that the same Record Resource might have multiple Instantiations, often derived from one another. It can happen that, eventually at least, we regard an Instantiation as representing a new Record. The [second](#when-does-a-derived-instantiation-represent-a-new-record) section discusses this; it is appropriate for an intermediate to advanced user of RiC.

In the [final](#instantiations-of-record-sets) section, we discuss the fact that a Record Set need not have an Instantiation, taking the documentary heritage of Charles Darwin as an example. This section would be appropriate for a beginner to intermediate user of RiC.


Do I have an Instantiation or a Record Resource?
-----------------------------------------------

As soon as archivists began to make use of reproduction techniques like photographing, microfilming and scanning, the same Record Resource could be accessed through different materialisations. This is very convenient for users of an archive, but results in an extra need to keep track of the relations between the 'original' and its reproductions. Furthermore, in a digital archive the same report could be stored in various ways, 'locations', and formats.

To capture the relations between these various materialisations/representations, RiC-CM introduced the concept of Instantiation. One Record Resource could have multiple Instantiations, but a Record or Record Part must have at least one (a Record Set need not; we shall return to this point [below](#instantiations-of-record-sets)). An Instantiation does not exist without a Record Resource. The Record Resource is the (abstract) thing that is materialised into a (concrete) Instantiation. This compares to how libraries in the latest standard model publications: a book is a (concrete) Item which is only one of a big heap of printed things capturing a certain (abstract) Work.

Knowing whether you are describing a Record Resource or an Instantiation might be answered with the question: is the archival metadata you want to capture about the concrete, physical thing, or does it describe an aspect that is independent of the way it is materialised? In the first case you're describing an Instantiation, in the second a Record Resource.

_Do you want to capture archival metadata that says that the text on a piece of paper is written by the Queen?_ Record Resource. If you scan the piece of paper, both the text on the paper and the scan are written by the Queen. This metadata is independent of whether we describe the piece of paper or the scan.

_Do you want to capture archival metadata that says that the thing is printed on paper?_ Instantiation.  "Made of paper" is a property of the physical thing. Scanning the thing results in a new, second Instantiation of the same Record Resource.

_Do you want to capture what resolution was used to scan a piece of paper?_ Instantiation. If you were to scan the same Record a second time with a different resolution (and thus create a further Instantiation), you would store the different resolutions with the different Instantiations: the resolution is a property of the physical representation that you are describing.

_Do you want to capture archival metadata about the administrative process (Activity) that produced the Record?_ Record Resource. Whether you find a printed copy or the original Word version of a Record in the (hybrid) Record Set you are describing, they are both the result of the same administrative process: the metadata is independent of whether the record is the printed variant of the Word file or not.

When does a derived Instantiation represent a new Record?
----------------------------------------------------------

As RiC-CM puts it in the Scope Notes for the Instantiation entity:

> Depending on the context, a new instantiation may represent a new record resource or the same record resource.

An example is given there, to which we refer the reader. For another, consider the case that we have a Record whose original Instantiation is a digital file. Suppose that this file is duplicated; the duplicate might  initially simply be regarded as representing the same Record. But it might be used by a researcher as source material, so that the duplicate can be regarded as (an Instantiation of) a Record of that researcher's endeavours. Or, for instance, it might be used within a criminal investigation, and become regarded as (an Instantiation of) a Record of that investigation. We illustrate this possibility in the diagram below.

[![Duplicate representing a new record](../diagrams/duplicate_representing_a_new_record.svg)](../diagrams/duplicate_representing_a_new_record.svg)

A rule of thumb might be that if an Instantiation is derived from another with the intention of being used for the same purpose, but has other properties (inscribed upon a different medium, or easier to read, say), and this derivation is a largely mechanistic process without intellect significantly being brought to bear, then the derived Instantiation might not be thought of as representing more than the original Record. For instance, a scanning of a Record which is an analogue photograph to an image file might simply be regarded as a new Instantiation of the original Record. Whereas if the photograph is digitized to a file format such as TIFF which allows making annotations, and this functionality is made use of, we might consider that it represents a new Record; see towards the end of [int-ref](int-ref:faq--how_to_describe_activities_such_as_digitization_appraisal_or_disposition:digitization) for an example of this, including a diagram which we now reproduce.

[![Digitization resulting in new record](../diagrams/digitization--new_record.svg)](../diagrams/digitization--new_record.svg)

This example illustrates that whether an Instantiation is regarded as representing a new Record may be time-dependent: until it is annotated, the TIFF file might be regarded only as representing the original Record, but once annotations are made and the file acquires a history of its own, we might then regard it as representing a new Record. See [int-ref](int-ref:faq--record_or_record_set:time-dependence) for more on sensitivity to time in RiC, this being an important aspect.

Transcription or translation, whether by human or artifical intelligence, is an in-between case. Aspects such as who or what carried it out, the kind of training or experience they or it received, when it took place, and assessments of accuracy, might be modelled as meta-metadata/paradata Records arising out of, and documenting, the transcription or translation activity itself, not having a direct bearing upon the question of whether we have a representation of a new Record. See [int-ref](int-ref:faq--general_questions_and_smaller_modelling_questions:do-you-have-examples-illustrating-chapter-6-of-ric-cm) for example.

But there are other cases, such as when the transcription or translation has semantic markup, e.g. is in [TEI format](https://en.wikipedia.org/wiki/Text_Encoding_Initiative), or, again, when the output is annotated with comments, where we might consider that this represents a new Record. In line with much of the discussion of [int-ref](int-ref:faq--record_or_record_set), we might also choose to regard a transcription or translation as a new Record when, for instance, we wish to emphasize the transcriber or translator's role: this might be in the context of consideration of the transcriber or translator's work more generally; or in a context in which the possibility of bias is a particularly sensitive one; or one of several other possibilities.

Instantiations of Record Sets
-----------------------------

It may be very useful to bring an Instantiation of a Record Set into one's descriptive context. A photo collection might, for instance, be instantiated as a digital photo album. RiC does not, though, require that a Record Set have an Instantiation. Let us discuss this a little.

Distinguishing between an archive and its physical arrangement might at one time have been thought artifical. However, digital material, especially digital-born material, radically challenges that perspective; in several ways, but not least the fact that it is metadata that under the hood sews together file systems together: a single digital file might be stored in two or more — to all intents and purposes random — locations.

One arrives at the idea of considering groupings/aggregations of records that are meaningful intellectually, but not reflected in a physical assembly of material. The private documentary heritage of Charles Darwin, for instance, is [held](https://www.cam.ac.uk/research/news/charles-darwin-archive-recognised-by-unesco) across at least six institutions.

[![Darwin's documentary heritage](../diagrams/darwin_record_set.svg)](../diagrams/darwin_record_set.svg)

This situation can equally well occur for public bodies, a typical cause being the merging and splitting of such bodies or sub-entities of them.

The freedom to form purely intellectual aggregations in a descriptive context is often very useful in practice. See for instance [int-ref](int-ref:case_study--how_might_ric_be_of_use_to_indigenous_communities_and_other_minority_groups:challenging-over-reliance-on-sources), [int-ref](int-ref:case_study--how_might_ric_be_of_use_to_indigenous_communities_and_other_minority_groups:weaving-together-fragments), and [int-ref](int-ref:extended_example--cervantes_and_the_printing_of_don_quixote:records-of-the-council-of-castile-i).
