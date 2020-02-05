Feature-Engineering-Handbook
============
Welcome! This repo provides an interactive and complete practical feature engineering tutorial in Jupyter Notebook. It contains three parts: [Data Prepocessing](1.%20Data%20Preprocessing.ipynb), [Feature Selection](2.%20Feature%20Selection.ipynb) and [Dimension Reduction](3.%20Dimension%20Reduction.ipynb). Each part is demonstrated separately in one notebook. Since some feature selection algorithms such as Simulated Annealing and Genetic Algorithm lack complete implementation in python, we also provide corresponding python scripts ([Simulated Annealing](SA.py), [Genetic Algorithm](GA.py)) and cover them in our tutorial for your reference. 


Brief Introduction
------------
- [Notebook One](1.%20Data%20Preprocessing.ipynb) covers data preprocessing on static continuous features based on [scikit-learn](https://scikit-learn.org/stable/), on static categorical features based on [Category Encoders](https://contrib.scikit-learn.org/categorical-encoding/), and on time series features based on [Featuretools](https://www.featuretools.com/).  
  
- [Notebook Two](2.%20Feature%20Selection.ipynb) covers feature selection including univariate filter methods based on [scikit-learn](https://scikit-learn.org/stable/), multivariate filter methods based on [scikit-feature](http://featureselection.asu.edu/), deterministic wrapper methods based on [scikit-learn](https://scikit-learn.org/stable/), randomized wrapper methods based on our implementations in python scrips, and embedded methods based on [scikit-learn](https://scikit-learn.org/stable/).
  
- [Notebook Three](3.%20Dimension%20Reduction.ipynb) covers supervised and unsupervised dimension reduction based on [scikit-learn](https://scikit-learn.org/stable/).


Table of Content
------------
<div class="toc"><ul class="toc-item"><li><span><a href="#Data-Prepocessing" data-toc-modified-id="Data-Prepocessing-1"><span class="toc-item-num">1&nbsp;&nbsp;</span>Data Prepocessing</a></span><ul class="toc-item"><li><span><a href="#Static-Continuous-Variables" data-toc-modified-id="Static-Continuous-Variables-1.1"><span class="toc-item-num">1.1&nbsp;&nbsp;</span>Static Continuous Variables</a></span><ul class="toc-item"><li><span><a href="#Discretization" data-toc-modified-id="Discretization-1.1.1"><span class="toc-item-num">1.1.1&nbsp;&nbsp;</span>Discretization</a></span><ul class="toc-item"><li><span><a href="#Binarization" data-toc-modified-id="Binarization-1.1.1.1"><span class="toc-item-num">1.1.1.1&nbsp;&nbsp;</span>Binarization</a></span></li><li><span><a href="#Binning" data-toc-modified-id="Binning-1.1.1.2"><span class="toc-item-num">1.1.1.2&nbsp;&nbsp;</span>Binning</a></span></li></ul></li><li><span><a href="#Scaling" data-toc-modified-id="Scaling-1.1.2"><span class="toc-item-num">1.1.2&nbsp;&nbsp;</span>Scaling</a></span><ul class="toc-item"><li><span><a href="#Stardard-Scaling-(Z-score-standardization)" data-toc-modified-id="Stardard-Scaling-(Z-score-standardization)-1.1.2.1"><span class="toc-item-num">1.1.2.1&nbsp;&nbsp;</span>Stardard Scaling (Z-score standardization)</a></span></li><li><span><a href="#MinMaxScaler-(Scale-to-range)" data-toc-modified-id="MinMaxScaler-(Scale-to-range)-1.1.2.2"><span class="toc-item-num">1.1.2.2&nbsp;&nbsp;</span>MinMaxScaler (Scale to range)</a></span></li><li><span><a href="#RobustScaler-(Anti-outliers-scaling)" data-toc-modified-id="RobustScaler-(Anti-outliers-scaling)-1.1.2.3"><span class="toc-item-num">1.1.2.3&nbsp;&nbsp;</span>RobustScaler (Anti-outliers scaling)</a></span></li><li><span><a href="#Power-Transform-(Non-linear-transformation)" data-toc-modified-id="Power-Transform-(Non-linear-transformation)-1.1.2.4"><span class="toc-item-num">1.1.2.4&nbsp;&nbsp;</span>Power Transform (Non-linear transformation)</a></span></li></ul></li><li><span><a href="#Normalization" data-toc-modified-id="Normalization-1.1.3"><span class="toc-item-num">1.1.3&nbsp;&nbsp;</span>Normalization</a></span></li><li><span><a href="#Imputation-of-missing-values" data-toc-modified-id="Imputation-of-missing-values-1.1.4"><span class="toc-item-num">1.1.4&nbsp;&nbsp;</span>Imputation of missing values</a></span><ul class="toc-item"><li><span><a href="#Univariate-feature-imputation" data-toc-modified-id="Univariate-feature-imputation-1.1.4.1"><span class="toc-item-num">1.1.4.1&nbsp;&nbsp;</span>Univariate feature imputation</a></span></li><li><span><a href="#Multivariate-feature-imputation" data-toc-modified-id="Multivariate-feature-imputation-1.1.4.2"><span class="toc-item-num">1.1.4.2&nbsp;&nbsp;</span>Multivariate feature imputation</a></span></li><li><span><a href="#Marking-imputed-values" data-toc-modified-id="Marking-imputed-values-1.1.4.3"><span class="toc-item-num">1.1.4.3&nbsp;&nbsp;</span>Marking imputed values</a></span></li></ul></li><li><span><a href="#Feature-Transformation" data-toc-modified-id="Feature-Transformation-1.1.5"><span class="toc-item-num">1.1.5&nbsp;&nbsp;</span>Feature Transformation</a></span><ul class="toc-item"><li><span><a href="#Polynomial-Transformation" data-toc-modified-id="Polynomial-Transformation-1.1.5.1"><span class="toc-item-num">1.1.5.1&nbsp;&nbsp;</span>Polynomial Transformation</a></span></li><li><span><a href="#Custom-Transformation" data-toc-modified-id="Custom-Transformation-1.1.5.2"><span class="toc-item-num">1.1.5.2&nbsp;&nbsp;</span>Custom Transformation</a></span></li></ul></li></ul></li><li><span><a href="#Static-Categorical-Variables" data-toc-modified-id="Static-Categorical-Variables-1.2"><span class="toc-item-num">1.2&nbsp;&nbsp;</span>Static Categorical Variables</a></span><ul class="toc-item"><li><span><a href="#Ordinal-Encoding" data-toc-modified-id="Ordinal-Encoding-1.2.1"><span class="toc-item-num">1.2.1&nbsp;&nbsp;</span>Ordinal Encoding</a></span></li><li><span><a href="#One-hot-Encoding" data-toc-modified-id="One-hot-Encoding-1.2.2"><span class="toc-item-num">1.2.2&nbsp;&nbsp;</span>One-hot Encoding</a></span></li><li><span><a href="#Hashing-Encoding" data-toc-modified-id="Hashing-Encoding-1.2.3"><span class="toc-item-num">1.2.3&nbsp;&nbsp;</span>Hashing Encoding</a></span></li><li><span><a href="#Helmert-Coding" data-toc-modified-id="Helmert-Coding-1.2.4"><span class="toc-item-num">1.2.4&nbsp;&nbsp;</span>Helmert Coding</a></span></li><li><span><a href="#Sum-(Deviation)-Coding" data-toc-modified-id="Sum-(Deviation)-Coding-1.2.5"><span class="toc-item-num">1.2.5&nbsp;&nbsp;</span>Sum (Deviation) Coding</a></span></li><li><span><a href="#Target-Encoding" data-toc-modified-id="Target-Encoding-1.2.6"><span class="toc-item-num">1.2.6&nbsp;&nbsp;</span>Target Encoding</a></span></li><li><span><a href="#M-estimate-Encoding" data-toc-modified-id="M-estimate-Encoding-1.2.7"><span class="toc-item-num">1.2.7&nbsp;&nbsp;</span>M-estimate Encoding</a></span></li><li><span><a href="#James-Stein-Encoder" data-toc-modified-id="James-Stein-Encoder-1.2.8"><span class="toc-item-num">1.2.8&nbsp;&nbsp;</span>James-Stein Encoder</a></span></li><li><span><a href="#Weight-of-Evidence-Encoder" data-toc-modified-id="Weight-of-Evidence-Encoder-1.2.9"><span class="toc-item-num">1.2.9&nbsp;&nbsp;</span>Weight of Evidence Encoder</a></span></li><li><span><a href="#Leave-One-Out-Encoder" data-toc-modified-id="Leave-One-Out-Encoder-1.2.10"><span class="toc-item-num">1.2.10&nbsp;&nbsp;</span>Leave One Out Encoder</a></span></li><li><span><a href="#Catboost-Encoder" data-toc-modified-id="Catboost-Encoder-1.2.11"><span class="toc-item-num">1.2.11&nbsp;&nbsp;</span>Catboost Encoder</a></span></li></ul></li><li><span><a href="#Time-Series-Variables" data-toc-modified-id="Time-Series-Variables-1.3"><span class="toc-item-num">1.3&nbsp;&nbsp;</span>Time Series Variables</a></span><ul class="toc-item"><li><span><a href="#Time-Series-Categorical-Features" data-toc-modified-id="Time-Series-Categorical-Features-1.3.1"><span class="toc-item-num">1.3.1&nbsp;&nbsp;</span>Time Series Categorical Features</a></span></li><li><span><a href="#Time-Series-Continuous-Features" data-toc-modified-id="Time-Series-Continuous-Features-1.3.2"><span class="toc-item-num">1.3.2&nbsp;&nbsp;</span>Time Series Continuous Features</a></span></li><li><span><a href="#Implementation" data-toc-modified-id="Implementation-1.3.3"><span class="toc-item-num">1.3.3&nbsp;&nbsp;</span>Implementation</a></span><ul class="toc-item"><li><span><a href="#Create-EntitySet" data-toc-modified-id="Create-EntitySet-1.3.3.1"><span class="toc-item-num">1.3.3.1&nbsp;&nbsp;</span>Create EntitySet</a></span></li><li><span><a href="#Set-up-cut-time" data-toc-modified-id="Set-up-cut-time-1.3.3.2"><span class="toc-item-num">1.3.3.2&nbsp;&nbsp;</span>Set up cut-time</a></span></li><li><span><a href="#Auto-Feature-Engineering" data-toc-modified-id="Auto-Feature-Engineering-1.3.3.3"><span class="toc-item-num">1.3.3.3&nbsp;&nbsp;</span>Auto Feature Engineering</a></span></li></ul></li></ul></li></ul></li><li><span><a href="#Feature-Selection" data-toc-modified-id="Feature-Selection-2"><span class="toc-item-num">2&nbsp;&nbsp;</span>Feature Selection</a></span><ul class="toc-item"><li><span><a href="#Filter-Methods" data-toc-modified-id="Filter-Methods-2.1"><span class="toc-item-num">2.1&nbsp;&nbsp;</span>Filter Methods</a></span><ul class="toc-item"><li><span><a href="#Univariate-Filter-Methods" data-toc-modified-id="Univariate-Filter-Methods-2.1.1"><span class="toc-item-num">2.1.1&nbsp;&nbsp;</span>Univariate Filter Methods</a></span><ul class="toc-item"><li><span><a href="#Variance-Threshold" data-toc-modified-id="Variance-Threshold-2.1.1.1"><span class="toc-item-num">2.1.1.1&nbsp;&nbsp;</span>Variance Threshold</a></span></li><li><span><a href="#Pearson-Correlation-(regression-problem)" data-toc-modified-id="Pearson-Correlation-(regression-problem)-2.1.1.2"><span class="toc-item-num">2.1.1.2&nbsp;&nbsp;</span>Pearson Correlation (regression problem)</a></span></li><li><span><a href="#Distance-Correlation-(regression-problem)" data-toc-modified-id="Distance-Correlation-(regression-problem)-2.1.1.3"><span class="toc-item-num">2.1.1.3&nbsp;&nbsp;</span>Distance Correlation (regression problem)</a></span></li><li><span><a href="#F-Score-(regression-problem)" data-toc-modified-id="F-Score-(regression-problem)-2.1.1.4"><span class="toc-item-num">2.1.1.4&nbsp;&nbsp;</span>F-Score (regression problem)</a></span></li><li><span><a href="#Mutual-Information-(regression-problem)" data-toc-modified-id="Mutual-Information-(regression-problem)-2.1.1.5"><span class="toc-item-num">2.1.1.5&nbsp;&nbsp;</span>Mutual Information (regression problem)</a></span></li><li><span><a href="#Chi-squared-Statistics-(classification-problem)" data-toc-modified-id="Chi-squared-Statistics-(classification-problem)-2.1.1.6"><span class="toc-item-num">2.1.1.6&nbsp;&nbsp;</span>Chi-squared Statistics (classification problem)</a></span></li><li><span><a href="#F-Score-(classification-problem)" data-toc-modified-id="F-Score-(classification-problem)-2.1.1.7"><span class="toc-item-num">2.1.1.7&nbsp;&nbsp;</span>F-Score (classification problem)</a></span></li><li><span><a href="#Mutual-Information-(classification-problem)" data-toc-modified-id="Mutual-Information-(classification-problem)-2.1.1.8"><span class="toc-item-num">2.1.1.8&nbsp;&nbsp;</span>Mutual Information (classification problem)</a></span></li></ul></li><li><span><a href="#Multivariate-Filter-Methods" data-toc-modified-id="Multivariate-Filter-Methods-2.1.2"><span class="toc-item-num">2.1.2&nbsp;&nbsp;</span>Multivariate Filter Methods</a></span><ul class="toc-item"><li><span><a href="#Max-Relevance-Min-Redundancy-(mRMR)" data-toc-modified-id="Max-Relevance-Min-Redundancy-(mRMR)-2.1.2.1"><span class="toc-item-num">2.1.2.1&nbsp;&nbsp;</span>Max-Relevance Min-Redundancy (mRMR)</a></span></li><li><span><a href="#Correlation-based-Feature-Selection-(CFS)" data-toc-modified-id="Correlation-based-Feature-Selection-(CFS)-2.1.2.2"><span class="toc-item-num">2.1.2.2&nbsp;&nbsp;</span>Correlation-based Feature Selection (CFS)</a></span></li><li><span><a href="#Fast-Correlation-based-Filter-(FCBF)" data-toc-modified-id="Fast-Correlation-based-Filter-(FCBF)-2.1.2.3"><span class="toc-item-num">2.1.2.3&nbsp;&nbsp;</span>Fast Correlation-based Filter (FCBF)</a></span></li><li><span><a href="#ReliefF" data-toc-modified-id="ReliefF-2.1.2.4"><span class="toc-item-num">2.1.2.4&nbsp;&nbsp;</span>ReliefF</a></span></li><li><span><a href="#Spectral-Feature-Selection-(SPEC)" data-toc-modified-id="Spectral-Feature-Selection-(SPEC)-2.1.2.5"><span class="toc-item-num">2.1.2.5&nbsp;&nbsp;</span>Spectral Feature Selection (SPEC)</a></span></li></ul></li></ul></li><li><span><a href="#Wrapper-Methods" data-toc-modified-id="Wrapper-Methods-2.2"><span class="toc-item-num">2.2&nbsp;&nbsp;</span>Wrapper Methods</a></span><ul class="toc-item"><li><span><a href="#Deterministic-Algorithms" data-toc-modified-id="Deterministic-Algorithms-2.2.1"><span class="toc-item-num">2.2.1&nbsp;&nbsp;</span>Deterministic Algorithms</a></span><ul class="toc-item"><li><span><a href="#Recursive-Feature-Elimination-(SBS)" data-toc-modified-id="Recursive-Feature-Elimination-(SBS)-2.2.1.1"><span class="toc-item-num">2.2.1.1&nbsp;&nbsp;</span>Recursive Feature Elimination (SBS)</a></span></li></ul></li><li><span><a href="#Randomized-Algorithms" data-toc-modified-id="Randomized-Algorithms-2.2.2"><span class="toc-item-num">2.2.2&nbsp;&nbsp;</span>Randomized Algorithms</a></span><ul class="toc-item"><li><span><a href="#Simulated-Annealing-(SA)" data-toc-modified-id="Simulated-Annealing-(SA)-2.2.2.1"><span class="toc-item-num">2.2.2.1&nbsp;&nbsp;</span>Simulated Annealing (SA)</a></span></li><li><span><a href="#Genetic-Algorithm-(GA)" data-toc-modified-id="Genetic-Algorithm-(GA)-2.2.2.2"><span class="toc-item-num">2.2.2.2&nbsp;&nbsp;</span>Genetic Algorithm (GA)</a></span></li></ul></li></ul></li><li><span><a href="#Embedded-Methods" data-toc-modified-id="Embedded-Methods-2.3"><span class="toc-item-num">2.3&nbsp;&nbsp;</span>Embedded Methods</a></span><ul class="toc-item"><li><span><a href="#Regulization-Based-Methods" data-toc-modified-id="Regulization-Based-Methods-2.3.1"><span class="toc-item-num">2.3.1&nbsp;&nbsp;</span>Regulization Based Methods</a></span><ul class="toc-item"><li><span><a href="#Lasso-Regression-(Linear-Regression-with-L1-Norm)" data-toc-modified-id="Lasso-Regression-(Linear-Regression-with-L1-Norm)-2.3.1.1"><span class="toc-item-num">2.3.1.1&nbsp;&nbsp;</span>Lasso Regression (Linear Regression with L1 Norm)</a></span></li><li><span><a href="#Logistic-Regression-(with-L1-Norm)" data-toc-modified-id="Logistic-Regression-(with-L1-Norm)-2.3.1.2"><span class="toc-item-num">2.3.1.2&nbsp;&nbsp;</span>Logistic Regression (with L1 Norm)</a></span></li><li><span><a href="#LinearSVR/-LinearSVC" data-toc-modified-id="LinearSVR/-LinearSVC-2.3.1.3"><span class="toc-item-num">2.3.1.3&nbsp;&nbsp;</span>LinearSVR/ LinearSVC</a></span></li></ul></li><li><span><a href="#Tree-Based-Methods" data-toc-modified-id="Tree-Based-Methods-2.3.2"><span class="toc-item-num">2.3.2&nbsp;&nbsp;</span>Tree Based Methods</a></span></li></ul></li></ul></li><li><span><a href="#Dimension-Reduction" data-toc-modified-id="Dimension-Reduction-3"><span class="toc-item-num">3&nbsp;&nbsp;</span>Dimension Reduction</a></span><ul class="toc-item"><li><span><a href="#Unsupervised-Methods" data-toc-modified-id="Unsupervised-Methods-3.1"><span class="toc-item-num">3.1&nbsp;&nbsp;</span>Unsupervised Methods</a></span><ul class="toc-item"><li><span><a href="#PCA-(Principal-Components-Analysis)" data-toc-modified-id="PCA-(Principal-Components-Analysis)-3.1.1"><span class="toc-item-num">3.1.1&nbsp;&nbsp;</span>PCA (Principal Components Analysis)</a></span></li></ul></li><li><span><a href="#Supervised-Methods" data-toc-modified-id="Supervised-Methods-3.2"><span class="toc-item-num">3.2&nbsp;&nbsp;</span>Supervised Methods</a></span><ul class="toc-item"><li><span><a href="#LDA-(Linear-Discriminant-Analysis)" data-toc-modified-id="LDA-(Linear-Discriminant-Analysis)-3.2.1"><span class="toc-item-num">3.2.1&nbsp;&nbsp;</span>LDA (Linear Discriminant Analysis)</a></span></li></ul></li></ul></li></ul></div>

Reference
------------
References have been included in each Jupyter Notebooks.

Author
------------
[**@Yingxiang Chen**](https://github.com/YC-Coder-Chen)  
[**@Zihan Yang**](https://github.com/echoyang48)

Contact
------------
**If there are any mistakes, please feel free to reach out and correct us!**  

Yingxiang Chen E-mail: chenyingxiang3526@gmail.com  
Zihan Yang E-mai: echoyang48@gmail.com
