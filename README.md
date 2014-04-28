To find the interestingness of a given article using Named Entity Recognition and live twitter sentiments

It comprises of 2 modules: 

1.Named Entity Extraction:

-Identify Pure Nouns

A word which is never been used as any POS
A word does not exist in English Language 

-Identify Pure Noun Phrase
Proximity of word with Pure Nouns
Classifying Named Entities
Use of Hypernym graphs, WordNet 

-Assign classes like Person, organization etc. to entities

2.Sentiment Analysis

-Open twitter stream to get live tweets for each entity derived for an article

-Preprocess Tweets:
Tweet words cleaning
Elimination of Stop Words
Spell  correction

-Classify into Positive and Negative Tweets
If num(Positive_Words>Negative_Words)
then class(Tweet)=Pos_Tweet
else
class(Tweet)=Neg_Tweet

-For each named entity calculate its sentiment score as:
Score(Entity)=(num(Pos_Tweet)-num(Neg_Tweet))/Num(Total_Entity_Tweets)

Finally I came up with an interestingness scores used for ranking of the articles based on each entity’s sentiment scores belonging to that article as:

I1 = ( ∑ | Score(Entity)) / Total_Entites
Incorporates Sentiment Of Entity


Final Ranking of the articles is based on the interestingness score I1 as calculated above




