
Cost function which helps in improving the network is quadratic in nature. So computing the gradient for each individual input and then averaging it across all training data is a daunting task (more so if the number of training input is large). What this basically means is that - learning process is going to be very slow. 

This is where the idea of Stochastic Gradient Descent (SGD) comes up. The idea is to calculate gradient for a small sample of randomly choosen training data/inputs. By averaging over this small sample it turns out that we can quickly get a good estimate of the true gradient ∇C, and this helps speed up gradient descent, and thus learning.

We'll label those random training inputs X1,X2,…,Xm, and refer to them as a mini-batch. This is provided the sample size m is large enough that the average value will be roughly same as average value over all inputs. 

∇C≈1/m∑j=1/m∇CXj

confirming that we can estimate the overall gradient by computing gradients just for the randomly chosen mini-batch.

Then we pick out another randomly chosen mini-batch and train with those. And so on, until we've exhausted the training inputs, which is said to complete an epoch of training. At that point we start over with a new training epoch.

### Removing m or n from average
And, in a similar way, the mini-batch update rulessometimes omit the 1/m term out the front of the sums. Conceptually this makes little difference, since it's equivalent to rescaling the learning rate η. But when doing detailed comparisons of different work it's worth watching out for.

### Example
For example, if we have a training set of size n=60,000, as in MNIST, and choose a mini-batch size of (say) m=10, this means we'll get a factor of 6,000 speedup in estimating the gradient! Of course, the estimate won't be perfect - there will be statistical fluctuations - but it doesn't need to be perfect: all we really care about is moving in a general direction that will help decrease C, and that means we don't need an exact computation of the gradient. In practice, stochastic gradient descent is a commonly used and powerful technique for learning in neural networks, and it's the basis for most of the learning techniques 

An extreme version of gradient descent is to use a mini-batch size of just 1. That is, given a training input, x, we update our weights and biases according to the rules wk→w′k=wk−η∂Cx/∂wk and bl→b′l=bl−η∂Cx/∂bl. Then we choose another training input, and update the weights and biases again. And so on, repeatedly. This procedure is known as online, on-line, or incremental learning. In online learning, a neural network learns from just one training input at a time (just as human beings do). 
