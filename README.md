# INF8460 - Polymtl

All projects of the INF8460 "Automatic Natural Language Processing" course.

## TP1

Basics of automatic language processing. Text classification algorithms: Naive Bayes, Logistic Regression, Neural Networks.

## TP2

Second practical work dedicated to the use of n-grams in natural language processing.
Understand how n-grams are used for tasks such as word prediction, autocompletion and text generation. Here are some concrete examples of their use:

- Word prediction: n-grams are used to predict the next word given the previous context. For example, in the sentence "I think therefore I ____", a bigram model might suggest "am" as the next word, based on previous observations.
- Autocompletion: Search engines use n-grams to offer search suggestions when you start typing a sentence. They are based on the prefixes of the current word and on sentences written by the user.
- Text generation: n-grams can be used to automatically generate text. They help a model to predict the next words based on the probabilities of the words that can be generated according to context.

Evaluating the quality of generative language models using perplexity.

## TP3

Building an automatic translator using the Transformer architecture. The idea is to use a machine translation system to translate SPARQL queries into English questions.

SPARQL is a knowledge base query language, similar to SQL. Knowledge bases are a source of data structured according to the standards, models and languages of the Semantic Web, enabling efficient access to large quantities of information in a wide variety of fields. However, their access is limited by the complexity of the queries, which prevents the public from using them directly. It is also difficult for the unsophisticated user to understand the meaning of a query. We therefore want to code a Transformer model that interprets a SPARQL query on the DBpedia knowledge base by associating an English question with it.  

In this way, our machine translation system will take a SPARQL query as input and produce as output an English sentence corresponding to the question posed by the query. For example:
  
- __Input__ _select distinct count ( ?uri ) where { dbr:Apocalypto dbo:language ?x . ?x dbp:region ?uri }_  
- __Expected output__ : _In how many other dbp:region do people live, whose dbo:language are spoken in dbr:Apocalypto?_  

Using elements with the prefix dbr /dbo/dbp that are associated with data in DBpedia and the knowledge base schema. dbr:Apocalypto is simply a URI that describes a resource (or data) in DBpedia.
Reproduction of the Transformer architecture using Keras layers.

## TP4

In this project, we perform natural language question annotation using different models with the aim of proposing a method that outperforms competing teams.

For example, given the question:
What is the country for head of state of Justin Trudeau?
The model should return :
what is the <\<wd:Q6256\>> for <\<wdt:P35\>> of <\<wd:Q3099714\>>?

Elements with the prefix wd are Wikidata URIs. For example wd:Q6256 corresponds to the URI https://www.wikidata.org/wiki/Q6256

Wikidata is a collaborative, structured database that, like Wikipedia, is part of the Wikimedia project. Unlike Wikipedia, which focuses on the creation and management of encyclopedic content, Wikidata specializes in the collection and management of structured data.

Fine-tuning LLMs such as BERT, ROBERTA, GPT...
