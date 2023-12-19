# Comparative Analysis of Machine Learning Classifiers on UCI Datasets
This study conducts a comprehensive analysis of three popular machine learning classifiers - Logistic Regression, SVM, and Random Forests- on three datasets from the UCI repository: Adult, German Credit, and Breast Cancer Wisconsin Diagnostic. Employing cross-validation techniques, we identify optimal hyperparameters for each classifier and dataset combination. Our findings offer insights into the classifiers' performance, measured by accuracy across varying data partitions. The results demonstrate notable trends in classifier effectiveness, with implications for practical applications in predictive modeling.

## Introduction
In the evolving field of machine learning, classifier comparison remains crucial for understanding the strengths and limitations of various algorithms. This study aims to evaluate Logistic Regression, SVM, and Random Forest classifiers using datasets from the UCI Machine Learning Repository. Our goal is to assess the performance of these classifiers, understanding their behavior across different datasets and training conditions.

## Method
Our methodology considers a rigorous cross-validation approach to fine-tune the hyperparameters of each classifier. The datasets employed—Adult, German Credit, and Breast Cancer Wisconsin Diagnostic—each have unique challenges, such as unbalanced classes, varying scales of measurement, and differing levels of feature correlations. To counter these challenges and to assess generalization performance, we split each dataset into three partitions: 20/80, 50/50, and 80/20, denoting the ratios of training data to testing data. 

## Datasets
We employ three datasets: Adult, German Credit, and Breast Cancer Wisconsin Diagnostic, each providing unique challenges and characteristics. 

### Adult dataset
This dataset, also known as the "Census Income" dataset, contains demographic information extracted from the 1994 Census database. It poses a binary classification problem where the task is to predict whether an individual earns more than $50,000 a year. The dataset is characterized by a mixture of continuous and categorical variables, including age, education, occupation, and hours per week.

### German credit dataset
The German Credit dataset presents data on individuals' credit risk from a German bank. Each entry represents a person described by a set of attributes, such as credit history, employment duration, and purpose of the loan. The target variable is binary, indicating high or low credit risk. The challenge with this dataset lies in its imbalanced nature and the presence of qualitative, subjective measures

### Breast cancer Wisconsin dataset
This dataset contains diagnostic information of breast cancer cases, where each case is labeled as malignant or benign. Features are computed from a digitized image of a fine needle aspirate (FNA) of a breast mass, describing characteristics of the cell nuclei present in the image. The complexity here is due to the high-dimensionality and the sensitive nature of the predictions

## Experiment
The cornerstone of our experimental design is a grid search strategy that traverses a predefined hyperparameter space for each classifier, seeking the configuration that yields the highest cross-validated accuracy. We train and test each classifier across the three datasets, meticulously recording performance metrics that reflect classification accuracy. The granularity of our approach allows us to not only capture a snapshot of each classifier's performance but also to interpret the broader trends that emerge across different datasets and training partitions.

## Results 
The results showcase how Logistic Regression, SVM, and Random Forest classifiers perform across three UCI datasets. Random Forest consistently excels, particularly with the Breast Cancer data, suggesting its strong fit for complex patterns. SVM shows competitive performance on the Adult dataset, indicating its capability with diverse features. Logistic Regression improves with more data, highlighting its reliance on larger datasets to better model relationships. Overall, more training data tends to enhance classifier accuracy, but the extent varies by classifier and dataset. These results align with expectations that more training data generally leads to better classifier performance.
![image](https://github.com/pranjlikhanna/COGS118A/assets/138069861/292f3ae2-6201-44b3-8b5f-5b3eb7e72b7a)

The results reveal a trend where the partition size impacts classifier performance. With the Breast Cancer dataset, Logistic Regression and Random Forest perform better with a more balanced split (50/50), suggesting they benefit from a sufficient amount of data to learn the intricate details. SVM's performance remains relatively lower across partitions, indicating potential issues with feature representation or model complexity.

For the Adult and German Credit datasets, the classifiers tend to perform better with more training data (80/20 split), highlighting the importance of ample examples to generalize effectively. However, the performance increase is not drastic, suggesting that after a certain point, additional data provides diminishing returns and that the quality of data and feature engineering may play a more significant role.
<img width="432" alt="image" src="https://github.com/pranjlikhanna/COGS118A/assets/138069861/17ed3607-f4b7-45ec-b182-13f1abf97106">
<img width="446" alt="image" src="https://github.com/pranjlikhanna/COGS118A/assets/138069861/194340f5-114e-4705-8818-167a3fdec901">
<img width="441" alt="image" src="https://github.com/pranjlikhanna/COGS118A/assets/138069861/9c3477d3-7630-4e1c-ac4a-9483e69f80ea">
In summary, while more data generally improves model performance, the optimal partition depends on the specific classifier and the dataset characteristics.

## Conclusion
The study confirms the efficacy of Random Forest in handling diverse datasets, showcasing its robustness, particularly in the Breast Cancer dataset. Logistic Regression, while performing admirably, is outshined by Random Forest in most cases. SVM, though competitive in certain partitions, does not consistently reach the performance heights of Random Forest. This comprehensive analysis aids in the informed selection of classifiers for specific datasets and scenarios, contributing valuable insights to the field of machine learning.
<img width="389" alt="image" src="https://github.com/pranjlikhanna/COGS118A/assets/138069861/56cf8cb7-b792-4c54-a1b9-2fff86bd8a52">
<img width="407" alt="image" src="https://github.com/pranjlikhanna/COGS118A/assets/138069861/99f65b1c-937c-421a-86b4-86003f1f34d6">
<img width="412" alt="image" src="https://github.com/pranjlikhanna/COGS118A/assets/138069861/13005228-6edc-481c-a97d-a1cef31f7447">

## References:
Caruana, R., & Niculescu-Mizil, A. (2006). An empirical comparison of supervised learning algorithms. In Proceedings of the 23rd international conference on Machine learning (pp. 161-168).

Dua, D., & Graff, C. (2019). UCI Machine Learning Repository [http://archive.ics.uci.edu/ml]. Irvine, CA: University of California, School of Information and Computer Science.













