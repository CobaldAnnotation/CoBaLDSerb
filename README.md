# General information

The Serbian CoBaLD dataset is derived from [the Serbian UD treebank](https://github.com/UniversalDependencies/UD_Serbian-SET) which is based on the [SETimes-SR](http://hdl.handle.net/11356/1200) corpus and additional news documents from the Serbian web. It consists of the first 300 sentences from the Serbian UD Treebank training set annotated additionally with semantics and its size is 8,866 tokens.

To create the dataset, we annotated the first 300 sentences from the Serbian UD treebank training set with the help of our DL-based parser trained on CoBaLD Rus with the use of XLM-RoBERTa Large encoders. After that, the annotation was manually checked by professional linguists. The initial quality of the parser was 90.8% for semantic (deep) relations (DSs), and 93.6% - for semantic classes (SCs) for Russian texts. The percent of manual corrections is 6.75% for DS and 14.18% for SC. 

# Annotation comments

As in other CoBaLD datasets, most tokens here are provided with both Semantic Class (SC) and a Deep Slot (DS). The exceptions are grammatical and idiomatical units. The former possess the semantical classes only as they do not express deep semantic relations.

There are also some remarks that should be made considering the differences between Serbian and other languages. 

One of the most notable questions for Serbian is how the particle\conjunction *da* should be annotated: there are several distinct cases of its use. In the UD standard, *da* is always marked up as *SCONJ* for the PoS, and *mark* for the dependency relation. Semantically, though, it seems to have two distinct meanings, one as a particle (cases like *zatvorska kazna mogla bi da zaplaši medije* 'a prison sentence could scare the media', or *Da li očekujete i promenu ekonomske situacije u zemlji* 'Do you also expect a change in the economic situation in the country?'), the other as a conjunction (cases like *Iskreno se nadam da se to neće desiti* 'I sincerely hope that doesn't happen'). The parser mostly annotated *da* with the SC CONJUNCTIONS, but there was often no SC, as well. We chose the SC according to those two cases. 

There are also several idiomatic expressions in Serbian which do not have their exact parallel in other languages, such as *bilo koja druga* 'any other', *nakon što* 'after', *zato što* 'because'. We had to make decisions for each of them separately, but normally we tend to annotate them as close to their counterparts in Russian and English as possible. 

Concerning deep slots, Serbian doesn't differ very much in its syntax from Russian, thus the main corrections concerned things prone to error during annotating Russian data as well: mostly, the DS such as Possessor/Experiencer/Agent and Object/Object_Situation were corrected. No corrections specific for Serbian were made. The low percent of these corrections may be explained by the small size of the dataset and repeated patterns in sentences.
