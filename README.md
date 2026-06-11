# Grape-Leaf-Disease-Classification-With-Image-Embeddings
![ alt text ](https://img.shields.io/badge/license-MIT-green?style=&logo=)
![ alt text ](https://img.shields.io/badge/-Jupyter-F37626?logo=Jupyter&logoColor=white)
![ alt text ](https://img.shields.io/badge/-Google_Colab-F9AB00?logo=googlecolab&logoColor=white)
![ alt text ](https://img.shields.io/badge/-NumPy-013243?logo=Numpy&logoColor=white)
![ alt text ](https://img.shields.io/badge/-TensorFlow-FF6F00?logo=TensorFlow&logoColor=white)
![ alt text ](https://img.shields.io/badge/-Keras-D00000?logo=Keras&logoColor=white)
![ alt text ](https://img.shields.io/badge/-scikit--learn-F7931E?logo=scikitlearn&logoColor=white)

Classification task using deep image embeddings extracted from pretrained CNNs. The following workflow to complete the task:

<p align='center'>
<img height="550" alt="obraz" src="https://github.com/user-attachments/assets/309e6401-ad13-405c-8c23-e0c0f31db29e" />
</p>

1. DenseNet121 Image Embeddings:

| Model               | Misclassified Images | Mean ROC-AUC | Mean F1 Score |
| ------------------- | -------------------: | -----------: | ------------: |
| SVC                 |             12       |       0.9997 |        0.9881 |
| Logistic Regression |             12       |       0.9995 |        0.9911 |
| Random Forest       |             20       |       0.9986 |        0.9791 |
| XGBoost             |             19       |       0.9990 |        0.9803 |

2. EfficientNetB0 Image Embeddings:

| Model                         | Misclassified Images | Mean ROC-AUC | Mean F1 Score |
|-------------------------------|---------------------:|-------------:|--------------:|
| k-NN                          |                   29 |       0.9908 |        0.9586 |
| Hist Gradient Boost           |                   17 |       0.9989 |        0.9717 |
| Multilayer Perceptron         |                    6 |       0.9996 |        0.9863 |
| Linear Discriminant Analysis  |                   10 |       0.9942 |        0.9752 |

An interesting insight is that the strong performances of LDA and logistic regression suggest that the extracted features are largely linearly separable, whereas the additional gains achieved by MLP and histogram-based gradient boosting indicate the presence of more complex non-linear patterns within the data. Consistent with this interpretation, the two-dimensional LDA projection shows substantial class separation in the reduced feature space.

<p align='center'>
<img height="400" alt="obraz" src="https://github.com/user-attachments/assets/6b9ee055-6c81-4ab4-80d1-910ce52073a7" />
</p>
