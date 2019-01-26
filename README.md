# Fashion-Mnist
# Context

Fashion-MNIST is a dataset of Zalando's article images—consisting of a training set of 60,000 examples and a test set of 10,000 examples. Each example is a 28x28 grayscale image, associated with a label from 10 classes. Zalando intends Fashion-MNIST to serve as a direct drop-in replacement for the original MNIST dataset for benchmarking machine learning algorithms. It shares the same image size and structure of training and testing splits.

The original MNIST dataset contains a lot of handwritten digits. Members of the AI/ML/Data Science community love this dataset and use it as a benchmark to validate their algorithms. In fact, MNIST is often the first dataset researchers try. "If it doesn't work on MNIST, it won't work at all", they said. "Well, if it does work on MNIST, it may still fail on others."

Zalando seeks to replace the original MNIST dataset

# Content

Each image is 28 pixels in height and 28 pixels in width, for a total of 784 pixels in total. Each pixel has a single pixel-value associated with it, indicating the lightness or darkness of that pixel, with higher numbers meaning darker. This pixel-value is an integer between 0 and 255. The training and test data sets have 785 columns. The first column consists of the class labels (see above), and represents the article of clothing. The rest of the columns contain the pixel-values of the associated image.

To locate a pixel on the image, suppose that we have decomposed x as x = i * 28 + j, where i and j are integers between 0 and 27. The pixel is located on row i and column j of a 28 x 28 matrix.
For example, pixel31 indicates the pixel that is in the fourth column from the left, and the second row from the top, as in the ascii-diagram below. 

# Labels

Each training and test example is assigned to one of the following labels:

0 T-shirt/top

1 Trouser

2 Pullover

3 Dress

4 Coat

5 Sandal

6 Shirt

7 Sneaker

8 Bag

9 Ankle boot 

TL;DR

Each row is a separate image
Column 1 is the class label.
Remaining columns are pixel numbers (784 total).
Each value is the darkness of the pixel (1 to 255)

# Download link for dataset
https://drive.google.com/open?id=1DlryirrEpJcuz2GPt3Jh2fl_Y5o8g4Zu

# Network Graph
![network](https://user-images.githubusercontent.com/26761067/33649439-fe79c44e-da83-11e7-894f-1c8531758b45.png)

# Visualization of Accuracies & Losses
![plots](https://user-images.githubusercontent.com/26761067/33649547-4df98e82-da84-11e7-9d81-35f1a0c4c84d.JPG)

# Using TensorBoard
You will need to use this `keras.callbacks.TensorBoard` if using keras

`tbcallback = keras.callbacks.TensorBoard(log_dir="./Graph", histogram_freq=0, write_graph=True, write_images=True)
history = model.fit(X_train, Y_train, batch_size=batch_size, epochs=epochs, verbose=1, validation_data=(X_val,Y_val), callbacks=[tbcallback])`

Call the callback in fit method

To open TensorBoard
**On Linux**

`$ tensorboard --logdir=<my_path>\Graph`

**On Windows** 

`tensorboard --logdir=foo:"<mp_path>\Graph"`

# Acknowledgements

Original dataset was downloaded from https://github.com/zalandoresearch/fashion-mnist

Dataset was converted to CSV with this script: https://pjreddie.com/projects/mnist-in-csv/
