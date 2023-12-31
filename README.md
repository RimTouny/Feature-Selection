# **Mobile Crowd Sensing (MCS) Data Analysis with NB and KNN Classifiers Using Differnet Feature Selection Methods**
Delved into advanced techniques to enhance ML performance during the uOttawa 2023 ML course. This repository offers Python implementations of Naïve Bayes (NB) and K-Nearest Neighbor (KNN) classifiers on the MCS dataset.

- Required libraries: scikit-learn, pandas, matplotlib.
- Execute cells in a Jupyter Notebook environment.

## Binary-class classification problem
Task is to classify the  MCS dataset legitimacy status: Legitimate / Fake.

### Independent Variables:
   +	Features include ID, Latitude, Longitude, Day, Hour, Minute, Duration, RemainingTime, Resources, Coverage, OnPeakHours, GridNumber.
### Target variable:
   +	'Legitimacy' column represents the target with two classes: 'Legitimate' and 'Fake'.

## **Key Tasks Undertaken**

1. **Dataset Splitting based on 'Day' Feature:**
   -  Created training (days 0, 1, 2) and test (day 3) datasets based on 'day' feature values.
       ![image](https://github.com/RimTouny/Mobile-Crowd-Sensing-MCS-Data-Analysis-with-NB-and-KNN-Classifiers/assets/48333870/c24aca3d-6ca6-43d3-91f1-5b10d4dd6515)

     
2. **Baseline Performance of NB and KNN:**
   - Presented confusion matrices and F1 scores as baseline performance measures for both classifiers.
       + Bernoulli Naive Bayes
       ![merge_from_ofoct](https://github.com/RimTouny/Mobile-Crowd-Sensing-MCS-Data-Analysis-with-NB-and-KNN-Classifiers/assets/48333870/4772b24d-fdfc-416c-a16d-bc83bd15bd5e)

       + K-Nearest Neighbors
         ![merge_from_ofoct (1)](https://github.com/RimTouny/Mobile-Crowd-Sensing-MCS-Data-Analysis-with-NB-and-KNN-Classifiers/assets/48333870/17930679-fd58-4b8a-a384-3daa19834cff)


     - 2D TSNE plots for Training and Testing Set
       ![merge_from_ofoct](https://github.com/RimTouny/Mobile-Crowd-Sensing-MCS-Data-Analysis-with-NB-and-KNN-Classifiers/assets/48333870/1e43cedd-ce31-4731-9377-b071a4e7b3e8)


3. **Dimensionality Reduction (DR) using PCA and Auto Encoder (AE):**
   - Explored PCA and AE methods to determine optimal reduced dimensions based on F1 scores of test datasets.
   - Plotted the number of components vs. F1 score for both classifiers, showcasing the best performance.
       ![merge_from_ofoct (1)](https://github.com/RimTouny/Mobile-Crowd-Sensing-MCS-Data-Analysis-with-NB-and-KNN-Classifiers/assets/48333870/84427dc4-8eea-4c01-826e-9a1affa450a4)

       + Maximum of PCA-Bernoulli Naive Bayes: 93.31858407079646
       * Best number of n_components PCA-Bernoulli Naive Bayes: 10
           ![merge_from_ofoct](https://github.com/RimTouny/Mobile-Crowd-Sensing-MCS-Data-Analysis-with-NB-and-KNN-Classifiers/assets/48333870/4853ceaf-8e52-4202-96f4-2af149037620)

       + Maximum of PCA-K-Nearest Neighbors: 94.81165600568585
       * Best number of n_components PCA-K-Nearest Neighbors: 2
           ![merge_from_ofoct (1)](https://github.com/RimTouny/Mobile-Crowd-Sensing-MCS-Data-Analysis-with-NB-and-KNN-Classifiers/assets/48333870/7c59c64d-2577-41bb-8fd4-49f43f13ee2c)

   4. **Feature Selection with Filter and Wrapper Methods:**
      
   - Explored feature selection methods such as Information Gain, Mutual Information, Variance Threshold, and Chi-Square to determine the optimal number of features and analyzed the relationship between the number of features and F1 scores, improving baseline performance.
     ![merge_from_ofoct (2)](https://github.com/RimTouny/Mobile-Crowd-Sensing-MCS-Data-Analysis-with-NB-and-KNN-Classifiers/assets/48333870/10547a76-166a-43a4-8637-72bd12311ee9)

   - Employed Wrapper Selection techniques like Forward Feature Elimination, Back Feature Elimination, and Recursive Feature Elimination to evaluate feature relevance. Investigated the correlation between the number of features and F1 scores, enhancing the baseline performance.
     ![merge_from_ofoct](https://github.com/RimTouny/Mobile-Crowd-Sensing-MCS-Data-Analysis-with-NB-and-KNN-Classifiers/assets/48333870/f7059485-053b-4f6f-a8ff-09575af60309)

   - Visualized results through 2D TSNE plots using the selected best method for both training and test datasets.
     ![merge_from_ofoct](https://github.com/RimTouny/Mobile-Crowd-Sensing-MCS-Data-Analysis-with-NB-and-KNN-Classifiers/assets/48333870/c8b6558b-e642-4317-9da7-280b76de6db2)

     ![merge_from_ofoct (2)](https://github.com/RimTouny/Mobile-Crowd-Sensing-MCS-Data-Analysis-with-NB-and-KNN-Classifiers/assets/48333870/288b213b-954b-4ffd-83c3-aaa6f5230c1b)


6. **Clustering Analysis using Latitude and Longitude:**
   - Explored clustering methods (K-means, SOFM, DBSCAN) on latitude and longitude features to identify legitimate-only clusters.
   - Plotted the total number of legitimate-only members in legitimate clusters against different cluster numbers for each algorithm.
     ![merge_from_ofoct (5)](https://github.com/RimTouny/Mobile-Crowd-Sensing-MCS-Data-Analysis-with-NB-and-KNN-Classifiers/assets/48333870/f9bdbda9-6603-4e7f-bf47-b84bc57b612c)


