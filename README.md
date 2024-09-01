

# Sentiment Classification Using LSTM on Disaster Tweets Dataset

## Overview

This project involves sentiment classification using an LSTM (Long Short-Term Memory) neural network on the Disaster Tweets Dataset. The goal is to classify tweets into two categories: tweets that are about real disasters (disaster-related) and tweets that are not related to disasters (non-disaster-related). The project leverages the power of deep learning, specifically LSTM, to capture the context and semantics of the tweets for effective classification.

## Table of Contents

- [Overview](#overview)
- [Dataset](#dataset)
- [Project Structure](#project-structure)
- [Installation](#installation)
- [Data Preprocessing](#data-preprocessing)
- [Modeling](#modeling)
- [Evaluation](#evaluation)
- [Results](#results)
- [Contributing](#contributing)
- [License](#license)

## Dataset

The **Disaster Tweets Dataset** contains a collection of tweets labeled as disaster-related or non-disaster-related. This dataset is commonly used to train models to automatically identify tweets that discuss real disasters.

**Dataset Features:**
- **id:** Unique identifier for each tweet.
- **text:** The content of the tweet.
- **target:** Label indicating whether the tweet is about a real disaster (`1`) or not (`0`).

The dataset can be downloaded from [Kaggle](https://www.kaggle.com/c/nlp-getting-started/data).

## Project Structure

```bash
├── data
│   ├── train.csv                      # Training dataset
│   ├── test.csv                       # Testing dataset
├── notebooks
│   ├── Sentiment_Classification_LSTM.ipynb  # Jupyter notebook for model development
├── models
│   ├── lstm_disaster_model.h5         # Saved trained LSTM model
├── README.md                          # Project README file
└── requirements.txt                   # Python packages required
```

## Installation

To run this project locally, follow these steps:

1. Clone the repository:

   ```bash
   git clone https://github.com/yourusername/disaster-tweets-sentiment-lstm.git
   cd disaster-tweets-sentiment-lstm
   ```

2. Create and activate a virtual environment (optional but recommended):

   ```bash
   python -m venv venv
   source venv/bin/activate   # On Windows use `venv\Scripts\activate`
   ```

3. Install the required Python packages:

   ```bash
   pip install -r requirements.txt
   ```

4. Download the Disaster Tweets Dataset and place it in the `data/` directory if it's not already included.

## Data Preprocessing

Data preprocessing involves several steps to prepare the text data for model training:

- **Text Cleaning:** Removing URLs, special characters, numbers, and converting text to lowercase.
- **Tokenization:** Splitting the text into individual words (tokens).
- **Padding:** Ensuring all sequences have the same length by padding shorter sequences.
- **Word Embeddings:** Using pre-trained word embeddings (e.g., GloVe) to convert words into dense vectors.

## Modeling

The core of this project is the implementation of an LSTM model for sentiment classification:

1. **Embedding Layer:** Converts words into dense vectors using pre-trained embeddings.
2. **LSTM Layers:** Capture the sequential dependencies and context within the tweets.
3. **Fully Connected Layers:** After the LSTM layers, dense layers are used to make predictions.
4. **Output Layer:** A sigmoid activation function is used to output a probability score for the binary classification task.

The model is compiled with binary cross-entropy loss and optimized using the Adam optimizer.

## Evaluation

The model is evaluated using the following metrics:

- **Accuracy:** The percentage of correctly classified tweets.
- **Precision, Recall, F1-Score:** Metrics to measure the quality of the classification, especially in terms of handling imbalanced classes.
- **Confusion Matrix:** To visualize the performance of the classifier in distinguishing between disaster and non-disaster tweets.

## Results

- The LSTM model achieved an accuracy of **X%** on the test dataset.
- The model demonstrated strong performance, effectively identifying disaster-related tweets with a high precision and recall.

*Note: Replace **X%** with the actual accuracy obtained from your model.*

## Contributing

Contributions are welcome! If you find any issues or have suggestions for improvements, please feel free to create a pull request or open an issue.

## License

This project is licensed under the MIT License - see the [LICENSE](LICENSE) file for details.


