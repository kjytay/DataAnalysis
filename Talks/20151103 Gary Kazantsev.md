**Date/Time:** 3 Nov 2015, 1400-1500H  
**Location:** NUS COM2 04-02  
**Speaker:** Gary Kazantsev, Head of R&D Machine Learning Group at Bloomberg  
**Title:** Machine Learning in Finance (or Teaching Machines to Read for Fun and Profit)  
&nbsp;  
  
### Sentiment Analysis  
**Key question of sentiment analysis in finance**: Is the information in the story likely to be interpreted as positive, negative or netural by a long position investor?  

- It is difficult to formulate such a question! Either  
  - Unsolvable (no consistency in how humans answer the question in the first place), or  
  - Useless (no bearing on financial markets).  
- Also, the question "what is neutral" is not easy to answer.

**Sentiment (even if you get it right) may *not* result in a trading strategy.**  

- There are cases where stock price goes up even when sentiment is overwhelmingly negative.  
- You have to look at the context. Maybe the negative news is not the most important thing in this context.  

**How have people approached sentiment analysis before?**  

- Topic classification (i.e. tag each document with a topic. Some topics are considered positive, some negative)
  - This is hard to do! E.g. "Bankruptcy": This is a good or bad topic depending on whether the company is entering or exiting bankruptcy.
- Lexicon methods (i.e. dictionary of words, assign weights to each word, aggregate across the document)
  - But what weight to use? E.g. "cut": cut prices? interest rates? projections?
  - Works surprisingly well for social media, but does not work well for news.
- Encode dependencies in rules (e.g. "bankruptcy" is bad if the word before is "enter")
  - This is an NP-hard problem!
- Bona fide ML methods
  - Useful as a baseline (66-68% accuracy) but not good enough. Human accuracy is typically > 80%.
- Support Vector Machines (SVM)  
&nbsp;  
  
### Product Impact  
**Given a news story, predict the likelihood of price impact.**  

- No supervision! We cannot give a human somet training data and ask him to correctly tag the probability of price ipmact.
- Regression methods result in unstable results
- Enter computer vision methods (e.g. edge detection)
- Linear scale-space representation theory  
&nbsp;  

### Future

- Incorporate non-text information?
- Can we capture causality instead of merely correlation?  
&nbsp;  

### Misc

- "90% of social media is positive."
- (About models) "Interpretable, accurate, mathematically convenient. Pick two (often)."