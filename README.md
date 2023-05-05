Download Link: https://assignmentchef.com/product/solved-dsl-assignment1-sentiment-analysis-task
<br>
In this competition, you have to perform a sentiment analysis task, analyzing user’s textual reviews, to understand if a comment includes a positive or negative mood.

In practice, you are required to build a robust classification model that is able to predict the sentiment contained in a text.

<h2>2.1         Dataset</h2>

The dataset for this competition has been specifically scraped from the <a href="https://www.tripadvisor.it/">tripadvisor.it</a> Italian web site. It contains 41077 textual reviews written in the Italian language.

The dataset is provided as textual files with multiple lines. Each line is composed of two fields: text and class. The text field contains the review written by the user, while the class field contains a label that can get the following values:

<ul>

 <li>pos: if the review shows a positive sentiment.</li>

 <li>neg: if the review shows a negative sentiment.</li>

</ul>

<strong>Dataset tree hierarchy </strong>The data have been distributed in two separate collections. Each collection is in a different file.

The dataset archive is organized as follows:

<ul>

 <li>csv (Development set): a collection of reviews <strong>with </strong>the class column. This collection of data has to be used during the development of the classification model.</li>

 <li>csv (Evaluation set): a collection of reviews <strong>without </strong>the class column. This collection of data has to be used to produce the submission file.</li>

 <li>csv: a sample submission file.</li>

</ul>

The dataset is located at:

http://dbdmg.polito.it/wordpress/wp-content/uploads/2020/01/dataset_winter_2020.zip

1

<h2>2.2         Task</h2>

You are required to build a classification pipeline to assign a label to each record in the Evaluation set. The label specifies the sentiment of the review.

<h2>2.3         Evaluation metric</h2>

Your submissions will be evaluated exploiting the <a href="https://scikit-learn.org/stable/modules/generated/sklearn.metrics.f1_score.html">f1_score</a> with the following configuration:

from sklearn.metrics import f1_score f1_score(y_true, y_pred, average=’weighted’)