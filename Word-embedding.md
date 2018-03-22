Neural Networks work on feature vectors which have finite values (binary or real numbers between 0 and 1 or numbers in a given range like [0,255] for grayscale image). Now when it comes to dealing with text or words we need to transform them as well in some form of vector. 

Different applications of NLP like machine translation, parsing, sentiment analysis deals with words. This would require some vector representation of each word. One obvious option could be to represent each word using one-hot encoding, but then it leads to a different problem. If you vocabulary contains 50,000 words then each word will be represented by a 50,000 dimensional vector. 

word(i) = Transpose of [0, 0 , 0 , 0, 1, 0, 0, ..... 0]

Such a large vocab with sparse representation is going to be quite in-efficient. 

One obvious solution would be to represent each word in the vocab using a small and dense vector of say manageable dimension like 500. This technique is called as embedding. Apply some magic sauce so it groups similar words together. This means that similar meaning or intent words will be part of the same cluster or closer to one another. 

For example - *I drink milk* is a valid sentence and if the embedding model knows that milk is closer to water then it will know that *I drink water* is also a valid sentence. 

The vector for each word is a semantic description of how that word is used in context, so two words that are used similarly in text will get similar vector represenations. Once you map words into vector space, you can then use vector math to find words that have similar semantics.

**Word embeddings are a type of word representation that allows words with similar meaning to have a similar representation.**
Each word is mapped to one vector and the vector values are learned in a way that resembles a neural network. Key to the approach is the idea of using a dense distributed representation for each word. The distributed representation is learned based on the usage of words. This allows words that are used in similar ways to result in having similar representations, naturally capturing their meaning. This can be contrasted with the crisp but fragile representation in a bag of words model where, unless explicitly managed, different words have different representations, regardless of how they are used.

### Word Embedding Approaches
**Word embeddings are considered to be among a small number of successful applications of unsupervised learning at present.** This model is used for learning vector representations of words, called "word embeddings".

1. Word2Vec
Word2vec is a particularly computationally-efficient predictive model for learning word embeddings from raw text.  It comes in two flavors, the Continuous Bag-of-Words model (CBOW) and the Skip-Gram model (Section 3.1 and 3.2 in Mikolov et al.). Algorithmically, these models are similar, except that CBOW predicts target words (e.g. 'mat') from source context words ('the cat sits on the'), while the skip-gram does the inverse and predicts source context-words from the target words. This inversion might seem like an arbitrary choice, but statistically it has the effect that CBOW smoothes over a lot of the distributional information (by treating an entire context as one observation). For the most part, this turns out to be a useful thing for smaller datasets. However, skip-gram treats each context-target pair as a new observation, and this tends to do better when we have larger datasets. 






#### References
1. https://www.tensorflow.org/tutorials/word2vec
2. http://blog.aylien.com/overview-word-embeddings-history-word2vec-cbow-glove/

