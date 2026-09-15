3D CNN - Geometric Shape Classification

This project uses a 3D Convolutional Neural Network (3D CNN) to classify 3D geometric shapes represented as voxel grids.

About the Project

The input data consists of 20×20×20 binary voxel grids. The model learns the 3D spatial features from these voxels and predicts which geometric shape the input represents.

The dataset contains 7 classes:

* Sphere
* Cube
* Cone
* Cylinder
* Ellipsoid
* Cuboid
* Pyramid

Model

The model is built using TensorFlow/Keras and consists of 3D convolutional and max-pooling layers followed by fully connected layers.

20×20×20×1 Voxel Input
        ↓
3D Convolution
        ↓
Max Pooling
        ↓
3D Convolution
        ↓
Max Pooling
        ↓
Flatten
        ↓
Dense Layers
        ↓
7-Class Output

The final layer predicts the probability of each of the 7 classes.

Dataset

The voxel data is stored as .npy files. Each file contains a 20×20×20 voxel representation of a shape.

The training data contains the corresponding labels, while the test data is used to generate the final predictions.

Preprocessing

* Loaded voxel data using NumPy
* Reshaped the data to include the channel dimension
* Encoded the class labels
* Split the training data into training and validation sets

The input to the CNN has the shape:

(20, 20, 20, 1)

Training

The model was trained using the Adam optimizer with categorical classification loss. Accuracy was used as the main evaluation metric.

The main parameters that can be tuned include:

* Number of epochs
* Batch size
* Learning rate
* Number of filters
* Dropout
* Network depth

Prediction

After training, the model is used to classify the test voxel grids. The predictions are saved in predictions.csv in the required format:

id,label
test_001,sphere
test_002,cube
test_003,pyramid

Results

Validation Accuracy: XX.XX%

Kaggle Accuracy: XX.XX%

Tech Stack

* Python
* TensorFlow / Keras
* NumPy
* Pandas
* Scikit-learn
* Matplotlib
* Jupyter Notebook / Kaggle

Files

├── notebook.ipynb
├── predictions.csv
└── README.md

Author

Anirban
