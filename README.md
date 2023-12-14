# Image-Classification-with-K-Fold-Cross-Validation-and-Performance-Metrics

The dataset we used in this project has been collected from this link: 

https://www.kaggle.com/datasets/ritesh2000/car-brand-images-dataset

The dataset comprises images of three car types, organized into three subfolders: 'audi', 'lamborghini' and 'mercedes'. 
Through accurate image classification of each car, we aim to enhance our understanding of their visual characteristics and improve the ability to distinguish between them in future applications.

** Instruction **:

Each code file in this project is independent, meaning there are no dependencies among them. The writer used Jupyter Lab to run the codes. To get started, download both the image dataset and the code files. You can then run the code files individually to observe their performance.

The datasets used in this project were prepared on a MacBook. Because of this, .DS_Store files also occupy the image datasets. While these files don't impact the functionality of the code, they might cause errors during execution. We recommend removing these files before running the code to ensure a smooth execution process. You can do so by running a command like find . -name ".DS_Store" -delete in the dataset directory.

Usually, we train our model using a training dataset, fine-tune hyperparameters using a validation dataset, and evaluate the model’s performance on a testing dataset. However, as our dataset lacks the validation part, we performed hyperparameter tuning using the training dataset, which is not ideal. 

1.	** image_preprocessing.ipynb **:

This code file contains all the necessary code for pre-processing images in the datasets. Specialized pre-processing techniques are essential to normalize variability and enhance the quality of input data. By tailoring image pre-processing to our specific needs, we can achieve better results when utilizing them in our code files.

The pre-processing techniques applied to our images are detailed below:

• Image Resizing: Images need to be resized to a specific size so that the model finds them easier to work with. The images in our datasets were resized to 224*224 pixels.

• Data normalization: This is performed to prevent features with large scales from dominating the learning process, which can result in biased model performance. The normalization applied to our dataset is min-max scaling.

•	Feature extraction: Feature extraction divides and reduces the size of data sets, making them more manageable to work with. In this project, we employed the Histogram of Oriented Gradients (HoG) feature extraction method. 

•	Hyperparameter Tuning: To optimize the performance of each model, we have employed hyperparameter tuning using Grid Search.

2.	Classifiers:
   
We checked the accuracy and performance of five different machine-learning models for the classification of car images in the dataset. 

•	cars_cnn.ipynb: This code file uses Convolutional Neural Network model.

•	cars_fcnn.ipynb: This code file uses Fully Connected Neural Network model.

•	cars_knn.ipynb: This code file uses K-Nearest Neighbours model.

•	cars_logistic.ipynb: This code file uses Logistic Regression model.

•	cars_svm.ipynb: This code file uses Support Vector Machine model.

3.	Performance Metrics:
   
These are the metrics we used to check the performance of each model.

•	We used K-Fold Cross Validation with 10 Folds.

•	We used Cohen’s Kappa.

•	We used Confusion Matrix with Accuracy, Precision, Recall, F1 Score, Specificity, and Sensitivity.


