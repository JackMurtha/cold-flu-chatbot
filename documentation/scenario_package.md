# 🩺 Cold / Flu Symptom Self-Assessment Chatbot  
### **Scenario Package**

---

## 📖 Scenario Background

In Halifax, Nova Scotia, the winter season sees a high incidence of both common colds and influenza. While their symptoms overlap, influenza is typically more severe, with sudden onset, high fever, and body aches.

Nova Scotia Health and the Public Health Agency of Canada (PHAC) publish patient-friendly guidelines to help residents distinguish and manage these common illnesses.

This scenario asks students to use the **Ollama + AnythingLLM** stack, combined with locally available, authoritative health education materials, to design a chatbot for Cold / Flu Symptom Self-Assessment.

---

## 🎯 Scenario Goals

- Help users distinguish between common cold and influenza symptoms  
- Guide users to recognize when they should see a doctor  
- Provide official home-care recommendations  
- Clearly communicate that the chatbot does **not** provide professional medical diagnoses

---

## 🗂 Recommended Knowledge Base Materials

Students should collect and organize retrievable, structured local health education materials to serve as their RAG (Retrieval-Augmented Generation) knowledge base. Recommended sources include:

- Nova Scotia Health – Cold vs. Flu Comparison Handouts  
- PHAC – Seasonal Influenza Symptoms and Self-Care FAQs  
- Health Canada – Guidance on When to See a Doctor for Flu-like Illness  
- Nova Scotia Health – Home Care Tips for Colds and Flu  
- Any relevant Nova Scotia government COVID/flu updates for local consistency  

> 📌 **Requirement:** Upload knowledge base files as `.pdf`, `.md`, or `.txt` using consistent filenames like:

knowledge_document_1.pdf
knowledge_document_2.md
knowledge_document_3.txt

---

## 🧪 Suggested User Questions for Testing

Your final system must be able to answer these questions using your uploaded knowledge base materials:

1. **"I have a fever of 38.5 °C and a runny nose—is this the flu or just a cold?"**  
2. **"If it's just a cold, how many days should I stay home and rest?"**

---

## 📦 Suggested GitHub Repository Structure

## 📦 GitHub Repository Structure

```
/cold-flu-chatbot
├── knowledge_base/
│   ├── knowledge_document_1.pdf
│   ├── knowledge_document_2.md
│   └── knowledge_document_3.txt
├── prompt/
│   └── system_prompt.txt
├── documentation/
│   ├── scenario_pack.md
│   └── use_case_description.md
├── demo/
│   ├── demo_video.mp4
│   └── chat_transcript.txt
└── README.md
``` 

---

## 🧪 Suggested User Questions for Testing

Your final system must be able to answer these questions using your uploaded knowledge base materials:

1. **"I have a fever of 38.5 °C and a runny nose—is this the flu or just a cold?"**  
2. **"If it's just a cold, how many days should I stay home and rest?"**

---

## 📑 Deliverables Summary

### ✅ Knowledge Base
- Upload all documents used in AnythingLLM  
- Use clean, consistent file naming  

### ✅ System Prompt
- Define the chatbot’s role, tone, scope, and ethical disclaimers  

### ✅ Use Case Description
- Document user pain points and success criteria  

### ✅ Demo Materials
- Screen recording showing chatbot answering core questions  
- Chat transcript file

### ✅ README.md
- Brief project summary  
- Local setup and testing instructions  
- Author and submission date  
- ⚠️ **Include: “Not Medical Diagnosis” disclaimer prominently**

---

## ⚠ Important Notes

- All files must be uploaded to a **public or private GitHub repository** for evaluation  
- This chatbot is for **educational research only** — not for clinical use  
- No real patient data should be used  
- Always include disclaimers and redirect emergency cases to 911

---


