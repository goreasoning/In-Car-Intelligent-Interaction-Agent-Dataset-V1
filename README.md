# 🚗 Customer-Centric Interaction Agent-OS C0.1

*Comfort. Ease. Joy. Yours. *

## 🆕 Customer-Centric in C0.1

| Update                                                                                    | Description                                                                                                                                                                                                                          |
|-------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| 😊 **Customer Personlized Comfort**                                                       | An integrated agent system for **comforting customers**, delivering **200+** personalized comforts via **open-source** RL agents—**180x cheaper** than GPT-5.2-Pro.                                                                  |
| 🧩 **Customer Satisfaction Score**                                                        | A **customer-centric** score to measure **satisfaction** in comfort-focused customers, **prioritizing comfort** over **accuracy** performance.                                                                                       |
| 🧩 **Benchmarking in Comparison with Sotas**                                              | Comparison with Gemini-3-Pro-Preview, GPT-5.2, GPT-5.2-Chat, and GPT-5.2-Pro across both **5 scenarios** and **200+** personalized comforts metrics: accuracy, customer-centric satisfaction score, price/sample, and latency/sample. |
| 🧠 **Support For Customer-Centric Training, Test, and Embedding Dataset Auto-Annotation** | **Personalized dataset** auto-collection with high-quality annotations for 200+ customer needs. **customer-centric annotation** support —**$30/W-Samples**.                                                          |

## 📦 Overview

| Agent-OS **30+** interaction samples for 365 days** | (Intent)5-Scenarios | (Intent)Over 200+ Scenes | (Intent)Satisfaction-Score1 | Ratio Latency/Single-LLM-API-Call | Price $/M Tokens | 
|-----------------------------------------------------|---------------------|--------------------------|-----------------------------|-----------------------------------|------------------|
| **GPT-5.2-Varients**                                | 69.49(0%-100%)      | 56.28                    | 57.14                       | 1.00                              | 15.75            | 
| **GPT-5.2-Varients-Pro**                            | 69.09               | 55.31                    | 55.60                       | 1.00                              | 197              | 
| **GPT-5.2-Varients-Chat**                           | 65.30               | 53.48                    | 54.08                       | 1.00                              | 15.75            | 
| **Gemini-3-Pro-Preview**                            | 70.65               | 57.51                    | 58.41                       | 1.00                              | 14.00            |
| **(Open-Source-LLM) Based RL-Agent-C0.1**           | 93.10               | 84.72                    | 85.92                       | 1.10                              | 1.1              | 

## 🆕 (Intent)Satisfaction-Score1 Calculation
### Customer-Centric Satisfaction Score

A weighted scoring system designed to evaluate model performance with a stronger emphasis on real-world customer experience, granularity of correctness, and natural language usage.

### Formula

- **Accuracy**: Binary (1 if correct, 0 if incorrect) or proportional score for the specific test case.
- **Customer-Centric_Weight_1**: Reflects the difficulty and granularity of getting a scenario fully correct.
- **Customer-Centric_Weight_2**: Reflects the complexity of language style and context.

The final score is the average across all evaluated cases.

#### Customer-Centric_Weight_1 (Granularity of Correctness), alternative weights for Weight_1 is also suggested. 

| Condition                              | Weight | Description                              |
|----------------------------------------|--------|------------------------------------------|
| Only 1 of 5 scenarios correct          | 0.3    | Low granularity — broad scenario failure |
| Only 1 of 208 scenes correct           | 0.5    | Medium granularity                       |
| Only 1 of 1000 instances correct       | 0.9    | High granularity — near-perfect required |

#### Customer-Centric_Weight_2 (Language Style & Context Complexity), alternative weights for Weight_2 is also suggested.

| Condition                              | Weight | Description                                      |
|----------------------------------------|--------|--------------------------------------------------|
| Standard single sentence correct       | 0.3    | Simple, formal, single-sentence input            |
| Standard multiple context correct      | 0.5    | Formal language with multi-turn or context       |
| Colloquial single sentence correct     | 0.7    | Informal/natural language, single sentence       |
| Colloquial multiple context correct    | 0.9    | Informal/natural language with multi-turn context|

#### Combined Weights (Weight_1 × Weight_2)

| Granularity (Weight_1) | Language/Context (Weight_2)       | Combined Weight | Example Scenario                                      |
|------------------------|----------------------------------|-----------------|-------------------------------------------------------|
| 0.3 (5 scenarios)      | 0.3 (Standard single)            | 0.09            | Easiest case, broad failure tolerated                 |
| 0.3                    | 0.5 (Standard multiple)          | 0.15            |                                                       |
| 0.3                    | 0.7 (Colloquial single)          | 0.21            |                                                       |
| 0.3                    | 0.9 (Colloquial multiple)        | 0.27            | Hardest language, but low granularity requirement     |
| 0.5 (208 scenes)       | 0.3 (Standard single)            | 0.15            |                                                       |
| 0.5                    | 0.5 (Standard multiple)          | 0.25            |                                                       |
| 0.5                    | 0.7 (Colloquial single)          | 0.35            |                                                       |
| 0.5                    | 0.9 (Colloquial multiple)        | 0.45            |                                                       |
| 0.9 (1000 instances)   | 0.3 (Standard single)            | 0.27            |                                                       |
| 0.9                    | 0.5 (Standard multiple)          | 0.45            |                                                       |
| 0.9                    | 0.7 (Colloquial single)          | 0.63            |                                                       |
| 0.9                    | 0.9 (Colloquial multiple)        | **0.81**        | Highest reward: near-perfect on hard, natural cases   |

## Purpose

This scoring system prioritizes:
- Real customer-like (colloquial, multi-turn) interactions
- **Fine-grained correctness** over **coarse scenario passes**
- Higher rewards for excellence in challenging, realistic conditions

Use this metric when standard accuracy feels disconnected from perceived customer satisfaction.

## 📊 Customer-Centric DataSet Statistics

| Module              | Samples  | Avg. Turns | Labels     |
|---------------------|----------|------------|------------|
| Standard Samples    | 13.7 K + | 1          | 208 Scenes |
| Colloquial Sampless | 86.3 K + | 2–5        | 208 Scenes |


## 💡 Applications

- Comfort. Ease. Joy. Yours. Enjoy More Your Life


## 📅 Version History

| Version    | Key Features                                                                   | Release    |
|------------|--------------------------------------------------------------------------------|------------|
| **V1.0**   | DataSet-V1 and Non-Commercial API Release                                      | 2025 10 16 |
| **V1.1**   | Benchmark-V1.1, Joint and Personalization Release                              | 2025 10 20 |
| **V1.2**   | Benchmark-V1.2, Multi-Modal Voice and Emotion Text Language Generation Release | 2025 10 31 |
| **V1.2.1** | Benchmark-V1.2.1, 200M+ Token with high quailty dataset released               | 2025 11 04 |
| **V1.2.2** | Benchmark-V1.2.2, Agent-Multi-Modal-Interation-Demo-V0.3 Release               | 2025 11 07 |
| **C0.1**   | Customer-Centric Interaction Agent-OS in Scenarios and Test Dataset Release    | 2025 12 17 | 


---

## 🚀 Getting Started
- [✅] To apply for dataset downloads and customer-centric personlized dataset annotation and api, please email <a href="mailto:deepreasoninggo@gmail.com">deepreasoninggo@gmail.com</a> **and** <a href="https://drive.google.com/file/d/1F46UhKrqP9TvJAyMzmuk-xWwxcuWWSJj/view?usp=sharing" target="_blank" rel="noopener noreferrer">fill out this form</a>.  
- [✅] Sample Customer-Centric Dataset C0.1 in Comparison With GPT5.2 and Gemini-3-Pro-Preview is in Huggingface, Visit [dataset](https://huggingface.co/datasets/deepgo/Customer_Centric_Agent_Benchmark_C0.1)
## 📜 License

**License:** CC-BY 4.0  
Free for research and commercial use with proper attribution.

---

## 📚 Citation

```bibtex
@dataset{di2025_incar_interaction_agent_p0_1,
  author       = {Xinhan Di},
  title        = {Customer-Centric Agent-OS V0.1},
  year         = {2025},
  url          = {https://github.com/your-og/Personlized Interaction Agent-OS V0.1},
  note         = {Dataset, Version 0.1},
}
```

---

## 🤝 Acknowledgements

Special thanks to all annotators, engineers, and collaborators contributing to personlized interaction agent-os V0.1 application.

---

> © 2025 Deepgo. All rights reserved.
