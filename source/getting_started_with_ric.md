## What is this part about?

This part of the Application Guidelines demonstrates how you could get started
with RiC using your own data. It takes an existing ISAD(G)-style catalogue and
maps the information to RiC-CM.  For more, see [int-ref](int-ref:mappings).

## Introduction

How do you start using RiC to describe your records? It's best to begin small,
with just a few pieces of information, creating relations that are already known
and using your existing finding aids if you have them.

Connections are often hidden in the narrative descriptions
and fields of finding aids, and one of the key purposes of RiC is to make these
connections explicit. These links often reveal new information about our
collections and they could connect our records to others in our own collections
and on the wider web. Creating a network in this way will also help you spot
what information is missing, so could prompt you to find the information from
the depositor (where possible) or for future deposits to improve your finding
aid.

RiC-CM is what is termed a 'general reference framework' which means that it is
a structured high-level guide, in this case for the description of archives. It
provides a common vocabulary, best practice and rules so you can lay the
foundations for implementing it in a consistent way. This means it includes some
general elements which can be used to broadly describe almost every archival
collection, with some more specific elements to describe your records at a more
detailed level. You do not need to use all of the elements from the start - or
at all - and you can add more over time, building your descriptive model step by
step. So which pieces of information do you need? Although nothing is mandatory
in RiC, there are some elements which may be especially useful for identifying,
retrieving, selecting and accessing records of interest to researchers, for
example most entities benefit from a Name and an Identifier. These are commonly
found in archival finding aids so are likely to be familiar and demonstrate how
easy it is to get started.

Many archives used
[ISAD(G)](https://www.ica.org/resource/isadg-general-international-standard-archival-description-second-edition/)
as a basis for their finding aids, either directly, via national standards, or
by using in-house guides taking inspiration from it. ISAD(G) provides key
information about records and specifies that the  *reference* (i.e. an
identifier), *title*, *creator*, *date*, *extent* and *level* fields are
considered essential (for the exchange of information). These are a great place
to start when describing records, and here we will explore how they can be
expressed in RiC.

As archivists and records managers we know that the people and organizations who
created, used and managed the records, their functions and activities, the
records' different forms, both analogue and digital, and the relations between
all of these things, are essential to understanding and using archives. RiC
gives us a single framework to describe these records because it encompasses
this wider context, building on both ISAD(G) and the complementary standards
[ISAAR(CPF)](https://www.ica.org/resource/isaar-cpf-international-standard-archival-authority-record-for-corporate-bodies-persons-and-families-2nd-edition/),
[ISDIAH](https://www.ica.org/resource/isdiah-international-standard-for-describing-institutions-with-archival-holdings/),
and
[ISDF](https://www.ica.org/resource/isdf-international-standard-for-describing-functions/).
In the example below we will cover the key fields but also some of the broader
aspects you are likely to encounter when you start working with RiC.


## Overview of Key RiC Elements

This section groups the entities into the broad questions asked by users of
records, namely 'what', 'who', 'when', 'where' and 'why'.

### The 'What': record resources and instantiations

#### Entities: E03 Record Set, E04 Record, E05 Record Part

Just as with a traditional finding aid, Records in Contexts helps us describe
individual archival records, parts of those records and groups of records.  The
entity Record Resource is used to describe these collectively. In RiC, a Record
is a discrete piece of information often associated with a single transaction,
for example a letter, memorandum, report, photograph or sound recording. A
Record Part could describe a paragraph of text within the Record, or a wax seal
attached to a charter, or an image file attached to an email. A Record Set is an
aggregation of Records, for example, a Fonds or a Series, because they are both
an organized group - or 'set' of Records. For RiC a physical folder containing a
number of letters is also a Record Set and reflects the definition given in
ISAD(G): '\[a\]n organized unit of documents grouped together \[...\] because
they relate to the same subject, activity, or transaction. A file is usually the
basic unit within a record series'. For born-digital records, an ISAD(G) file is
often considered to be a digital folder containing a number of individual
digital objects such as Word or PDF files - again RiC's definition of a Record
Set as an aggregation of records matches the previous standard.

#### Entity: E06 Instantiation

This entity may be the most challenging to understand as it separates the
description of the physical features of the record resource from the description
of the content it contains. ISAD(G) does not make this distinction but
describes both physical and intellectual features of a record in a single
description. The concept of an Instantiation means we can distinguish between
the intellectual content of the Record, such as the writer of a letter and its
content, and the physical form it takes.  For example, the description of the
Instantiation of a letter could include the Carrier Extent (e.g. A4 size) and
Carrier Type (paper), and the Production Technique: handwriting. A description
of the Instantiation of a digital letter might include its Instantiation Extent
(1.4MB), its Carrier Type (optical disk). A single record could have multiple
Instantiations, for example the letter written on paper could have been scanned
and a digital Instantiation created as a PDF file. With RiC we can describe both
the PDF and the paper Instantiations of the letter and link them both to a
single description of the Record. This allows us to be more specific in what we
are describing and more efficient as we only need to describe the content once
rather than duplicate the description for both entries.

In RiC every Record and Record Part has or had at least one Instantiation
because they will always have a physical aspect even if it no longer exists, for
example we might have a description of a charter from an old finding aid which
has been lost or destroyed since the finding aid was created. This makes sense
if we think of the Instantiation as the 'object' we hold in the archive. In most
cases we will be able to say something about the Instantiation of a Record, for
example, where it can be consulted or whether it is born-digital, digitised or
analogue.

As you would expect, Instantiations are linked by a relationship to Records, for
example a digitised version of a photograph or a military service record is
linked to the description of its intellectual content. But Instantiations can
also be linked to Record Sets, for example if the lowest level of description is
a physical folder containing many individual letters, the instantiation would
describe the physical characteristics of that folder as a whole and if the
letters were then digitised as a single PDF, that PDF would be described as an
instantiation of the Record Set.

For a more detailed discussion of the distinctions between Records, Record Sets
and Instantiations see RiC-CM v1 Section 2.2.2.

### The 'Who': people and organizations

#### Entity: E07 Agent / E11 Corporate Body

Archivists often struggle to create a single hierarchy for a series which has
been created or managed by more than one person or organization as prescribed by
the principle of Respect des Fonds with ISAD(G). Knowing which individuals,
families or organizations created, held, used and maintained the records over
time is essential but does not always reflect the social and material complexity
of the records' origin. RiC recognizes that provenance can be understood in
various ways and enables us to represent the complex network of relations that
surround every record over time. To do this the entity of Agent has an equal
standing with the Record and Record Sets and can indicate that they were created
by more than one person or group, and that those persons or groups have played
different roles depending on their functions and mandates.

In the example below, we have used Corporate Body (a fourth level entity)
instead of Agent (a second level and 'core' entity) because it is more specific.
This is an easy choice to make if you know the type of creators and choosing the
more specific elements means your descriptions will be less ambiguous.

### The 'When' - the temporal context we're describing

#### Entity: E18 Date

One of the differences between RiC-CM and ISAD(G) is that RiC-CM is an entity
relationship model, meaning that it views entities and the relations between
them as just as important as the records. Dates are therefore treated as
entities in RiC as they are key to understanding the records. This means we can
describe the temporal context of the other entities instead of just adding a
date as an attribute, i.e.  information about an entity.

By making the date an entity we can be far more explicit about what it means.
Is it the date of creation or a date that is associated with the contents of the
record? Is it from the Gregorian or Julian calendar? Is it only an
approximation?  Is it not just the date of creation but a significant date that
is relevant to the record? By making the date an entity we can make its relation
to the Record, Agent or Record Set really clear, For example, the Date entity
8th May 1945 can be linked to a Person entity with a relation of 'is death date
of' but it can also be linked to a Record with the relation 'is creation date
of' and given a name 'Victory in Europe (VE) Day' and linked to an Event entity:
the day that the Second World War in Europe ended. By treating date as an entity
we can link it to a variety of other entities and see potential links between
them all: a Person, a Record and an Event.

As archival data are increasingly used for computational purposes, modelling
dates as entities rather than attributes ensures they are machine-readable as
well as meaningful for humans. Simple dates in existing finding aids, such as
'12 October 1958' or '1978-1980' can be used in the Expressed date attribute.
Many finding aids. however, have dates such as 'c.1650' or '1920s' or '17th
century'. We can still use those dates in RiC in the Expressed date attribute
but we can also define them in a machine readable way in the
Normalized date attribute. They might become 1650-01-01/1650-12-31,
1920-01-01/1929-12-31 and 1600-01-01/1699-12-31 (or
1601-01-01/1700-12-31, depending upon how one defines a
[century](https://en.wikipedia.org/wiki/Century)), and can then be
found by database searches.

For a more detailed discussion of Date see RiC-CM v1 Section 2.2.6.

### The 'Where': the location we're describing

#### Entity: E22 Place

Records are created in places, are about places and are held in places All of
this information is usefulto researchers, so RiC provides a way of describing
any place to any level of detail alongside how it relates to the Record
Resource.

For a more detailed discussion of Place see RiC-CM v1 Section 2.2.7.

### The 'Why': the reason for the Record Resource's existence

#### Entity: E15 Activity

An activity is a kind of event performed by an agent, and in many archival
contexts this means it is the same as a function. Instead of using the term
function, however, RiC uses the term Activity because some types of Agent, such
as a Person or a Family, do not perform functions in the traditional archival
sense.

For a more detailed discussion of Activity see RiC-CM v1 Section 2.2.4.

### Attributes

Every entity in RiC including Records, Record Sets and Instantiations has a list
of attributes. These attributes reflect characteristics of the records such as
the description, the unique reference number and the access conditions. Some of
these attributes can be filled in as free text, while others can be chosen from
a set of predefined terms, for example physical formats (CD, box etc.) or
authority terms.

For a more detailed discussion of attributes see RiC-CM v1 Section 3.

### Relations

Relations are key to RiC: with relations we can create a rich network of
connections with explicit links between all the entities including Records,
Record Sets, Instantiations and Agents. With a relation, one to many
Instantiations can be linked to the same Record so it is clear that they convey
the same content. The Instantisations can also be linked to each other, to say
for example that a digital instantiation is derived from an analogue one.
Relations also link Records and Record Sets, so that the hierarchy and the
sequences used in traditional finding aids can be maintained. Relations can also
link entities outside of the traditional hierarchy. This makes it possible to
link parts of our collections for a variety of reasons including similar
content, or because they were used by the same individual, or relate to the same
legislation or event, or because they document the same activity or chain of
activities. Outside of our institution, we can use relations to link our records
to those held by other archives. In time, these connections will form a huge
network, describing the multiple contexts in which archival documents have been
created and managed. For users this could expand the horizons of their research
as the connections could extend far beyond those in a traditional finding aid.

For a more detailed discussion of relations see RiC-CM v1 Section 5.

## Example

This simple example shows how part of an existing finding aid - based on
ISAD(G), ISAAR(CPF), and with a few additional entities - can be turned into
RiC-CM. The example is taken from
[Discovery](https://discovery.nationalarchives.gov.uk/details/r/C405), the
online finding aid of the National Archives, UK. To create this example we have
included metadata from the catalogue and supplemented it with data that is not
included in the current catalogue such as Instantiation and Activity.

We have included some frequently used fields such as identifier, name, language
and dates, and added some which would be included from ISAAR(CPF), ISDIAH and
ISDF to demonstrate how RiC incorporates all of the earlier ICA standards. In
addition we have included a link to Wikidata to illustrate how a finding aid can
be extended beyond its traditional boundaries to an external source of
information.

Perhaps the most important point to take from this section is that once learnt,
using RiC to describe your collections will not take more time or be more
difficult than your current processes.

### Elements

For reference, the following are the entities, attributes and relationships used
in the example.

<table>
<tbody>
<tr class="header"><th scope="rowgroup" colspan="2"><em>Entities</em></th></tr>
<tr><td>E03</td><td>Record Set</td></tr>
<tr><td>E04</td><td>Record</td></tr>
<tr><td>E06</td><td>Instantiation</td></tr>
<tr><td>E11</td><td>Corporate Body</td></tr>
<tr><td>E15</td><td>Activity</td></tr>
<tr><td>E18</td><td>Date</td></tr>
<tr><td>E22</td><td>Place</td></tr>
</tbody>
<tbody>
<tr class="header"><th scope="rowgroup" colspan="2"><em>Attributes</em></th></tr>
<tr><td>A08</td><td>Conditions of Access</td></tr>
<tr><td>A19</td><td>Expressed Date (a human readable date such as 1920s, the Middle Ages or November 19th 1975)</td></tr>
<tr><td>A22</td><td>Identifier</td></tr>
<tr><td>A25</td><td>Language</td></tr>
<tr><td>A28</td><td>Name</td></tr>
<tr><td>A29</td><td>Normalized Date (a machine readable date such as 1920/1929, 500~/1500~, 1975-11-19)</td></tr>
<tr><td>A35</td><td>Record Resource Extent</td></tr>
<tr><td>A36</td><td>Record Set Type (e.g. Fonds, Series, ...)</td></tr>
<tr><td>A37</td><td>Representation Type</td></tr>
</tbody>
<tbody>
<tr class="header"><th scope="rowgroup" colspan="2"><em>Relations</em></th></tr>
<tr><td>R024</td><td><span class="relation">Record Set <span class="relation-name">includes or included</span> Record or Record Set</span></td></tr>
<tr><td>R025</td><td><span class="relation">Record Resource <span class="relation-name">has or had instantiation</span> Instantiation</span></td></tr>
<tr><td>R025i</td><td><span class="relation">Instantiation <span class="relation-name">is or was instantiation of</span> Record Resource</span></td></tr>
<tr><td>R027</td><td><span class="relation">Record Resource or Instantiation <span class="relation-name">has creator</span> Agent</span></td></tr>
<tr><td>R033</td><td><span class="relation">Record Resource or Instantiation <span class="relation-name">documents</span> Activity</span></td></tr>
<tr><td>R033i</td><td><span class="relation">Activity <span class="relation-name">documented by</span> Record Resource or Instantiation</span></td></tr>
<tr><td>R039</td><td><span class="relation">Agent is or was holder of Record Resource or Instantiation</span></td></tr>
<tr><td>R039i</td><td><span class="relation">Record Resource or Instantiation <span class="relation-name">has or had holder</span> Agent</span></td></tr>
<tr><td>R069</td><td><span class="relation">Date <span class="relation-name">is beginning date of</span> Thing</span></td></tr>
<tr><td>R075</td><td><span class="relation">Place <span class="relation-name">is or was location of</span> Thing (e.g. Corporate Body)</span></td></tr>
<tr><td>R075i</td><td><span class="relation">Thing (e.g. Corporate Body) <span class="relation-name">has or had location</span> Place</span></td></tr>
<tr><td>R080</td><td><span class="relation">Date <span class="relation-name">is creation date of</span> Record Resource or Instantiation (note that this is not used for an Agent: R069 could be used in that case)</span></td></tr>
<tr><td>R083</td><td><span class="relation">Date <span class="relation-name">is or was creation date of most members of</span> Record Set</span></td></tr>
</tbody>
</table>

This choice of elements may be missing some you feel are important, such as
Scope and content and History. These are usually considered core for traditional
finding aids as some kind of free-text description is usual for a large Record
set. If you have this information it can be used as it stands but *in addition*,
you can also structure the information so that the Linked Data technologies can
read it and find those hidden connections. You can do this by creating subjects
linked to instances of Thing with the relation _is or was subject of_, for the
topics that the Record Set or the Record relate to.

Alternatively, you could use several instances of Event, related to the Record
set or Record using the Relation _affects or affected_, to link events that are
relevant to the history of the Record Resource. So RiC is flexible: you can
start with the less structured elements and refine your finding aid by adding
more elements over time, keeping both the narrative text alongside the
individual instances of events or topics to make it clearer how they link to the
Record Resource. In this way RiC allows you to keep a broader history *and*
include more structured information at specific record level, which is often
missing completely in some finding aids. If you have this information, then
include it, perhaps splitting it up into different elements such as functions,
mandates, agents and dates linked by relations.

The tables below can be tricky to interpret, so the first entity includes a
brief explanation of how to read the tables as natural language statements. For
a visualisation of the data, see the diagram [at the end](#conclusion).


### Record Resources and Instantiations

#### Entity of type Record Set E03: The Records created or inherited by the
Bodies for Devolved Government in Wales

This entity includes the most commonly used relations to link it to other
entities. Some of the differences between RiC and ISAD(G) become obvious here,
for example the Creator is not an attribute of the fonds but an entity in its
own right. This means that once we create an entity for the Welsh Assembly
Government with its own attributes such as dates of existence and history, as
well as related agents with dates of the relations etc, it can be linked to this
fonds and to any number of other entities.

This example also shows how a Record Set's dates are described as an entity so
that those dates can be expressed in both machine- and human-readable formats
and even gives them an identifier in order to be able to (uniquely) refer to
them.

The final relation shows how a fonds is linked to its series. A relation is used
to show that the fonds includes specific series. In this example we show only
one of those series: WA 16.

The tables can be difficult to interpret so it's easiest to think of the
information as simple sentences as you read through it. In the table below the
fonds is the entity - as indicated by the text in the first row. Every attribute
and relation refers to that fonds so it can be read as follows:

-   The entity has the Record Set Type of 'Fonds'

-   The fonds has the identifier 'WA'

-   The fonds has the name 'Records created or inherited by the Bodies for
    Devolved Government in Wales'

-   The fonds is made up of records in the language 'English'

-   The fonds is made up of records that have the access condition 'Open'

-   The fonds includes or included a Record Set with the name 'London 2012
    Olympic and Paralympic Games: Digital and Paper Records' and the identifier
'WA 16'

-   The fonds has or had an owner with the name 'The National Archives' and the
    identifier '66'

-   The fonds has a creator with the name 'Welsh Government' and the identifier
    of 'GB/NNAF/C287344' etc…

<table id="WA">
<colgroup>
<col class="header-column" />
<col class="data-column-1" />
<col class="data-column-2" />
</colgroup>
<tbody>
<tr>
<th scope="row"><span class="entity-type">Entity type</span></th>
<td colspan="2">Record Set (E03)</td>
</tr>
</tbody>
<tbody>
<tr>
<th colspan="3" scope="rowgroup"><em>This entity has the following attributes:</em></th>
</tr>
<tr class="header">
<th scope="col"><em>Attribute</em></th>
<th scope="col" colspan="2"><em>Value</em></th>
</tr>
<tr>
<th scope="row"><span class="attribute">Identifier</span> (A22)</th>
<td colspan="2">WA</td>
</tr>
<tr>
<th scope="row"><span class="attribute">Name</span> (A28)</th>
<td colspan="2">Records created or inherited by the Bodies for Devolved Government in Wales</td>
</tr>
<tr>
<th scope="row"><span class="attribute">Record Set Type</span> (A36)</th>
<td colspan="2">Fonds</td>
</tr>
<tr>
<th scope="row"><span class="attribute">Language</span> (A25)</th>
<td colspan="2">English</th>
</tr>
<tr>
<th scope="row"><span class="attribute">Conditions of Access</span> (A08)</th>
<td colspan="2">Open</td>
</tr>
</tbody>
<tbody>
<tr>
<th colspan="3" scope="rowgroup"><em>This entity is the source of the following
relations:</em></th>
</tr>
<tr class="header">
<th><em>Relation</em></th><th><em>Name (A28)</em></th><th><em>Identifier (A22)</em></th>
</tr>
<tr>
<th scope="row"><span class="relation">Record Set <span class="relation-name">includes or included</span> Record or Record Set</span> (R024)</th>
<td><a href="#WA-16" class="entity-in-example">London 2012 Olympic and Paralympic Games: Digital and Paper Records</a></td>
<td><a href="#WA-16" class="entity-in-example">WA 16</td>
</tr>
<tr>
<th scope="row"><span class="relation">Record Set <span class="relation-name">has or had holder</span> Agent</span> (R039i)</th>
<td><a href="#66" class="entity-in-example">The National Archives</a></td>
<td><a href="#66" class="entity-in-example">66</a></td>
</tr>
<tr>
<th scope="row"><span class="relation">Record Resource or Instantiation <span class="relation-name">has creator</span> Agent</span> (R027)</th>
<td><a href="#GB-NNAF-C287344" class="entity-in-example">Welsh Government</a></td>
<td><a href="#GB-NNAF-C287344" class="entity-in-example">GB/NNAF/C287344</a></td>
</tr>
<tr>
<th scope="row"><span class="relation">Record Resource or Instantiation <span class="relation-name">has creator</span> Agent</span> (R027)</th>
<td><a href="#GB-NNAF-C287343" class="entity-in-example">Welsh Assembly Government</a></td>
<td><a href="#GB-NNAF-C287343" class="entity-in-example">GB/NNAF/C287343</a></td>
</tr>
<tr>
<th scope="row"><span class="relation">Record Resource or Instantiation <span class="relation-name">has creator</span> Agent</span> (R027)</th>
<td>National Assembly for Wales</td>
<td>GB/NNAF/C284400</td>
</tr>
</tbody>
</table>

#### Entity of type Date E18: 1969 to the present day

Note that this and any date entity could be reused by another entity with the
same span such as another Record Set (such as a Series or Fonds) or an Agent
(such as a Corporate Body or Person).

To create links each entity needs an identifier. Giving an identifier to a Date
seems unusual if you are used to working with an ISAD(G) style catalogue
especially as a date is always a property of a Record or a Record Set. In RiC, a
date is an entity, just like a Record Set, a Record or an Agent because it is
something we want to describe in more detail. We may want to say that this is
only an approximate date, or that there is a human or computer readable version
of the date also supplied. If each date was only a property we would have no way
of adding that information using RiC-CM.

As Date is an entity each one in the catalogue or finding aid needs an
identifier so it can link to other entities such as Records and Record Sets.
This can be randomly generated, although using letters rather than numbers is
less confusing. You will see in TNA's catalogue that dates are properties, so
the identifiers in the example were invented.

Note that only the relation indicates the kind of date for the described entity.
For example it could be the creation date of a Record Set or an Instantiation,
the birth date of a Person or the date a Record will be open to the public.

<table>
<colgroup>
<col class="header-column" />
<col class="data-column-1" />
<col class="data-column-2" />
</colgroup>
<tbody>
<tr>
<th scope="row"><span class="entity-type">Entity type</span></th>
<td colspan="2">Date (E18)</td>
</tr>
</tbody>
<tbody>
<tr>
<th colspan="3" scope="rowgroup"><em>This entity has the following attributes:</em></th>
</tr>
<tr class="header">
<th scope="col"><em>Attribute</em></th>
<th scope="col" colspan="2"><em>Value</em></th>
</tr>
<tr>
<th scope="row"><span class="attribute">Identifier</span> (A22)</th>
<td colspan="2">abc</td>
</tr>
<tr>
<th scope="row"><span class="attribute">Expressed date</span> (A19)</th>
<td colspan="2">01/01/1969-</td>
</tr>
<tr>
<th scope="row"><span class="attribute">Normalized date</span> (A29)</th>
<td colspan="2">1969-01-01/...</td>
</tr>
</tbody>
<tbody>
<tr>
<th colspan="3" scope="rowgroup"><em>This entity is the source of the following
relations:</em></th>
</tr>
<tr class="header">
<th><em>Relation</em></th><th><em>Name (A28)</em></th><th><em>Identifier (A22)</em></th>
</tr>
<tr>
<th scope="row"><span class="relation">Date <span class="relation-name">is or was creation date of most members of</span> Record Set</em> (R083)</th>
<td><a href="#WA" class="entity-in-example">Records created or inherited by the Bodies for Devolved Government in Wales</a></td>
<td><a href="#WA" class="entity-in-example">WA</a></td>
</tr>
</tbody>
</table>

#### Entity of type Record Set E03: London 2012 Olympic and Paralympic Games:
Digital and Paper Records

<table id="WA-16">
<colgroup>
<col class="header-column" />
<col class="data-column-1" />
<col class="data-column-2" />
</colgroup>
<tbody>
<tr>
<th scope="row"><span class="entity-type">Entity type</span></th>
<td colspan="2">Record Set (E03)</td>
</tr>
</tbody>
<tbody>
<tr>
<th colspan="3" scope="rowgroup"><em>This entity has the following attributes:</em></th>
</tr>
<tr class="header">
<th scope="col"><em>Attribute</em></th>
<th scope="col" colspan="2"><em>Value</em></th>
</tr>
<tr>
<th scope="row"><span class="attribute">Identifier</span> (A22)</th>
<td colspan="2">WA 16</td>
</tr>
<tr>
<th scope="row"><span class="attribute">Name</span> (A28)</th>
<td colspan="2">London 2012 Olympic and Paralympic Games: Digital and Paper Records</td>
</tr>
<tr>
<th scope="row"><span class="attribute">Record Set Type</span> (A36)</th>
<td colspan="2">Series</td>
</tr>
<tr>
<th scope="row"><span class="attribute">Language</span> (A25)</th>
<td colspan="2">English</td>
</tr>
<tr>
<th scope="row"><span class="attribute">Conditions of Access</span> (A08)</th>
<td colspan="2">Open</td>
</tr>
<tr>
<th scope="row"><span class="attribute">Record Resource Extent</span> (A35)</th>
<td colspan="2">5664 paper files and digital records</td>
</tr>
</tbody>
<tbody>
<tr>
<th colspan="3" scope="rowgroup"><em>This entity is the source of the following
relations:</em></th>
</tr>
<tr class="header">
<th><em>Relation</em></th><th><em>Name (A28)</em></th><th><em>Identifier (A22)</em></th>
</tr>
<tr>
<th scope="row"><span class="relation">Record Set <span class="relation-name">includes or included</span> Record or Record Set</span> (R024)</th>
<td><a href="#WA-16-6" class="entity-in-example">London 2012 Olympic and Paralympic Games: Welsh Affairs Committee inquiry into tourism benefits; meetings between Minister for Culture, Welsh Language and Sport and Assembly Sponsored Bodies</a></td>
<td><a href="#WA-16-6" class="entity-in-example">WA 16/6</a></td>
</tr>
<tr>
<th scope="row"><span class="relation">Record Set <span class="relation-name">includes or included</span> Record or Record Set</span> (R024)</th>
<td><a href="#WA-16-QX-Z" class="entity-in-example">UKWO Programme Board 25_08_11- Papers 1 from S Krouwel 20110822.msg</a></td>
<td><a href="#WA-16-QX-Z" class="entity-in-example">WA 16/QX/Z</a></td>
</tr>
<tr>
<th scope="row"><span class="relation">Record Resource or Instantiation <span class="relation-name">documents</span> Activity</span> (R033)</th>
<td><a href="#L98" class="entity-in-example">Organisation of the London 2012 Olympic and Paralympic Games</a></td>
<td><a href="#L98" class="entity-in-example">L98</a></td>
</tr>
</tbody>
</table>

#### Entity of type Date E18: 2003-2016

<table>
<colgroup>
<col class="header-column" />
<col class="data-column-1" />
<col class="data-column-2" />
</colgroup>
<tbody>
<tr>
<th scope="row"><span class="entity-type">Entity type</span></th>
<td colspan="2">Date (E18)</td>
</tr>
</tbody>
<tbody>
<tr>
<th colspan="3" scope="rowgroup"><em>This entity has the following attributes:</em></th>
</tr>
<tr class="header">
<th scope="col"><em>Attribute</em></th>
<th scope="col" colspan="2"><em>Value</em></th>
</tr>
<tr>
<th scope="row"><span class="attribute">Identifier</span> (A22)</th>
<td colspan="2">dfg</td>
</tr>
<tr>
<th scope="row"><span class="attribute">Expressed date</span> (A19)</th>
<td colspan="2">2003-2016</td>
</tr>
<tr>
<th scope="row"><span class="attribute">Normalized date</span> (A29)</th>
<td colspan="2">2003/01/01-2016/12/31</td>
</tr>
</tbody>
<tbody>
<tr>
<th colspan="3" scope="rowgroup"><em>This entity is the source of the following
relations:</em></th>
</tr>
<tr class="header">
<th><em>Relation</em></th><th><em>Name (A28)</em></th><th><em>Identifier (A22)</em></th>
</tr>
<tr>
<th scope="row"><span class="relation">Date <span class="relation-name">is or was creation date of most members of</span> Record Set</span> (R083)</th>
<td><a href="#WA-16" class="entity-in-example">London 2012 Olympic and Paralympic Games: Digital and Paper Records</a></td>
<td><a href="#WA-16" class="entity-in-example">WA 16</a></td>
</tr>
</tbody>
</table>

#### Entity of type Record Set E03: London 2012 Olympic and Paralympic Games:
Welsh Affairs Committee inquiry into tourism benefits; meetings between Minister
for Culture, Welsh Language and Sport and Assembly Sponsored Bodies

<table id="WA-16-6">
<colgroup>
<col class="header-column" />
<col class="data-column-1" />
<col class="data-column-2" />
</colgroup>
<tbody>
<tr>
<th scope="row"><span class="entity-type">Entity type</span></th>
<td colspan="2">Record Set (E18)</td>
</tr>
</tbody>
<tbody>
<tr>
<th colspan="3" scope="rowgroup"><em>This entity has the following attributes:</em></th>
</tr>
<tr class="header">
<th scope="col"><em>Attribute</em></th>
<th scope="col" colspan="2"><em>Value</em></th>
</tr>
<tr>
<th scope="row"><span class="attribute">Identifier</span> (A22)</th>
<td colspan="2">WA 16/6</td>
</tr>
<tr>
<th scope="row"><span class="attribute">Name</span> (A28)</th>
<td colspan="2">London 2012 Olympic and Paralympic Games: Welsh Affairs Committee
inquiry into tourism benefits; meetings between Minister for Culture,
Welsh Language and Sport and Assembly Sponsored Bodies</td>
</tr>
<tr>
<th scope="row"><span class="attribute">Record Set Type</span> (A36)</th>
<td colspan="2">File (as defined in ISAD(G))</td>
</tr>
<tr>
<th scope="row"><span class="attribute">Language</span> (A25)</th>
<td colspan="2">English</td>
</tr>
<tr>
<th scope="row"><span class="attribute">Conditions of Access</span> (A08)</th>
<td colspan="2">Open</td>
</tr>
<tr>
<th scope="row"><span class="attribute">Record Resource Extent</span> (A35)</th>
<td colspan="2">1 file</td>
</tr>
</tbody>
<tbody>
<tr>
<th colspan="3" scope="rowgroup"><em>This entity is the source of the following
relations:</em></th>
</tr>
<tr class="header">
<th><em>Relation</em></th><th><em>Name (A28)</em></th><th><em>Identifier (A22)</em></th>
</tr>
<tr>
<th scope="row"><span class="relation">Record or Record Set <span class="relation-name">is or was included in</span> Record or Record Set</span> (R024i)</th>
<td><a href="#WA-16" class="entity-in-example">London 2012 Olympic and Paralympic Games: Digital and Paper Records</a></td>
<td><a href="#WA-16" class="entity-in-example">WA 16</a></td>
</tr>
</tbody>
</table>

#### Entity of type Date E18: 1st Jan 2005 - 31st Dec 2009

<table>
<colgroup>
<col class="header-column" />
<col class="data-column-1" />
<col class="data-column-2" />
</colgroup>
<tbody>
<tr>
<th scope="row"><span class="entity-type">Entity type</span></th>
<td colspan="2">Date (E18)</td>
</tr>
</tbody>
<tbody>
<tr>
<th colspan="3" scope="rowgroup"><em>This entity has the following attributes:</em></th>
</tr>
<tr class="header">
<th scope="col"><em>Attribute</em></th>
<th scope="col" colspan="2"><em>Value</em></th>
</tr>
<tr>
<th scope="row"><span class="attribute">Identifier</span> (A22)</th>
<td colspan="2">djp</td>
</tr>
<tr>
<th scope="row"><span class="attribute">Expressed date</span> (A19)</th>
<td colspan="2">2005 Jan 01 - 2009 Dec 31</td>
</tr>
<tr>
<th scope="row"><span class="attribute">Normalized date</span> (A29)</th>
<td colspan="2">2005/01/01-2009/12/31</td>
</tr>
</tbody>
<tbody>
<tr>
<th colspan="3" scope="rowgroup"><em>This entity is the source of the following
relations:</em></th>
</tr>
<tr class="header">
<th><em>Relation</em></th><th><em>Name (A28)</em></th><th><em>Identifier (A22)</em></th>
</tr>
<tr>
<th scope="row"><span class="relation">Date <span class="relation-name">is or was creation date of most members of</span> Record Set</span> (R083)</th>
<td><a href="#WA-16-6" class="entity-in-example">London 2012 Olympic and Paralympic Games: Welsh Affairs Committee inquiry into tourism benefits; meetings between Minister for Culture, Welsh Language and Sport and Assembly Sponsored Bodies</a></td>
<td><a href="#WA-16-6" class="entity-in-example">WA 16/6</a></td>
</tr>
</tbody>
</table>


#### Entity of type Record E04: UKWO Programme Board 25\_08\_11- Papers 1 from S Krouwel 20110822.msg

The following two tables describe a born-digital record and an instantiation of
it. Many of the attributes are the same: both have an identifier and a name and
they are both linked to the same date with the relation _is creation date of_.
One of the differences is the extent attributes where the attribute is specific
to the entity. The Record is described in terms that make sense to a human using
it: as one digital record. The Instantiation is described in terms of the
digital storage size of this specific file: one megabyte.

Note that the same attribute can mean something different when applied to
different entities. In this example the Conditions of Access of 'Open' for the
Instantiation means primarily that this actual file can be viewed by anyone,
whereas for the Record it could mean that there are no 'intellectual' obstacles
preventing it being available, for example no privacy issues or withholding of
permission to view from the owner. Alternatively, the Conditions of Access for
the Record might be 'Open' but for the Instantiation it could be 'Closed' if,
for example, the format was obsolete and there was currently no technology
available to read the file. If the record was physical the Record could be
'Open' but the Instantiation could be 'Closed' because it is too fragile to
produce.

<table id="WA-16-QX-Z">
<colgroup>
<col class="header-column" />
<col class="data-column-1" />
<col class="data-column-2" />
</colgroup>
<tbody>
<tr>
<th scope="row"><span class="entity-type">Entity type</span></th>
<td colspan="2">Record (E04)</td>
</tr>
</tbody>
<tbody>
<tr>
<th colspan="3" scope="rowgroup"><em>This entity has the following attributes:</em></th>
</tr>
<tr class="header">
<th scope="col"><em>Attribute</em></th>
<th scope="col" colspan="2"><em>Value</em></th>
</tr>
<tr>
<th scope="row"><span class="attribute">Identifier</span> (A22)</th>
<td colspan="2">WA 16/QX/Z</td>
</tr>
<tr>
<th scope="row"><span class="attribute">Name</span> (A28)</th>
<td colspan="2">UKWO Programme Board 25_08_11- Papers 1 from S Krouwel 20110822.msg</td>
</tr>
<tr>
<th scope="row"><span class="attribute">Language</span> (A25)</th>
<td colspan="2">English</td>
</tr>
<tr>
<th scope="row"><span class="attribute">Conditions of Access</span> (A08)</th>
<td colspan="2">Open</td>
</tr>
<tr>
<th scope="row"><span class="attribute">Record Resource Extent</span> (A35)</th>
<td colspan="2">1 digital record</td>
</tr>
</tbody>
<tbody>
<tr>
<th colspan="3" scope="rowgroup"><em>This entity is the source of the following
relations:</em></th>
</tr>
<tr class="header">
<th><em>Relation</em></th><th><em>Name (A28)</em></th><th><em>Identifier (A22)</em></th>
</tr>
<tr>
<th scope="row"><span class="relation">Record Resource <span class="relation-name">has or had instantiation</span> Instantiation</span> (R025)</th>
<td><a href="#WA-16-QX-Z-1" class="entity-in-example">UKWO Programme Board 25_08_11- Papers 1 from S Krouwel 20110822.msg</a></td>
<td><a href="#WA-16-QX-Z-1" class="entity-in-example">WA 16/QX/Z1</a></td>
</tr>
</tbody>
</table>

#### Entity of type Instantiation E06: UKWO Programme Board 25\_08\_11- Papers 1 from S Krouwel 20110822.msg

<table id="WA-16-QX-Z-1">
<colgroup>
<col class="header-column" />
<col class="data-column-1" />
<col class="data-column-2" />
</colgroup>
<tbody>
<tr>
<th scope="row"><span class="entity-type">Entity type</span></th>
<td colspan="2">Instantiation (E06)</td>
</tr>
</tbody>
<tbody>
<tr>
<th colspan="3" scope="rowgroup"><em>This entity has the following attributes:</em></th>
</tr>
<tr class="header">
<th scope="col"><em>Attribute</em></th>
<th scope="col" colspan="2"><em>Value</em></th>
</tr>
<tr>
<th scope="row"><span class="attribute">Identifier</span> (A22)</th>
<td colspan="2">WA 16/QX/Z1</td>
</tr>
<tr>
<th scope="row"><span class="attribute">Name</span> (A28)</th>
<td colspan="2">UKWO Programme Board 25_08_11- Papers 1 from S Krouwel 20110822.msg</td>
</tr>
<tr>
<th scope="row"><span class="attribute">Conditions of Access</span> (A08)</th>
<td colspan="2">Open</td>
</tr>
<tr>
<th scope="row"><span class="attribute">Instantiation Extent</span> (A23)</th>
<td colspan="2">Approximate size 1MB</td>
</tr>
<tr>
<th scope="row"><span class="attribute">Representation Type</span> (A37)</th>
<td colspan="2">Digital textual</td>
</tr>
</tbody>
<tbody>
<tr>
<th colspan="3" scope="rowgroup"><em>This entity is the source of the following
relations:</em></th>
</tr>
<tr class="header">
<th><em>Relation</em></th><th><em>Name (A28)</em></th><th><em>Identifier (A22)</em></th>
</tr>
<tr>
<th scope="row"><span class="relation">Instantiation <span class="relation-name">is or was instantiation of</span> Record Resource</span> (R025i)</th>
<td><a href="#WA-16-QX-Z" class="entity-in-example">UKWO Programme Board 25_08_11- Papers 1 from S Krouwel 20110822.msg</a></td>
<td><a href="#WA-16-QX-Z" class="entity-in-example">WA 16/QX/Z</a></td>
</tr>
</tbody>
</table>

Extent is a good example of where RiC-CM may not give you the granularity you
want when you come to implement your new RiC finding aid as Linked Data. The
example above uses the Record Resource Extent attribute to hold the short
sentence 'approx image size 1 MB' which may be enough for most users. But what
if someone is researching email archives and wants to know the average size of
an email in this series or in your whole collection. To answer this question,
you would need to split the digit from the rest of the text and then identify
the unit of measurement using the RiC-O [<u>Instantiation
Extent</u>](https://www.ica.org/standards/RiC/ontology#InstantiationExtent)
class. This allows you to describe the extent as an entity of its own with
separate properties for 'quantity' and 'unitOfMeasurement'.

<table id="WA-16-QX-Z-1">
<colgroup>
<col class="header-column" />
<col class="data-column-1" />
<col class="data-column-2" />
</colgroup>
<tbody>
<tr>
<th scope="row"><span class="entity-type">RiC-O class</span></th>
<td colspan="2"><a href="https://www.ica.org/standards/RiC/RiC-O_1-1.html#InstantiationExtent" class="entity-in-example">rico:InstantiationExtent</a></td>
</tr>
</tbody>
<tbody>
<tr>
<th colspan="3" scope="rowgroup"><em>This individual is the source of the following RiC-O datatype properties:</em></th>
</tr>
<tr class="header">
<th scope="col"><em>Datatype property</em></th>
<th scope="col" colspan="2"><em>Value</em></th>
</tr>
<tr>
<th scope="row"><span class="attribute"><a href="https://www.ica.org/standards/RiC/RiC-O_1-1.html#quantity" class="entity-in-example">rico:quantity</a></span></th>
<td colspan="2">1</td>
</tr>
<tr>
<th scope="row"><span class="attribute"><a href="https://www.ica.org/standards/RiC/RiC-O_1-1.html#unitOfMeasurement" class="entity-in-example">rico:unitOfMeasurement</a></span></th>
<td colspan="2">MB</td>
</tr>
</tbody>
<tbody>
<tr>
<th colspan="3" scope="rowgroup"><em>This individual is the source of the following RiC-O object properties:</em></th>
</tr>
<tr class="header">
<th><em>Object property</em></th><th><em>Name of target</em></th><th><em>Identifier of target</em></th>
</tr>
<tr>
<th scope="row"><span class="relation">rico:InstantiationExtent <span class="relation-name">rico:isExtentOf</span> rico:Instantiation</span></th>
<td><a href="#WA-16-QX-Z-1" class="entity-in-example">UKWO Programme Board 25_08_11- Papers 1 from S Krouwel 20110822.msg</a></td>
<td><a href="#WA-16-QX-Z-1" class="entity-in-example">WA 16/QX/Z1</a></td>
</tr>
</tbody>
</table>

#### Entity of type Date E18: 25th August 2011

<table>
<colgroup>
<col class="header-column" />
<col class="data-column-1" />
<col class="data-column-2" />
</colgroup>
<tbody>
<tr>
<th scope="row"><span class="entity-type">Entity type</span></th>
<td colspan="2">Date (E18)</td>
</tr>
</tbody>
<tbody>
<tr>
<th colspan="3" scope="rowgroup"><em>This entity has the following attributes:</em></th>
</tr>
<tr class="header">
<th scope="col"><em>Attribute</em></th>
<th scope="col" colspan="2"><em>Value</em></th>
</tr>
<tr>
<th scope="row"><span class="attribute">Identifier</span> (A22)</th>
<td colspan="2">hyp</td>
</tr>
<tr>
<th scope="row"><span class="attribute">Expressed date</span> (A19)</th>
<td colspan="2">25th August 2011</td>
</tr>
<tr>
<th scope="row"><span class="attribute">Normalized date</span> (A29)</th>
<td colspan="2">2011-08-25</td>
</tr>
</tbody>
<tbody>
<tr>
<th colspan="3" scope="rowgroup"><em>This entity is the source of the following
relations:</em></th>
</tr>
<tr class="header">
<th><em>Relation</em></th><th><em>Name (A28)</em></th><th><em>Identifier (A22)</em></th>
</tr>
<tr>
<th scope="row"><span class="relation">Date <span class="relation-name">is creation date of</span> Record Resource or Instantiation</span> (R080)</th>
<td><a href="#WA-16-QX-Z" class="entity-in-example">UKWO Programme Board 25_08_11- Papers 1 from S Krouwel 20110822.msg</a></td>
<td><a href="#WA-16-QX-Z" class="entity-in-example">WA 16/QX/Z</a></td>
</tr>
</tbody>
</table>

### Corporate Bodies

The following tables contain a minimal set of attributes selected from the
creators and the owners of records in the fonds WA. Using RiC-CM and linked data
we can link multiple bodies to the single fonds, providing a many to one link
between them.

#### Entity of type Corporate Body E11: Welsh Government

<table id="GB-NNAF-C287344">
<colgroup>
<col class="header-column" />
<col class="data-column-1" />
<col class="data-column-2" />
</colgroup>
<tbody>
<tr>
<th scope="row"><span class="entity-type">Entity type</span></th>
<td colspan="2">Corporate Body (E11)</td>
</tr>
</tbody>
<tbody>
<tr>
<th colspan="3" scope="rowgroup"><em>This entity has the following attributes:</em></th>
</tr>
<tr class="header">
<th scope="col"><em>Attribute</em></th>
<th scope="col" colspan="2"><em>Value</em></th>
</tr>
<tr>
<th scope="row"><span class="attribute">Identifier</span> (A22)</th>
<td colspan="2">GB/NNAF/C287344</td>
</tr>
<tr>
<th scope="row"><span class="attribute">Name</span> (A28)</th>
<td colspan="2">Welsh Government</td>
</tr>
</tbody>
<tbody>
<tr>
<th colspan="3" scope="rowgroup"><em>This entity is the source of the following
relations:</em></th>
</tr>
<tr class="header">
<th><em>Relation</em></th><th><em>Name (A28)</em></th><th><em>Identifier (A22)</em></th>
</tr>
<tr>
<th scope="row"><span class="relation">Agent <span class="relation-name">is creator of</span> Record Resource or Instantiation</span> (R027i)</th>
<td><a href="#WA" class="entity-in-example">Records created or inherited by the Bodies for Devolved Government in Wales</a></td>
<td><a href="#WA" class="entity-in-example">WA</a></td>
</tr>
</tbody>
</table>

#### Entity of type Date E18: 12th May 2011

<table>
<colgroup>
<col class="header-column" />
<col class="data-column-1" />
<col class="data-column-2" />
</colgroup>
<tbody>
<tr>
<th scope="row"><span class="entity-type">Entity type</span></th>
<td colspan="2">Date (E18)</td>
</tr>
</tbody>
<tbody>
<tr>
<th colspan="3" scope="rowgroup"><em>This entity has the following attributes:</em></th>
</tr>
<tr class="header">
<th scope="col"><em>Attribute</em></th>
<th scope="col" colspan="2"><em>Value</em></th>
</tr>
<tr>
<th scope="row"><span class="attribute">Identifier</span> (A22)</th>
<td colspan="2">fds</td>
</tr>
<tr>
<th scope="row"><span class="attribute">Expressed date</span> (A19)</th>
<td colspan="2">12th May 2011</td>
</tr>
<tr>
<th scope="row"><span class="attribute">Normalized date</span> (A29)</th>
<td colspan="2">2011-05-12</td>
</tr>
</tbody>
<tbody>
<tr>
<th colspan="3" scope="rowgroup"><em>This entity is the source of the following
relations:</em></th>
</tr>
<tr class="header">
<th><em>Relation</em></th><th><em>Name (A28)</em></th><th><em>Identifier (A22)</em></th>
</tr>
<tr>
<th scope="row"><span class="relation">Date <span class="relation-name">is beginning date of</span> Thing</span> (R069)</th>
<td><a href="#GB-NNAF-C287344" class="entity-in-example">Welsh Government</a></td>
<td><a href="#GB-NNAF-C287344" class="entity-in-example">GB/NNAF/C287344</a></td>
</tr>
</tbody>
</table>

#### Entity of type Corporate Body E11: Welsh Assembly Government

<table id="GB-NNAF-C287343">
<colgroup>
<col class="header-column" />
<col class="data-column-1" />
<col class="data-column-2" />
</colgroup>
<tbody>
<tr>
<th scope="row"><span class="entity-type">Entity type</span></th>
<td colspan="2">Corporate Body (E11)</td>
</tr>
</tbody>
<tbody>
<tr>
<th colspan="3" scope="rowgroup"><em>This entity has the following attributes:</em></th>
</tr>
<tr class="header">
<th scope="col"><em>Attribute</em></th>
<th scope="col" colspan="2"><em>Value</em></th>
</tr>
<tr>
<th scope="row"><span class="attribute">Identifier</span> (A22)</th>
<td colspan="2">GB/NNAF/C287343</td>
</tr>
<tr>
<th scope="row"><span class="attribute">Name</span> (A28)</th>
<td colspan="2">Welsh Assembly Government</td>
</tr>
</tbody>
<tbody>
<tr>
<th colspan="3" scope="rowgroup"><em>This entity is the source of the following
relations:</em></th>
</tr>
<tr class="header">
<th><em>Relation</em></th><th><em>Name (A28)</em></th><th><em>Identifier (A22)</em></th>
</tr>
<tr>
<th scope="row"><span class="relation">Agent <span class="relation-name">is creator of</span> Record Resource or Instantiation</span> (R027i)</th>
<td><a href="#WA" class="entity-in-example">Records created or inherited by the Bodies for Devolved Government in Wales</a></td>
<td><a href="#WA" class="entity-in-example">WA</a></td>
</tr>
</tbody>
</table>

#### Entity of type Corporate Body E11: The National Archives

<table id="66">
<colgroup>
<col class="header-column" />
<col class="data-column-1" />
<col class="data-column-2" />
</colgroup>
<tbody>
<tr>
<th scope="row"><span class="entity-type">Entity type</span></th>
<td colspan="2">Corporate Body (E11)</td>
</tr>
</tbody>
<tbody>
<tr>
<th colspan="3" scope="rowgroup"><em>This entity has the following attributes:</em></th>
</tr>
<tr class="header">
<th scope="col"><em>Attribute</em></th>
<th scope="col" colspan="2"><em>Value</em></th>
</tr>
<tr>
<th scope="row"><span class="attribute">Identifier</span> (A22)</th>
<td colspan="2">66</td>
</tr>
<tr>
<th scope="row"><span class="attribute">Name</span> (A28)</th>
<td colspan="2">The National Archives</td>
</tr>
</tbody>
<tbody>
<tr>
<th colspan="3" scope="rowgroup"><em>This entity is the source of the following
relations:</em></th>
</tr>
<tr class="header">
<th><em>Relation</em></th><th><em>Name (A28)</em></th><th><em>Identifier (A22)</em></th>
</tr>
<tr>
<th scope="row"><span class="relation">Agent <span class="relation-name">is or was holder of</span> Record Resource or Instantiation</span> (R039)</th>
<td><a href="#WA" class="entity-in-example">Records created or inherited by the Bodies for Devolved Government in Wales</a></td>
<td><a href="#WA" class="entity-in-example">WA</a></td>
</tr>
<tr>
<th scope="row"><span class="relation">Thing <span class="relation-name">has or had location</span> Place</span> (R075i)</th>
<td><a href="#Q1740301" class="entity-in-example">Kew</a></td>
<td><a href="#Q1740301" class="entity-in-example">Q1740301</a></td>
</tr>
</tbody>
</table>

### Places

#### Entity of type Place E22: Kew, Surrey

If The National Archives had branches in other parts of the country, additional
places could be added to the finding aid, enabling us to distinguish between the
various sites of the organization.

As places are included in other Linked Data graphs, the identifier for the place
is the URI used by [WikiData](https://www.wikidata.org/wiki/Q1740301) giving us
the opportunity to link to data sets outside of The National Archives.

<table id="Q1740301">
<colgroup>
<col class="header-column" />
<col class="data-column-1" />
<col class="data-column-2" />
</colgroup>
<tbody>
<tr>
<th scope="row"><span class="entity-type">Entity type</span></th>
<td colspan="2">Place (E22)</td>
</tr>
</tbody>
<tbody>
<tr>
<th colspan="3" scope="rowgroup"><em>This entity has the following attributes:</em></th>
</tr>
<tr class="header">
<th scope="col"><em>Attribute</em></th>
<th scope="col" colspan="2"><em>Value</em></th>
</tr>
<tr>
<th scope="row"><span class="attribute">Identifier</span> (A22)</th>
<td colspan="2"><a href="http://www.wikidata.org/entity/Q1740301" class="entity-in-example">wd:Q1740301</a></td>
</tr>
<tr>
<th scope="row"><span class="attribute">Name</span> (A28)</th>
<td colspan="2">Kew</td>
</tr>
</tbody>
<tbody>
<tr>
<th colspan="3" scope="rowgroup"><em>This entity is the source of the following
relations:</em></th>
</tr>
<tr class="header">
<th><em>Relation</em></th><th><em>Name (A28)</em></th><th><em>Identifier (A22)</em></th>
</tr>
<tr>
<th scope="row"><span class="relation">Place <span class="relation-name">is or was location of</span> Thing</span> (R075)</th>
<td><a href="#66" class="entity-in-example">The National Archives</a></td>
<td><a href="#66" class="entity-in-example">66</a></td>
</tr>
</tbody>
</table>

### Activities

#### Entity of type Activity E15: Organisation of the London 2012 Olympic and
Paralympic Games

With RiC-CM we are able to link disparate collections of records relating to the
same activity, as in this example where the organization of the London Olympic
and Paralympic games in 2012 are both linked to an Activity entity.

<table id="L98">
<colgroup>
<col class="header-column" />
<col class="data-column-1" />
<col class="data-column-2" />
</colgroup>
<tbody>
<tr>
<th scope="row"><span class="entity-type">Entity type</span></th>
<td colspan="2">Activity (E15)</td>
</tr>
</tbody>
<tbody>
<tr>
<th colspan="3" scope="rowgroup"><em>This entity has the following attributes:</em></th>
</tr>
<tr class="header">
<th scope="col"><em>Attribute</em></th>
<th scope="col" colspan="2"><em>Value</em></th>
</tr>
<tr>
<th scope="row"><span class="attribute">Identifier</span> (A22)</th>
<td colspan="2">L98</td>
</tr>
<tr>
<th scope="row"><span class="attribute">Name</span> (A28)</th>
<td colspan="2">Organisation of the London 2012 Olympic and Paralympic Games</td>
</tr>
</tbody>
<tbody>
<tr>
<th colspan="3" scope="rowgroup"><em>This entity is the source of the following
relations:</em></th>
</tr>
<tr class="header">
<th><em>Relation</em></th><th><em>Name (A28)</em></th><th><em>Identifier (A22)</em></th>
</tr>
<tr>
<th scope="row"><span class="relation">Activity <span class="relation-name">documented by</span> Record Resource or Instantiation</span> (R033i)</th>
<td><a href="#WA-16" class="entity-in-example">London 2012 Olympic and Paralympic Games: Digital and Paper Records</a></td>
<td><a href="#WA-16" class="entity-in-example">WA 16</a></td>
</tr>
<tr>
<th scope="row"><span class="relation">Activity <span class="relation-name">documented by</span> Record Resource or Instantiation</span> (R033i)</th>
<td>London Organising Committee of the Olympic and Paralympic Games: Policies and Processes: Records relating to the Competitions and the Ceremonies</td>
<td>LOC 4</td>
</tr>
<tr>
<th scope="row"><span class="relation">Activity <span class="relation-name">documented by</span> Record Resource or Instantiation</span> (R033i)</th>
<td>Arts Council England: Vision 2012 Team , Cultural Olympiad national funding for the London 2012 Olympics: digital records file plan
</td>
<td>ACE 1</td>
</tr>
</tbody>
</table>

## Conclusion

This section gives an idea of how RiC-CM could be used with an ISAD(G) style
finding aid. You can see that it is easy to map the fields between the two
approaches, and once this has been completed for your finding aid (or just a
part of it), you can progress to putting the data into RiC-O and realising the
benefits described in [int-ref](int-ref:what_are_the_benefits_of_using_ric) by
building the network of links.

[![London 2012 Olympics](../diagrams/london_2012_olympics.svg)](../diagrams/london_2012_olympics.svg)
