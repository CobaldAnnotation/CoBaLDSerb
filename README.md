# Summary

The Serbian CoBaLD dataset is derived from [the Serbian UD treebank](https://github.com/UniversalDependencies/UD_Serbian-SET) which is based on the [SETimes-SR](http://hdl.handle.net/11356/1200) corpus and additional news documents from the Serbian web. It consists of the first 300 sentences from the Serbian UD Treebank training set annotated additionally with semantics and its size is 8,866 tokens.

# Introduction

To create the dataset, we took the first 300 sentences from the Serbian UD treebank training set and annotated them with the help of our DL-based parser trained on CoBaLD Rus with the use of XLM-RoBERTa Large encoders. After that, the annotation was manually checked by professional linguists. The percent of manual corrections is 6.75% for DS and 14.18% for SC. 
