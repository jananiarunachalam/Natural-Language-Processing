<br>

In this project, I trained probabilistic language models to distinguish between words in different languages. Rather than looking up whole words in a dictionary, I built models of character sequences to make a guess about the language of unseen words. I used NLTK and the Universal Declaration of Human Rights corpus. I compared different languages from the Universal Declaration of Human Rights documents. I used the following code to load the corpus and create sets of four languages: 

<br>


```import nltk
from nltk.corpus import udhr
english = udhr.raw('English-Latin1')
french = udhr.raw('French_Francais-Latin1')
italian = udhr.raw('Italian_Italiano-Latin1')
spanish = udhr.raw('Spanish_Espanol-Latin1') 
```

<br>

I created unigram, bigram and trigram models to compare English and French texts, and Italian and Spanish texts. I then compared the accuracies of these three models. 
