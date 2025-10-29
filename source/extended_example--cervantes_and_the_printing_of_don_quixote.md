What is this part about?
--------------------------

We present a narrative form example of extended archival description in RiC. We hope it may be a source of inspiration — the approach as much as the details.

We do not wish to suggest that every description in RiC will or should look like this: far from it. It is fully possible to express older and more traditional approaches in RiC: see [int-ref](int-ref:getting_started_with_ric) and [int-ref](int-ref:mappings). Many smaller modelling examples can be found in [int-ref](int-ref:faq--general_questions_and_smaller_modelling_questions). Think of this last part of the Application Guidelines as the fireworks at the finale!


Introduction
------------

In 1604, on the 11th of September in Valladolid, Antonio de Herrera y Tordesillas ([PARES](https://pares.mcu.es/ParesBusquedas20/catalogo/autoridad/143353?nm), [Wikipedia](https://en.wikipedia.org/wiki/Antonio_de_Herrera_y_Tordesillas)) wrote, in response to a memorial submitted to the Council of Castile ([PARES](https://pares.mcu.es/ParesBusquedas20/catalogo/autoridad/46623?nm), [Wikipedia](https://en.wikipedia.org/wiki/Council_of_Castile)) by Miguel de Cervantes ([PARES](https://pares.mcu.es/ParesBusquedas20/catalogo/autoridad/117180?nm), [Wikipedia](https://en.wikipedia.org/wiki/Miguel_de_Cervantes)) pertaining to the novel Don Quixote ([PARES](https://pares.mcu.es/ParesBusquedas20/catalogo/autoridad/120178?nm#), [Wikipedia](https://en.wikipedia.org/wiki/Don_Quixote)), that:

> se le podrá dar licencia para imprimille [a license to print it should be granted].

These [two records](https://pares.mcu.es/ParesBusquedas20/catalogo/description/12631375?nm) — Cervantes' memorial and Herrera's report — are of rather complex provenance, and fit into a rich context. Let us explore how RiC, along with complementary standards, can express aspects of this.


Councils
--------

By the time Cervantes wrote his memorial the kingdoms of Castile and Aragon, though still to a large degree distinct, had had a single monarch since the marriage of Queen Isabella I of Castile ([PARES](https://pares.mcu.es/ParesBusquedas20/catalogo/autoridad/46207), [Wikipedia](https://en.wikipedia.org/wiki/Isabella_I_of_Castile)) and King Ferdinand II of Aragon ([PARES](https://pares.mcu.es/ParesBusquedas20/catalogo/autoridad/46340?nm), [Wikipedia](https://en.wikipedia.org/wiki/Ferdinand_II_of_Aragon)) in the 15th century. In addition to making up roughly the mainland of modern Spain, the one or the other of the kingdoms controlled what is now referred to as the Spanish empire (including much of the Americas and considerable parts of Europe).

Governance was through entities known as <a href="https://en.wikipedia.org/wiki/Polysynodial_System">councils</a> (consejos), one each originally for Castile and Aragon, these pre-dating the unification of their crowns. Gradually numerous councils were split off from these two, with responsibility either for a particular territory, for example the Council of the Indies ([PARES](https://pares.mcu.es/ParesBusquedas20/catalogo/autoridad/46286?nm), [Wikipedia](https://en.wikipedia.org/wiki/Council_of_the_Indies)), or for a particular function, for example the Council of Finance ([PARES](https://pares.mcu.es/ParesBusquedas20/catalogo/autoridad/50914?nm)); both had their origin in the Council of Castile. Councils were also created from scratch, the most important of which had both kingdoms within their remit, for example the Council of State ([PARES](https://pares.mcu.es/ParesBusquedas20/catalogo/autoridad/46620?nm), [Wikipedia](https://en.wikipedia.org/wiki/Spanish_Council_of_State)).

That Herrera was in Vallodolid situates our two records at a quite specific point in time. The royal court in Castile, to which the Council of Castile was attached, had been in Madrid for several decades until 1601, and moved to Valladolid only from 1601 to 1606, whereupon it moved permanently back to Madrid. This event is of archival significance because in conjunction with the move a transfer of some records of the Council of Castile to Simancas was made, along with records of certain of the other councils.


Simancas
--------

Let us pause to discuss the General Archive of Simancas ([PARES](https://pares.mcu.es/ParesBusquedas20/catalogo/autoridad/46558?nm), [Wikipedia](https://en.wikipedia.org/wiki/Archivo_General_de_Simancas)) a little; it is important both for its holdings and its history. In RiC, one would primarily regard an archive as a Corporate Body, namely as an institution working with archival material; in this sense, the General Archive of Simancas was founded around sixty years before Cervantes' request, as we shall discuss in more detail below. Secondly, an archive usually has a physical location, Place in RiC; in the case of the General Archive of Simancas, its purpose-built location within the pre-existing Castle of Simancas is regarded as having being completed in the 1580s. We can model this as follows.

[![General archive of Simancas](../diagrams/general_archive_of_simancas.svg)](../diagrams/general_archive_of_simancas.svg)

The date given here for the founding of the General Archive of Simancas comes from a [royal decree](https://pares.mcu.es/ParesBusquedas20/catalogo/description/12883369?nm) of the 16th of September 1540. It stipulates that certain documents be sent to Juan Mosquera de Molina, an official (alcaide: commandant/warden) at the Castle of Simancas — Simancas is not mentioned explicitly. We could embellish the above modelling as follows to capture this, noting that the RiC relation _has or had authority over_ only implies some kind of authority, not over-arching authority. Included is the nuance that the decree was, apart from the signature, actually written not by the king but by Juan Vázquez de Molina ([PARES](https://pares.mcu.es/ParesBusquedas20/catalogo/autoridad/168028?nm), [Wikipedia](https://es.wikipedia.org/wiki/Juan_V%C3%A1zquez_de_Molina)) (in Flanders, as it happens, though we do not include this in the diagram!).

[![General archive of Simancas — royal decree](../diagrams/general_archive_of_simancas--royal_decree.svg)](../diagrams/general_archive_of_simancas--royal_decree.svg)


Records of the Council of Castile I
-----------------------------------

Although the _Collection of the Council of Castile_ in the two diagrams above is [described](https://pares.mcu.es/ParesBusquedas20/catalogo/description/117085) as a fonds, the holdings at Simancas encompass only a small proportion of the archived records of the Council of Castile. Of these, apart from those mentioned earlier which were sent to Simancas in 1606, many — mainly older, including those specified in the founding royal decree of 1540 — were organized and collected through the work of Diego de Ayala, the first archivist at Simancas, between his appointment by royal decree in 1561 (along with a second archivist who died shortly afterwards, in 1563) and his death in 1594. Almost all other records travelled to Madrid with the royal court. The following diagram models all of this. Here _Records of the Council of Castile held at Simancas_ is the same as _Collection of the Council of Castile_ above; a different terminology has been chosen for clarity.

[![Records of the Council of Castile](../diagrams/records_of_the_council_of_castile.svg)](../diagrams/records_of_the_council_of_castile.svg)

Any model in RiC can be understood as having an 'open-world' semantics: information can always be added for a higher degree of nuance and accuracy. Here details could be included from the royal decree mandating Diego de Ayala's appointment as head archivist at Simancas, or Record Sets corresponding to accruals at Simancas after 1606 could be brought in.

Points of note in the modelling include the following.

1. A distinction is available in RiC between the end date of a Record Set and the last date of creation of a Record in that Record Set. A Record Set might indeed have been 'open' for a period of time after the last record belonging to it was created — as long as an organization existed, for example, if the Record Set documents the activities of that organization. Both variants appear in the model, by means of the relations _has end date_ and _has or had all members with creation date_ (the latter being a period of time): that all of the records of the Council of Castile held at Simancas were created between 1437 and 1648 [comes from PARES](https://pares.mcu.es/ParesBusquedas20/catalogo/description/117085); whilst we can at least say that the last record arranged by Diego de Ayala was created before his death, even if we do not have the exact date.
2. As in [int-ref](int-ref:case_study--how_might_ric_be_of_use_to_indigenous_communities_and_other_minority_groups:challenging-over-reliance-on-sources) and [int-ref](int-ref:case_study--how_might_ric_be_of_use_to_indigenous_communities_and_other_minority_groups:weaving-together-fragments), free use has been made of the Record Set entity as an intellectual abstraction; namely that, unlike a Record, it is not required to have an Instantiation, as discussed in [int-ref](int-ref:faq--the_instantiation_entity:instantiations-of-record-sets). For instance, though _Records of the Council of Castile arranged by Diego de Ayala_ is a meaningful aggregation intellectually and plays a useful role in the model, it does not have a physical counterpart: the collections of records which Diego de Ayala arranged are stored here and there at Simancas, within the physical incarnations of the fonds and series which they are identified in PARES as belonging to — the fact that Diego de Ayala arranged them was not a principle which had an immediate bearing on their physical organization.

    On the other hand, as is likely for any Record Set corresponding to a traditional archival entity such as a fonds or series, _Records of the Council of Castile held at Simancas_ does have an Instantiation; whilst _Records of the Council of Castile held at the royal court after its move to Madrid in 1606_ may have had one.
3. The two Activities in the diagram each have an _Activity Type_ attribute corresponding to a fundamental archival practice: arrangement and accrual. Classifying an Activity in this way is important for discovery — allowing arrangement and accrual to be used as entry points — as well as for inter-operability. See [int-ref](int-ref:faq--how_to_describe_activities_such_as_digitization_appraisal_or_disposition) for further discussion.
4. In the model, Event is used once, and Activity twice. As discussed in [int-ref](int-ref:faq--general_questions_and_smaller_modelling_questions:can-you-elaborate-upon-the-difference-between-activity-and-event), RiC-CM defines the difference between the two as follows.

    > An Activity is an agent designed and performed event that has an intended purpose or purposes.

    The movement of the royal court to Madrid, though it had archival consequences, was not made for archival reasons; it 'simply happened' from an archival point of view, hence we have regarded it as an Event. The two Activities in the model, on the other hand, correspond to archival practices, i.e. were carried out with the involvement of an archivist, with intended archival repercussions.
5. It is almost always the case in RiC that a relation or attribute can be used more than once for the same entity, as _has or had location_ is in the diagram. That the Habsburg royal court had both Valladolid and Madrid as locations would likely prompt somebody for whom this is significant to dig more deeply to understand it; in this way, the flexibility can facilitate discovery, which can be aided by inclusion of meta-metadata (as discussed in [int-ref](int-ref:faq--general_questions_and_smaller_modelling_questions:do-you-have-examples-illustrating-chapter-6-of-ric-cm)), and/or by rich surrounding description.

   To elaborate a little, in this context RiC allows for the elaboration upon relations by certain attributes, as mentioned in [int-ref](int-ref:faq--general_questions_and_smaller_modelling_questions:do-you-have-examples-illustrating-chapter-6-of-ric-cm). Here for instance Date of Relation could be used in conjunction with _has or had location_ to express that the court was at Valladolid from 1601 to 1606, and similarly for Madrid.

    RiC-O makes use of a technical device known as an n-ary relation class to formalise relation attributes. It could look as follows in this case, where [rico:PlaceRelation](https://www.ica.org/standards/RiC/RiC-O_1-1.html#PlaceRelation) is the n-ary relation class, and the relation _is associated with place_, of which _has or had location_ is a sub-relation, becomes a shortcut for the path consisting of the two horizontal arrows in the diagram. We mean 'shortcut' only informally here, but in fact it exists in a formal sense in RiC-O, albeit one more arrow would have been needed in the diagram — we shall not go into this further here.

[![Dates in Valladolid](../diagrams/dates_in_valladolid_relation_attribute.svg)](../diagrams/dates_in_valladolid_relation_attribute.svg)


Records of the Council of Castile II
------------------------------------

Literature was censored in Habsburg Spain at the time, and requests for licenses for printing such as Cervantes' were handled by the Escribanía de Cámara (Notary of the Chamber). Thus Cervantes' memorial and Herrera's report belonged to the sub-fonds [Escribanía de cámara de Ayala. Consejo de Castilla](https://pares.mcu.es/ParesBusquedas20/catalogo/description/1538322) corresponding to the notary in office at the time (Ayala —  not the archivist at Simancas) — specifically to the series [Expedientillos de la Escribanía de Ayala. 1606](https://pares.mcu.es/ParesBusquedas20/catalogo/description/12631373).

These records were amongst those which moved with the royal court to Madrid. Over the next couple of centuries, they remained at the part of the court handling matters of justice: the offices of the subsequent notaries [Pinilla](https://pares.mcu.es/ParesBusquedas20/catalogo/autoridad/10069?nm), [Escariche](https://pares.mcu.es/ParesBusquedas20/catalogo/autoridad/10067?nm), [Granados](https://pares.mcu.es/ParesBusquedas20/catalogo/autoridad/10068?nm), [Carranza](https://pares.mcu.es/ParesBusquedas20/catalogo/autoridad/10066?nm), and [Vicario](https://pares.mcu.es/ParesBusquedas20/catalogo/autoridad/10070?nm) inherited the records of their predecessors. The Ancien Régime gradually fell, and the Council of Castile was dissolved in 1834; the [Supreme Court](https://pares.mcu.es/ParesBusquedas20/catalogo/autoridad/48873?nm) and [Ministry of Grace and Justice](https://pares.mcu.es/ParesBusquedas20/catalogo/autoridad/48968), both enshrined in Spain's constitution of 1812, took over its role with respect to justice.

The records of the Council of Castile fell into a certain state of neglect; a need to address this was recognized, but Simancas had no space to receive them. Eventually — omitting the details of various earlier alleviations — the National Historical Archive ([PARES](https://pares.mcu.es/ParesBusquedas20/catalogo/autoridad/48087?nm), [Wikipedia](https://en.wikipedia.org/wiki/National_Historical_Archive_(Spain))) was constructed in the second half of the nineteenth century, and between 1896 and 1899 the fonds of the Council of Castile held at the Supreme Court and the Ministry of Grace and Justice, as well as at the Council of State, were sent there.


Cervantes' memorial and Herrera's report belonged by this time to the series [Archivo Antiguo de Consejo. Consultas y Decretos](https://pares.mcu.es/ParesBusquedas20/catalogo/description/7306718) (Ancient Archive of the Council. Consultations and Decrees), compiled from the records of Escribanías de Cámara (Notaries of the Chamber) around the time of the dissolving of the Council of Castile in the 1830s. It is not clear which of the afore-mentioned three institutions held this series, but if we assume for the sake of concreteness that it was the Supreme Court, we can model much of all this as follows.

[![Transfer to Archivo Histórico Nacional](../diagrams/transfer_to_national_historical_archive.svg)](../diagrams/transfer_to_national_historical_archive.svg)

The relation attribute Certainty of Relation in RiC-CM could have been used in the model in conjunction with the _has or had holder_ and _is or was performed by_ relations in the model which point to the Supreme Court to indicate that they are uncertain, or more precisely that they express one of three possibilities.


Extraction of Cervantes' memorial
---------------------------------

In the 1980s, archivists at the National Historical Archive made the decision to extract into a new Record Set ([Colección de pergaminos y documentos del Consejo de Castilla](https://pares.mcu.es/ParesBusquedas20/catalogo/description/12631375?nm)) records of the Council of Castile whose instantiations were identified as vulnerable from a conservation or display point of view. Cervantes' memorial and Herrera's report were moved into this Record Set (both intellectually and physically — the new Record Set has an Instantiation: the Instantiations of the Records belonging to it are held together, not in their original locations) around 2011-12, when a high level of interest in and requests for consultation of the material led to conservation concerns.

As the description of this new Record Set in PARES draws attention to, the creation of it did not adhere to traditional organic provenance principles, though much had already been lost in this regard by the time of the transfer to the National Historical Archive — the arrangement of records following the move did not necessarily much ameliorate the situation, it seems. RiC's conception of a Record Set, explored in [int-ref](int-ref:faq--record_or_record_set), [int-ref](int-ref:faq--the_instantiation_entity:instantiations-of-record-sets), and [int-ref](int-ref:case_study--how_might_ric_be_of_use_to_indigenous_communities_and_other_minority_groups), does, though, fully encompass definition according to conservation criteria, the decentralized nature of RiC allowing for the provenance to be as accurately expressed in this case as in a hierarchical approach. We illustrate one way to model it in this case below — one could include more, as one almost always can!

[![Extraction of Cervantes' memorial](../diagrams/extraction_of_cervantes_memorial.svg)](../diagrams/extraction_of_cervantes_memorial.svg)

Given that RiC makes a careful distinction between record resources and their instantiations, one might balk a little at the above: is it not solely a matter of the original instantiation of Cervantes' memorial, so that it is wrong to refer above to the extraction of the latter as a record? A Record, though, is more in RiC than its contents: all aspects of its context, as far as these are relevant archivally, play a role in defining it. That certain instantiations of a record are conservationally vulnerable is both relevant for an archivist working with the record and has implications for users of the record. The regarding of Cervantes' memorial as belonging to a new Record Set expresses this, adding a new layer of context to Cervantes' memorial as a Record. In this way, RiC's conception of a Record is a dynamic one: over time, a record's context can be added to and refined.


Broader cultural heritage aspects
---------------------------------

As discussed in [int-ref](int-ref:faq--general_questions_and_smaller_modelling_questions:is-describing-the-content-of-a-record-within-rics-domain), whilst the content of a Record is a priori outside the domain of RiC, RiC allows for and encourages the use of other standards to this end. Let us give an example of this.

Cervantes' memorial contains his signature, which is of both archival — with regard for example to the authoritativeness of the memorial as a Record — and wider scholarly significance; it would be appropriate to model it in RiC as a Record Part. We could assert in free-text, by means of the Scope and content attribute or via an Activity, that the content of this Record Part is Cervantes' signature, but RiC cannot directly express this in a structured way.

In [CIDOC CRM](https://cidoc-crm.org/), though — discussed in [int-ref](int-ref:combining_ric_with_other_standards:other-kinds-of-cultural-heritage-objects) — Cervantes' signature can be modelled as both a [Mark](http://cidoc-crm.org/cidoc-crm/7.1.3/E37_Mark) and an [Appellation](http://cidoc-crm.org/cidoc-crm/7.1.3/E41_Appellation), viewing the memorial in which it appears as a [Document](http://cidoc-crm.org/cidoc-crm/7.1.3/E31_Document). We can view Cervantes himself as an [Actor](http://cidoc-crm.org/cidoc-crm/7.1.3/E39_Actor), and make use of the properties [shows visual item](http://cidoc-crm.org/cidoc-crm/7.1.3/P65_shows_visual_item) and [is identified by](http://cidoc-crm.org/cidoc-crm/7.1.3/P1_is_identified_by) in the manner illustrated below. One could go much further in this direction!

[![Cervantes' signature](../diagrams/cervantes_signature.svg)](../diagrams/cervantes_signature.svg)


Ransoming of Cervantes
----------------------

Cervantes had an eventful life! It is not only as the author of the memorial on the printing of Don Quixote that he appears in the archives of the Councils, as we shall now explore a little.

In the early 1570s, Cervantes served as a soldier, but was captured at sea by pirates, along with his brother, in 1575; for several years he was held for ransom in Algiers. Cervantes' mother, Leonor de Cortinas, worked to free her sons; a [royal decree from 1576](http://www.universocervantes.com/archivo-documental/2) details the granting to her of 60 escudos to this end. In 1578 the [Council of War](https://pares.mcu.es/ParesBusquedas20/catalogo/autoridad/46764), one of the territory-wide councils which [took form in the 1500s](#councils), granted merchandise valuing 2000 ducats towards the paying off Cervantes' ransom, in view of his good service — albeit that she had requested 8000 ducats' worth! A [transcript](https://www.cultura.gob.es/va/dam/jcr:cb292c05-5e31-43df-95aa-c7ca05bcdd9b/18-gym-lib-34-2-66.pdf) of the record of this is available.

Meanwhile, Cervantes' father, Rodrigo de Cervantes, lobbied for his release too. This is documented by a record of the Council of the Indies ([PARES](https://pares.mcu.es/ParesBusquedas20/catalogo/autoridad/46286), [Wikipedia](https://en.wikipedia.org/wiki/Council_of_the_Indies)), again from 1578, belonging to the Record Set [Expediente sobre los méritos y servicios de Miguel de Cervantes Saavedra](https://pares.mcu.es/ParesBusquedas20/catalogo/description/126853) (Dossier on the merits and services of Miguel de Cervantes Saavedra) which is held at the General Archive of the Indies ([PARES](https://pares.mcu.es/ParesBusquedas20/catalogo/autoridad/46555?nm), [Wikipedia](https://en.wikipedia.org/wiki/General_Archive_of_the_Indies)). That the provenance principle behind the formation of this dossier was one of subject matter is no hindrance in RiC.

In the diagram below we suggest a way in RiC to place both of these records, along with a third which also belongs to the afore-mentioned dossier, into the context of the ransoming of Cervantes. We include Cervantes' memorial on the printing of Don Quixote to illustrate how Cervantes can be seen as providing a bridge between archival contexts.

[![Concerning Cervantes' ransom](../diagrams/cervantes_ransom.svg)](../diagrams/cervantes_ransom.svg)


Beyond the traditional archival context
---------------------------------------

The use of archives — in legal matters, for research, and so on — situates the archival domain in a very broad context. Whilst the latter is not directly within RiC's scope, RiC does allow for building a bridge from the archives to the uses of archival records in the world beyond. Let us discuss how in a couple of examples.

In Spain, a project was begun a few years ago linking archival materials to scholarly documents citing them, resulting in the online catalogue [MetaPARES](https://pares.cultura.gob.es/metapares/inicio). Though it is not complete at the time of writing, there are already [quite a number](https://pares.cultura.gob.es/metapares/generalSearchForm?textGen=Cervantes&pagNum=1&pagSize=10) of entries pertaining to Cervantes.

[One of these](https://pares.cultura.gob.es/metapares/vistaunica?id=235742522) concerns an [article from 2016](https://analescervantinos.revistas.csic.es/index.php/analescervantinos/article/view/325) bringing to light new biographical details on Cervantes, these coming from certain records held at the Archivo General de Indias. The article contains within it transcriptions of these records. In the diagram below we suggest how in RiC one might bring the article into the archival description context. This enriches the latter — facilitating the discovery of the transcriptions, for instance — as well as the wider scholarly context in which it resides.

[![New biographical details](../diagrams/new_biographical_details.svg)](../diagrams/new_biographical_details.svg)

Here, in addition to RiC, we have made use of the [Bibliographic Ontology](https://www.dublincore.org/specifications/bibo/), [Dublin Core](https://www.dublincore.org/specifications/dublin-core/dcmi-terms/), and the [RDF schema](https://www.w3.org/TR/rdf11-schema/). A few points of note:

1. As discussed in [int-ref](int-ref:faq--the_instantiation_entity:when-does-a-derived-instantiation-represent-a-new-record), an Instantiation derived from another, such as the transcription in the diagram above, might be regarded as an Instantiation of a new Record; this is a matter of judgement. That we have not introduced such a new Record into the diagram is primarily because the transcription, being found within the text of the research article, arguably has a relatively subservient character — easing the reading of the source materials to which the article refers, for instance — and thus perhaps does not have the import which judging it a new Record might be thought to imply.
2. We see how Thing is useful when forming a bridge between RiC and other domains; several relations in RiC allow Thing in their domain, range, or both, and it can be very helpful, as in the diagram, to employ these in such cases.
3. The diagram illustrates how RiC allows for making contact with broader conceptions of a document. From a bibliographic point of view, the Record in the diagram is indistinguishable ontologically from any other cited document; within RiC it is something more.

Let us explore a second example. The intellectual Dámaso Alonso ([PARES](https://pares.mcu.es/ParesBusquedas20/catalogo/autoridad/142688), [Wikipedia](https://en.wikipedia.org/wiki/D%C3%A1maso_Alonso)) explored material in the reading rooms of the National Historical Archive (as well the General Archive of the Indies and other Spanish archival institutions); the Record Set [Expediente de investigación del Archivo Histórico Nacional correspondiente a Dámaso Alonso Fernández de las Redondas](https://pares.mcu.es/ParesBusquedas20/catalogo/description/13002913) (Research file of the National Historical Archive relating to Dámaso Alonso) documents his studies.

Alonso was also a noted Cervantes scholar; for instance, in 1969, he wrote the essay _Oscillation in the character of Sancho_. In the diagram below we suggest one way in which both the latter work and the research file could be joined in RiC via Dámaso Alonso, making use of the same three additional standards. As well as simply enriching the context of Cervantes' memorial, this might allow for influences upon Alonso's work of archival or wider scholarly significance to more readily be perceived.

[![Dámaso Alonso link to Cervantes](../diagrams/alonso_link_to_cervantes.svg)](../diagrams/alonso_link_to_cervantes.svg)
