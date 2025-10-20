# 🚗 In-Car Intelligent Interaction Agent Dataset V1.2

*A large-scale, multi-modal Chinese dataset for vehicle intent recognition, multi-turn dialogue, and emotion-aware in-car AI assistants.*

---

## 🆕 What’s New in V1.2

| Update | Description |
|---------|--------------|
| 🗣️ **User Personalization** | Each utterance in the Personalized Style such as humor, brevity, empathy. |
| 😊 **Joint Intent Recognition, Sloter and Personlization and Chatting in the Agent System** | Together, these components in the Hierarchical Agent System enable the agent to deliver context-aware, human-like interactions that seamlessly blend task execution with natural conversation, creating a personalized and intelligent in-car experience. |
| 🧩 **LLM Training-Free Modules** | Efficiant RL Training outside of LLM Parameters in Typical Agent Modules, enabling continual improvement of agent behavior without retraining the entire large language model.|
| 🔊 **Self-Score and Perference** | Build new Self-Score and Custom Perference modules for User Personlization, dynamically evaluate user satisfaction and adapt interactions based on individual preferences, enhancing personalized dialogue and task execution. |
| 🧠 **Benchmarking in Comparison with SOTAs** | Evaluates the agent system against state-of-the-art models across key metrics such as intent recognition accuracy|
| 🧰 **Schema v2.0** | Unified schema across all modules for easier fine-tuning. |
| 🪶 **Cleaned Text** | Enhanced Chinese punctuation normalization and slang handling. |

---

## 📦 Overview

| Agent-Systems | Car Control | Travel & Navigation | Search & Information | Chit-Chat |Vehicle Knowledge & Q&A | Sloter Success | Talk Smoothness | Persalization | 
|---------|--------------|----------|-------------|-----------|-----------|
| **GPT-5-Varients** | 79.61(0-100) | 79.33 | 80.54 | 79.21 | 79.79 | 0.72(0-1) | 0.78 | 0.75 |
| **Qwen-Think-Varients** | 51.46 | 51.91 | 51.75 | 50.18 | 51.33 | 0.43 | 0.47 | 0.52 |
| **Doubao-Think-Varients** | 49.37 | 50.12 | 49.88 | 50.45 | 49.71 | 0.46 | 0.42 | 0.48 |
| **Qwen-Think-Ours** | 94.27 | 95.83 | 94.91 | 95.14 | 94.66 | 0.82 | 0.89 | 0.85 |
| **Doubao-Thibk-Ours** | 92.45 | 93.12 | 92.87 | 93.54 | 92.31 | 0.89 | 0.84 | 0.87 |

---

## 🚙 1. Vehicle Intent Classification

**Goal:** classify Chinese in-car utterances into 100 + fine-grained vehicle intents.

### Main Categories
1. **Car Control** – A/C, windows, lights, seats.  
2. **Travel & Navigation** – routing, traffic, parking, refueling.  
3. **Search & Information** – media, weather, POI search.  
4. **Chit-Chat** – casual or emotional conversation.  
5. **Vehicle Knowledge & Q&A** – maintenance, driving tips.  

**Example**
```json
{
  "text": "打开副驾驶的座椅加热",
  "intent_category": "Car Control",
  "sub_intent": "Seat Heating",
  "slots": {"position": "front passenger"}
}
```

---

## 🗣️ 2. In-Vehicle Interactive Agent Dataset

**Focus:** realistic multi-turn dialogues between drivers and assistants.  
Each dialogue contains contextual state tracking and agent strategy.

**Example**
```json
{
  "dialogue_id": "D03125",
  "turns": [
    {"role": "user", "text": "有点热。"},
    {"role": "agent", "text": "要我调低温度吗？", "strategy": "confirmation"},
    {"role": "user", "text": "好，设到二十四度。"},
    {"role": "agent", "text": "好的，空调已调到24度。", "strategy": "task_completion"}
  ],
  "category": "Car Control"
}
```

---

## 🧩 3. Hierarchical In-Vehicle Agent Dataset

**Focus:** multi-modal annotation for deep contextual understanding.

**Annotations**
- 🎧 **Speech Transcription** (verified ASR)  
- 😊 **Emotion Labels** (5-class taxonomy)  
- 🔁 **Context Reasoning** (co-reference + elliptical intent)  
- 🧱 **Fine-Grained Slots** (action/target/parameter)  

**Example**
```json
{
  "utterance_id": "E20781",
  "speech_file": "audio/E20781.wav",
  "speech_transcription": "打开天窗。",
  "emotion": "neutral",
  "context_description": "用户刚启动车辆。",
  "intent_category": "Car Control",
  "intent_action": "open",
  "intent_target": "sunroof",
  "slots": {"position": "front"},
  "asr_alignment": {"start_ms": 0, "end_ms": 1220}
}
```

---

## 📊 Statistics

| Module | Samples | Avg. Turns | Modalities | Labels |
|---------|----------|-------------|-------------|---------|
| Intent Classification | 250 K + | 1 | Text | Intent |
| Interactive Agent | 130 K + | 3–7 | Text | Intent + Strategy |
| Hierarchical Agent | 70 K + | Variable | Speech + Text | Emotion + Context + Slots |

---

## 💡 Applications

- Vehicle intent detection  
- Multi-turn dialogue management  
- Emotion-aware agent response generation  
- Contextual reasoning and elliptical intent resolution  
- Multimodal in-car AI assistant training  

---

## 🧰 Usage

```python
import json

with open('1_intent_classification/data.json', 'r', encoding='utf-8') as f:
    samples = json.load(f)
    print(samples[0])
```

---

## 📅 Version History

| Version | Key Features | Release |
|----------|--------------|----------|
| **V1.1** | DataSet-V1 and Non-Commercial API Release| 2025 10 16 |
| **V1.2** | Benchmark-V1, Joint and Personalization Release | 2025 10 20 |

---

## 🚀 Getting Started
- [✅] To apply for dataset downloads and api for academic research purposes only, please email <a href="mailto:deepreasoninggo@gmail.com">deepreasoninggo@gmail.com</a> **and** <a href="https://drive.google.com/file/d/1F46UhKrqP9TvJAyMzmuk-xWwxcuWWSJj/view?usp=sharing" target="_blank" rel="noopener noreferrer">fill out this form</a>.  

## 📜 License

**License:** CC-BY 4.0  
Free for research and commercial use with proper attribution.

---

## 📚 Citation

```bibtex
@dataset{di2025_incar_interaction_agent_v1_2,
  author       = {Xinhan Di},
  title        = {In-Car Intelligent Interaction Agent Dataset V1.2},
  year         = {2025},
  url          = {https://github.com/your-org/Car-Interaction-Agent-Dataset-V1},
  note         = {Dataset, Version 1.2},
}
```

---

## 🤝 Acknowledgements

Special thanks to all annotators, engineers, and collaborators contributing to in-car intelligent-interaction research.

---

## 📧 Contact

- **Maintainer:** Xinhan Di  
- **Email:** [deepreasoningo@gmail.com](mailto:deepreasoningo@gmail.com)  
- **GitHub:** [https://github.com/your-org/Car-Interaction-Agent-Dataset-V1](https://github.com/your-org/Car-Interaction-Agent-Dataset-V1)
