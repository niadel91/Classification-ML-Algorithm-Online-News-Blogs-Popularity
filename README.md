## Classification Project - Online News Popularity
Checking the popularity of different online news posts.
<hr>

Data Set Information:
<ul>
<li>The articles were published by Mashable (www.mashable.com) and their content as the rights to reproduce it belongs to them. Hence, this dataset does not share the original content but some statistics associated with it. The original content be publicly accessed and retrieved using the provided urls.</li>
<li>Acquisition date: January 8, 2015</li>
<li>The estimated relative performance values were estimated by the authors using a Random Forest classifier and a rolling windows as assessment method. See their article for more details on how the relative performance values were set.</li>
<li>We have assumed that the most popular posts are shared the most and calculated the average number of posts as 3501. We have also divided the data into 2 classes</li>
  </ul>

<li>class-4(popular posts, if the average number of posts>3501) and</li>
<li>class-2 (not-so-popular posts, if the average number of posts<=3501) We intend to anticipate the popularity(class) of the post and it is our target variable.</li>
  
## Data Source - UCI
Data source link - https://archive.ics.uci.edu/ml/datasets/Online+News+Popularity#

## Model Summary
The Accuracy score for the reduced dataset is similar or somewhat better than the score of the unreduced dataset(exception - Logistic Regression, where the Accuracy rate for the unreduced data is 88.93% which is better than 87.3% for the unreduced dataset and also Decision Tree Models).

We have used 2 PC for our different models. There is not much difference in the scores for the reduced and unreduced data, maybe because we have taken fewer number of Principal Components.

We also noticed that there is a huge variance that is being explained by the Eigen Vectors.
<table>
  <tr>
    <td>
      Voting Classifers Scores
    </td>
    <td>Hard Voting
      </td>
    <td>Soft Voting
      </td>
    </tr>
<tr>
  <td>Train
    </td>
  <td>.85
    </td>
  <td>.86
    </td>
  </td></tr>
<tr>
  <td>Test
    </td>
  <td>.89
    </td>
  <td>.89
    </td>
  </td></tr>
</table>
Soft Voting has better score than Hard Voting.

<table>
  <tr>
    <td>
      Bagging Scores
    </td>
    <td>DTree
      </td>
    <td>Logistic Regression
      </td>
    </tr>
<tr>
  <td>Train
    </td>
  <td>.84
    </td>
  <td>.84
    </td>
  </td></tr>
<tr>
  <td>Test
    </td>
  <td>.89
    </td>
  <td>.89
    </td>
  </td></tr>
</table>

There is no difference in the Train and Test Scores for both the models.

<table>
  <tr>
    <td>
      Pasting Scores
    </td>
    <td>RBF
      </td>
    <td>Linear Kernel
      </td>
    </tr>
<tr>
  <td>Train
    </td>
  <td>.84
    </td>
  <td>.84
    </td>
  </td></tr>
<tr>
  <td>Test
    </td>
  <td>.89
    </td>
  <td>.89
    </td>
  </td></tr>
</table>

There is no difference in the Train and Test Scores for both the models.
<table>
  <tr>
    <td>
      Pasting Scores
    </td>
    <td>DTree without Depth
      </td>
    <td>DTree with max_depth - 5
      </td>
    </tr>
<tr>
  <td>Train
    </td>
  <td>.84
    </td>
  <td>.93
    </td>
  </td></tr>
<tr>
  <td>Test
    </td>
  <td>.89
    </td>
  <td>.87
    </td>
  </td></tr>
</table>
This is a case of overfitting for the DTree with max_depth=5

Gradient Boosting Classifier

Train Score - 0.8472 , Test Score - 0.8814

<b>ANN</b>

The Artificial Neural Network has also given us a good enough Accuracy Score for our model(87.31%), which is in sync with the accuracy scores of our other models so the perceptron model is said to be working for our dataset.
