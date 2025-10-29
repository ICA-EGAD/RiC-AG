## What is this part about?

People who are looking for information don't think that much about how that
information is stored. They just want to find the information quickly and
efficiently, and to assess its quality and authenticity. With the World Wide
Web, and Linked Data in particular, archives have the opportunity to move from
siloed architectures towards data driven structures. For the archival field,
Records in Contexts is the means to achieve that. This part of the Application
Guidelines looks at the benefits of RiC for end users, archival practitioners
and managers in archival institutions respectively. After reading this part you
should know why it is worthwhile to invest in understanding and using RiC.

## For end users

The benefit for end users comes mostly from the network structure that is one of
the foundations of RiC. After all, records may not only be related through a
common provenance, but may also be related to common people and places. This
makes it easier for end users to answer questions like: 'what archival material
is available about my home?' or 'what archival material relates to my
grandmother?' or 'what archival material relates to healthcare in the 1950s?'.

### Multiple points of access

RiC ensures that multiple routes to information are created. Currently you need
to know exactly where archived information is in order to find it, or you need
to know who created the records – something that is not usually intuitive for a
member of the public. Thanks to RiC's network structure it is possible to use
relationships to get to certain information independent of where it is held.
With RiC based metadata, any RiC entity (such as a Person or a Place) can become
an access point alongside the hierarchical structure of an original finding aid.
So, in addition to drilling down from the fonds to the record, browsing via
persons and places becomes much more effective as they are part of a network of
data and documented relationships. That network could be between archival
resources within one repository, but also linked to data somewhere else, outside
of your institution. Related content may include, for example, collections by
the same creator held at different institutions, collections by members of the
same family held at the same or different institutions, or collections relating
to the same event held at the same or different institutions.

Because multiple avenues of access are offered, more types of users can reach
archival material and, depending what the data is linked to, even users who are
not specifically looking for archival material can find it too.

### Use the context of information

Using Records in Contexts creates a network of data, which makes data better
contextualized. The data is no longer presented in isolation (like the old silos
of finding aids, indexes and image databases), but always related to other
sources, people or places, which leads to a better understanding of the data. As
a result, the data becomes more meaningful.

The network structure of RiC also enables new visualizations of search results.
We're already familiar with the table (when the metadata is most important), the
timeline (when chronology is most important) and the map (when geography is most
important). For the user who is interested in the relationships between the
people, places, events and records that form the network, the representation (or
visualization) of this network of related entities as a graph can be very
helpful. It enables you to browse or explore such a network by following a trail
of nodes that are of interest.

### Facilitate methods of analysis and connection

When you combine RiC with Linked Data techniques you can infer information that
your local system doesn't know.  Linked Data is a way of expressing information
in statements following the pattern 'subject/predicate/object', as in 'William
Shakespeare (subject) is the author of (predicate) Macbeth (object).' RiC
implemented as Linked Data adds benefits to resource discovery, in particular
the ability to include data that is not stored locally but is available in a
related record elsewhere. For example, another system might store the statement
'Macbeth was published in 1623'. When linked to the entity 'Macbeth', both
pieces of information–authorship and publication date of Macbeth–can become
available to the same system despite originating in separate systems.

When RiC is combined with Linked Data techniques it is ideally suited for:

- selecting data: doing research with your own specific, dedicated subset

- combining data: relating the research data with data available in other
sources

- inferring data: using the available, standardized rules in RiC-O or creating
your own rules to add data that can be deduced from the existing metadata

- keeping track of references: storing the origin of the data for future
 researchers to study

Although these activities can be carried out using existing techniques, Linked
Data makes it possible to perform them more precisely and will provide more data
for the same or less effort. Increasingly, researchers are looking for technical
ways to use archival sources, and RiC enables these approaches to be used
alongside the traditional methods. As a result, more people will be able to find
and use your archival material.

## For archival practitioners

Archival practitioners are passionate about making sure that the quality of
their metadata is high. However, practitioners often encounter the limits of the
existing data model. For example, within a traditional hierarchical system, a
record can be described at only one position in the hierarchy. Most of the time
this position is related to the arrangement and the provenance of the record
(e.g., financial records are part of the series of records created by the
financial department), and not accessible through the subject (e.g. 'travel
expenses' or 'personnel') that an end user might want to study. That means an
end user must know how to drill down the hierarchy to discover the right
archival source. With Records in Contexts (note that 'Contexts' is plural!)
subjects can be added at the same time as the provenance and the arrangement are
added. RiC does not consider these two elements of context as the only two, as
is the case in a hierarchy, and allows professionals to move from a
mono-hierarchical perspective to a multidimensional description.  They no longer
have to choose a single location in a hierarchy for the records they describe,
but rather are invited to represent the network of entities in which these
records are placed.

With born-digital records this problem becomes even more complex: in a document
management system there are all kinds of relations between records and computer
files. Records in Contexts defines clearcut entities, and relations to connect
those entities to each other. These relations give several points of entry to a
record, and also essential contexts. In a hierarchical system much of this
information would get lost. At best, it is stored in the description, which
makes it messy and difficult to analyse.

Another important benefit is that Records in Contexts introduces new concepts to
model digital and digitised sources. An archival record can be instantiated more
than once, besides its original paper form or digitally appraised computer file.
It makes the conceptual model robust for the future, while enabling, for
instance, all kinds of AI technology to be used as well. Handwritten Text
Recognition (HTR) and Optical Character Recognition are tremendously useful to
all kinds of users: you can search within the data of the record itself. Because
in Records in Contexts the transcript is a separate entity, you can store
metadata about it. When was the transcript made, from which scan, and with which
model? When you have a better HTR model, you can easily select old versions of
the texts to be replaced by new ones. See
[int-ref](int-ref:faq--general_questions_and_smaller_modelling_questions:do-you-have-examples-illustrating-chapter-6-of-ric-cm)
for more on this.

The introduction of additional entities like Activity and Rule (see
[int-ref](int-ref:faq--general_questions_and_smaller_modelling_questions:are-activity-and-event-central-entities-in-ric-how-about-rule-and-place))
provides for nuanced expressions of archival practice, helping the archivist to
model clearly the provenance and the history of archival material.  Such
approaches enable a more unified approach to describing records before and after
their transfer to an archival institution. Metadata captured by records creators
can be reused in archival description systems. Simply put: Records in Contexts
makes sure that metadata is captured where it should be. With more entities, and
properties for those entities, and relations with a specific name, the
practitioner has many more options to describe records in their contexts.

When you combine RiC with Linked Data you have the opportunity to integrate all
kinds of controlled vocabularies, authority records and value lists into your
system, and to use them to standardize metadata. Controlled value lists are
already in use in the archival field to varying degrees, but the benefit of the
Linked Data technique is that it is so much more interoperable with other
sources. As an archivist you can use this to benefit from other people's work.
For instance, if a certain agent is important to your collection, you probably
want to include the name of this person in one of your own lists. You can link
this list to external sources, such as Wikidata. When someone else has found out
the date of birth and death, you can simply import this information. It saves
you the time of researching those dates yourself. And it prevents redundancy of
metadata. The more you standardize, the more time it saves you. This leads to
improved work processes.

Introducing RiC as Linked Data can be realized by using the standardized RiC
Ontology (RiC-O). RiC-O contains all the RiC entities and its predefined types
of properties, called 'relations', complemented by a lot of other entities and
properties. Some of these enable you to provide more accurate descriptions,
others enable backwards compatibility. Using RiC-O to publish your archival
metadata helps to link it with archival description in other heritage
institutions and exchange metadata if necessary, widening the network of data
available to the researcher.


## For IT managers and CIOs

With Records in Contexts we have one global and consistent reference model,
maintained by and for the professional community which uses it. It can be used
as a way to break down internal silos and design a data-oriented enterprise
architecture. In this architecture, processes can be organized more efficiently
using software components that are interoperable and easily interchangeable - if
the components comply with the standard. The resulting architecture is better
suited to archival processes and will meet the needs of existing and future end
users.

It is important to note that the standard can be introduced step-by-step
following an iterative approach. The implementation can be organized as a series
of modular projects carried out over time. During these projects the reference
model can be extended if needed. For more on this see
[int-ref](int-ref:implementation_strategies).

Introducing Linked Data and the Records in Contexts Ontology helps transform the
metadata you hold and publish it in a variety of forms suitable for various
needs. It also ensures your organization complies with international standards
for reusable data sets in scientific research, like
[FAIR](https://www.go-fair.org/fair-principles/).

## For general managers

The introduction of Records in Contexts in your organization is worth the extra
effort and resources as it results in greater control of the ever-increasing
amount of data. Through a better understanding of the components of the data and
the software, the quality of the metadata in your collection improves, as well
as the efficiency of the processes handling it.

Records in Contexts makes your organization ready for the future. New
technologies, like AI, can be hooked into the new infrastructure. For the first
time it provides a framework for describing both born-digital material and
analogue records, and as a result will help with the processing of both paper
and digital records, as well as hybrid collections, which have grown in recent
years. Thirdly, as a common reference model, Records in Contexts enables
connection of your archival material and data to other organizations, especially
if you implement it in Linked Data, and makes cooperation with these
organizations easier. As RiC is adopted by more organizations, it is likely that
funding partners will require you to introduce RiC into your institution and
project, as a condition for funding.

The transformation of your finding aids from the old standards to Records in
Contexts is a considerable undertaking, and will mean changes to how you work,
but it will improve processes and enable researchers to use your data in ways
that are not possible now. The change will not happen overnight. Implementing
RiC is an iterative process and approaches to this, along with how to get
started, will be described in the following parts.

