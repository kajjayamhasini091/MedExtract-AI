# MedExtract-AI
# MedExtract-AI: Autonomous Clinical Intelligence & Question Extraction
> Official Submission for **3SVK Season 4 — Cloud Innovation Challenge**  
> **Powered by Adaption Labs**

[![Live App](https://img.shields.io/badge/Live%20App-my--app--roeu4f.adaptionlabs.app-00C781?style=for-the-badge&logo=rocket)](https://my-app-roeu4f.adaptionlabs.app)
[![Platform](https://img.shields.io/badge/Powered%20By-Adaption%20Labs-7B2CBF?style=for-the-badge)](https://adaptionlabs.ai)
[![Author](https://img.shields.io/badge/Contributor-Hasini%20Kajjayam-2A9D8F?style=for-the-badge)](https://github.com/kajjayamhasini09)

---

## 🌟 Overview
**MedExtract-AI** is an AI-powered clinical intelligence system designed to reduce cognitive load for physicians, resident doctors, and trainees during emergency department triage and clinical case reviews. 

Built end-to-end on **Adaption Labs**, the system converts messy, unstructured clinical notes and patient vignettes into **atomic, categorized diagnostic questions** paired with **guideline-concordant expert management protocols**.

---

## 🚀 Official Live Application
Experience the deployed application live in production:  
👉 **[https://my-app-roeu4f.adaptionlabs.app](https://my-app-roeu4f.adaptionlabs.app)**

---

## 💡 Key Capabilities
- **Atomic Clinical Question Extraction**: Parses complex narratives (symptoms, vitals, 12-lead ECG findings, cardiac biomarkers) into structured, categorized clinical queries.
- **Evidence-Based Guideline Concordance**: Follows international clinical practice guidelines (AHA/ACC STEMI guidelines, ADA standards of medical care, Surviving Sepsis campaign).
- **Clinical Hallucination Mitigation**: Constrained using Adaption's recipe pipeline with explicit chain-of-thought reasoning traces.
- **Contraindication & Red Flag Warnings**: Proactively highlights high-risk contraindications (e.g., avoiding sublingual nitrates in suspected Right Ventricular Infarction).
- **Interactive Teaching & Review UI**: Zero-latency reactive dual-pane interface built and hosted natively on Adaption Labs.

---

## 🛠️ Adaption Labs Architecture & Pipeline

```
          Unstructured Clinical Vignette / Medical Note
                               │
                               ▼
┌─────────────────────────────────────────────────────────────┐
│             Adaption Labs Adaptive Engine                   │
│                                                             │
│  1. Data Evaluation & Diagnostic (Initial Grade C baseline) │
│  2. Recipe Optimization Stack:                              │
│     ├── Chain-of-Thought Reasoning Traces                   │
│     ├── Hallucination Mitigation Guardrails                 │
│     ├── Prompt Metadata Injection                           │
│     └── Deduplication & House Special Filtering             │
│  3. Custom Blueprint System Steering                        │
│  4. Synthetic Expansion: 3,264 Clinical QA Pairs            │
└──────────────────────────────┬──────────────────────────────┘
                               │
                               ▼
┌─────────────────────────────────────────────────────────────┐
│           Production Adaptive Web Interface                 │
│            https://my-app-roeu4f.adaptionlabs.app           │
│                                                             │
│  • ED Chest Pain / STEMI Reperfusion Decision Pathways      │
│  • New T2DM Diagnosis & Pharmacotherapy Workups              │
│  • Pediatric Febrile Infant Stratification                  │
└─────────────────────────────────────────────────────────────┘
```

---

## 🔬 Sample Clinical Evaluation
### Input Vignette (Emergency Department):
> *"A 58-year-old man with a 30 pack-year smoking history and poorly controlled hypertension presents to the emergency department with 2 hours of crushing substernal chest pain radiating to the left jaw, associated with diaphoresis and nausea. BP 158/94, HR 102, SpO2 96%. 12-lead ECG shows 3mm ST-elevation in leads II, III, and aVF. Initial high-sensitivity troponin is markedly elevated. The team is considering reperfusion strategy and antiplatelet loading."*

### Model Extraction & Guideline Protocol:
1. **Diagnosis & Triage Urgency:** Acute Inferior STEMI with ongoing transmural ischemia. Activates primary PCI pathway (<90 min door-to-balloon target).
2. **Reperfusion Selection:** Primary PCI preferred; fibrinolysis indicated if door-to-device transfer delay exceeds 120 minutes and presentation is within 12 hours.
3. **Antiplatelet Loading:** Immediate dual antiplatelet therapy (Chewable Aspirin 325 mg + Ticagrelor 180 mg) combined with parenteral anticoagulation.
4. **Critical Safety Contraindication:** Right ventricular involvement must be evaluated via right-sided precordial lead (V4R) before administering sublingual nitrates or morphine, as nitrates induce profound venodilation and precipitate catastrophic hypotension in RV infarction.

---

## ⚖️ Jury Rubric Calibration

| Evaluation Pillar | Target Judge | Alignment & Impact |
| :--- | :--- | :--- |
| **Best Use of Adaption ($100 Prize)** | Adaption Labs Core Team | Leveraged the complete stack: Data Diagnosis, Recipe Layer, Custom Blueprint Steering, 3,200+ Synthetic Expansion, and Public Web App Hosting. |
| **Autonomous AI & Life Sciences** | Yogen Ghodke (AI Solutions Engineer) | Directly addresses high-acuity medical decision support with structured clinical reasoning and explicit contraindication flags. |
| **Open Source & Research Rigor** | Aditya Kumar Singh / Wei-Yin K. | Cleanly documented, fully reproducible methodology, architectural diagrams, and a dedicated research report. |

---

## 📄 Research Report
The comprehensive technical paper and evaluation methodology is detailed in `3SVK_Submission_Report.md`.
