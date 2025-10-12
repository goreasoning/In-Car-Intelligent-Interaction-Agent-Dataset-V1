# 🚗 In-Car Intelligent Interaction Agent Dataset V1

**Car Intelligent Interaction Agent Dataset V1**  
A large-scale, open-source Chinese dataset for **in-vehicle intelligent interaction**, designed to support research and development of **voice assistants, multi-turn dialogue systems, and emotion-aware car agents**.

---

## 📦 Overview

| Module | Description                                                                    | Samples | Categories |
|--------|--------------------------------------------------------------------------------|----------|-------------|
| **Vehicle Intent Classification Dataset** | Car command & intent recognition                                               | 200K+ | 100+ |
| **In-Vehicle Interactive Agent Dataset** | Multi-turn human–agent dialogues                                               | 100K+ | 5 main classes |
| **Hierarchical In-Vehicle Agent Dataset** | Speech transcription, emotion, context understadning, fine-grained annotations | 50K+ | Multi-level labels |

---

## 🧠 Dataset Structure

```
Car-Interaction-Agent-Dataset-V1/
│
├── 1_intent_classification/             # Vehicle Intent Classification Dataset
│   ├── data.json
│   ├── label_schema.json
│   └── examples/
│
├── 2_interactive_agent_dataset/         # In-Vehicle Interactive Agent Dataset
│   ├── dialogues.json
│   ├── multi_turn_samples/
│   └── scenarios/
│
├── 3_hierarchical_agent_dataset/        # Hierarchical Interaction Agent Dataset
│   ├── speech_transcription/            # Transcribed speech text
│   ├── emotion_annotations/             # Emotion labels
│   ├── context_understanding/           # Contextual understanding
│   └── fine_grained_examples/           # Slot-level examples
│
└── README.md
```

---

## 🚙 1. Vehicle Intent Classification Dataset

### 🏷️ Five Major Intent Categories
1. **Car Control**  
   Vehicle control commands such as air conditioning, windows, sunroof, lights, and seats.  
   - Example:  
     - “Turn on the A/C and set to 25 degrees.”  
     - “Close the right rear window.”

2. **Travel & Navigation**  
   Navigation, route planning, traffic info, parking, fuel/charging stations, etc.  
   - Example:  
     - “Navigate to the nearest charging station.”  
     - “How long will it take to get to work tomorrow morning?”

3. **Search & Information**  
   Music, weather, restaurant, news, or POI search.  
   - Example:  
     - “Play Jay Chou’s songs.”  
     - “Find good Japanese restaurants nearby.”

4. **Chit-Chat**  
   Casual conversations and emotional engagement with the in-car assistant.  
   - Example:  
     - “How are you today?”  
     - “I’m tired, talk to me.”

5. **Vehicle Knowledge & Q&A**  
   Questions about car usage, maintenance, and driving tips.  
   - Example:  
     - “What should I do if tire pressure is low?”  
     - “How to enable cruise control?”

> ✅ Includes **100+ fine-grained intent subcategories**, covering all major in-car voice assistant scenarios.

---

## 🗣️ 2. In-Vehicle Interactive Agent Dataset

This module focuses on **multi-turn interactions** between the user and the in-car assistant, simulating realistic dialogue flow.

Each dialogue sample includes:
- User query or speech transcription  
- Agent clarification or response  
- Contextual history tracking  
- Dialogue type label (Car Control / Travel / Search / Chat / Knowledge)

**Example:**
```json
{
  "dialogue_id": "T00087",
  "turns": [
    {"role": "user", "text": "It’s a bit hot."},
    {"role": "agent", "text": "Would you like me to lower the temperature?"},
    {"role": "user", "text": "Yes, set it to 24 degrees."},
    {"role": "agent", "text": "Got it, setting A/C to 24 degrees now."}
  ],
  "category": "Car Control"
}
```

---

## 🧩 3. Hierarchical In-Vehicle Agent Dataset

This module focuses on **multi-level annotations** to enhance agent understanding, including:
- 🎧 **Speech Transcription** (manually verified ASR text)
- 😊 **Emotion Labels** (sentiment and emotional response)
- 🔁 **Context Understanding** (elliptical intent resolution and history tracking)
- 🔍 **Fine-Grained Examples** (slot-level and semantic-level details)

**Example:**
```json
{
  "utterance_id": "E10492",
  "speech_transcription": "Open the window.",
  "emotion": "calm",
  "context": "Driver just started the car.",
  "intent": {
    "category": "Car Control",
    "target": "window",
    "action": "open",
    "slot": {"position": "driver side"}
  }
}
```

---

## 📊 Statistics

| Module | Samples | Avg. Turns | Annotation Dimensions |
|---------|----------|-------------|------------------------|
| Intent Classification | 200K+ | Single-turn | Intent Label |
| Interactive Agent | 100K+ | 2–6 turns | Intent + Response |
| Hierarchical Agent | 50K+ | Multi-modal | Speech + Emotion + Context |

---

## 💡 Applications

- Vehicle intent recognition & command understanding  
- Multi-turn dialogue management  
- Emotion-aware car assistant design  
- Hierarchical reasoning and contextual agent learning  
- Multi-modal human–vehicle interaction research  

---

## 🧰 Usage

```bash
# Clone the repository
git clone https://github.com/your-org/Car-Interaction-Agent-Dataset-V1.git

# Load sample data
import json

with open('1_intent_classification/data.json', 'r', encoding='utf-8') as f:
    data = json.load(f)
    print(data[0])
```

---

## 📅 Version Plan

| Version | Content                                                  | Status     |
|----------|----------------------------------------------------------|------------|
| **V1.0** | Base Intent + Multi-turn Dialogue + Hierarchical Dataset | ✅ Released |
| **V1.1** | Coming Soon                                              | Qct 2025   |

## 🚀 Getting Started
- [✅] To apply for dataset downloads for academic research purposes only, please email <a href="mailto:deepreasoninggo@gmail.com">deepreasoninggo@gmail.com</a> **and** <a href="https://drive.google.com/file/d/1F46UhKrqP9TvJAyMzmuk-xWwxcuWWSJj/view?usp=sharing" target="_blank" rel="noopener noreferrer">fill out this form</a>.  
---

## 🧾 License

- This dataset is released for **research and commercial use**.  
- Please cite as:  
@misc{Di2025_InCarIntelligentInteractionAgentDatasetV1,
  author       = {Di, Xinhan},
  title        = {In-Car Intelligent Interaction Agent Dataset V1},
  year         = {2025},
  howpublished = {\url{https://scholar.google.com/citations?hl=en&user=CDijR8YAAAAJ}},
  note         = {Dataset}
}


---

## 🤝 Acknowledgements

Special thanks to all contributors who supported the creation of this dataset and the advancement of in-car intelligent interaction research.

---

## 📧 Contact

- Maintainer: [Xinhan Di]  
- Email: deepreasoningo@gmail.com  
- GitHub: [https://github.com/your-org/Car-Interaction-Agent-Dataset-V1](https://github.com/your-org/Car-Interaction-Agent-Dataset-V1)

---

> © 2025 Deepgo. All rights reserved.
