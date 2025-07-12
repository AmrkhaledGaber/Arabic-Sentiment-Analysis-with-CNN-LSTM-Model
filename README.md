# Arabic Sentiment Analysis with CNN-LSTM Model

This project explores the use of a combined **Convolutional Neural Network (CNN)** and **Long Short-Term Memory (LSTM)** model for **Arabic sentiment analysis**, specifically focusing on classifying Arabic text (such as tweets) into positive or negative sentiments. The model addresses the challenges posed by the Arabic language's rich morphology and the lack of accurate preprocessing tools.

## Key Features

* **Combined CNN-LSTM Architecture**: Utilizes CNNs for feature extraction and LSTMs for capturing sequential dependencies in the text.
* **Multiple Sentiment Analysis Levels**: Includes character-level, 5-gram character-level, and word-level analysis to handle the diverse forms of Arabic words.
* **Diverse Datasets**: Evaluated on various datasets, including the **Arabic Health Services (AHS)**, **Ar-Twitter**, and **Arabic Sentiment Tweets Dataset (ASTD)**.

## Methodology

### Data Preprocessing:

* **Normalization**: Arabic text is normalized by removing diacritics, punctuation, etc.
* **Tokenization**: Text is tokenized at the character, 5-gram character, and word levels.
* **Padding**: Sequences are padded to a fixed length for model input.

### Model Architecture:

1. **Input Layers**: Separate input layers for each sentiment analysis level.
2. **Embedding Layers**: Word embeddings to represent tokens as dense vectors.
3. **Convolutional Layers**: Filters are applied to extract features from text.
4. **Max-Pooling Layers**: Downsample feature maps to capture key features.
5. **LSTM Layers**: Process sequences of features, accounting for long-term dependencies.
6. **Fully Connected Layer**: Combines LSTM outputs and applies activation.
7. **Output Layer**: Sigmoid activation for binary classification (positive/negative).

### Training and Evaluation:

* **Training**: Trained on 80% of each dataset, validated on 20%.
* **Evaluation Metric**: Accuracy is used as the primary evaluation metric.

## Results

| Dataset        | Char-Level Accuracy | 5-gram Level Accuracy | Word-Level Accuracy |
| -------------- | ------------------- | --------------------- | ------------------- |
| **Main-AHS**   | 0.8941              | 0.9163                | 0.9424              |
| **Sub-AHS**    | 0.9164              | 0.9568                | 0.9510              |
| **Ar-Twitter** | 0.8131              | 0.8283                | 0.8810              |
| **ASTD**       | 0.7419              | 0.7762                | 0.7641              |

## Conclusion

The combined **CNN-LSTM model** demonstrates strong performance for Arabic sentiment analysis, especially at the word-level and 5-gram character-level. The model’s success indicates that deep learning can be a powerful tool for handling the complexities of Arabic sentiment classification.

## Future Work

* Incorporate pre-trained **word embeddings** like **Word2Vec**, **GloVe**, or **FastText** to enhance performance.
* Explore other model architectures and **hyperparameter tuning** for further optimization.
* Apply the model to other **Arabic NLP tasks** to broaden its applicability.

This project illustrates how combining **CNN** and **LSTM** architectures can effectively tackle sentiment analysis in Arabic, showing promising results and a potential path for future improvements.
