MNIST Handwritten Digit Classification
Overview
This project demonstrates a basic deep learning workflow using TensorFlow and Keras to classify handwritten digits from the MNIST dataset. The model takes a grayscale image of a digit (0–9) and predicts which digit it represents.
Dataset
The notebook uses the built-in MNIST dataset provided by tf.keras.datasets.mnist.load_data().
- Training set: 60,000 images
- Test set: 10,000 images
- Image size: 28 × 28 pixels
- Image format: Grayscale
- Classes: Digits 0 through 9
The dataset is loaded automatically by TensorFlow the first time the notebook runs, so a separate download step is not required.
Model Architecture
The notebook defines a Sequential neural network with the following layers:
1. Flatten: Converts each 28 × 28 image into a one-dimensional vector of 784 values.
2. Dense (128 units, ReLU): Learns patterns useful for recognizing digits.
3. Dense (10 units, Softmax): Produces a score/probability distribution across the ten digit classes.
Training configuration
- Optimizer: Adam
- Loss function: Sparse categorical cross-entropy
- Metric: Accuracy
- Epochs: 3
Data Preprocessing
Pixel values are originally in the range 0–255. The notebook divides image values by 255 to normalize them to the range 0–1. It also displays an example image and prints the dataset shapes and labels for inspection.
Evaluation
After training, the model is evaluated on the MNIST test set. The notebook prints the test loss and test accuracy. The actual accuracy depends on the run and environment; run the notebook to obtain your result.
Requirements
- Python 3.9 or a compatible Python version supported by your TensorFlow installation
- TensorFlow
- Matplotlib
- Jupyter Notebook or JupyterLab
Installation
Install the required libraries:
pip install tensorflow matplotlib notebook
How to Run
1. Clone or download this repository.
2. Open a terminal in the project directory.
3. Install the dependencies listed above.
4. Launch Jupyter Notebook:
   jupyter notebook
5. Open DL_Assignment1.ipynb.
6. Run the notebook cells in order. The MNIST dataset will be loaded, preprocessed, and visualized; the neural network will then be trained and evaluated.
7. After successful execution, the trained model is saved as my_mnist_model.keras in the current working directory.
Saved Model
The notebook saves the trained Keras model as:
my_mnist_model.keras
This file can be loaded later with:
import tensorflow as tf

model = tf.keras.models.load_model("my_mnist_model.keras")
Project Structure
.
├── DL_Assignment1.ipynb
└── README.md
After running the notebook, my_mnist_model.keras will also be present in the working directory.
Notes
- The notebook currently trains for 3 epochs.
- No separate validation split is configured during training; the test set is used for evaluation after training.
- Test accuracy is not hard-coded in this README because it may vary between runs.
License
This project is provided for educational and academic use.
