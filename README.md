# Time-Series-Classification-in-Unsupervised-way
Here is the grammatically corrected version:

---

Developed and implemented innovative classification models for analyzing time series data from IoT devices, securing 1st place in the competition. 
Utilized advanced techniques in Python and Sklearn, enhancing predictive accuracy and efficiency in signal processing tasks.

**Data Processing:**
  
  1. Chunked the dataset into time stamps of 125 to align with the test dataset.
  2. Normalized the entire dataset to avoid ECAPA errors.

**Feature Engineering:** This is the main step in the entire model.

  1. Since the time-series data is represented in the form of signals, we can identify signals by their properties such as mean, variance, kurtosis,
     skewness, slope, number of peaks, power, area under the curve, entropy, percentiles, and moments.
  2. The given dataset is in the time domain, so we can apply Fourier Transformations to convert it into the frequency domain and use
     frequency domain features like magnitude of frequency, spectral centroid, spectral bandwidth, mean, variance, surface area, autocorrelation, etc.
  3. Similarly to step 2, I converted the entire signal into the energy domain and used some features from this domain.
  4. In the last step, I applied a clustering algorithm to the entire time series dataset and used the elbow method to find the optimal number of
     clusters for this dataset. After getting the cluster centroids, I used the distance between a datapoint and its cluster centroid as a feature.
     The previous three steps gave me about 60% accuracy, but this additional feature boosted it by 5-6 %, helping me win the contest.

For training, I used KNN, after experiment with different values of K, Got the optimal results at K = 110. Beacuse making K too small makes the model
prone to overfitting and making K too large make to underfitting.

Final scores: 
  Accuracy: 0.662514619883041
  Precision: 0.6511196063429346
  Recall: 0.662514619883041
  F1 Score: 0.6549743899756382


Competition link : https://www.kaggle.com/competitions/unsupervised-learning-m2023/overview



You can acess dataset from here : https://drive.google.com/file/d/18ZLq11vlaiL_OgJvoeWLRWAaSzIvGT-E/view?usp=sharing
