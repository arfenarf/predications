## Background

[SemRep](https://semrep.nlm.nih.gov/) is a rule-based biomedical relationship extraction system developed by the
National Library of Medicine.
Given a document, SemRep extracts within-sentence relationship triples of the form <subject, predicate, object>, where
predicate
is the type of the relationship asserted. For example, SemRep might extract <aspirin, TREATS, headaches> from the
sentence "This
study found that aspirin is a suitable treatment for mild headaches."
In SemRep lingo, these triples are called "predications".
SemRep has been periodically run over the entire collection of PubMed abstracts. The extracted predications were then
collected into
[SemMedDB](https://skr3.nlm.nih.gov/SemMedDB/index.html).
SemMedDB contains many millions of predications and could therefore benefit a variety of literature-based
discovery tasks.
However, [we have found](https://www.sciencedirect.com/science/article/pii/S1532046414000057) that the true performance
of
SemRep is low as many predications are not, in fact, asserted in their source sentence. This limits SemRep's usefulness.

## Task

Your task is to design and implement a **deep learning** approach to filter predications belonging to the following
subset of
predicates from SemMedDB, informally called the "Substance Interactions" group:

* INTERACTS\_WITH
* STIMULATES
* INHIBITS

You can find more details about these predicates in the appendix
of [this article](https://bmcbioinformatics.biomedcentral.com/articles/10.1186/1471-2105-12-486).

We have annotated 3,000 predications from this group with binary labels indicating whether or not the given predication
is truly asserted in the source sentence. These are given in `data/substance_interactions.csv`. You are to split these
3,000 predications into a training and test set, and report precision, recall, and F1 score of your model on both
training and test.

You must extract features from the `SENTENCE` column in the dataset. You may also use other columns, as you see fit.

## Submission

You will submit a Jupyter Notebook using Python>=3.6 detailing your implementation. In addition to your code, the
notebook should include
a brief writeup that addresses the following points.

1. A description of your approach.
2. A discussion of your results.
3. A very brief discussion of the limitations of your approach and possible future work.

You may also submit, as you deem necessary:

* `requirements.txt`, giving versions of any Python packages you use.
* `README.txt` describing any special instructions for running your submission.
* other files (e.g. `.py, .csv, .txt`) containing code or data imported by your notebook.

**N.B.** The `{SUBJECT,OBJECT}_{START,END}_INDEX` columns in the SemMedDB data are supposed to correspond to indices in
the
original document, which is a MEDLINE formatted abstract. Unfortunately, there is missing information in this version
of SemMedDB which means it is not possible to reconcile these indices with the mentions given in the sentence.

Please direct any questions about how to complete this task to Jake Vasilakes at vasil024@umn.edu
