# General information

The Serbian CoBaLD dataset is derived from [the Serbian UD treebank](https://github.com/UniversalDependencies/UD_Serbian-SET) which is based on the [SETimes-SR](http://hdl.handle.net/11356/1200) corpus and additional news documents from the Serbian web. It consists of the first 300 sentences from the Serbian UD Treebank training set annotated additionally with semantics and its size is 8,866 tokens.

To create the dataset, we annotated the first 300 sentences from the Serbian UD treebank training set with the help of our DL-based parser trained on CoBaLD Rus with the use of XLM-RoBERTa Large encoders. After that, the annotation was manually checked by professional linguists. The initial quality of the parser was 90.8% for semantic (deep) relations (DSs), and 93.6% - for semantic classes (SCs) for Russian texts. The percent of manual corrections is 8.49% for DS and 13.34% for SC. 

# Annotation comments

As in other CoBaLD datasets, most tokens here are provided with both Semantic Classes (SCs) and a Deep Slots (DSs). The exceptions are grammatical and idiomatical units - they possess the semantical classes only as such units do not express deep semantic relations.

There are also some remarks that should be made considering the differences between Serbian and other languages. 

One of the most notable questions for Serbian is how the particle\conjunction *da* should be annotated. There are several cases of its use. In the UD standard, *da* is always marked as *SCONJ* for the PoS, and *mark* for the dependency relation. Semantically, though, it seems to have two distinct meanings, one as a particle (in cases like *zatvorska kazna mogla bi da zaplaši medije* 'a prison sentence could scare the media', or *Da li očekujete i promenu ekonomske situacije u zemlji* 'Do you also expect a change in the economic situation in the country?'), the other - as a conjunction (in cases like *Iskreno se nadam da se to neće desiti* 'I sincerely hope that doesn't happen'). In most sentences, the parser annotated *da* with the SC CONJUNCTIONS, but there were also many examples, where the SC was not defined. In such cases, we annotated the SC as PARTICLES or CONJUNCTIONS manually according to the senses mentioned above. 

There are also several idiomatic expressions in Serbian which do not have their exact parallel in other languages, such as *bilo koja druga* 'any other', *nakon što* 'after', *zato što* 'because'. We tried  to annotate them as close to their counterparts in Russian and English as possible. 

