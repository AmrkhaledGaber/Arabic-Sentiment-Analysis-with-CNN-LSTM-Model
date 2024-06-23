 Arabic Sentiment Analysis with CNN-LSTM Model

This project explores the application of a combined Convolutional Neural Network (CNN) and Long Short-Term Memory (LSTM) model for Arabic sentiment analysis. The model aims to classify Arabic text (primarily tweets) into positive or negative sentiments, addressing the unique challenges posed by the Arabic language's rich morphology and the scarcity of accurate preprocessing tools.

# Key Features

*   **Combined CNN-LSTM Architecture:** Leverages the strengths of both CNNs for feature extraction and LSTMs for capturing sequential dependencies in text.
*   **Multiple Sentiment Analysis Levels:** Explores character-level, 5-gram character-level, and word-level analysis to account for the diverse forms of Arabic words.
*   **Diverse Datasets:** Evaluated on multiple datasets, including the Arabic Health Services (AHS) dataset, Ar-Twitter dataset, and the Arabic Sentiment Tweets Dataset (ASTD).

### Methodology

1.  Data Preprocessing:
    *   Normalization of Arabic text (removing diacritics, punctuation, etc.).
    *   Tokenization at character, 5-gram character, and word levels.
    *   Padding sequences to a fixed length.

2.  Model Architecture:
    *   Input Layers Separate input layers for each sentiment analysis level.
    *   Embedding Layers : Word embeddings to represent tokens as dense vectors.
    *   Convolutional Layers: Apply filters of varying sizes to extract features.
    *   Max-Pooling Layers: Downsample feature maps to capture most salient features.
    *   LSTM Layers:** Process sequences of features, considering long-term dependencies.
    *   Fully Connected Layer: Combine LSTM outputs and apply activation function.
    *   Output Layer: Sigmoid activation for binary classification (positive/negative).

3.  Training and Evaluation:
    *   Trained on 80% of each dataset, validated on 20%.
    *   Evaluated using accuracy as the primary metric.

 Results

| Dataset      | Char-Level Accuracy | 5-gram Level Accuracy | Word-Level Accuracy |
| :----------- | :------------------ | :-------------------- | :------------------ |
| Main-AHS     | 0.8941              | 0.9163               | **0.9424**          |
| Sub-AHS      | 0.9164              | **0.9568**            | 0.9510              |
| Ar-Twitter   | 0.8131              | 0.8283               | **0.8810**          |
| ASTD         | 0.7419              | 0.7762               | 0.7641              |

# Conclusion

The combined CNN-LSTM model demonstrates promising results for Arabic sentiment analysis, particularly when using word-level and 5-gram character-level representations. The model's performance highlights the potential of deep learning techniques in addressing the complexities of Arabic sentiment classification.

# Future Work

*   Incorporate pre-trained word embeddings (e.g., Word2Vec, GloVe, FastText) to potentially improve performance.
*   Explore other model architectures and hyperparameter tuning.
*   Apply the model to other Arabic NLP tasks.
