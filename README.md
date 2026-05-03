# Empathy-bot
Elevanceskills internship project
#  Sentiment-Aware Empathetic Chatbot (SARS)

[![Python](https://img.shields.io/badge/Python-3.9%2B-blue)](https://www.python.org/)
[![Streamlit](https://img.shields.io/badge/Frontend-Streamlit-FF4B4B)](https://streamlit.io/)
[![HuggingFace](https://img.shields.io/badge/Model-RoBERTa--GoEmotions-orange)](https://huggingface.co/SamLowe/roberta-base-go_emotions)

##  Problem Statement
Standard automated customer service agents often lack the "emotional intelligence" required to handle complex human interactions. This leads to robotic exchanges that can escalate customer frustration, especially during service failures. 

**Objective:** Integrate advanced sentiment analysis into the chatbot's core logic to detect and respond appropriately to user emotions, recognizing nuanced states across positive, negative, and neutral spectrums.

---

##  Methodology & Architecture
The system utilizes a **Perception-to-Action** pipeline to ensure "human-like" responses[cite: 1]:

1.  **Semantic Encoding:** User input is processed via a Transformer-based encoder[cite: 1].
2.  **Emotional Feature Extraction:** Utilizing the `RoBERTa-base-go_emotions` model to identify 28 distinct emotional labels[cite: 1].
3.  **Intensity Thresholding:** A confidence threshold of **0.80** is applied to trigger high-empathy response modifiers[cite: 1].
4.  **Dynamic Response Generation:** The bot's persona adapts by selecting from "Validation Hooks" (for negative input) or "Mirroring Hooks" (for positive input)[cite: 1].

---

##  Performance Metrics
The system is evaluated based on its ability to behave like a "normal person" while maintaining technical accuracy[cite: 1]:

| Metric | Target Value | Evaluation Method |
| :--- | :--- | :--- |
| **Model Precision** | **87.4%** | F1-Macro Score against GoEmotions dataset[cite: 1] |
| **Inference Latency** | **~120ms** | Average real-time processing speed per string[cite: 1] |
| **Sentiment Recovery** | **92%** | Successful transition from Negative to Neutral/Positive user state[cite: 1] |
| **False Positive Rate** | **< 5%** | Frequency of inappropriate "Toxic Positivity"[cite: 1] |

---

##  System Requirements
To run this project, the following dependencies are required[cite: 1]:

* `streamlit>=1.30.0` (Frontend and Chat Interface)
* `transformers>=4.35.0` (Deep Learning Inference)
* `torch>=2.1.0` (Neural Network Backend)
* `pandas>=2.0.0` (Data Logging and Analytics)
* `cloudflared` (High-speed secure tunneling for remote access)

---

##  Installation & Usage

### 1. Clone the Repository
```bash
git clone [https://github.com/deva424/empathy-bot.git](https://github.com/your-username/empathy-bot.git)
cd empathy-bot
