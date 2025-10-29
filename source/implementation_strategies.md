## What is this part  about?

Now that you understand its benefits
([int-ref](int-ref:what_are_the_benefits_of_using_ric)), a question remains: how
would you approach the implementation of RiC in your organization? This needs
thinking about, and may take serious effort. You will need to develop an
understanding of the needs and goals of your organization in relation to the
changes in archival description practice that RiC reflects.

We cannot provide a step-by-step guide to implemententing RiC — the huge variety
of specific use-cases make this impossible. Instead, our aim in this part of the
Application Guidelines is to provide a list of actions that might be considered.
It should not be regarded as complete or definitive. In describing some possible
scenarios, we hope to give you an idea of steps that might prove useful in your
own situation.

The following broad topics will be covered:

- Why does one need RiC?

- How to start with RiC?

- What to do with legacy data?

- How to describe records using RiC?

- What needs to be changed to implement RiC?

We will make recommendations intended to help you define a proof of concept for
the implementation of RiC and/or to define a business case, balancing the
benefits which RiC brings with the necessary investment of resources.

## Overview

Implementing RiC is a change, and needs clear goals.
[Identifying](#identify-needs-and-set-goals) the expected outcomes is a good
place to start. You will need to [become familiar with RiC](#learn-ric) to
ensure it will meet your needs. RiC is [new](#a-new-way-of-thinking) and, taken
as a whole, quite complex, so [start with small
steps](#start-small-and-evolve-over-time). A pilot project is a good place to
start, especially if there is legacy data. The latter must be reviewed and
[transformed into RiC](#map-your-legacy-data-to-ric), and existing cataloguing
processes [will need to be
adapted](#introduce-ric-in-your-software). If there are
software tools, they may need to be adjusted or replaced. We elaborate on all of
this below.

## Identify needs and set goals

Ask yourself: what is the most useful thing that RiC will give you? Archival
description is a practical activity, carried out to achieve various aims such as
summarizing the content of a body of records; revealing their contexts for a
better understanding; improving their management; and improving access to them.
These aims can change over time, so any organization should regularly review
their processes to align them with emerging needs. A change in this regard might
be a suitable moment for implementing RiC.

If you are an organization with very few records, whose focus is more upon
administrative aspects of custodianship, less upon facilitating an improved
experience for users, then a full, extensive implementation of RiC might not be
the best solution for you, though it may still prove useful. In contrast, if you
for instance carry out large-scale digitisation of paper records; if you have
many entities to describe (records and/or agents and/or functions and more) and
you need to reveal their complex links; or if you have large holdings and you
are keen to link your data with the wider cultural heritage environment, then
RiC could prove to be a valuable tool to use. These examples are not exhaustive;
the point is that adopting RiC should be connected to needs and goals.

A pilot project might involve an assessment of your current practices and
contexts, and identification of issues. For instance:

- your current archival descriptions might be siloed, making it difficult to
  express complex relationships between records, agents, functions or events;

- your descriptions might be duplicated due to the creation of copies of records
  on microfilm, in a digital format, or because there are several descriptions
of the same records in different finding aids;

- it might be difficult to describe how records came to be created and used
  accurately because of parallel provenances;

- your archival contexts are presented in a few limited ways (either
  hierarchical or in flat lists, for instance), limiting discoverability and
usability.

- in your administrative or societal landscape, there might be pressure towards
  sharing your data with various institutions, or integrating it into various
networks.

As a result, you might conclude that more flexible and connected descriptions
are needed.

The pin-pointing of such issues might come from internal staff — archivists, ICT
specialists, and others — or from users. The tools and methodologies used to
gather this information might include focus groups, surveys, and interviews.
Carrying out these activities can be time-consuming, and the results will need
to be reviewed and compiled to reach a well-defined set of requirements.

This stakeholder analysis report might also go a step further, to describe the
expected benefits of adopting RiC as a solution, guiding an implementation
process. For indeed, by implementing RiC, some of the above issues may find a
solution:

- RiC will enhance discovery of archival resources by linking records to their
  creators, functions, and events;

- it will ease the transition from hierarchical (multi-level) to networked
  (multi-dimensional) archival descriptions, providing more ways to reveal the
rich network of contexts for records;

- it will enable interoperability with other cultural heritage institutions;

- it will provide metadata for AI/ML applications (e.g. entity extraction,
  knowledge graphs).

If your organization concludes that RiC will meet its needs, then you will
likely need to begin to explore how to implement it in detail, including
building up a business case. We turn now to how you might proceed.

## Start small and evolve over time

RiC implementation is likely to work best as an evolutionary process. It might
start with describing a specific type of data such as Agents, or upgrading
infrastructure to support RiC, such as moving to holding data in triple stores.
Or you might begin by focusing upon improving publication of data on/from your
records, via APIs for instance, and only afterwards focus upon your descriptions
themselves. Again, it is up to each organization to decide its goals and how
much of RiC should be used.

A pilot project, either at the earlier stage discussed
[above](#identify-needs-and-set-goals) or when starting to actually implement
RiC, might involve working initially with a small set of data, then, based on
the lessons learnt, planning the next phase of work.

At the same time, it should be kept in mind that, in a preliminary phase, not
all details about how your implementation of RiC will look may be clear. You may
not yet know the specifics of activities that will need to be carried out, or
exactly the resources that will be needed — whether with regard to finance,
time, expertise, or software. Your focus should then likely be upon business
objectives, upon impact, and upon high-level strategy: the need to retrofit the
existing data, or to adapt or purchase software, infrastructure, processes, and
expertise.

## Learn RiC

Becoming familiar with RiC in-depth is an important early step for your whole
team, so that the viewpoints and needs of people in all kinds of roles are
considered. Indeed, although it is key that those who will be most heavily
involved in the implementation, and those who have a strategic or leadership
role within your organization, are familiar with RiC, a RiC implementation is
more than a simple new process for describing your records; it will have an
impact on the work of many people, internal and amongst your users. Archivists
and records managers might look at RiC-CM from the perspective of the process of
describing records; IT staff will need to consider the required technology; data
analysts might focus upon the transformations needed to migrate from an existing
data model to a new one.

This learning process might consist of workshops and training courses on RiC-CM;
of exploring the rest of these Application Guidelines; reading documentation of
and experimenting with existing implementations of RiC: or comparing RiC with
existing standards that were used previously in your organization (e.g.
ISAD(G), EAC-CPF, or EAD). See [int-ref](int-ref:mappings) for more on the
latter.

Learning RiC will allow a more concrete impression of what a RiC implementation
might consist of, for everybody involved. It will open the door to a preliminary
and high-level gap analysis between existing practice (metadata, relations, data
structures, software) and your desired outcomes. You might use your knowledge to
design a roadmap divided into short, medium, and longer-term milestones.

Having a clear view of what implementing RiC will require, you will be able to
realistically assess what will be required to achieve your objectives — people,
time, and a budget — and an assessment of the risks. The economic dimension is
important, since as in any such circumstances, the dreams may be many, but
resources may be few - goals may need to be prioritised. Key performance
indicators might be defined. Potential resource savings from implementing RiC
could be brought into the economic rationale, along with added value more
generally. All of these elements can contribute to building a business case.

## Map your legacy data to RiC

In many cases, implementation of RiC will be made in an environment where legacy
data exists. In order to migrate into a new system compatible with RiC, your
data will need to be prepared and improved. During this process, RiC-O can be
used as a tool, [providing](https://www.ica.org/standards/RiC/ontology) RiC-CM's
entities, attributes, and relations in the form of
[OWL](https://en.wikipedia.org/wiki/Web_Ontology_Language) classes, datatype
properties, and object properties respectively.

Specifically, a migration of legacy data might involve defining a one-to-one
mapping from old standards to RiC-O classes and properties. The data would be
mapped as closely as possible as-is to RiC-O, or, where necessary, to an
extension of RiC-O accommodating local requirements. This is the simplest kind
of migration; it might later be complemented by data processing, or one might
carry out the latter at the same time.

In contrast to previous descriptive standards like ISAD(G) which rely heavily on
free-text narrative description, RiC is an entity-relation model: it identifies
the things to be described and how they relate to each other, and is far more
structured. To get the most out of legacy data, you may need to do some work
identifying structure within your existing descriptions, extracting as many RiC
entities as possible, and linking them using RiC relations. See
[int-ref](int-ref:getting_started_with_ric) for an example of this
approach.

Since the migration and improvement of legacy data is likely to be a gradual
process, it may be a good idea early on — for example as part of a pilot project
as discussed earlier — to gather a subset of data that encompasses all of the
attributes and relations in RiC-CM that you anticipate that you will have a need
for. As you scale up, you will hopefully then avoid encountering a new
requirement that throws a spanner in the works of your implementation.

Even if you do not immediately have a need for certain attributes or relations,
a good option when migrating might be to leave open as far as possible — in code
and in processes — the possibility of future improvements to your data, either
for new data or through processing of existing data, which might allow for, or
indeed necessitate, use of more of RiC.

However you proceed, once you have scripts and other tools and processes to
transform your legacy metadata (EAD, CSV, and so on) into RiC compliant formats
(RDF or JSON-LD for instance), test them robustly with diverse examples, and
don't hesitate to ask for feedback from the RiC community.

## A new way of thinking

A RiC implementation has at least two facets: methodological — describing
records — and technical: a RiC compatible information system which stores,
maintains, and possibly publishes your descriptions. Let us begin with
methodology.

In contrast to previous ICA standards, RiC is not a prescriptive, ready-to-use
standard, but rather a framework — a conceptual model. As we have emphasized, it
will be necessary to understand and define how RiC can be made to work for you.

Although migration was our focus [above](#map-your-legacy-data-to-ric), RiC is
not simply about formatting existing data, or changing the way this data is
presented to users. It also bears upon the writing of new descriptions, by
humans or a machine. Whilst the latter might be programmed to perform the task
in a certain way, an archivist/records manager has a mindset, and a way of
describing records, that might need to be adjusted somewhat to reflect RiC.

Changes to software tools may need to be grappled with in the actual writing of
descriptions. Minor updates to a graphical user interface might suffice, or more
major adaptations may be involved, for instance if descriptions are written at a
lower, more technical level, say EAD descriptions.

From a strictly methodological perspective, describing with RiC may continue to
be performed quite similarly to in a classical hierarchical (e.g. ISAD(G))
context: there is an object of description that must be characterized using
certain properties.  A Record Set in RiC has different attributes and relations
available for a file, say, than ISAD(G), but many such differences be overcome
by intermediary software, for example the design of a graphical user interface.

Discernible changes of perspective may arise if the use of relations in RiC is
embraced for expression of information included in previous elements of
description. Your description processes may then enter into a transitional
phase; a hierarchical approach may still sometimes be taken, but as one way of
relating Record Sets and other entities amongst several, all equal in importance
and validity. A separating out of attributes and relations referring to
Instantiation of Records may be embarked upon.

Relations between Record Resources may be introduced top-down or bottom-up. In
the bottom-up approach, a Record Set might be introduced when enough Records
have something in common that it makes sense to extract this into an aggregating
principle. Having too many Records aggregating into the same Record Set might,
though, eventually prove cumbersome and time-consuming, and the old approach of
dividing large Record Sets into smaller ones might be employed. In this case,
the ISAD(G) requirement that archival arrangement must be carried out prior to
description may still be relevant, even though this is not mandatory in RiC.

Moving beyond a transitional period, RiC allows for a variety of approaches to
description, in which the advantages RiC has will become more apparent. For
instance, if an element of the context of a Record Resource has an aspect that
is particularly significant, it might be used as a starting point for the
description of it. For a first example, let's assume that we have a corpus of
Records illustrating a specific place. Using the Place entity, the description
may begin with the latter, e.g. documenting it both spatially (subdivisions,
adjacent places,...) and temporally (historical evolution), before describing
and linking the Records themselves to it.

Take instead as an example the description of events such as the creation of the
European Union as agreed in the Maastricht Treaty of 1992. We might introduce an
Event entity, relating it along a temporal axis to other Events such as the
Schengen Agreement of 1985, and linking it to Agents such as army divisions
(Group), physical people (Person), and then placing Records into this rich
context.

In summary, establishing methodologies for implementing RiC will likely involve
consideration of the entities in RiC which you wish to use in your organization,
based both requirements that already exists and evolution of your descriptive
practices in the future. It is important to consider this extensibility aspect,
and neither to impose rules that are too rigid, nor to be too constrained by
what your current software allows.

## Introduce RiC in your software

Let us turn to the latter point; the technological aspect of implementation of
RiC. This presents several challenges, pertaining both to IT industry aspects
and the requirements of such an implementation.

Software implementing RiC might be developed bespoke — whether in-house or by an
external company — or purchased as or within a commercial, off-the-shelf (COTS)
product. As always, the former approach is more flexible, allowing for tailoring
to your specific needs, but has a higher cost both for development and
maintenance; it will take longer before it is able to be used; and it may not
benefit from broader experience of good solutions implemented in other
environments. A COTS product too, though, may require non-trivial configuration,
and relying on a vendor is not risk-free: if the client base is not large,
delays may be encountered, and customization or new functionality may require
dedicated development, which again is cost-intensive. In practice, the most
common approach is to buy from a third-party vendor, in which you will need to
prepare your requirements carefully, for instance based upon use of RiC-O, and
ensure that your vendor can and will implement them.

RiC compatible software can either replace an existing system or be implemented
from scratch. One might consider gradually implementing RiC functionality in
different domains: managing, describing, or publishing, for example. We outline
a few scenarios:

- you might first upgrade your publication portal. Even if using an information
  system based on traditional description in your backend, a new portal based
upon RiC may illustrate the benefits it brings, and be a trigger for using it
more broadly. Such an approach would involve something akin to a [migration of
legacy data](#map-your-legacy-data-to-ric), perhaps in the form of on-the-fly
conversion of it to RiC, facilitating viewing and working with it from a
multidimensional perspective.

- a two-phase scenario might be followed along lines discussed
  [above](#a-new-way-of-thinking): first, a one-to-one
[migration](#map-your-legacy-data-to-ric) of existing data RiC, and second, the
gradual introduction of additional descriptive and functional possibilities
offered by RiC, so that your staff experience as smooth a transition as possible

- you might instead begin by introducing new functionalities based on RiC
  alongside existing ones, firstly implementing the same functionality as
before, but with RiC in the background; then adding functionality that your
staff and users see an immediate need for and would be popular; finally
introducing more innovative functionality.

The quality and range of functionality of your software will be a game-changer
for transitioning to RiC in your descriptive processes. Functionality suggesting
and semi-automating the creation of relations between entities, or integration
with controlled vocabularies, would be an invaluable assistance. Since RiC
encompasses considerably more entities than Records and Record Sets, the
workflows of your software and the arrangement of these entities in user
interfaces will play an important role in change and adoption: an archivist or
records manager wishes to capture an object of description, not concern themself
directly with RiC entities, whilst users will be looking for information, not
for RiC entities specifically — the technicalities should be under the hood.

No particular technology or infrastructure is prescribed for implementing RiC.
As discussed [above](#map-your-legacy-data-to-ric), RiC-O might prove a useful
and efficient tool, in which case infrastructure such as a triple-store or graph
database might be appropriate. But you should be able to implement RiC-CM in an
SQL database or using XML documents too. Keep in mind scalability and potential
future use-cases, though — a relational database may not be optimal when working
with networks of relations which are several steps deep, or when it comes to
introducing new entities, attributes, or relations into the database schema.

As in any such case, an implementation project will necessitate training of
staff and users, and changes in management processes. In the end, software and
the technical use of RiC is just a tool; the [mindset](#a-new-way-of-thinking)
of archivists/records managers and users is more important.

## Tips for preparing for RiC

- Start small! Pilot projects are useful both to assess the process and its
  benefits. It is OK to fail, but at the least possible cost!

- Go one step at a time! The process may take time, and you can proceed in
  stages.

- Make sure you have staff with the requisite skills, including technical
  skills, or train them to acquire these skills. Neither archivists/records
managers nor software engineers and IT staff alone can achieve a successful
implementation of RiC alone, it is a question of teamwork.

- Every situation is different! Understand your use case, set your goals, and
  identify the benefits you envision. RiC is not a fashion, but a tool to help
you do your job.

- Take the time to evaluate your data and your situation.

- You are not alone. Ask the RiC community for help (and share your experience).
  The RiC [mailing list](https://groups.google.com/g/Records_in_Contexts_users/)
is a good place for this. RiC is a framework that others are using, so tell
people what you are doing - you may find others who are doing the same. Sharing
your experience will help other people.

- Implementations are still at an early stage, but some exist, as do tools.  See
  the RiC [Resource
List](https://ica-egad.github.io/RiC-ResourceList/index.html) for more, and
contribute your work to it.
