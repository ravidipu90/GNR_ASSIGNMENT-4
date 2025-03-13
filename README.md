# CNN Optimizer Comparison

This repository contains an implementation of a Convolutional Neural Network (CNN) for image classification. The model is trained on a dataset of images using different optimizers to analyze how they impact the training process. Loss curves are plotted to compare how quickly or slowly the models converge.

## Project Structure
```
├── data/                  # Dataset directory (not included in repo)
├── cnn_optimizer.py       # Main script for training CNN with different optimizers
├── README.md              # Project documentation
```

## Requirements
Make sure you have the following dependencies installed:

```bash
pip install tensorflow numpy matplotlib
```

## Dataset
The dataset should be organized inside the `data/` directory in the following format:
```
data/
├── class_1/
│   ├── image1.jpg
│   ├── image2.jpg
│   └── ...
├── class_2/
│   ├── image1.jpg
│   ├── image2.jpg
│   └── ...
└── ...
```

## Implementation Details
- A CNN model with three convolutional layers followed by a fully connected layer is implemented.
- The dataset is preprocessed using `ImageDataGenerator`, which includes data augmentation.
- Three optimizers are tested: **Adam**, **SGD (with momentum)**, and **RMSprop**.
- The model is trained for **40 epochs**, and training history is recorded.
- Loss curves are plotted to compare the optimization performance.

## Usage
To train the model and generate loss plots, run the script:

```bash
python cnn_optimizer.py
```

The training process will output loss curves comparing the optimizers.

## Results
The model is trained using three optimizers, and loss curves are plotted to visualize their convergence rates.

### Expected Outcome:
- **Adam**: Typically converges faster.
- **SGD**: Can be slower but generalizes well.
- **RMSprop**: Works well for non-stationary data.

A sample loss curve comparison:
![Loss Curves](loss_plot.png)

## License
This project is open-source and available for modification and distribution.
