# Heart Failure Survival Analysis, Winter 2026

Survival analysis of heart failure patients to identify key factors that distinguish survival from death. Students will learn visualization, statistical analysis, and machine learning techniques to predict patient outcomes.

**Key Finding**: Two features are sufficient to distinguish survival from death using different classifiers.

**[View Project Website](https://michigandatascienceteam.github.io/W26-MDST-Project_Heart-Failure-Survival-Analysis/)**

## Structure

Below is a high-level overview of the main components of this project.

<ins>**Dataset**</ins> {<small>`heart_failure_clinical_records_dataset.csv`</small>}
<br>
Heart failure clinical records from 299 patients with 13 features including age, ejection fraction, serum creatinine, and follow-up time. Binary outcome: survival or death.

<ins>**Week 1: Data Exploration**</ins> {<small>`Week1.ipynb`</small>}
<br>
Introduction to the dataset, exploratory data analysis, and visualization techniques using Pandas, Seaborn, and Matplotlib.

<ins>**Week 2: Statistical Analysis**</ins> {<small>`Week2.ipynb`</small>}
<br>
Hypothesis testing (T-test, Mann-Whitney U), correlation analysis, multiple testing correction (FDR), feature variance analysis, and Variance Inflation Factor (VIF) for detecting multicollinearity.

<ins>**Week 3: Unsupervised Learning**</ins> {<small>`Week3.ipynb`</small>}
<br>
Data normalization (Z-score), dimensionality reduction with PCA, K-Means clustering, hierarchical (agglomerative) clustering, confusion matrices, silhouette scores, and the elbow method.

<ins>**Week 4: Supervised Learning**</ins> {<small>`Week4.ipynb`</small>}
<br>
Train/test splitting with stratification, feature normalization, and classification algorithms including Logistic Regression, Random Forest, Support Vector Machines (SVM), and K-Nearest Neighbors (KNN). Model evaluation using accuracy, precision, recall, and F1-score metrics.

<ins>**Week 5: Hyperparameter Optimization**</ins> {<small>`Week5.ipynb`</small>}
<br>
Advanced techniques for tuning machine learning models using GridSearchCV, Random Search, and Bayesian Optimization with Optuna. Learn to efficiently search hyperparameter space and find optimal model configurations.

<ins>**Week 6: Ensemble Methods & Boosting**</ins> {<small>`Week6.ipynb`</small>}
<br>
From Random Forest to Gradient Boosting to LightGBM. Learn how ensemble methods combine weak learners into strong predictors. Includes hyperparameter tuning with Optuna, evaluation with 4 metrics, and hands-on exercises.

<ins>**Week 7: Feature Selection Methods**</ins> {<small>`Week7.ipynb`</small>}
<br>
Why fewer features often outperform more: Lasso (L1 penalty), Elastic Net (L1+L2), and MRMR filter method. Learn to identify which clinical features truly drive heart failure survival prediction.

<ins>**Week 8: Deep Learning for Medical Data**</ins> {<small>`Week8.ipynb`</small>}
<br>
Introduction to deep learning with Convolutional Neural Networks (CNNs) and Long Short-Term Memory (LSTMs). Learn neural network fundamentals, backpropagation, activation functions, and how to apply deep learning to clinical prediction tasks.

<ins>**Week 9: AI Model Interpretation (PLS-DA & SHAP)**</ins> {<small>`Week9.ipynb`</small>}
<br>
Interpretability and explainability in machine learning. Partial Least Squares Discriminant Analysis (PLS-DA) for supervised dimensionality reduction, and SHAP (SHapley Additive exPlanations) for understanding model predictions and feature importance in black-box models.

<ins>**Tutorials**</ins> {<small>`Git_Tutorial.ipynb`, `Venv_Tutorial.ipynb`</small>}
<br>
Interactive Jupyter notebooks for [Git basics](Git_Tutorial.ipynb) and [Python virtual environments](Venv_Tutorial.ipynb). Also available as markdown guides in [tutorials/](tutorials/) folder.

## Schedule

| **Week** | **Topic** | **Links** |
| --- | --- | --- |
| 1 | Data Exploration | [Notebook](Week1.ipynb), [Seaborn Docs](https://seaborn.pydata.org/), [Pandas Docs](https://pandas.pydata.org/docs/) |
| 2 | Statistical Analysis | [Notebook](Week2.ipynb), [Slides](slides/week2_slides.pdf), [Scipy Stats](https://docs.scipy.org/doc/scipy/reference/stats.html), [Statsmodels VIF](https://www.statsmodels.org/stable/generated/statsmodels.stats.outliers_influence.variance_inflation_factor.html) |
| 3 | Unsupervised Learning | [Notebook](Week3.ipynb), [Slides](slides/week3_slides.pdf), [PCA Guide](https://scikit-learn.org/stable/modules/decomposition.html#pca), [Clustering](https://scikit-learn.org/stable/modules/clustering.html) |
| 4 | Supervised Learning | [Notebook](Week4.ipynb), [Slides](slides/week4_slides.pdf), [Scikit-learn Classifiers](https://scikit-learn.org/stable/supervised_learning.html), [Model Evaluation](https://scikit-learn.org/stable/modules/model_evaluation.html) |
| 5 | Hyperparameter Optimization | [Notebook](Week5.ipynb), [Slides](slides/week5_slides.pdf), [Optuna Docs](https://optuna.readthedocs.io/), [GridSearchCV](https://scikit-learn.org/stable/modules/generated/sklearn.model_selection.GridSearchCV.html) |
| 6 | Ensemble Methods & Boosting | [Notebook](Week6.ipynb), [Slides](slides/week6_slides.pdf), [LightGBM Docs](https://lightgbm.readthedocs.io/), [Chicco & Jurman (2020)](https://bmcmedinformdecismak.biomedcentral.com/articles/10.1186/s12911-020-1023-5) |
| 7 | Feature Selection Methods | [Notebook](Week7.ipynb), [Scikit-learn Feature Selection](https://scikit-learn.org/stable/modules/feature_selection.html) |
| 8 | Deep Learning for Medical Data | [Notebook](Week8.ipynb), [TensorFlow Docs](https://www.tensorflow.org/), [Keras API](https://keras.io/), [Understanding Neural Networks](https://colah.github.io/posts/2014-03-NN-Manifolds-Topology/) |
| 9 | AI Model Interpretation (PLS-DA & SHAP) | [Notebook](Week9.ipynb), [Slides](slides/Week9_AI_Interpretation_PLSDA_SHAP.pptx), [SHAP Docs](https://shap.readthedocs.io/), [PLS-DA Guide](https://scikit-learn.org/stable/modules/cross_decomposition.html) |

## Research Background

This project is based on the paper by Chicco & Jurman (2020):

> **Machine learning can predict survival of patients with heart failure from serum creatinine and ejection fraction alone**
> *BMC Medical Informatics and Decision Making, 20, 16*

**Key Findings from the Paper:**
- Applied several ML classifiers (Random Forest, Gradient Boosting, SVM, etc.) to predict survival
- Discovered that **serum creatinine** and **ejection fraction** alone achieve strong predictive performance
- Random Forest achieved the best results with Matthews Correlation Coefficient (MCC) of 0.418
- Feature ranking analysis revealed time, serum creatinine, and ejection fraction as top predictors
- Demonstrated that complex models with all 13 features do not significantly outperform simpler 2-feature models

**Clinical Relevance:**
- Serum creatinine indicates kidney function, often impaired in heart failure patients
- Ejection fraction measures heart pumping efficiency, a direct indicator of cardiac health
- These two biomarkers are routinely measured and can guide clinical decision-making

[Read the full paper](https://bmcmedinformdecismak.biomedcentral.com/articles/10.1186/s12911-020-1023-5)

## Resources

### Project
- [Project Website](https://michigandatascienceteam.github.io/W26-MDST-Project_Heart-Failure-Survival-Analysis/)
- [UCI Dataset](https://archive.ics.uci.edu/ml/datasets/Heart+failure+clinical+records)

### Setup Tutorials (Interactive Jupyter Notebooks)
- [Git Tutorial](Git_Tutorial.ipynb) - Installation, setup, commands, workflows, branching
- [Virtual Environment Tutorial](Venv_Tutorial.ipynb) - Python venv, package management, troubleshooting

### Libraries & Tools
- [Scikit-learn](https://scikit-learn.org/stable/) - Machine learning
- [Pandas](https://pandas.pydata.org/docs/) - Data manipulation
- [Seaborn](https://seaborn.pydata.org/) - Data visualization
- [LightGBM](https://lightgbm.readthedocs.io/) - Gradient boosting
- [Optuna](https://optuna.readthedocs.io/) - Hyperparameter optimization

## Acknowledgements

<big>**Leads**</big>
<br>
Sina Bonakdar
<br>
Terry Zhang

## License

This project is licensed under the MIT License - see the [LICENSE](LICENSE) file for details.
