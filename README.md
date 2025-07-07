# phishing-detection-with-ai  
Detecting phishing emails using classical ML and hybrid deep learning models on preprocessed text data.

# 🎯 Phishing Detection with AI: ML and Deep Learning Hybrid System

## 📌 Project Overview  
Phishing emails continue to pose serious threats to digital security. This project uses text-based phishing detection via machine learning and deep learning models. By applying NLP techniques like TF-IDF vectorization and regex-based cleaning, we train and evaluate models on real phishing datasets — demonstrating robust classification performance across multiple architectures.

The pipeline includes both traditional models (SVM, Random Forest, etc.) and deep learning models (CNN, RNN, CNN-LSTM, etc.), trained on merged and cleaned phishing datasets.

---

## 📂 Dataset & Source

- **Datasets**:
  - `a.csv` - [Traditional phishing dataset](https://www.kaggle.com/datasets/subhajournal/phishingemails)
  - `b.csv` - [CEAS phishing challenge data](https://www.kaggle.com/datasets/naserabdullahalam/phishing-email-dataset/data?select=phishing_email.csv)
  - `CEAS_08.csv` - [Evaluation dataset](https://www.kaggle.com/datasets/naserabdullahalam/phishing-email-dataset/data?select=CEAS_08.csv)
- **Combined Format** (merged manually):
Text,label
"Your account has been suspended, click here to recover",1
"Here is your monthly newsletter",0


---

## 🔍 Insights & Findings

- 🔤 Text preprocessing via regex, stemming, and TF-IDF gives a strong representation of phishing content.
- 📊 ANN outperformed all models with highest classification accuracy.
- 🧠 Deep learning models trained on reshaped TF-IDF arrays improved precision/recall significantly over traditional models.

| Model                  | Accuracy (Est.) |
|------------------------|-----------------|
| Logistic Regression    | ~81%            |
| SVM                    | ~81%            |
| Random Forest          | ~84%            |
| CNN                    | ~99.11%         |
| ANN                    | ~99.27%         |

---

## 🤖 AI Pipeline Summary

| Task                   | Input                            | Output                           |
|------------------------|----------------------------------|----------------------------------|
| Preprocessing          | Raw email text                   | Cleaned tokens (lowercase, regex)|
| Vectorization          | Cleaned text                     | TF-IDF matrix (max 6000 features)|
| Classification         | TF-IDF vector                    | Class: phishing / legitimate     |
| Evaluation             | Predictions vs actual labels     | Metrics, confusion matrix        |

---

## 📈 Visualizations (Notebook Output)

- Confusion matrices per model
- Heatmaps of classification accuracy
- Training vs validation loss/accuracy curves
- Side-by-side model performance summaries

---

## 🛠️ Model Architectures Used

- **Classical Models**:
- Support Vector Machine (SVC)
- Logistic Regression
- Random Forest Classifier
- K-Nearest Neighbors

- **Deep Learning Models**:
- ANN
- RNN
- CNN
- CNN-LSTM

All trained using:
- `binary_crossentropy` loss
- `Adam` optimizer
- Early stopping (patience=5)
- Batch size: 64, Epochs: 50

---

## 📁 Project Structure
```
phishing-detection-with-ai/
├──Text-classification-phishing-detection-with-AI.ipynb.ipynb
├──README.md
├──LICENSE
└──results/
```
---

## 🔮 Future Enhancements

- Upgrade from TF-IDF to transformer-based encoders (ALBERT)

---

## 🛡️ License

This project is licensed under the [MIT License](./LICENSE).

---

## 👤 Author

**Johristein**  
GitHub: Johristein

---

> 📦 This project demonstrates how hybrid AI systems can be applied to detect phishing content using structured text classification — suitable for research, education, and deployment in security systems.
