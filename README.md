# Fashion-MNIST-Image-Classification

# Google Colab link: https://colab.research.google.com/drive/1dFLPDTZiVU6aapz2yIstk6_mVmlwKVWn?usp=sharing


#1. What is the Fashion MNIST dataset?
Is a collection of 70,000 small black&white pictures of everyday clothing, T-shirts, shoes, and bags. 
Out of these, 60,000 images are used to train a model, and 10,000 are used to test how well it learned. 
Each picture fits into one of 10 clothing categories.

#2. Why do we normalize image pixel values before training?
Image pixel values from 0–255 to 0–1 so the model can learn more easily. 
This helps training run faster, stay stable, and produce better accuracy by keeping the numbers simple and consistent.

#3. List the layers used in the neural network and their functions.
Flatten layer – Changes the 28×28 image into a simple list of numbers so the model can easily read and process it.
Dense layer (128 neurons, ReLU activation) – Helps the model learn and recognize important patterns and features in the images.
Dense layer (10 neurons) – Gives one output for each of the 10 clothing categories, which is later turned into probabilities using Softmax.

#4. What does an epoch mean in model training?
An epoch is one full pass of the training data through the model, allowing it to learn and update its weights to improve accuracy.

#5. Compare the predicted label and actual label for the first test image.
Predicted label:
From predictions[0], you get an array of probabilities for each class.
predicted_label = np.argmax(predictions[0]) → the index of the highest probability in that

Actual label:
From test_labels[0], you get the real class of the first test image.
Let’s call it true_label = test_labels[0].

#6. What could be done to improve the model’s accuracy?
Adding more layers allows the network to learn more complex patterns in the images.
Train for 20–30 epochs.
ubtract the mean and divide by standard deviation → makes training more stable.
Normalization & Batch Norm: Stabilize training.
Better activations: Improve learning efficiency.
