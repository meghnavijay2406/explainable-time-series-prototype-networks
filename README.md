📊 Prototype-Aligned Embedding for Time Series Forecasting
📌 Overview

This repository contains the implementation and research work for the Master’s Thesis:

“Prototype Aligned Embedding for Time Series Forecasting”

The thesis focuses on developing an interpretable deep learning framework for multivariate time-series forecasting by combining:

🧠 Prototype-based learning (ProSeNet)
📈 Time-series forecasting (LSTM-based models)
🗣️ Natural language explanations using LLMs
🔗 Multimodal learning (numerical + textual embeddings)

🚀 Motivation

Deep learning models for time-series forecasting often act as black boxes, limiting trust and adoption.

This work addresses that problem by:

Introducing prototype-based explainability
Generating human-readable explanations
Improving transparency without sacrificing accuracy
🧠 Key Contributions
✅ Extension of Prototype Similarity Network (ProSeNet) to time-series forecasting
✅ Integration of LLM-based textual explanations for interpretability
✅ Development of a multimodal framework combining:
Time-series embeddings
Textual embeddings
✅ Evaluation on real-world (ETT) and synthetic datasets
✅ Demonstration of accurate + interpretable forecasting

🏗️ Methodology
🔹 Model Architecture

The proposed framework consists of:

Encoder (BiLSTM)
Extracts temporal features from input sequences
Prototype Layer
Learns representative patterns (prototypes)
Explains predictions via similarity to prototypes
Forecasting Head
Predicts future time steps using prototype similarity
LLM-based Explanation Module
Generates natural language explanations from:
Predictions
Nearest prototype
Input sequence
Multimodal Extension
Combines:
Time-series embeddings
Text embeddings (Sentence Transformers)

📊 Datasets
1. Real Dataset
Electricity Transformer Temperature (ETT) dataset
Features:
HUFL, HULL, MUFL, MULL, LUFL, LULL
Target:
Oil Temperature (OT)
2. Synthetic Dataset
Generated using:
Sine, cosine, square, and composite signals
Designed to simulate:
Low vs High temperature patterns

⚙️ Training Details
Framework: PyTorch
Encoder: 3-layer BiLSTM
Optimizer: Adam / AdamW
Loss Functions:
Forecasting Loss (MSE)
Clustering Loss
Evidence Loss
Diversity Loss
Forecast Horizon:
12, 24, 48, 72 time steps

📈 Evaluation Metrics
Forecasting
MSE (Mean Squared Error)
MAE (Mean Absolute Error)
RMSE
R² Score
Classification
Accuracy
Precision / Recall / F1-score
Confusion Matrix
Explanation Quality
Readability
Fluency
Completeness
Length

🔍 Results
✔️ High forecasting accuracy across multiple horizons
✔️ Stable performance even for long-term predictions
✔️ Interpretable predictions via prototype similarity
✔️ Improved reasoning using multimodal (text + time-series) learning
💡 Example Insight

Instead of saying:

“Prediction = 75°C”

The model explains:

“This forecast is similar to Prototype X, which represents high load conditions with increasing temperature trends.”

🧰 Tech Stack
Python
PyTorch
NumPy / Pandas
Scikit-learn
tslearn (DTW clustering)
LangChain (RAG pipeline)
Sentence Transformers
LLM: SmolLM2-1.7B-Instruct

🔮 Future Work
Extend to other domains (healthcare, finance)
Improve prototype interpretability metrics
Explore larger LLMs for explanation quality
Real-time deployment of explainable forecasting systems

👩‍💻 Authors
Anila Shaji
Meghna Vijay

📜 License

This project is for academic and research purposes.

⭐ Acknowledgements

Special thanks to supervisors and faculty at Halmstad University for guidance and support.
