# 🚗 Customer-Centric Interaction Agent-OS C0.2(Professonal and Focus on In-Car Smart Hardware Equipment)

*Comfort. Ease. Joy. Yours. Premium&Luxury (In-Car Hardware) Experience.*

## 🆕 Customer-Centric in C0.2 (Updated)

| Update                                              | Description                                                                                                                                                                                                                                                                                                                                                           |
|-----------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------| 
| 🧠 **Trained with Primary Level Business CoT Data** | Trained with primary level business CoT data, focus on enhancing the ability of **Empathy-to-Act** in **in-car-equips**, enabling more precise translation of emotional insights and unstated user needs into real-time hardware-level comfort actions.                                                                                                               |
| ❤️ **Empathy (In-Car-Equips) CoTs**                 | A dynamic **Primary Empathy-to-Act CoT Ability** focused on users’ **unstated expectations, hidden frustrations, and the emotional logic behind their behaviors** — with the ultimate goal of **building trust and enhancing the in-car experience**. Translating these insights **directly into hardware-level actions**, enabling real-time hardware-level actions. |
| 🧩 **Customer Satisfaction Score**                  | A **customer-centric score** to measure **satisfaction** in comfort-focused customers, **prioritizing comfort over accuracy** performance.                                                                                                                                                                                                                            |
| 🧩 **Benchmarking in Comparison with SOTAs**        | Comparison with Gemini-3-Pro, GPT-5.2, Grok4 across both **40 equips** and **2000+ actions personalized comfort metrics**: accuracy, customer-centric satisfaction score, price/sample, and latency/sample.                                                                                                                                  

## 📦 Overview

| Agent-OS **30+** interaction samples for 365 days** | (Intent)40-Equip | (Action)Over 2000+ action | (Action)Satisfaction-Score2 | Ratio Latency/Single-LLM-API-Call | Price $/M Tokens | 
|---------------------------------------------------|------------------|---------------------------|-----------------------------|-----------------------------------|------------------|
| **GPT-5.2-Varients**                              | 58.29(0%-100%)   | 54.72                     | 54.28                       | 1.00                              | 15.75            | 
| **Gemini-3-Pro**                                  | 58.73            | 55.47                     | 54.79                       | 1.00                              | 14.00            | 
| **Grok4**                                         | 59.14            | 56.19                     | 55.29                       | 1.00                              | 18.00            |
| **RL-Agent-C0.2**                                 | 91.06            | 85.16                     | 70.63                       | 1.10(350ms)                       | 1.1              | 

## 🆕 (Intent)Satisfaction-Score1 Calculation
### Customer-Centric Satisfaction Score

A weighted scoring system designed to evaluate model performance with a stronger emphasis on real-world customer experience and hardware-level empathy, granularity of correctness, and natural language usage.

### Formula

- **Accuracy**: Binary (1 if correct, 0 if incorrect) or proportional score for the specific test case.
- **Customer-Centric_Weight_1**: Reflects the complexity of hardware-level empathy.
- **Customer-Centric_Weight_2**: Reflects the difficulty and granularity of getting a scenario fully correct.
- **Customer-Centric_Weight_3**: Reflects the complexity of language style and context.

The final score is the average across all evaluated cases.

#### Customer-Centric_Weight_1 (Primary-Hardware-Level Empathy), alternative weights for Weight_1 is also suggested. 

| Condition                                                                                                                                                                | Weight | Description                                                                                                                 |
|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------|--------|-----------------------------------------------------------------------------------------------------------------------------|
| Limited Empathy: action triggered for direct control                                                                                                                     | 0.1    | Minimal or zero empathy realization                                                                                         |
| Single Empathy: Hardware-level action applied to only 1 primary in-car equip primary user's empathy                                                                      | 0.5    | Basic empathy realization — addresses one key emotional/physiological need via single equip                                 |
| Multiple Empathy: Hardware-level actions applied simultaneously to multiple in-car equipsfor primary user's empathy | 0.9    | Comprehensive empathy realization — coordinated multi-equip response creates primary-holistic, immersive comfort experience |

#### Customer-Centric_Weight_2 (Granularity of Correctness), alternative weights for Weight_2 is also suggested. 

| Condition                     | Weight | Description                              |
|-------------------------------|--------|------------------------------------------|
| Only 1 of 40 Equip correct    | 0.3    | Low granularity — broad intent failure   |
| Only 1 of 200 Action correct  | 0.5    | Medium granularity                       |
| Only 1 of 2000 Action correct | 0.9    | High granularity — near-perfect required |

#### Customer-Centric_Weight_3 (Language Style & Context Complexity), alternative weights for Weight_3 is also suggested.

| Condition                              | Weight | Description                                      |
|----------------------------------------|--------|--------------------------------------------------|
| Standard single sentence correct       | 0.3    | Simple, formal, single-sentence input            |
| Standard multiple context correct      | 0.5    | Formal language with multi-turn or context       |
| Colloquial single sentence correct     | 0.7    | Informal/natural language, single sentence       |
| Colloquial multiple context correct    | 0.9    | Informal/natural language with multi-turn context|

#### Combined Weights (Weight_1 × Weight_2 × Weight_3)

| Hardware-Level Empathy (Weight_1) | Correctness (Weight_2)              | Language/Context (Weight_3)              | Combined Weight | Example Scenario                                      |
|-----------------------------------|-------------------------------------|------------------------------------------|------------------|-------------------------------------------------------|
| 0.1 (Limited Empathy)             | 0.3 (Only 1 of 40 Equip correct)    | 0.3 (Standard single sentence)           | 0.009            | Easiest case, very minimal empathy tolerated          |
| 0.1                               | 0.3                                 | 0.9 (Colloquial multiple context)        | 0.027            | Hard language, but almost no empathy required         |
| 0.1                               | 0.9 (Only 1 of 2000 Action correct) | 0.9                                      | 0.081            | Near-perfect correctness + hard language, minimal empathy |
| 0.5 (Single Empathy)              | 0.3                                 | 0.3                                      | 0.045            |                                                       |
| 0.5                               | 0.5 (Only 1 of 200 Action correct)  | 0.5 (Standard multiple context)          | 0.125            |                                                       |
| 0.5                               | 0.5                                 | 0.9                                      | 0.225            |                                                       |
| 0.5                               | 0.9                                 | 0.3                                      | 0.135            |                                                       |
| 0.5                               | 0.9                                 | 0.9                                      | 0.405            | Good single-equip empathy + high correctness + natural language |
| 0.9 (Multiple Empathy)            | 0.3                                 | 0.3                                      | 0.081            |                                                       |
| 0.9                               | 0.5                                 | 0.5                                      | 0.225            |                                                       |
| 0.9                               | 0.7                                 | 0.7 (Colloquial single sentence)         | 0.441            |                                                       |
| 0.9                               | 0.9                                 | 0.9                                      | **0.729**        | Highest reward: comprehensive multi-equip empathy, near-perfect correctness, hardest natural multi-turn context |

This scoring system prioritizes:
- Real-Time Primary Hardware-level Empathy For Premium&Luxury (In-Car Hardware) Experience.
- Real customer-like (colloquial, multi-turn) interactions


Use this metric when standard accuracy feels disconnected from perceived customer satisfaction.

## 📊 Customer-Centric Training DataSet Statistics(C0.2)

| Module                   | Samples  | Avg. Turns | Labels        |
|--------------------------|----------|------------|---------------|
| Standard Samples         | 23.1 K + | 1-2        | 2000+ Actions |
| Primary-Empathy Sampless | 76.9 K + | 1-2        | 2000+ Actions |


## 💡 Applications

- Comfort. Ease. Joy. Yours. Enjoy More Your Life


## 📅 Version History

| Version    | Key Features                                                                         | Release    |
|------------|--------------------------------------------------------------------------------------|------------|
| **V1.0**   | DataSet-V1 and Non-Commercial API Release                                            | 2025 10 16 |
| **V1.1**   | Benchmark-V1.1, Joint and Personalization Release                                    | 2025 10 20 |
| **V1.2**   | Benchmark-V1.2, Multi-Modal Voice and Emotion Text Language Generation Release       | 2025 10 31 |
| **V1.2.1** | Benchmark-V1.2.1, 200M+ Token with high quailty dataset released                     | 2025 11 04 |
| **V1.2.2** | Benchmark-V1.2.2, Agent-Multi-Modal-Interation-Demo-V0.3 Release                     | 2025 11 07 |
| **C0.1**   | Customer-Centric Interaction Agent-OS in Scenarios and Test Dataset Release          | 2025 12 17 | 
| **C0.2**   | Customer-Centric Interaction Agent-OS (Primary-Empathy (In-Car Hardware) Experience) | 2026 02 15 | 

---

## 🚀 Getting Started
- [✅] To apply for dataset downloads and customer-centric personlized dataset annotation and api, please email <a href="mailto:deepreasoninggo@gmail.com">deepreasoninggo@gmail.com</a> **and** <a href="https://drive.google.com/file/d/1F46UhKrqP9TvJAyMzmuk-xWwxcuWWSJj/view?usp=sharing" target="_blank" rel="noopener noreferrer">fill out this form</a>.
- [✅] Demo Customer-Centric Dataset C0.2 Visit [WebPage](https://goreasoning.github.io/mm_rl_agent_demos/)
- [✅] Sample Customer-Centric Dataset C0.2 in Comparison With GPT5.2, Gemini-3-Pro and Grok4 is in Huggingface, Visit [dataset](https://huggingface.co/datasets/deepgo/Customer_Centric_Agent_Benchmark_C0.2)
## 📜 License

**License:** CC-BY 4.0  
Free for research and commercial use with proper attribution.

---

## 📚 Citation

```bibtex
@dataset{di2025_incar_interaction_agent_p0_2,
  author       = {Xinhan Di},
  title        = {Customer-Centric Agent-OS C0.2},
  year         = {2026},
  url          = {https://github.com/your-og/Personlized Interaction Agent-OS C0.2},
  note         = {API, Version 0.2},
}
```

---

## 🤝 Acknowledgements

Special thanks to all annotators, engineers, and collaborators contributing to personlized interaction agent-os V0.1 application.

---

> © 2026 Deepgo. All rights reserved.
