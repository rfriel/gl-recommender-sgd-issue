# gl-recommender-sgd-issue
Illustration of a problem I've encountered with graphlab's factorization recommender

When [working with rating data from Goodreads](https://github.com/rfriel/goodreads_social_rating_prediction), I noticed some strange behavior in the graphlab recommender I was using.  Some more tests showed that this was due to the learning rate decay schedule, which does not seem to be fully under the user's control, and was too fast for good convergence.  The [demo notebook](https://github.com/rfriel/gl-recommender-sgd-issue/blob/master/gl-recommender-sgd-issue.ipynb) in this repo reproduces this behavior on toy data, and shows that a recommender using vanilla SGD can do much better on this data (as it could on my Goodreads data).
