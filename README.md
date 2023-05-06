# Plant Health LSTM Classifier

This repository contains an LSTM model for classifying the health of plants based on their time series data. The dataset consists of approximately 5,000 files each for healthy and diseased plants. Each file contains time series data with 9 features.

## Getting Started

These instructions will help you set up the project on your local machine for development and testing purposes.

### Prerequisites

To run this project, you will need Python 3.x and the following libraries installed:

- pandas
- numpy
- scikit-learn
- keras
- tensorflow

You can install the libraries using pip:

```bash
pip install pandas numpy scikit-learn keras tensorflow

Usage
Clone this repository to your local machine:
bash
Copy code
git clone https://github.com/your_username/plant-health-lstm-classifier.git
Change to the project directory:
bash
Copy code
cd plant-health-lstm-classifier
Run the main script:
bash
Copy code
python main.py
This will train the LSTM model and output the test accuracy and loss.

Model Architecture
The LSTM model consists of the following layers:

An LSTM layer with 50 units and 'return_sequences=True' to enable the following LSTM layer to receive sequences as input.
A Dropout layer with a rate of 0.2 to reduce overfitting by randomly setting input units to 0 during training.
Another LSTM layer with 50 units.
A Dropout layer with a rate of 0.2 to further reduce overfitting.
An output Dense layer with a single neuron and a sigmoid activation function for binary classification.
