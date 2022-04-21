# Cell Neuclei Detection using Semantic Segmentation with U-Net

## 1. Summary of the project
The aim of this porject is to detect cell nuclei from biomedical images effectively. As cell nuclei vary in shapes and sizes, semantic segmentation proves to be the best approach to detect them.
A deep learning model is trained and deployed for this task. The model is trained with dataset from [2018 Data Science Bowl](https://www.kaggle.com/c/data-science-bowl-2018).

## 2. IDE and Framework
This project is created using Spyder as the main IDE. The main frameworks used in this project are:
- TensorFlow
- Numpy
- Matplotlib
- OpenCV
- Scikit-learn

## 3. Methodology

### _3.1 Data Pipeline_
The dataset files contains a train folder for training data and test folder for testng data, in th format of images for inputs and images masks for the labels.
The input images are preprocessed with feature scaling. The labels are preprocessed such that the values are in binary of 0 and 1. No data augmentation is applied for the dataset.
The train data is split into train-validation sets, with a ratio of 80:20.

### _3.2 Model Pipeline_
The model architecture used for this project is U-Net. You can refer to the TensoFlow documentation for further details. In summary, the model consist of two components, the downward stack, 
which serves as the feature extractor, and upward stack, which helps to produce pixel-wise output. The model structureis shown in the figure below.

![alt text](https://github.com/paan234/AI05-repo-4/blob/main/Image/Model.png )

The model is trained with a batch size of 16 and 100 epochs. Early stopping is also applied in the model training. The training stops at epoch 22, with a training accuracy of
97% and validation accuracy of 96%. The model training graphs are shown in figures below.

![alt text](https://github.com/paan234/AI05-repo-4/blob/main/Image/Loss_graph.png)

![alt text](https://github.com/paan234/AI05-repo-4/blob/main/Image/Accuracy_graph.png)

The graphs show a clear sign of model convergence at an excellent convergence point.

## 4. Results
The model is evaluated with the test data. The loss and accuracy are shown in figure below.

![alt text](https://github.com/paan234/AI05-repo-4/blob/main/Image/Test_result.png)

Some predictions are also been made with the model using some of the test data. The actual output masks and prediction masks are shown in figures below.

![alt text](https://github.com/paan234/AI05-repo-4/blob/main/Image/Prediction(1).png)
![alt text](https://github.com/paan234/AI05-repo-4/blob/main/Image/Prediction(2).png)
![alt text](https://github.com/paan234/AI05-repo-4/blob/main/Image/Prediction(3).png)
