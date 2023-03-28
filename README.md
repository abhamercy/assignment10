# assignment10
Documentation:

I first used Perspective API to create toxicity scores for all comments in the dataframe, it printed only the scores for the first 20 comments to not exceed capabilities.

I then calculated basic stats about the data like how many toxic and non toxic comments there are and the toxicity distribution.

I then took 20 comments from the data as an example to determine the toxicity threshold. I created a histogram with the x axis going from 0 to 1 on the toxicity score range. Based on what I saw, I decided 0.5 should be the threshold.

Hypothesis: My hypothesis is that the perspective API will not accurately assign toxicity scores to comments with sarcasm and irony as they are't obviously depicting toxicity in the text but is understood by the underlying tone of the statement by the reader.

I created a small test set of 15 comments containing sarcasm and irony and 15 comments that are straightforward and not sarcastic or ironic. By comparing the toxicity score results of both test sets I was able to see if my hypothesis is correct.

Based on the results, it seems like the perspective API was able to distinguish between the sincere and sarcastic comments a bit and reported low toxicity scores for the comments that were sincere. However, the scores are not as high as they should be for the sarcastic comments and are below the toxic threshold in my opinion.

Conclusion: Based on the data provided, it appears that the toxicity score is generally higher for sarcastic comments than for non-sarcastic comments (my hypothesis was partly wrong). But the scores are not as high as they would be for outright toxic comments that were not conveyed through sarcasm. I do not believe my hypothesis was completely wrong since I don't believe it accurately assigned toxicity scores to the sarcastic comments even if it was able to find the difference between the sarcastic and sincere comments.

The low sample size makes the data easier to be manipulated by internal bias and does not represent how the general population speaks sarcastically or sincerely since these are statements I came up with according to my own understanding of the concepts.

Step 4: Write about your results

After analyzing the toxicity scores produced by the Perspective API, I found that the majority of the comments were not toxic, with an average toxicity score of 0.030. However, there were a few comments that had higher scores, with toxicity scores ranging from 0.5 to 0.9. It is important to note that the sample size was relatively small even though there are thousands of comments in the set, as there are billions of people on the internent leaving comments of varying toxicity levels and these results may not be representative of the population as a whole.

One possible bias in the model is that it may not accurately capture the nuances of language and cultural differences. The model was trained on a dataset of minly English-language comments,although there were some of examples of other languages such as Japanese and Korean, and may not be as effective at identifying toxic comments in all languages or cultural contexts. Additionally, the model may not be able to detect certain types of toxicity, such as sarcasm or irony (as my hypothesis testing has shown).

Another potential bias is that the model may reflect the biases of the dataset it was trained on. If the dataset contains a disproportionate number of comments from certain demographics or geographic regions, the model may be less effective at identifying toxic comments from other groups.

My theory is that my results were the way they are because of specific words present in the comments that act as key words for the api, as it has been trained to spot words with negative connotations. I think it finds those words and compares it to the other words in the comments to determine the toxicity score.
