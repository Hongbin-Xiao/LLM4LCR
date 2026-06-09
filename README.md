# PEAT-LLM4LCR: An AI-Assisted Human-Computer Collaboration Framework for Chinese Legal Contract Review

<div align="center">

[![Paper](https://img.shields.io/badge/Paper-IJHCS-blue)](https://www.sciencedirect.com/journal/international-journal-of-human-computer-studies)
[![Demo](https://img.shields.io/badge/Video-Demo-red)](https://www.youtube.com/watch?v=eyIikQDkv0E)
[![License](https://img.shields.io/badge/License-MIT-green)](LICENSE)
[![GitHub Stars](https://img.shields.io/github/stars/Hongbin-Xiao/PEAT-LLM4LCR)](https://github.com/Hongbin-Xiao/PEAT-LLM4LCR/stargazers)

</div>

> **PEAT-LLM4LCR** (Prompt Engineering and Agent Technology for Large Language Model-based Legal Contract Review) is a specialized AI framework for automated Chinese legal contract review, combining structured prompt engineering, iterative expert-feedback optimization, and multi-agent graph-structured workflow orchestration.

📄 **Paper:** *PEAT-LLM4LCR: An AI-Assisted Human-Computer Collaboration Framework for Chinese Legal Contract Review*
🎬 **Video Demo:** [Watch on YouTube](https://www.youtube.com/watch?v=eyIikQDkv0E)

---

## 📊 Key Results at a Glance

| Metric | Result |
|--------|--------|
| 🎯 Risk Identification Accuracy | **92%** |
| ✅ Suggestion Qualification Rate | **96%** (↑28pp vs. best baseline) |
| ⚡ Time Reduction (Professionals) | **77%** (26.4 min → 6.0 min) |
| 📈 Novice Quality Improvement | **0.0 → 2.6** (0–4 scale) |
| 👥 User Study Participants | **18** (Novice / Professional / Expert) |

---

## 📝 Overview

Legal contract review is a critical but resource-intensive task. Non-legal professionals often lack the expertise to identify risks, while legal experts face significant time burdens (**2–4 hours per contract**). Existing AI solutions fail to provide actionable modification suggestions, particularly in the complex linguistic and legal context of **Chinese law (China Civil Code)**.

PEAT-LLM4LCR addresses these challenges through three core innovations:

- 🔗 **Structured Prompt Engineering** — Encodes legal expert knowledge into 28 Chain-of-Thought (CoT) prompt templates across 3 review dimensions
- 🔄 **LR-STRB** — A novel iterative prompt optimization method driven by expert feedback, requiring no gradient-based model training
- 🤖 **Agent-GoTFlow** — A multi-agent orchestration engine using a graph-structured workflow for coordinated contract analysis

<img width="8810" height="1912" alt="System Overview" src="https://github.com/user-attachments/assets/8882d8fd-7847-464c-9c9f-eceb8e456ee0" />

<img width="14795" height="6288" alt="Framework Architecture" src="https://github.com/user-attachments/assets/d35b8cc6-ecdc-46fd-b161-86cbd9d1374f" />

<img width="4347" height="6162" alt="Workflow Detail" src="https://github.com/user-attachments/assets/2d5b7542-33f9-4cb5-aa1f-2c7dc84cc6ec" />

---

## 🌟 Key Contributions

### 1. 🏗️ PEAT-LLM4LCR Multi-Agent Collaborative Architecture
A distributed cognitive system integrating prompt engineering with multi-agent collaboration, featuring:
- **Information Sharing Pool** for cross-agent communication and consistency
- **Agent-GoTFlow** graph-structured workflow engine for coordinated task execution
- Full interpretability and transparency of the review process

### 2. 🧠 Chain-of-Thought Prompt Template Methodology
A three-stage prompt construction process:
1. **CoT Design** — Logical reasoning paths for each clause category
2. **Parameter Mapping** — Formalizing rules into structured components (`Role`, `Action`, `Risk`, `Solution`, etc.)
3. **Template Instantiation** — 28 finalized templates covering 3 review dimensions

### 3. 🔄 LR-STRB: Legal Rules Self-Taught Reasoner Bootstrap
A novel self-supervised iterative optimization method that:
- Collects error cases from real contract tests
- Incorporates senior lawyer feedback (avg. 15 years experience) for root-cause analysis
- Refines prompt templates **without updating model weights** — ideal for data-scarce legal domains
- Reduces "Score 0" (completely incorrect) outputs by **10–25%**

### 4. 💻 End-to-End Contract Review Platform
A three-panel interactive system featuring:
- **Left Panel**: Original contract text with word count and translation toggles
- **Center Panel**: Structured findings by dimension (Basic / High-Risk / IP) with color-coded risk badges
- **Right Panel**: AI Q&A assistant for natural language queries and legal reasoning explanations

---

## 🏗️ Framework Architecture

<img width="8259" height="7515" alt="Methodology Overview" src="https://github.com/user-attachments/assets/85f677f2-663d-41da-9087-d9bccbdb1cc1" />

<img width="7680" height="4320" alt="Agent-GoTFlow Architecture" src="https://github.com/user-attachments/assets/4f9ad92b-02e2-4e94-a0a2-9c3398e24efc" />

<img width="1637" height="629" alt="Prompt Template Structure" src="https://github.com/user-attachments/assets/0f4622b4-1a49-43d0-934f-f861e290e466" />

---

## 📋 Review Clause Classification System

The framework covers **28 review items** across three dimensions:

| Dimension | Count | Key Items |
|-----------|-------|-----------|
| **Basic Element Review** | 18 | Party compliance, Price composition, Performance period, Delivery method, Acceptance criteria, Breach liability |
| **High-Risk Identification** | 8 | Consistency of party names, Payment & invoicing sequence, Performance location, Liquidated damages |
| **Intellectual Property** | 5 | Ownership of existing/newly formed IP, IP defect warranty, Party identity confirmation |

---

## 📈 Experimental Results

### Technical Performance (vs. Baselines)

| Method | Accuracy | Precision | Recall | Qualification Rate |
|--------|----------|-----------|--------|--------------------|
| RBNLP (Rule-based) | 81.8% | 81.8% | 81.8% | — |
| SVM+SGD (ML) | 88.0% | 91.0% | 91.0% | — |
| GPT-4o (Optimized Prompt) | 78.0% | 91.0% | 87.0% | 52% |
| TY (Optimized Prompt) | 82.0% | 85.0% | 83.0% | 68% |
| **PEAT-TY (Ours)** | **92.0%** | **93.0%** | **90.0%** | **96%** |

### User Study Results (n=18, Controlled Experiment)

**Review Quality (0–4 scale):**

| Group | Without Tool | With Tool | Improvement |
|-------|-------------|-----------|-------------|
| Novice | 0.0 | 2.6 | **+2.6** |
| Professional | 0.6 | 2.8 | **+2.2** |
| Expert | 4.0 | 4.0 | Maintained ceiling |

**Review Efficiency (minutes per contract):**

| Group | Without Tool | With Tool | Reduction |
|-------|-------------|-----------|-----------|
| Novice | 15.0 min | 7.4 min | **↓51%** |
| Professional | 26.4 min | 6.0 min | **↓77%** |
| Expert | 11.2 min | 7.4 min | **↓34%** |

> 💡 **Expertise Bridging Effect:** Professionals using the tool (Score 2.8, 6.0 min) approach expert-level quality (Score 4.0, 11.2 min) in nearly half the time.

---

## 🗂️ Dataset

| Property | Details |
|----------|---------|
| Training Set | 50+ real-world anonymized Chinese contracts |
| Test Set | 10 independent contracts across 9 industry subtypes |
| Industries Covered | Chemical, Construction, Electronics, Machinery, Furniture, etc. |
| Annotation | 118 problematic clauses across 28 review categories |
| Privacy | Fully anonymized (enterprise names, addresses, registration numbers removed) |

---

## 👥 Authors

- **Hongbin Xiao** — Guangxi Normal University
- **Shuru Tan** — Guangxi Normal University
- **Ye Li** — Microsoft Asia-Pacific R&D Group
- **Xin Zhou** — Beijing Aivigate Co. Ltd.
- **Zhi Li** *(Corresponding Author)* — Guangxi Normal University
- **Zhi Jin** — Peking University
- **Xiaolan Xie** — Guilin University of Technology
- **Wanglong Liu** — Guilin University of Technology

---

## 📄 Citation

If you find this work useful, please cite our paper:

```bibtex
@article{xiao2026peat,
  title     = {PEAT-LLM4LCR: An AI-Assisted Human-Computer Collaboration Framework for Chinese Legal Contract Review},
  author    = {Xiao, Hongbin and Tan, Shuru and Li, Ye and Zhou, Xin and Li, Zhi and Jin, Zhi and Xie, Xiaolan and Liu, Wanglong},
  journal   = {International Journal of Human-Computer Studies},
  year      = {2026},
  publisher = {Elsevier}
}
```

---

## 📬 Contact

For questions or collaboration inquiries, please contact the corresponding author:
**Zhi Li** — Guangxi Normal University
📧 *(Please refer to the published paper for contact details)*

---

<div align="center">
⭐ If this project helps your research, please consider giving it a star!
</div>
