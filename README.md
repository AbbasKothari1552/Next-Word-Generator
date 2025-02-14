

# Next Character & Next Word Prediction using LSTM in PyTorch

## 🚀 **Overview**  
This repository contains an implementation of **Next Character Generation** and **Next Word Generation** using **LSTM (Long Short-Term Memory) networks** in **PyTorch**. The model is trained on a given text file to predict the next character or word based on previous sequences.  

---

## 🛠 **Project Structure**  
| File | Description |  
|------|------------|  
| **`LSTM_word_generator.ipynb`** | Implements next word prediction using LSTM. |  
| **`LSTM_next_character_generator.ipynb`** | Implements next character prediction using LSTM. |  
| **`processed_data.zip`** | Preprocessed dataset stored as input-target sequences for character prediction. |  
| **`Alice’s Adventures in Wonderland.txt`** | The text file used for training the model. |  

---

## 🧠 **About LSTM & PyTorch**  
### 🔹 **LSTM (Long Short-Term Memory)**  
LSTM is a type of **Recurrent Neural Network (RNN)** that can capture long-term dependencies in sequential data. Unlike traditional RNNs, LSTMs solve the **vanishing gradient problem** and perform well for text-based tasks like **language modeling, text generation, and sequence prediction**.  

### 🔹 **Why PyTorch?**  
- PyTorch provides **dynamic computation graphs**, making it more flexible for deep learning experiments.  
- It has **built-in support** for GPU acceleration.  
- The **`torch.nn.LSTM`** module simplifies LSTM implementation in just a few lines of code.  

---

## 📌 **How to Run**  
### **1️⃣ Install Dependencies**  
Ensure you have **PyTorch** installed. If not, install it using:  
```bash
pip install torch numpy
```

### **2️⃣ Train the Model**  
Run either of the scripts:  
```bash
python LSTM_word_generator.ipynb
```
or  
```bash
python LSTM_next_character_generator.ipynb
```

### **3️⃣ Load Preprocessed Data**  
The dataset has already been processed and saved in **`processed_data.pkl`**. You can load it directly to save preprocessing time:  
```python
import pickle
with open("processed_data.pkl", "rb") as f:
    X, y, char_to_idx, idx_to_char = pickle.load(f)
```

---

## 📄 **Dataset**  
The model is trained on **`Alice’s Adventures in Wonderland.txt`**, which contains the text used for learning character/word sequences. You can replace this file with any other text of your choice to train a different model.

---

## 🎯 **Future Improvements**  
- Experiment with **different LSTM architectures** (stacked LSTMs, bidirectional LSTMs).  
- Implement **GRU (Gated Recurrent Unit)** for comparison.  
- Fine-tune hyperparameters for better accuracy.  

---

## 🤝 **Contributing**  
Feel free to **fork** this repository, improve the model, and submit a **pull request**.  

---

