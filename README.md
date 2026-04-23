# LSTM-IMDB-
Used LSTM to classify between movies with their reviews and predicted if they have a positive feedback or not
# 🎬 IMDB Sentiment Analysis using LSTM (Deep Learning)

 Overview

This project performs **sentiment analysis** on movie reviews from the IMDB dataset using a **Bidirectional LSTM neural network**.

The goal is to classify reviews as:

* **Positive (1)**
* **Negative (0)**

This is a classic **Natural Language Processing (NLP)** problem where text data is converted into numerical form and processed using deep learning.

---

 Dataset

* Dataset: **IMDB Movie Reviews**
* Total samples: **50,000**

  * Training: 25,000
  * Testing: 25,000
* Balanced dataset:

  * 50% Positive
  * 50% Negative
* Source: Built-in dataset from Keras (`keras.datasets.imdb`)

---

 Data Preprocessing

* Limited vocabulary to top **5000 most frequent words**
* Converted text into integer sequences
* Applied **padding** to make all reviews equal length:

  * `maxlen = 250`
  * Short reviews → padded with zeros
  * Long reviews → truncated

---

 Model Architecture

```
Input (250 words)
↓
Embedding Layer (5000 → 64)
↓
Bidirectional LSTM (64 units)
↓
Dense Layer (32, ReLU)
↓
Dropout (0.3)
↓
Output Layer (Sigmoid)
```

---

 Key Concepts Used

* Word Embeddings
* Sequence Padding
* Recurrent Neural Networks (RNN)
* **LSTM (Long Short-Term Memory)**
* Bidirectional LSTM
* Binary Classification
* Overfitting Control (Dropout)

---

 Training Details

* Optimizer: **Adam**
* Loss Function: **Binary Crossentropy**
* Metrics: **Accuracy**
* Epochs: **10**
* Batch size: **64**

---

Results

* Achieved **~80% – 88% accuracy** on test data
* Significant improvement over basic RNN (~50%)

---

 Model Performance

* Training vs Validation Accuracy plotted
* Training vs Validation Loss plotted

---
 Prediction

The model can predict sentiment of unseen reviews:

* Output > 0.5 → Positive
* Output ≤ 0.5 → Negative



 Technologies Used

* Python
* TensorFlow / Keras
* NumPy
* Matplotlib

---
 Why LSTM?

Traditional RNNs struggle with long-term dependencies due to the **vanishing gradient problem**.

LSTM solves this using:

* Forget Gate
* Input Gate
* Output Gate

This allows the model to **retain important information over long sequences**, making it ideal for text data.

---

 How to Run

```bash
# Install dependencies
pip install tensorflow numpy pandas matplotlib

# Run the script
python imdb_lstm.py
```

---

 Future Improvements

* Use **GRU** instead of LSTM
* Add **pretrained embeddings (GloVe, Word2Vec)**
* Hyperparameter tuning
* Deploy as a web app

---

## 👨‍💻 Author

Syed Aoun Haider

---

##  If you found this useful

Give this repo a star  and share it!
