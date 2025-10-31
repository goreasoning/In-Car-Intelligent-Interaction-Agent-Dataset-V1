# 🚗 In-Car Intelligent Interaction Agent Dataset V1.2

*A large-scale, multi-modal English/Chinese In-Car Intelligent Interaction Agent for vehicle interaction recognition, multi-turn dialogue, and emotion-aware in-car AI assistants.*

---

## 🆕 What’s New in V1.2

| Update | Description |
|---------|--------------|
| 😊 **Joint Intent Recognition, Rewrite, Sloter, Chat and Speech in the Agent System V1.2** | An integrated agent system designed to handle **colloquial user queries** in **multi-turn conversations**, emphasizing **joint text and speech generation and reasoning** for efficient generative interaction.|
| 🧩 **Multi-Modal Interaction For In-Car System V1.2** | An **agent-based** human-vehicle interaction framework designed for In-Car Intelligent Interaction, emphasizing the integration of **multiple input/output modalities** (e.g., voice, text language) to enable **natural**, distraction-minimizing communication between drivers/passengers and the vehicle's infotainment, navigation, and assistance systems.|
|  **Support for Human-Like Interaction and Machine-Like Interaction Through Reasoning** | Support for **Personlization-Emotional Interaction** with Joint Understanding and Generation of Language and Speech, Integrated with a Standardized Control Language(Machine-Like Interaction) for In-Car Systems.|
| 🧠 **Benchmarking in Comparison with SOTAs** | Evaluates the agent system against state-of-the-art models across key metrics, a demo v1_3_machine_interation_for_colloquial_user_queries(including one_user personlization_queries for in-car functions) is free to download without register.|
| 🧰 **Schema v2.0** | Unified schema across all modules for easier fine-tuning. |
| 🪶 **Cleaned Text** | Enhanced Chinese punctuation normalization and slang handling. |
---

## 📦 Overview

| Agent-Systems **Colloquialism Covery(>60%), Multi-turn Agent Reasoning Covery(>60%)** |Car Control | Travel & Navigation | Search & Information | Chit-Chat | Vehicle Knowledge & Q&A | Standardlization Ratio | Sandardlization Semantic Accuracy | Sloter Success | Talk Smoothness(Text) | Talk Emotional Reasoning(Text) | Talk Emotional Reasoning(Voice) | Persalization | 
|---------|--------------|----------|-------------|-----------|-----------|-----------|-----------|-----------|-----------|-----------|-----------|-----------|-----------|
| **GPT-5-Varients** | 80.10(0-100) | 80.53 | 81.39 | 81.02 | 81.15 | 0.81(0-1) | 0.80 | 0.79| 0.77| 0.81| 0.78| 0.76| 0.71 |
| **Qwen-Think-Varients(Agent-Learning-Common,Agents<=3B)** | 60.90 | 61.29 | 61.27 | 60.51 | 61.59 | 0.62 | 0.59 | 0.58 | 0.61 | 0.60 | 0.63 | 0.58  0.61 |
| **Doubao-Think-Varients(Agent-Learning-Common,Agents-flash)** | 60.49 | 61.35 | 60.10 | 60.22 | 61.84 | 0.61 | 0.57 | 0.60 | 0.59| 0.58| 0.61| 0.59 | 0.60 |
| **Ours-v1.2-Agents-Learning-V0,Agent-flash** | 92.37 | 93.85 | 92.63 | 93.19 | 92.91 | 0.93 | 0.92  | 0.92 | 0.91 | 0.91 | 0.92 | 0.91 | 0.92 |
---

## 🔊 Multi-Modal Demo V1.2 will be released soon:) Besides machine languages, I will provide **emotional benefits response ** to car **customers** through **supporting-emotion** text and voice languages :)

## 📊 Statistics

| Module | Samples | Avg. Turns | Modalities | Labels |
|---------|----------|-------------|-------------|---------|
| Intent Classification | 250 K + | 1 | Text | Intent |
| Interactive Agent | 130 K + | 2–5 | Text | Intent + Strategy |
| Hierarchical Agent | 70 K + | Variable | Speech + Text | Emotion + Context + Slots |

---

## 💡 Applications

- Vehicle intent detection  
- Multi-turn dialogue management  
- Emotion-aware agent response generation  
- Contextual reasoning and elliptical intent resolution  
- Multimodal in-car AI assistant training  
---

## 📅 Version History

| Version | Key Features | Release |
|----------|--------------|----------|
| **V1.0** | DataSet-V1 and Non-Commercial API Release| 2025 10 16 |
| **V1.1** | Benchmark-V1.1, Joint and Personalization Release | 2025 10 20 |
| **V1.2** | Benchmark-V1.2, Multi-Modal Voice and Emotion Text Language Generation Release | 2025 10 27 |

---

## 🚀 Getting Started
- [✅] To apply for dataset downloads and api for academic research purposes only, please email <a href="mailto:deepreasoninggo@gmail.com">deepreasoninggo@gmail.com</a> **and** <a href="https://drive.google.com/file/d/1F46UhKrqP9TvJAyMzmuk-xWwxcuWWSJj/view?usp=sharing" target="_blank" rel="noopener noreferrer">fill out this form</a>.  

## 📜 License

**License:** CC-BY 4.0  
Free for research and commercial use with proper attribution.

---

## 📚 Citation

```bibtex
@dataset{di2025_incar_interaction_agent_v1_3,
  author       = {Xinhan Di},
  title        = {In-Car Intelligent Interaction Agent Dataset V1.3},
  year         = {2025},
  url          = {https://github.com/your-og/Car-Interaction-Agent-Dataset-V1},
  note         = {Dataset, Version 1.2},
}
```

---

## 🤝 Acknowledgements

Special thanks to all annotators, engineers, and collaborators contributing to in-car intelligent-interaction research.

---

## 📧 Contact
