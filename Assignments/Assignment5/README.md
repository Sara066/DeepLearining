# RNN vs LSTM vs GRU for Sequence Classification

## 📌 Overview

This project implements and compares three types of Recurrent Neural Network architectures — **Simple RNN, Long Short-Term Memory (LSTM), and Gated Recurrent Unit (GRU)** — for sequence classification tasks.

The objective is to understand how different recurrent architectures learn temporal dependencies in sequential data and evaluate their performance using appropriate classification metrics.

All three models are trained and evaluated on the same dataset with consistent preprocessing and experimental conditions to ensure a fair comparison.

## 🎯 Objectives

- Understand the working principles of RNN, LSTM, and GRU architectures.
- Implement all three models for sequence classification.
- Learn how recurrent networks process sequential data.
- Compare the ability of different architectures to capture short-term and long-term dependencies.
- Evaluate model performance using multiple classification metrics.
- Analyze the trade-offs between model accuracy, computational efficiency, and complexity.

## 🧠 Models Implemented

### 1. Simple RNN

A Recurrent Neural Network processes sequential information by maintaining a hidden state that carries information from previous time steps.

**Characteristics:**
- Maintains a hidden state to remember previous inputs.
- Suitable for learning short-term dependencies.
- Suffers from the vanishing gradient problem when learning long sequences.
- Has a relatively simple architecture and fewer parameters.

### 2. Long Short-Term Memory (LSTM)

LSTM is an advanced form of RNN designed to overcome the vanishing gradient problem and capture long-term dependencies.

It uses three gates:

- **Forget Gate:** Determines what information should be discarded.
- **Input Gate:** Determines what new information should be stored.
- **Output Gate:** Determines what information should be passed to the next time step.

**Characteristics:**
- Better at learning long-term dependencies.
- Uses a cell state to preserve information.
- Handles longer sequences more effectively.
- Has more parameters and computational overhead than a simple RNN.

### 3. Gated Recurrent Unit (GRU)

GRU is a simplified version of LSTM that combines certain gating mechanisms to reduce architectural complexity.

It uses two gates:

- **Update Gate:** Controls how much previous information should be retained.
- **Reset Gate:** Controls how much past information should be forgotten.

**Characteristics:**
- Captures long-term dependencies.
- Has fewer parameters than LSTM.
- Generally requires less computational time.
- Offers a balance between performance and model complexity.

## ⚙️ Technologies Used

- **Programming Language:** Python
- **Deep Learning Framework:** TensorFlow / Keras
- **Numerical Computing:** NumPy
- **Data Processing:** Pandas
- **Data Visualization:** Matplotlib, Seaborn
- **Evaluation:** Scikit-learn

## 📂 Project Structure

```text
RNN-LSTM-GRU-Comparison/
│
├── dataset/
│   └── dataset.csv
│
├── notebooks/
│   └── sequence_classification.ipynb
│
├── models/
│   ├── rnn_model.keras
│   ├── lstm_model.keras
│   └── gru_model.keras
│
├── results/
│   ├── model_comparison.png
│   ├── confusion_matrices.png
│   └── training_history.png
│
├── README.md
└── requirements.txt
```

## 🔄 Implementation Workflow

1. **Dataset Loading:** Load the sequential dataset and examine its structure.
2. **Data Preprocessing:** Clean the data, encode labels, and convert sequences into a suitable numerical representation.
3. **Train-Test Split:** Divide the dataset into training and testing sets.
4. **Model Building:** Implement Simple RNN, LSTM, and GRU architectures.
5. **Model Training:** Train all three models using consistent experimental settings.
6. **Model Evaluation:** Evaluate the trained models on the test dataset.
7. **Performance Comparison:** Compare the models using evaluation metrics and visualizations.

## 📊 Evaluation Metrics

The following metrics are used to evaluate and compare the models:

| Metric | Description |
|---|---|
| Accuracy | Percentage of correctly classified samples. |
| Precision | Measures how many predicted positive samples are actually positive. |
| Recall | Measures how many actual positive samples are correctly identified. |
| F1-Score | Harmonic mean of precision and recall. |
| Confusion Matrix | Shows correct and incorrect classification predictions. |
| Training Time | Measures the time required to train each model. |

### Mathematical Formulas

**Accuracy:**

Accuracy = (TP + TN) / (TP + TN + FP + FN)

**Precision:**

Precision = TP / (TP + FP)

**Recall:**

Recall = TP / (TP + FN)

**F1-Score:**

F1 = 2 × (Precision × Recall) / (Precision + Recall)

Where:
- TP = True Positives
- TN = True Negatives
- FP = False Positives
- FN = False Negatives

## 📈 Model Comparison

The models are compared based on their classification performance and computational efficiency.

| Parameter | Simple RNN | LSTM | GRU |
|---|---|---|---|
| Architecture | Basic recurrent units | Three gates | Two gates |
| Long-term dependency learning | Limited | Excellent | Very Good |
| Vanishing gradient problem | More susceptible | Reduced | Reduced |
| Number of parameters | Lowest | Highest | Generally lower than LSTM |
| Training complexity | Low | High | Moderate |
| Computational efficiency | High | Lower | Generally better than LSTM |

*Note: These are general architectural characteristics. Actual performance depends on the dataset, sequence length, hyperparameters, and implementation.*

## 🚀 Installation and Execution

### 1. Clone the Repository

```bash
git clone https://github.com/your-username/RNN-LSTM-GRU-Comparison.git

cd RNN-LSTM-GRU-Comparison
```

### 2. Create a Virtual Environment (Optional)

```bash
python -m venv venv
```

Activate the environment:

**Windows:**
```bash
venv\Scripts\activate
```

**Linux / macOS:**
```bash
source venv/bin/activate
```

### 3. Install Dependencies

```bash
pip install -r requirements.txt
```

### 4. Run the Project

Open the Jupyter Notebook:

```bash
jupyter notebook
```

Run `sequence_classification.ipynb` to execute the complete implementation, train the models, and compare their performance.

## 📦 Requirements

The project requires the following Python libraries:

```text
numpy
pandas
matplotlib
seaborn
tensorflow
scikit-learn
jupyter
```

Install all dependencies using:

```bash
pip install -r requirements.txt
```

## 📌 Expected Outcomes

After completing the project, the following observations can be made:

- Simple RNN provides a basic understanding of recurrent learning but may struggle with long-term dependencies.
- LSTM can preserve information over longer sequences through its gating mechanisms.
- GRU provides a computationally efficient alternative to LSTM while maintaining strong sequence-learning capabilities.
- Comparing accuracy, precision, recall, F1-score, and training time helps identify the most suitable architecture for a given sequence classification task.

## 🔮 Conclusion

This project demonstrates the implementation and comparative analysis of three important recurrent neural network architectures: RNN, LSTM, and GRU.

By evaluating their classification performance and computational requirements under consistent experimental conditions, the project highlights the strengths and limitations of each architecture.

The comparison helps understand why gated architectures such as LSTM and GRU are often preferred over traditional RNNs for tasks involving complex sequential dependencies.

---

**Project Type:** Deep Learning | Sequence Classification  
**Models:** RNN, LSTM, GRU  
**Framework:** TensorFlow / Keras
