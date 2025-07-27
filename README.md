# <img src="https://img.icons8.com/color/48/000000/robot-2.png" width="24"/> ColdFluChatbot: LLM-Powered Cold vs. Flu Symptom Checker

This chatbot helps users in Nova Scotia distinguish between cold and flu symptoms, identify when to seek medical attention, and follow trusted self-care guidance. It uses a Retrieval-Augmented Generation (RAG) pipeline powered by AnythingLLM and a local model via Ollama.

> ⚠️ **Disclaimer:** This chatbot does **not** provide professional medical advice or diagnoses. It is intended for educational use only. If you are experiencing a medical emergency, call 911 or visit the nearest emergency department.

---

## <img src="https://img.icons8.com/fluency/48/checked.png" width="20"/> Project Overview

* **Scenario:** Cold / Flu Symptom Self-Assessment Chatbot
* **Goal:** Build a domain-specific chatbot that:

  * Distinguishes cold vs. flu symptoms
  * Provides official home-care advice
  * Identifies when to seek medical care
  * Clearly states that it is not a diagnostic tool

---

## <img src="https://img.icons8.com/color/48/engineering.png" width="20"/> Tech Stack

| Layer           | Tool                           | Role                        |
| --------------- | ------------------------------ | --------------------------- |
| LLM Frontend    | AnythingLLM                    | UI + RAG + Prompt Injection |
| LLM Backend     | Ollama                         | Local model engine          |
| LLM Model       | Mistral (via Ollama)           | Generates responses         |
| Documents       | NS Health, PHAC, Health Canada | Knowledge Base              |
| Dev Environment | VS Code + GitHub               | Authoring & Collaboration   |

---

## <img src="https://img.icons8.com/ios/50/folder-invoices--v1.png" width="20"/> Folder Structure

```
/cold-flu-chatbot
├── knowledge_base/
│   ├── knowledge_document_1.pdf
│   ├── knowledge_document_2.md
│   ├── knowledge_document_3.txt
│   └── ...
├── prompt/
│   └── system_prompt.txt
├── documentation/
│   ├── scenario_pack.md
│   ├── project-description.pdf
│   └── use_case_description.md
├── demo/
│   ├── demo_video.mp4
│   └── chat_transcript.txt
└── README.md
```

---

## <img src="https://img.icons8.com/windows/32/document--v1.png" width="20"/> Knowledge Base File Structure

```
/cold-flu-chatbot
└── knowledge_base/
    ├── knowledge_document_1.pdf       ← [NS 811: Colds and the Flu](https://811.novascotia.ca/health_topics/colds-and-the-flu/)
    ├── knowledge_document_2.txt       ← [U of Lethbridge: Cold or Flu Brochure](https://www.ulethbridge.ca/sites/default/files/Cold%20or%20Flu%20brochure%20layout%20%284%29.pdf)
    ├── knowledge_document_3.pdf       ← [St. Joe's Cold vs Flu (May 2021)](https://www.stjoes.ca/patients-visitors/patient-education/patient-education-a-e/cold-vs-flu-may-2021.pdf)
    ├── knowledge_document_4.md        ← [NS 811: Preventing the Flu](https://811.novascotia.ca/health_topics/preventing-the-flu/)
    ├── knowledge_document_5.md        ← [NS 811: About 811](https://811.novascotia.ca/about-811/)
    └── knowledge_document_6.md        ← [PHAC: Flu/Influenza Overview](https://www.canada.ca/en/public-health/services/diseases/flu-influenza.html)
```

---

## <img src="https://img.icons8.com/ios-filled/50/idea.png" width="20"/> Prompt Engineering

* **System Prompt** was crafted to:

  * Define role: friendly wellness coach (not a doctor)
  * Ensure tone: warm, factual, accessible
  * Set boundaries: no diagnosis, refer serious cases to emergency services
  * Include disclaimers: repeated as needed in responses
  * Handle crisis triggers: forward users to emergency care

> The final system prompt is saved in `prompt/system_prompt.txt` and loaded directly into the AnythingLLM workspace.

---

## <img src="https://img.icons8.com/ios-glyphs/30/synchronize.png" width="20"/> Integration Workflow

1. **Install and launch Ollama**

   ```bash
   ollama pull mistral
   ollama run mistral
   ```
2. **Launch AnythingLLM Desktop App**
3. **Create new workspace:** `ColdFluChatbot`
4. **Upload documents** into the workspace knowledge base
5. **Paste custom system prompt** into Chat Settings > System Prompt
6. **Connect Ollama as the LLM Provider**

   * Global setting: Ollama
   * Model name: `mistral`
7. **Test chatbot using required questions**
8. **Save transcript + screen recording**

---

## <img src="https://img.icons8.com/color/48/experimental-test-tube.png" width="20"/> Testing Questions

The bot was tested using the following scenario questions:

> "I have a fever of 38.5 °C and a runny nose—is this the flu or just a cold?"

> "If it's just a cold, how many days should I stay home and rest?"

Both answers were evaluated for tone, content accuracy, document use, and disclaimers. The transcript is saved in `/demo/chat_transcript.txt`.

---

## <img src="https://img.icons8.com/fluency/48/youtube-play.png" width="20"/> Demo Video

* The chatbot demo shows full setup, document usage, and responses to both scenario questions.
* File: `/demo/demo_video.mp4`

---

## <img src="https://img.icons8.com/ios-filled/50/user-male-circle.png" width="20"/> Author

**Jack Murtha**,
Master of Business Analytics, Saint Mary's University,
July 2025,
jack.murtha@smu.ca
