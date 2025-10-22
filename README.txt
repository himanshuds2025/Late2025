---------------------------------------------------------------------------

22/10/2025

-----------------------------------------------------------------------------------------

This is one of my projects that took multiple hours of understanding and hardwork and I'm  quite proud of it.
I built  a fake news classifier from scratch using TF-IDF and 3 different models to improve the overall accuracy selection.
LogisticRegression, MultinomialNB, and RandomForestClassifier were the chosen models for this project.
I built an auto-detect feature that would consider the most commonly used feature and label column names in related dataset, automatically. If by some off chance it doesn't recognize automatically, simple manual intervention would solve it.

After that, data will be cleaned ('Preprocessing') which simply means all the stopwords like 'is, an, and, with' and all the punctuations would be removed as they'd just create noise for the models. By that I mean, they don't add much value. Sounds weird to us humans, but for machines, it is how it works.
There is also a point to be noted that if you want to sample on a smaller dataset to prioritise speed, change the "sample" parameter to "True" in cell 8. In my case, I wanted to preprocess all of my dataset, therefore, it was kept "False"

Initially, I had put thee max_features for TF-IDF's max_features to 20,000, however the accuracy and recall were about 50-50. There, I thought I might have given too much vocabulary for the models to learn and they had hallucinated.
Therefore, after further tweaking, I kept going for lower max_features, from 20k-to-15k-to-10k-to-5k and ultimately 2000 where I noticed the most balanced rates of accuracy and recall.
The top performing model was RandomForestClassifier with an accuracy of 70.64% and a recall rate of .70 on both label values (Real and Fake), followed by MultiomialNB and LogisticRegression with accuracy rates of 63.38% and 63.06% respectively.

In my understanding, the reason RandomForestClassifier feteched the most amount of accuracy and recall rates was because it isn't just one model, but rather build on hundreds of decision  trees, where the majority vote was count in decision of identifying whether the news was fake or real (I just summarized the theory that was stuck in my head because of the never ending lectures that I went through this year). So it didn't cling to just one possibility.
Moreover, it didn't really overfit on the training data, which i tested with a sample in the end (it identified the fake news :D ).
On the other hand, I think LogisticRegression was just trying to oversimplify it with its mathematics.
MultinomialNB, I wasn't familiar with it, but I had read that it was much better with text classification as it works directly with big vocabs. I had high expectations from it but it turned out to be 'average' for my dataset :)

Next, the confusion_matrix of the best performing model will be shown (which in my case was rf).
It will also save the best model for later use, which i think is a nice feature.

In the end, I'd say that this was a very new and informative project to me, and I enjoyed most of it, except the syntax errors because of my old keyboard.

PS: I'm not a professional README writer, I typed what I did and dealt with throughout this project.

-----------------------------------------------------------------------------------------------------------