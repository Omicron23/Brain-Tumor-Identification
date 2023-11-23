# Brain-Tumor-Identification

This project addresses a problem related to the detection of brain tumors using convolutional neural networks (CNNs). Here's a breakdown of the code and the problem it aims to solve:

>Data Preparation:
>>The code loads brain MRI images from the kaggle data repository.
>>It uses a LabelEncoder to convert categorical labels (folder names) into numerical values and then converts them into one-hot encoded format.
>>The image data is normalized by dividing pixel values by 255.
>>The dataset is split into training and testing sets.

>Data Augmentation:
>>The code uses the ImageDataGenerator from TensorFlow to perform data augmentation on the training set. This involves applying random transformations like >>rotation, zooming, and shifting to artificially increase the diversity of the training data.

>CNN Model Definition:
>>A convolutional neural network (CNN) model is defined using the TensorFlow Keras API.
>>The model consists of convolutional layers with max-pooling, followed by fully connected layers. It uses the ReLU activation function and includes dropout to prevent overfitting.
>>The output layer has softmax activation for multi-class classification.

>Model Compilation and Training:
>>The model is compiled using the Adam optimizer and categorical crossentropy loss.
>>The training is performed using the augmented data generated by the ImageDataGenerator.
>>Training history is stored for later visualization.

>Individual Predictions Visualization:
>>Random images from the test set are selected and their true and predicted labels are displayed along with the images. Correct predictions are highlighted in >>green, while incorrect predictions are highlighted in red.

>Training History Visualization:
>>The training history, including accuracy and loss over epochs, is visualized using Altair and Seaborn.

>Model Evaluation:
>>The trained model is evaluated on the validation set, and the validation accuracy is printed.

>In summary, this code is a pipeline for building, training, and evaluating a CNN for the classification of >>brain MRI images to detect brain tumors. The use of data augmentation helps improve the model's generalization >>by exposing it to a variety of image transformations during training. The visualizations provided help in >>understanding the model's performance and training progress.

>Shortcomings
>>The overall model accurracy is quite unstable: fixes will be made in future
>>Adding additional neural layers drastically reduces model accuracy
