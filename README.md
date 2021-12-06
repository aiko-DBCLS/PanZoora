# PanZoora
PanZoora is a database for prevention of pandemics caused by zoonoses to link related notes and publications data annotated on PubAnnotation/TextAE.

## About_PanZoora_1
PanZoora consists two parts basically, "lexical cues" picked up and annotated from publications and "notes" beyond/connected meanings with papers.

## About_PanZoora_2
I am not a physician, ecologist and specialist for each animal just an annotator. I would appreciate any your comments and suggestions.

## About_PanZoora_3
Lexical cues parts; each publications related zoonoses from PubMed was annotated manually using [PubAnnotation/TextAE](https://pubannotation.org/). A few but I believe manually annotated data will support you. A basic usage of PubAnnotation is for numbers of publications and automatical annotation. Same time PubAnnotation provides us the simple and easy way to share data using URLs. Using this cool system, PanZoora would present you a new style of data shown.

## About_PanZoora_4
Marked up key words were not only listed both original and translated to Japanese but linked to IDs of MeSH, Gene and Taxonomy basically and URLs on PubAnnotation. You can easy to get exact positions those key words on the papers via PubAnnotation. Sets of cues, external information and positions are important for NLP, aren't they?

## About_PanZoora_5
Notes; our knowledge for zoonoses are shortage and whenever we want to know them well the situations would be emergency. One of the efficient ways is collect and connect with any information related them and find many ways for resolving of them. For more spending the time to think and discuss, and making them better, DBs should be easy to show you more meaningful data. Here it is called just "notes" temporally.

## About_PanZoora_6
We have to caution for other zoonoses may happen to be caused by our any behaviors even though manage to prevent one zoonosis. Zoonoses are so complicated and connected to each other. PanZoora might support your new notice to them by showing other risks or sides of zoonoses.

## Details_common_tables_1
Two common tables are PanZoora_table_Categories and PanZoora_table_SpeciesZoonoses for both publication data and notes.

## Details_common_tables_2
PanZoora_table_Categories; Category-id gives each category of zoonoses and is used in tables below.

## Details_common_tables_3
PanZoora_table_SpeciesZoonoses; Species-Zoonoses-id gives each species as Sp-id (including categories) or zoonosis as Zoonosis-id (including categories) and is used in tables below.

## Details_lexis_tables_1
One main and four children are tables, PanZoora_table_lexisMain, PanZoora_table_lexisOnTextAE, Panzoora_table_lexisGroup, PanZoora_table_DicID and PanZoora_table_lexisDic, respectively, for publication data.

## Details_lexis_tables_2
PanZoora_table_lexisMain; lexisMain-id gives each set of lexisGroup-id, Species-Zoonoses-id, spZooCategory-id and Category-id used in common and child tables.

## Details_lexis_tables_3
Panzoora_table_lexisGroup; lexisGroup-id gives each annotated group of lexisOnTextAE-ids used in PanZoora_table_lexisOnTextAE for putting and categorizing of cues together.

## Details_lexis_tables_4
PanZoora_table_lexisOnTextAE; lexisOnTextAE-id gives each set of lexicalTextAE-span, lexisDic-id, Dic-id and PubMed-id. lexicalTextAE-span is the URL of the cue on the external web application, PubAnnotation/TextAE.

## Briefs_of_PubAnnotation/TextAE_1
Brief descriptions of [PubAnnotation/TextAE](https://pubannotation.org/): 
PubAnnotation/TextAE shows you annotated cue as URL. Once access to it, you can get results selecting buttons listed on the middle of the page as tab, tsv or json format which you like. This URL (span) is just for a selected cue. Click PubMedID shown the left upper of the page and below Zoonoses button to reselect whole cues and annotated results of one literature, PubAnnotation/TextAE prepared you all results. You easily access all of them as the same way above.

## Briefs_of_PubAnnotation/TextAE_2
PubAnnotation also provides you whole results of this PanZoora project as tgz format. Click Zoonoses button shown the left upper of the page and move to top page of Zoonoses project. Annotations, third area of the page, prepared you Download button. Tsv or json folders are included in annotations folder. Each literature-named file contains annotated results.

## Details_lexis_tables_5
PanZoora_table_DicID; Dic-id gives each set of lexicalCue, exactID and synonymID. exactIDs are exact matched to MeSH, Gene and Taxonomy (sometimes GlyTouCan ID or URL of other ontology) and synonymIDs are a little different but similar to them, or just memo. Added standard words to lexicalCue when it is original or typo.

## Details_lexis_tables_6
PanZoora_table_lexisDic; lexisDic-id gives each set of lexicalCue and lexicalCue_jpn (translated to Japanese). Added standard words to lexicalCue when it is original or typo.

## Others_1
ZoonosesDic; this is not a table of PanZoora. Just a simple use example of connected PanZoora_table_DicID and PanZoora_table_lexisDic. It may help you as one of zoonotic dictionary connected with external ontology IDs.

## Details_note_tables_1
One main and two children are tables, PanZoora_table_relatedNote, PanZoora_table_NoteOnTextAE and PanZoora_table_Note, respectively, for notes data.

## Details_note_tables_2
PanZoora_table_relatedNote; relatedNote-id gives each set of Species-Zoonoses-id, spZooCategory-id, Category-id and NoteOnTextAE-id used in common and child tables.

## Details_note_tables_3
PanZoora_table_NoteOnTextAE; NoteOnTextAE-id gives each set of Note-id, NoteTextAE-span and PubMed-id. NoteTextAE-span is the URL of the whole or a part of sentence on the external web application, PubAnnotation/TextAE.

## Details_note_tables_4
PanZoora_table_Note; Note-id gives each set of Note and Note_jpn (translated to Japanese). These notes are not exact same what each publication tells us but similar to when we read through some publications. PanZoora would shorten your spending time for reading and searching zoonotic information.

## Details_note_tables_5
A few but some data in PanZoora_table_NoteOnTextAE have no URLs. There are two types and not bugs. One of them is categories of Japanese Act, cited from HPs of Japanese government, not exists in Zoonoses project on PubAnnotation/TextAE as publications. The other is a shortage of evidences what the text want to show you on publications stored in PanZoora at present, but could guess indirectly. This is one of challenges on PanZoora. It is not standard way but I prefer to relate meanings of data and show you rather than not entry them. Someday exact matched paper will be found from huge numbers of publications and could register URLs of them.

## Others_2
[PanZooraView](http://togodb.org/db/panzooraview); this is also not a table of PanZoora but exactly what I want to show you. The web pages or dynamic somethings are ordinal form but I have no skills and this is the only way which I can show you.
### About_PanZooraView_1
Using advanced search button listed on the bottom of center of TogoDB, you can select contexts from PanZoora by putting keywords, the name of zoonoses, species or categories. Those results are connected with different publications, other species or zoonoses and show you the different point of views and extra information.
### About_PanZooraView_2
Sorry, the viewer of PanZoora has no pulldown menu. It is hard for you to search what PanZoora stored in TogoDB using this.

## About_PanZoora_7
Both Species-Zoonoses-id and spZooCategory-id show species which have zoonotic disease or pathogens, or show zoonoses. The former is exactly the same written in publications and the latter is groups including the former. Formal rules of grouping have not decided yet and there are differences categorized standards. Some categories might be changed in future.

## About_PanZoora_8
Most data were just annotated and cited from abstract of publications. There is many valuable information in full texts. Please follow them if you have any interests.

## About_PanZoora_9
PanZoora has been continuously updating, revising partial error and adding new records. Just inform dates at column of Last-updated (or Registered) against insignificant changes for avoiding abundant notices.

## Details_other_tables_1
PanZoora_relateNote_and_lexis; this is a table but not any use for other tables of PanZoora. This table connect PanZoora_table_lexisMain (publication data) and PanZoora_table_relatedNote (notes). relatedNote-id shows set of Species-Zoonoses-id, spZooCategory-id, Category-id and lexisMain-id. When you need superordinate concept from cues (words) on each publication, this may be what you want.

## Messages_from_PanZoora_1
Need further information and surveillance about zoonotic vector animals especially bats and primate, globally. But also need PPEs when contact with them for preventing next artificial zoonoses, because as you know those animals are the trigger or most human-like ones. Zoonoses are complicated diseases in which pathogens, reservoirs, intermediate vectors, hosts and patients take part intricately, as it were invisible spider webs. Not only share points of dangerous and ways for preventing zoonoses but should provide suitable PPEs if they don't prepare for One-Health surveillance (especially low-income areas). PPEs are more expensive than treatment cost of millions of people and global economic loss caused by lockdown? It may not easy to find keys or links of zoonoses but continuous supports are needed for never ever cause next pandemics ourselves.

## Messages_from_PanZoora_2
Of course, not only for animal researches but for low-middle income areas where long shortage of any PPEs and medical disposables to treat patients we should provide those items. Even a few sets of them, medical workers in those areas really want to get and those prevent new transmissions between them, patients and their families. Unfortunately, any outbreaks may occur but control them and prevent them to become pandemics is one of the best ways for all humans living on the earth. In total, many lives become safe by a few PPEs. When you have unneeded ones, please think about them again.

## Messages_from_PanZoora_3
If humans were bats and birds, we could overcome pandemics? Most of them are asymptomatic for fatal zoonoses to most mammals. They can live safely and coevolve with zoonotic pathogens. They can fly and move where they want. Bats are the most evolved mammals? It is unfortunate happenings or errors for those pathogens transmitted living things stay on the ground under the sky and are easy to die? Should we evolve like as bats and birds? Even if the answer is yes, but we including humans can not do that. What else can we do? PanZoora believe there are many hints and keys on their genomes, ecology and lifestyles of them, and their surroundings. Not all or enough but some of them were already printed on publications, and are or will. Some notices for studying of them and imitating them are one of ways PanZoora want to present to all of you.

## Messages_from_PanZoora_4
spZooCategory-id was additionally made. Species-Zoonoses-id shows species or zoonoses written in publications but there are many ways to express species' names and sometimes (maybe usually) information about themselves, mean hosts or intermediators, and zoonoses, have limited. How about referencing similar species or zoonoses and previous reports about not same but not far different diagnoses? spZooCategory-ids, groups of Species-Zoonoses-ids, would connect and show you various and similar information.

## Messages_from_PanZoora_5
Birds which survived the mass extinction and are offspring of dinosaurs, have coevolved with various viruses during hundreds of millions of years. After the era of dinosaurs, mammals which were small and preys by them at that time have evolved. Nobody knows when the next extinction will have come or not but one of mammals had been able to evolve to fly. It is as you know, bats. Both birds and bats have also gotten the symbiotic relations with most of pathogens. Some of them, of course, cause of deaths but most of them are asymptomatic for both animals. The abilities of volant and symbiosis look like, as it were, the most powerful defensive measures against crises. 
Human beings have been evolved like those? Humans can fly with additional goods by artificial machines for example airplanes but coevolved with few or no viruses. Now the public health is important for us but it had been also needed to live with pathogens even though made a few sacrifices, for getting biological resistances against them. Human intellect had presented us the ways of medical treatments but also agricultures using chemicals and farming other animals. Clean and artificial evolution had been kept for thousands of years by humans. Under these situations, human beings also have been evolved artificially and it might had better to be said we are also domestic. 
Domestic animals are weak against various pathogens which live safety together in wild living things. Only domestic livings can go back on the past and re-evolve with those pathogens? Are there any ways to find keys and resolve problems except to link and connect with any kinds of knowledge? No enough time and as One Health. PanZoora believes the diverse is one of critical rules on the earth and still left niches for living on the surface of the ground.
PanZoora especially propose study for microbiome made from insects and plants we often called medical using but sorry for the information of them are shortage in. This database is for zoonoses and just only a few of them at present. Please connect and widen between those researches. Natural things are good but never forget any cautions and public health need using for domestic animals avoiding other or next zoonoses, please.

## Messages_from_PanZoora_6
Infectious pathogens and their reservoir hosts (putting off those viruses are living things or not) have been living safety and friendly. On the points of view from those pathogens, transmissions from natural hosts to others are sometimes not happy. Others are so weak to be easily die cause also pathogens themselves death. Pathogens might prefer to stay in comfortable bio-containers. How and who break these balances? If keeping suitable distances and balances, and quick preventing for some time happened outbreaks, can we live with those hosts and pathogens in future without any dramatic our evolutions?

## Messages_from_PanZoora_7
Please never ever forget ebolaviruses are BSL-4, some of the most harmful viruses. Should not easy and unsuitable slaughter when livestock were infected and highly pathogenicity, it causes spreading ebolaviruses into the environment and be infected not only workers but many people and animals. Never ever distribute any meat polluted by ebolaviruses for avoiding economic loss and scarcity of food, even though customers don't know which meat is infected. Remember pandemics of COVID-19 but ebolaviruses are tremendous harmful compared to them. Don't leave everything up to workers and epidemic area. Only few people can handle with BSL-4 viruses and know-hows are not common. Confine and control viruses at epidemic areas and not make it pandemics into the globe, every living thing needs and appreciates your efforts and cooperation under One Health.

## Messages_from_PanZoora_8
Continuous surveillance for highly pathogenic avian influenza is, of course, needed but for ebolaviruses is also mustest. Differences of them are not only their virulence but their hosts, avian or mammals. Ebolaviruses which hosts are mammals, are easy to spillover to other animals but there is high taxonomic barrier for avian viruses. We have managed to attempt to control Ebola viruses’ infections between humans but primates and livestock (domestic pigs) also have them. We are a member of primates and easy to transmit to each other. Livestock are made meat, food. When whole livestock have to be slaughtered, causes scarcity of food and death of starvation especially in low-income countries. Not direct to infectious mortality but related one will be drastically increased.

## Backgrounds_of_PanZoora
The beginning was just to annotate publications about COVID-19. But no sooner I did several papers than many casts appeared on it. COVID-19 is one of zoonoses means includes not only human but candidate hosts, intermediate animals, of course pathogen SARS-CoV2 and surroundings all of them. Some hosts also have other zoonotic pathogens and some pathogens are similar to other zoonotic ones. The more I annotated about COVID-19 the more animals, zoonoses, pathogens and problems for or unknown are linked. Just only knowledge about COVID-19 we cannot stop pandemics of it. The mechanism of it might be more complicated and between some animals, others, some zoonoses, others, some pathogens and others are closely intertwined each other. This is the reason I made PanZoora. Most of casts are not harmful themselves and usually live friendly with us but once the balance of it is broken many of them will threaten humans. But we should consider who did, do and will do it even though intentionally or not. Problems and unknown are usually invisible but pay close attention to unshown spider webs. We human of course never should become spiders. Only living things what can fly like bats and birds, could escape webs and make future on the earth?

## Histories_of_PanZoora_1
All data were transferred and revised from panzoora_beta (includes panzoora_beta_original and panzoora_beta_relation) to PanZoora and beta version was disused on 2021-09-27.

## Histories_of_PanZoora_2
First structural change of PanZoora was added new column, spZooCategory-id, to PanZoora_table_relatedNote and PanZoora_table_lexisMain.

## Histories_of_PanZoora_3
ZoonosesDic (old name was panzoora_zoonoses_dic) was full exchanged because of incorrect duplications.

## Histories_of_PanZoora_4
All tables were transferred from TogoDB to GitHub and just [panzoora_view](http://togodb.org/db/panzoora_view) (old name was panzoora_view_relate_data) remains in TogoDB.

## Histories_of_PanZoora_5
All tables were copied from GitHub to TogoDB. Now same PanZoora exist in both.

## Afterwords_1
I hope PanZoora is something for all of you.
May some hopes still remain under any zoonotic pandemics. 
 
Sincerely yours, 
PanZoora.
