# HireMetrics AI: An Automated AI-Powered Resume Screening and ATS Evaluation System

![Python](https://img.shields.io/badge/Python-3.9%2B-blue.svg)
![Streamlit](https://img.shields.io/badge/Streamlit-1.30%2B-red.svg)
![Google Gemini](https://img.shields.io/badge/Google%20Gemini-2.5%20%2F%202.0%20Flash-purple.svg)
![License](https://img.shields.io/badge/License-MIT-green.svg)

**HireMetrics AI** is an intelligent talent acquisition and recruitment automation platform built to replace traditional keyword-matching Applicant Tracking Systems (ATS) with deep semantic reasoning. By leveraging Google's Gemini Generative AI models, Optical Character Recognition (OCR), and multi-format document parsing, HireMetrics AI delivers accurate candidate-job alignment scoring, skill-gap identification, document layout auditing, custom interview question generation, and high-volume batch ranking.

The platform includes a local deterministic rule-based fallback engine that ensures continuous operation even during network latency or cloud API quota disruptions.

---

## 🌟 Key Features

* **🎯 Module 1: Resume Match Score Engine**
  * Evaluates candidate qualifications against job descriptions across three customizable depths: **Summary**, **Standard**, and **Detailed Analysis**.
  * Evaluates true domain experience rather than exact keyword overlaps.

* **🔍 Module 2: Missing Skills Finder Engine**
  * Performs differential skill gap analysis between job mandates and candidate backgrounds.
  * Outputs three clear categories: **Verified Matched Skills**, **Missing Skill Gaps**, and **Actionable Upgrade Recommendations**.

* **🛠️ Module 3: Resume Format Checker & ATS Audit Engine**
  * Audits document layout for parser-breaking risks: contact obfuscation, unconventional section headers, decorative symbol clutter, and non-standard date formats.
  * Generates an **ATS Readability Score (0–100%)** and a categorical risk level classification (*Passed*, *Moderate Risk*, *High Risk*).

* **🎙️ Module 4: Tailored Interview Question Generator**
  * Synthesizes stage-specific interview prompts grounded in the candidate's verified project history and job specifications.
  * Categorizes questions into **Technical Screening**, **System Design & Architecture**, and **Behavioral Leadership**.

* **🏆 Module 5: Bulk Resume Ranker Engine**
  * Batch-processes multi-candidate file sets concurrently against a master job description.
  * Computes keyword density and semantic alignment, categorizes candidates into match tiers (🟢 Strong Match, 🟡 Potential Match, 🔴 Low Match), ranks them sequentially, and exports a unified **Leaderboard CSV**.

* **⚡ Zero-Downtime Deterministic Fallback Engine**
  * Seamlessly transitions execution to a local rule-based system (Jaccard similarity, stop-word filtering, and Regex pattern auditing) if cloud API limits or outages occur.

---

## 🛠️ Technology Stack

* **Frontend & Web UI:** Streamlit
* **Core Language:** Python 3.9+
* **Generative AI & LLM:** Google Gemini API (`gemini-2.5-flash` via `google-genai` SDK)
* **OCR & Computer Vision:** Tesseract OCR (`pytesseract`), Pillow (`PIL`)
* **Document Parsing:** `PyPDF`, `python-docx`, Native Text Streaming
* **Data Processing & Export:** `pandas`, `io`, Regular Expressions (`re`)

---

## 📁 Repository Structure

```text
HIRE-METRICS-AI/
│
├── HireMetrics_AI_Report.pdf   # Academic/Project Technical Documentation
├── app.py                      # Main Streamlit application and UI engine
├── requirements.txt            # Python package dependencies
└── README.md                   # Project documentation
