# Musk-Classification
Classifying the organic compounds into musk and non-musk category.


INTRODUCTION:
The given task is solved by using the Sequential Model(Deep Learning) in order to classify musk and non-musk compounds on the basis of features given in the dataset and accuracy of the developed model is calculated by splitting the data in the ratio of 80:20 of training and testing respectively.

MODEL USED:
The model used to complete the task is Sequential Model. The model comes under Keras framework. The Sequential Model is a Deep learning model which is linear stack of layers. The model treats each layer as an object that feeds into the next layer. It uses hidden layers to classify the different features. I have used ‘sigmoid’ as an activation function to bring the values from the previous layers in the range of 0 to 1 to classify the compounds on the basis of the given features.
You can create a Sequential Model by adding layer instances via .add() method:
model.add(tf.keras.layers.Dense(166,activation='sigmoid'))
model.add(tf.keras.layers.Dense(300, activation='sigmoid'))
The first parameter in the method is used to specify the density of the hidden layer i.e., the number of neurons in the layer.
 
PREPROCESSING:
Firstly, the unwanted data columns are removed from the data:
data.drop(["ID", "molecule_name,"conformation_name"],axis=1,inplace=True)
Secondly, the leftover data columns are stored in variable X except the ‘class’ column which is stored in variable Y:
X = data.drop(["class"],axis=1)
Y = data["class"]
Thirdly, the data is split in the ratio of 80:20 for training and testing respectively:
x_train,x_test,y_train,y_test = train_test_split(X , Y , test_size = 0.2)


FINAL PERFORMANCE MEASURES:

For epoch=8:
Accuracy=0.9773
Loss=0.0320
Precision=0.85034
Recall=0.5896
F1 Score=0.6964




