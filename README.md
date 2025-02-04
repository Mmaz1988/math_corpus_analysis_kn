# math_corpus_analysis_kn

Requires English spacy model.

```
python -m spacy download en_core_web_sm
```


# MathCorpus - Linear Algebra (J. Hefferon)

### Linear Algebra Corpora

A directory to collect corpora obtained from the book 
[Linear Algebra (Jim Hefferon)](https://hefferon.net/linearalgebra/), 
available with a license at [Jim Hefferon GitHub repository](https://gitlab.com/jim.hefferon/linear-algebra/-/tree/master). 
These corpora are gathered at the request of 
[Valeria de Paiva](https://vcvpaiva.github.io/) to be used in experiments 
extracting mathematical concepts for the [Topos Institute](https://topos.institute/), 
according to the **Job Description** below.

**Note**: This process did not follow the Universal Dependencies script, but instead 
applied **spaCy** in Python to collect the relevant statistics.

---------------------

### Job description:

After collecting a book, the student should make a GitHub repo and then use `spacy’ (https://spacy.io/) (or a similar off-the-shelf tool) to process it, producing stats (the script for the stats is from https://github.com/UniversalDependencies/tools/blob/master/udlib.pm . It’s called conllu-stats.pl), like was done for the nLab in https://github.com/ToposInstitute/nlab-corpus and for an updated nLab in  https://github.com/ToposInstitute/nLab2024-corpus. A nice, short  (4 min) tutorial on spacy is presented in https://medium.com/@pankaj_pandey/harnessing-the-power-of-spacy-a-comprehensive-guide-to-natural-language-processing-ffa6b1e6ff44.

A description of a similar project, building up corpora and benchmarks for mathematical text can be seen in the project Parmesan of Collard and de Paiva, which is particularly interested in Category Theory. The project has one example of a book “Basic Category Theory”, by Tom Leinster, processed this way and can be found here: https://github.com/ToposInstitute/CT-corpus/blob/main/bct.conll. 
As an illustration sentence 33 of the book looks like the following:

#sent_id = 33

#text = In subjects such as number theory and combinatorics, some questions are simple to state but extremely hard to answer.

| Token ID | Token        | Lemma         | Part of Speech (POS) | Morphological Tag | Morphological Features              | Head ID | Dependency Relation | Space Info       |
|----------|--------------|---------------|-----------------------|--------------------|--------------------------------------|---------|----------------------|------------------|
| 1        | In           | in            | ADP                  | IN                 | _                                    | 13      | prep                | _                |
| 2        | subjects     | subject       | NOUN                 | NNS                | Number=Plur                          | 1       | pobj                | _                |
| 3        | such         | such          | ADJ                  | JJ                 | Degree=Pos                           | 4       | amod                | _                |
| 4        | as           | as            | ADP                  | IN                 | _                                    | 2       | prep                | SpaceAfter=No    |
| 5        | \n           | \n            | SPACE                | _SP                | _                                    | 7       | dep                 | SpaceAfter=No    |
| 6        | number       | number        | NOUN                 | NN                 | Number=Sing                          | 7       | compound            | _                |
| 7        | theory       | theory        | NOUN                 | NN                 | Number=Sing                          | 4       | pobj                | _                |
| 8        | and          | and           | CCONJ                | CC                 | ConjType=Cmp                         | 7       | cc                  | _                |
| 9        | combinatorics | combinatoric | NOUN                 | NNS                | Number=Plur                          | 7       | conj                | SpaceAfter=No    |
| 10       | ,            | ,             | PUNCT                | ,                  | PunctType=Comm                       | 13      | punct               | _                |


We want statistics of the corpus, done for each book, so we need a lot of annotations.
