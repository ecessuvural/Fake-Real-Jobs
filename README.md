
## **SUMMARY**
In this project, various machine learning algorithms were used to detect fake and real job postings. This dataset was evaluated using DBSCAN, Random Forest, K-Means, and Logistic Regression. Gaining insight into the patterns that distinguish real job postings from fake ones will provide a basis for additional research and possible use in job posting verification.

## **METRICS**
**-Analysis of Exploratory Data (EDA)**

The dataset was analysed for feature properties, class distributions, and missing values during the EDA phase.  Further preprocessing procedures were guided by the understanding of underlying patterns and possible data problems provided by visualisations and statistical summaries.

**-Data Preprocessing**

Since the dataset contains many categorical and textual values, one of the most important steps was to convert them to numeric values ​​so that they can work with machine learning algorithms. Label encoding was used for the conversion of categorical values, and TfidfVectorizer was used for the conversion of text values. NaN values ​​were filled and the dataset was prepared for Machine Learning.

**-Supervised Learning**

For this part, Logistic Regression and Random Forest were compared in order. The reason for choosing Logistic Regression is that it is designed for binary classification models. For example, in my dataset, job advertisements can be considered as Real and Fake. The reason for choosing Random Forest is that it works well with categorical data and can automatically calculate important features. Precision, Recall and F1-Score values ​​were examined for comparison. For example, Logistic Regression gave 0.925, Random Forest 0.910 values ​​for Precision, Logistic Regression gave 0.920, Random Forest 0.905 for Recall, Logistic Regression gave 0.915, Random Forest 0.905 for F1-Score. As a result of the comparison, we continued with Logistic Regression, which gave higher values. Because higher scores show us that the model can make better predictions in the test data. Then, hyperparameter operations were performed with RandomizedSearch and compared with the old scores together with the graph. The reason for choosing this was to save time, but Grid Search could have been preferred for a wider scope. As a result, the train operations were completed, seeing that we got higher scores.

**-Unsupervised Learning**

Here, we proceeded with K-Means and DBSCAN. Because K-Means is simpler and faster than others. DBSCAN uses a density-based approach and can provide a great advantage for detecting density differences between real/fake job advertisements. It also identifies isolated points by performing Noise Detection, which can give us an idea about fake job advertisements. Silhouette scores were examined to compare these two algorithms. It was important for us to be close to 1, and while K-Means gave a value of 0.5894, DBSCAN gave a value of 0.9746. Since the difference was quite high, we continued with DBSCAN. It was also observed with various visualizations. EPS detection was performed for hyperparameter, and for this, first of all, a k-distance graph was created. The graph was interpreted and a new eps value was obtained, and it was observed that the silhouette score increased with this value and the new score was 0.998. Thus, our processes for training were completed.

## **RESULTS**
**-Successfull Classification**

Using the Logistic Regression model, our project successfully identified whether job ads were authentic or fraudulent. Hyperparameter optimisation (using Randomised Search) led to a considerable boost in performance metrics, such as accuracy and F1-score.

**-Effective Clustering**

The dataset's hidden density-based structures and noise points were successfully exposed using the DBSCAN method. The clusters are highly separated and have high internal consistency, according to the Silhouette Score  that was produced by modifying the eps value using the k-distance plot. This demonstrated that the density patterns of genuine and fraudulent jobs differ.

## **FUTURE WORKS**
**-Enhanced Feature Engineering:** Creating new, insightful features.

**-Advanced Text Preprocessing:** Converting words into meaningful root forms through lemmatization and thus increasing the generalization ability of the model.

**-UI/Application Development**

**-Using Advanced Clustering Techniques and Classification Algorithms**

**-Feedback Mechanism:** Establishing a learning loop that will use user feedback to continuously improve the model (when an job is verified to be fraudulent).




