# 🌿 Fine-Tuned E-commerce Chatbot for Ferns & Petals

## 🚀 Overview
This repository contains the fine-tuning process and implementation of an **e-commerce chatbot** specifically designed for **Ferns & Petals (FNP)**. The chatbot is trained using **Llama-2-7B** and optimized with **LoRA fine-tuning**, allowing it to provide **human-like, personalized, and proactive responses** to customer queries.

---

## 📌 Features
✅ **Pre-Trained LLM Fine-Tuning** – Optimized using **TinyPixel/Llama-2-7B-bf16-sharded**  
✅ **LoRA Optimization** – Enhancing adaptability while reducing training costs  
✅ **Custom Synthetic Dataset** – Created with ChatGPT, available on **Hugging Face**  
✅ **Realistic Customer Interactions** – Handling order tracking, recommendations, & support  
✅ **Efficient Training Pipeline** – Using **BitsAndBytes quantization**, AdamW optimizer, and BLEU scoring  
✅ **Personalization & Proactive Engagement** – Future-ready for advanced NLU enhancements  

---

## 📂 Dataset
The model was fine-tuned using a custom **synthetic dataset**:  
📌 **[deepsolv_ecommerce_chatbot](https://huggingface.co/datasets/monoid07/deepsolv_ecommerce_chatbot)**  
This dataset, generated with ChatGPT, includes **customer concerns** and corresponding **chatbot responses**, ensuring **realistic e-commerce conversations**.

---

## 🎯 Model Selection & Training
### 🔹 **Why Llama-2-7B?**
- **Powerful text generation** for high-quality responses
- **Efficient performance** with LoRA fine-tuning & quantization

### 🔹 **Fine-Tuning Setup**
- **Quantization:** `bnb_4bit_quant_type="nf4"`, `fp16 training`
- **LoRA Configuration:** `lora_alpha=16`, `rank=8`
- **Trainer:** `SFTTrainer` from Hugging Face `transformers`
- **Optimizer:** AdamW (`paged_adamw_32bit`)
- **Batch Size:** `1 sequence per device`, Gradient Accumulation: `4`
- **Learning Rate:** `2e-4`, **Max Steps:** `100`

---

## 📊 Evaluation Metrics
To ensure high-quality responses, the following metrics were used:
- **BLEU Score** – Evaluates text fluency & similarity
- **Perplexity (PPL)** – Measures model confidence & coherence
- **Loss Monitoring** – Tracks training efficiency with `PrintMetricsCallback`

---

## 🤖 Enhanced Chatbot Capabilities
### 🔹 **Post-Fine-Tuning Enhancements**
✅ **Improved Response Quality** – More natural & contextual answers  
✅ **Personalization** – Laying the foundation for personalized customer engagement  
✅ **Proactive Interactions** – Predictive conversations for abandoned carts  
✅ **Advanced NLU (Future Scope)** – Enhanced intent recognition & response generation  

---



### 📌 **Running the Chatbot**
```bash
python main.py
```



---

## 💡 Future Improvements
- **Fine-tuning with real customer interactions**
- **Improved personalization with user history tracking**
- **Multilingual support for global reach**
- **Integration with FNP’s existing chatbot systems**

---
