<!DOCTYPE html>
<html>
  <head>
    <title>TweetsClustering</title>
  </head>
  <body>
    <h1>TweetsClustering</h1>
    <p>
      Twitter provides a service for posting short messages. In practice, many
      of the tweets are very similar to each other and can be clustered
      together. By clustering similar tweets together, we can generate a more
      concise and organized representation of the raw tweets, which will be very
      useful for many Twitter-based applications (e.g., truth discovery, trend
      analysis, search ranking, etc.)
    </p>

    <p>
      Here, the tweets are clustered using Jaccard distance metric and K-means
      clustering algorithm.
    </p>

    <p>
      <strong>Jaccard Distance (Explanation)</strong><br />
      The Jaccard distance, which measures dissimilarity between two sample sets
      (A and B). It is defined as the difference of the sizes of the union and
      the intersection of two sets divided by the size of the union of the sets.
      <br />
      <code>Dist(A, B) = 1 - |A intersection B|/|A union B|</code>
    </p>

    <p>
      For example, consider the following tweets:<br />
      <em
        >Tweet A: the long march<br />
        Tweet B: ides of march</em
      >
    </p>

    <p>
      |A intersection B | = 1 and |A union B | = 5, therefore the distance is 1
      – (1/5)
    </p>

    <p>
      <strong
        >Jaccard Distance Dist(A, B) between tweet A and B has the following
        properties:</strong
      ><br />
      1. It is small if tweet A and B are similar.<br />
      2. It is large if they are not similar.<br />
      3. It is 0 if they are the same.<br />
      4. It is 1 if they are completely different (i.e., no overlapping words).
    </p>

    <p>
      <strong>Dataset:</strong>
      <a href="https://archive.ics.uci.edu/ml/datasets/Health+News+in+Twitter"
        >https://archive.ics.uci.edu/ml/datasets/Health+News+in+Twitter</a
      >
    </p>

    <p><strong>Main steps:</strong> Tweets Preprocessing:</p>

    <ul>
      <li>tweet ids and timestamps are removed.</li>
      <li>
        words that start with the symbol '@', e.g., @AnnaMedaris, are removed.
      </li>
      <li>
        hashtag symbols are removed, e.g., #depression is converted to
        depression.
      </li>
      <li>any URL is removed.</li>
      <li>every word is converted to lowercase.</li>
    </ul>

    <p>
      <strong>K-Means Clustering Algorithm</strong><br />
      K-means clustering algorithm is implemented from scratch, without using
      any machine learning libraries.
    </p>

    <ol>
      <li>
        The code uses "bbchealth.txt" by default for the tweets data. - A user
        can change the url path to another data file as desired from the given
        files.
      </li>
      <li>
        The code uses, "3 clusters" by default and performs "5 experiments" one
        after another.
      </li>
      <li>
        User can change the default value of initial clusters (k) and the number
        of experiments to be performed.
      </li>
      <li>
        The program returns the value of SSE (sum of squared error) and the size
        of each cluster after every experiment (plotted).
      </li>
    </ol>

  </body>
</html>
