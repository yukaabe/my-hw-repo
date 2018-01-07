### ***Design Write-up Feedback***

***Nico Van de Bovenkamp***

***

**Overall**  
Awesome project! I really like this project. It is a well defined problem with **TONS** of room for creativity in the models you create and features you decide to engineer.

***Regarding sentiment analysis***  
Sentiment analysis is a very interesting, very specific, sect of ML folks, linguists, and computer scientists. There are some really handy APIs out there:
https://www.quora.com/What-is-the-best-way-to-do-sentiment-analysis-with-Python-I%E2%80%99m-looking-for-a-sentiment-analysis-API-that-I-can-add-an-emoticon-dictionary-to-I-have-no-idea-how-to-use-NLTK-Can-anyone-help-me-with-that

https://cloud.google.com/natural-language/docs/sentiment-tutorial

That said, I would encourage you to first build a base model, maybe just including bag-of-words type techniques like tfidf or counts with ngrams. Then, from there, see what happens if you add in an engineered feature of sentiment!

***Incorrect data***  
Incorrect data is a concern, but another concern is null/missing values. Check if you have any because you will have to deal with some. Also, another huge concern in text data, and, in particular, user submitted text data, is that you will have to clean that data. And even once it is clean, you will have tons of spelling issues, uncommon uses of language, etc. that will mess with your model. For example, maybe someone has written "great" and that would be an indicator for good reviews, but someone else wrote "gret!". How frustrating!

***Goals of your project***  
This is an additional step, but maybe you could do some interesting audience profiling from this! If you can build a model that predicts, via text, what they intended, then maybe you can make profiles of people!
