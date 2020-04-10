<br>
The learning goals of this project are:
<ul>
<li>Understand and implement common NLP evaluation methods - precision, recall and F1 measure.</li>
<li>Employ experimental design practices in NLP. Splitting the corpus into training/development/test sets, implementing baselines to determine how difficult the task is, and experimenting with features and models.
<li>Getting acquainted with sklearn.
<li>Learning about basic text classification algorithms.
<li>Learning about vector semantics and getting familiarity with word embeddings.
</ul>



Problem #1: We need functions to assess and evaluate the performance of our models. We will implement those first.
Created functions to calculate precision, recall and f-measure without using sklearn.

<br>

# Text Classification

Problem #2: Majority Class Baseline. We will create majority class baseline to evaluate our initial model performance – which is the simplest baseline. 

Problem #3: Review Length Baseline. We will create baseline to evaluate our model performance – which takes into account length of the review. For this baseline, you should try setting various thresholds of review length to classify them as positive or negative. For example, all reviews > 50 words in length can be classified as positive.

Problem #4: Implementing the Naïve Bayes classifier.

Problem #5: Implementing the Multinominal Naive Bayes classifier.

Problem #6: Performance of the different models.

Data Used: [Large Movie Review Dataset](https://ai.stanford.edu/~amaas/data/sentiment/). It contains movie reviews in two classes – positive and negative. The dataset is
split into training and test directories already. Raw text and already processed bag of words formats have also been provided by the authors – c.f. README in the directory.

<br>

# Vector Sematics

Similar to language models, embeddings are trained directly from a large collection of natural language text without being tied to a specific NLP application or subtask. How can we measure the quality of learned embeddings? Some of the commonly accepted extrinsic evaluation methods are based on word similarity tasks, word analogies (e.g., “man is to woman as king is to queen).

Analogy Dataset Mikolov’s analogy dataset [2] includes four semantic relations and four syntactic relations. In the test files, each line represents one analogy question, in the form of four words <a, b, c, d>. For example: “Bangkok Thailand Cairo Egypt” A question is counted as correctly answered only if the predicted word is the same as the given word. For example, given the first three words “Bangkok Thailand Cairo”, the task is to predict “Egypt”.

Data Used: [Mikolov's Analogy Dataset](http://www.fit.vutbr.cz/~imikolov/rnnlm/word-test.v1.txt). The full set of analogy questions can be found in the file word-test.v1.txt. 

The groups of relations are delimited by lines starting with a colon (:) and you should only work with these groups: capital-world, currency, city-in-state, family, gram1-adjective-to-adverb, gram2-opposite, gram3-comparative, and gram6-
nationality-adjective. Word Embeddings “Pretrained” word embeddings are word embeddings that are already constructed in advance of your NLP project (whether your project is a neural language model, a text classifier, or a class assignment). The advantage of pretraining is that it simplifies learning your model, because the embedding parameters are fixed in advance. The disadvantage is that, if your embeddings happen to be bad for your task, you’re stuck with them. 

Here are some popular choices:
<ul>
<li>[Word2vec](https://code.google.com/archive/p/word2vec/)
<li>[GloVe](http://nlp.stanford.edu/projects/glove/)
<li>[Dependency-based. embeddings](https://levyomer.wordpress.com/2014/04/25/dependency-based-wordembeddings/)
</ul>
<br>
