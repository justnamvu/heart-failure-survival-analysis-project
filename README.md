# Heart Failure Survival Analysis | Michigan Data Science Team - W26

Survival analysis of heart failure patients to identify key factors that distinguish survival from death. Key findings: Two features are sufficient to distinguish survival from death using different classifiers.

**[View Project Website](https://michigandatascienceteam.github.io/W26-MDST-Project_Heart-Failure-Survival-Analysis/)**

## Structure

**Dataset** (<small>`heart_failure_clinical_records_dataset.csv`</small>)
<br>
Heart failure clinical records from 299 patients with 13 features including age, ejection fraction, serum creatinine, and follow-up time. Binary outcome: survival or death.

**Week 1: Data Exploration** (<small>`week_1.ipynb`</small>)
<br>
Introduction to the dataset, exploratory data analysis, and visualization techniques using Pandas, Seaborn, and Matplotlib.

**Week 2: Statistical Analysis** (<small>`week_2.ipynb`</small>)
<br>
Hypothesis testing (T-test, Mann-Whitney U), correlation analysis, multiple testing correction (FDR), feature variance analysis, and Variance Inflation Factor (VIF) for detecting multicollinearity.

**Week 3: Unsupervised Learning** (<small>`week_3.ipynb`</small>)
<br>
Data normalization (Z-score), dimensionality reduction with PCA, K-Means clustering, hierarchical (agglomerative) clustering, confusion matrices, silhouette scores, and the elbow method.

**Week 4: Supervised Learning** (<small>`week_4.ipynb`</small>)
<br>
Train/test splitting with stratification, feature normalization, and classification algorithms including Logistic Regression, Random Forest, Support Vector Machines (SVM), and K-Nearest Neighbors (KNN). Model evaluation using accuracy, precision, recall, and F1-score metrics.

**Week 5: Hyperparameter Optimization** (<small>`week_5.ipynb`</small>)
<br>
Advanced techniques for tuning ML models using GridSearchCV, Random Search, and Bayesian Optimization with Optuna. Learn to efficiently search hyperparameter space and find optimal model configurations.

**Week 6: Ensemble Methods & Boosting** (<small>`week_6.ipynb`</small>)
<br>
From Random Forest to Gradient Boosting to LightGBM. Learn how ensemble methods combine weak learners into strong predictors. Includes hyperparameter tuning with Optuna, evaluation with 4 metrics, and hands-on exercises.

**Week 7: Feature Selection Methods** (<small>`week_7.ipynb`</small>)
<br>
Why fewer features often outperform more: Lasso (L1 penalty), Elastic Net (L1+L2), and MRMR filter method. Learn to identify which clinical features truly drive heart failure survival prediction.

**Week 8: Deep Learning for Medical Data** (<small>`week_8.ipynb`</small>)
<br>
Introduction to deep learning with Convolutional Neural Networks (CNNs) and Long Short-Term Memory (LSTMs). Learn neural network fundamentals, backpropagation, activation functions, and how to apply deep learning to clinical prediction tasks.

**Week 9: AI Model Interpretation (PLS-DA & SHAP)** (<small>`week_9.ipynb`</small>)
<br>
Interpretability and explainability in ML. Partial Least Squares Discriminant Analysis (PLS-DA) for supervised dimensionality reduction, and SHAP (SHapley Additive exPlanations) for understanding model predictions and feature importance in black-box models.

**Tutorials** (<small>`git_tutorial.ipynb`, `venv_tutorial.ipynb`</small>)
<br>
Interactive Jupyter notebooks (also available as markdown guides) for [Git basics](tutorials/git_tutorial.ipynb) and [Python virtual environments](tutorials/venv_tutorial.ipynb) in [tutorials/](tutorials/) folder.

## Schedule

| Week | Topic | Links |
| - | - | - |
| 1 | Data Exploration | [Notebook](week_1.ipynb), [Seaborn Docs](https://seaborn.pydata.org/), [Pandas Docs](https://pandas.pydata.org/docs/) |
| 2 | Statistical Analysis | [Notebook](week_2.ipynb), [Slides](slides/week_2_slides.pdf), [Scipy Stats](https://docs.scipy.org/doc/scipy/reference/stats.html), [Statsmodels VIF](https://www.statsmodels.org/stable/generated/statsmodels.stats.outliers_influence.variance_inflation_factor.html) |
| 3 | Unsupervised Learning | [Notebook](week_3.ipynb), [Slides](slides/week_3_slides.pdf), [PCA Guide](https://scikit-learn.org/stable/modules/decomposition.html#pca), [Clustering](https://scikit-learn.org/stable/modules/clustering.html) |
| 4 | Supervised Learning | [Notebook](week_4.ipynb), [Slides](slides/week_4_slides.pdf), [Scikit-learn Classifiers](https://scikit-learn.org/stable/supervised_learning.html), [Model Evaluation](https://scikit-learn.org/stable/modules/model_evaluation.html) |
| 5 | Hyperparameter Optimization | [Notebook](week_5.ipynb), [Slides](slides/week_5_slides.pdf), [Optuna Docs](https://optuna.readthedocs.io/), [GridSearchCV](https://scikit-learn.org/stable/modules/generated/sklearn.model_selection.GridSearchCV.html) |
| 6 | Ensemble Methods & Boosting | [Notebook](week_6.ipynb), [Slides](slides/week_6_slides.pdf), [LightGBM Docs](https://lightgbm.readthedocs.io/), [Chicco & Jurman (2020)](https://bmcmedinformdecismak.biomedcentral.com/articles/10.1186/s12911-020-1023-5) |
| 7 | Feature Selection Methods | [Notebook](week_7.ipynb), [Scikit-learn Feature Selection](https://scikit-learn.org/stable/modules/feature_selection.html) |
| 8 | Deep Learning for Medical Data | [Notebook](week_8.ipynb), [TensorFlow Docs](https://www.tensorflow.org/), [Keras API](https://keras.io/), [Understanding Neural Networks](https://colah.github.io/posts/2014-03-NN-Manifolds-Topology/) |
| 9 | AI Model Interpretation (PLS-DA & SHAP) | [Notebook](week_9.ipynb), [Slides](slides/week_9_slides.pptx), [SHAP Docs](https://shap.readthedocs.io/), [PLS-DA Guide](https://scikit-learn.org/stable/modules/cross_decomposition.html) |

## Research Background

This project is based on the paper:

> **Chicco, D., Jurman, G. Machine learning can predict survival of patients with heart failure from serum creatinine and ejection fraction alone. BMC Med Inform Decis Mak 20, 16 (2020). https://doi.org/10.1186/s12911-020-1023-5**

Key Findings:
- Applied several ML classifiers (Random Forest, Gradient Boosting, SVM, etc.) to predict survival
- Discovered that **serum creatinine** and **ejection fraction** alone achieve strong predictive performance
- Random Forest achieved the best results with Matthews Correlation Coefficient (MCC) of 0.418
- Feature ranking analysis revealed time, serum creatinine, and ejection fraction as top predictors
- Demonstrated that complex models with all 13 features do not significantly outperform simpler 2-feature models

Clinical Relevance:
- Serum creatinine indicates kidney function, often impaired in heart failure patients
- Ejection fraction measures heart pumping efficiency, a direct indicator of cardiac health
- These two biomarkers are routinely measured and can guide clinical decision-making

## Resources

### Project

- [Project Website](https://michigandatascienceteam.github.io/W26-MDST-Project_Heart-Failure-Survival-Analysis/)
- [UCI Dataset](https://archive.ics.uci.edu/ml/datasets/Heart+failure+clinical+records)

### Setup Tutorials (Jupyter Notebooks)

- [Git Tutorial](tutorials/git_tutorial.ipynb) - Installation, setup, commands, workflows, branching
- [Virtual Environment Tutorial](tutorials/venv_tutorial.ipynb) - Python venv, package management, troubleshooting

### Libraries & Tools

- [Scikit-learn](https://scikit-learn.org/stable/) - Machine learning
- [Pandas](https://pandas.pydata.org/docs/) - Data manipulation
- [Seaborn](https://seaborn.pydata.org/) - Data visualization
- [LightGBM](https://lightgbm.readthedocs.io/) - Gradient boosting
- [Optuna](https://optuna.readthedocs.io/) - Hyperparameter optimization

## Acknowledgements

Sina Bonakdar, Terry Zhang

## License

This project is licensed under the MIT License - see the [LICENSE](LICENSE) file for details.
