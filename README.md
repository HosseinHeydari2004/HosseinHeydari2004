<h1 align="center">Hossein Heydari</h1>

<p align="center">
  <strong>AI Engineer · LLM & RAG Systems · Data Science</strong>
</p>

<p align="center">
  <strong>Co-Founder & Technical Lead at AI Builders · LLM Team Lead</strong>
</p>

<p align="center">
  Building practical AI systems from <strong>data and documents to retrieval, reasoning, APIs, and deployment.</strong>
</p>

<p align="center">
  <a href="https://github.com/HosseinHeydari2004">
    <img src="https://img.shields.io/badge/GitHub-181717?style=for-the-badge&logo=github&logoColor=white"/>
  </a>
  <a href="https://www.linkedin.com/in/hossein-heydari2004">
    <img src="https://img.shields.io/badge/LinkedIn-0A66C2?style=for-the-badge&logo=linkedin&logoColor=white"/>
  </a>
  <a href="https://www.kaggle.com/mrhosseinheydari">
    <img src="https://img.shields.io/badge/Kaggle-20BEFF?style=for-the-badge&logo=kaggle&logoColor=white"/>
  </a>
  <a href="mailto:hosseinheydari992020@gmail.com">
    <img src="https://img.shields.io/badge/Email-D14836?style=for-the-badge&logo=gmail&logoColor=white"/>
  </a>
  <a href="https://t.me/Hossein_h830">
    <img src="https://img.shields.io/badge/Telegram-0088CC?style=for-the-badge&logo=telegram&logoColor=white"/>
  </a>
</p>

---

## 👋 About Me

I am a Computer Engineering student and AI Engineer focused on building **LLM, RAG, Ai Agent and practical AI systems** that move beyond experiments into usable software.

My work covers the full path from **document ingestion and retrieval to grounded generation, APIs, user interfaces, testing, and deployment**.

I am also a **Co-Founder and Technical Lead at AI Builders**, where I contribute to the technical direction of the organization and lead the **LLM team** across RAG, LLM, and AI-agent projects.

My engineering background also includes **Machine Learning, Deep Learning, Computer Vision, and Data Science**, giving me experience working with both structured data and real-world unstructured inputs.

> **Build systems. Understand the trade-offs. Ship what works.**

---

## 🚀 What I Build

My main focus is practical AI engineering, particularly systems that connect models with real data and real users.

- **LLM Applications** — Turning foundation models into useful software products.
- **RAG Systems** — Building retrieval pipelines that ground model responses in trusted documents.
- **Document Intelligence** — Processing PDFs, DOCX, TXT, Markdown, and scanned documents.
- **AI Agents** — Exploring systems that can reason, retrieve information, and execute multi-step tasks.
- **Machine Learning & Data Science** — Building reliable ML pipelines and analytical applications.
- **AI Deployment** — Packaging AI systems behind APIs, interfaces, and containers.

---

## 🧠 RAG Engineering Journey

I intentionally build RAG systems in progressive levels.

Each project introduces a new retrieval concept rather than simply adding more technologies.

| Level | Project | Focus | Status |
|---|---|---|---|
| 1 | [**simple-pdf-rag**](https://github.com/HosseinHeydari2004/simple-pdf-rag) | End-to-end baseline RAG | ✅ Completed |
| 2 | [**SmartDocs-RAG**](https://github.com/HosseinHeydari2004/SmartDocs-RAG) | Metadata-aware retrieval & filtering | 🔨 Built |
| 3 | [**HybridDocs-RAG**](https://github.com/HosseinHeydari2004/HybridDocs-RAG) | Hybrid retrieval | 🚧 In Development |

### Level 1 — simple-pdf-rag

A practical baseline for asking questions over personal documents.

**Pipeline:**

`Documents → Chunking → Embeddings → ChromaDB → Retrieval → Grounded Answer`

Supports PDF, DOCX, TXT, and Markdown files with local embeddings, persistent ChromaDB storage, provider-independent LLM generation, source citations, Streamlit UI, and Docker Compose deployment.

**Stack:** Python · LangChain · ChromaDB · Streamlit · Docker

### Level 2 — SmartDocs-RAG

A more structured RAG architecture introducing **metadata-aware retrieval and filtering**.

The goal is to make retrieval more precise by allowing the system to use document metadata alongside semantic similarity.

**Stack:** Python · LangChain · Vector Database · Docker

### Level 3 — HybridDocs-RAG

The next stage of the retrieval pipeline, focused on combining different retrieval strategies to improve search quality across different query types.

**Status:** 🚧 In development

---

# 🔥 Applied LLM & RAG Systems

## 📚 ChemLib-AI

[**ChemLib-AI**](https://github.com/AI-Builders-Iran/ChemLib-AI) is an intelligent RAG assistant designed for a university chemistry library.

Instead of manually searching through books and documents, students and researchers can ask questions in **Persian or English** and receive answers grounded in the library's own content.

### Why it matters

The system is designed around a simple principle:

> **If the documents cannot support the answer, the system should not invent one.**

### Key capabilities

- 📄 **Multi-format ingestion** — Processes PDF, DOCX, TXT, and other document sources.
- 🔎 **Semantic retrieval** — Uses local BGE-M3 embeddings with ChromaDB for multilingual retrieval.
- 🖨️ **Scanned-document support** — Uses vision-based OCR when standard text extraction is insufficient.
- 🛡️ **Pre-generation grounding check** — Avoids unnecessary LLM calls when retrieved context is insufficient.
- 📚 **Source citations** — Answers can reference the underlying books and pages.
- 🔄 **LLM provider fallback** — Automatically switches from Gemini to OpenRouter when necessary.
- 👤 **Private document mode** — User documents remain session-scoped instead of being added to the shared knowledge base.
- ⚙️ **Admin management** — Administrators can add, replace, and remove shared documents.
- 🔀 **Cross-source comparison** — Supports comparing information across multiple sources.
- 🌐 **REST API** — Exposes functionality through FastAPI.
- 🧪 **Automated testing** — Includes mock-based pytest coverage.
- 🐳 **Containerized deployment** — Supports Docker-based execution.

**My contribution:** Technical Lead at AI Builders and LLM Team Lead, contributing to the design and development of the LLM/RAG system and its engineering workflow.

**Stack:** Python · RAG · LangChain · ChromaDB · BGE-M3 · Gemini · OpenRouter · FastAPI · Streamlit · Docker · Pydantic · pytest

---

## 🦺 IAI-001 Safety Monitoring System

[**IAI-001 Safety Monitoring System**](https://github.com/AI-Builders-Iran/IAI-001-Safety-Monitoring-System) connects Computer Vision, rule-based analysis, and LLM generation to transform workplace video events into management-ready HSE reports.

### Pipeline

`Video → YOLOv8 → ByteTrack → Rule Engine → Structured Alerts → Local LLM → HSE Report`

### Key capabilities

- 🎥 Detects relevant events from worksite video.
- 🧠 Converts visual observations into structured safety events.
- 📋 Uses a rule engine for deterministic safety logic.
- 🤖 Uses locally served Qwen2.5 for report generation.
- 🌍 Supports Persian and English reports.
- 🧩 Uses Jinja2 templates for controlled prompt generation.
- ⚡ Exposes the LLM reporting layer through FastAPI.

### My role

**LLM Team Lead**

I led the LLM workstream, including prompt engineering, local model inference with Hugging Face Transformers, Pydantic report schemas, and integration behind the API layer.

**Stack:** FastAPI · Docker Compose · Gradio · Qwen2.5 · Transformers · Jinja2 · Pydantic

---

# 🧪 Computer Vision & Medical AI

| Project | Description | Stack |
|---|---|---|
| [**Brain-MRI-Tumor-Analysis**](https://github.com/HosseinHeydari2004/Brain-MRI-Tumor-Analysis) | Two-stage MRI analysis pipeline combining classification and segmentation with visual overlays and downloadable reports. | PyTorch · OpenCV · FastAPI · Docker |
| [**medvision**](https://github.com/HosseinHeydari2004/medvision) | Open-source toolkit for detecting and correcting common MRI/CT imaging artifacts before model training. | MONAI · OpenCV |
| [**Data-Science-Laboratory**](https://github.com/HosseinHeydari2004/Data-Science-Laboratory) | Modular application for preprocessing, EDA, feature engineering, and machine-learning workflows. | scikit-learn · Streamlit |

---

# 🏗️ Engineering Principles

I care about more than simply making a model produce an answer.

Some engineering decisions I actively consider:

### 1. Refuse before generating

If retrieved context is not sufficiently relevant, there is little value in asking the LLM to guess.

A retrieval-quality check can therefore reduce **hallucinations, latency, and unnecessary model usage**.

### 2. Separate retrieval from generation

Embeddings and retrieval should remain independently testable from the generation layer.

This makes it easier to evaluate where an answer went wrong.

### 3. Prefer structured outputs

Pydantic models provide a predictable contract between the LLM and the rest of the application.

### 4. Design for provider failure

LLM APIs can fail.

Fallback providers can improve availability while keeping the user informed about what happened.

### 5. Treat user documents as a privacy boundary

Private documents should not automatically become part of a shared knowledge base.

### 6. Build progressively

Rather than adding technologies for their own sake, I prefer introducing new components when they solve a measurable engineering problem.

---

# 🛠️ Technology Stack

### LLM & RAG

<p>
  <img src="https://img.shields.io/badge/Python-3776AB?style=flat-square&logo=python&logoColor=white"/>
  <img src="https://img.shields.io/badge/LangChain-1C3C3C?style=flat-square"/>
  <img src="https://img.shields.io/badge/ChromaDB-FF6F61?style=flat-square"/>
  <img src="https://img.shields.io/badge/HuggingFace-FFD21E?style=flat-square&logo=huggingface&logoColor=black"/>
  <img src="https://img.shields.io/badge/Transformers-FFD21E?style=flat-square"/>
  <img src="https://img.shields.io/badge/Pydantic-E92063?style=flat-square&logo=pydantic&logoColor=white"/>
</p>

LangChain · ChromaDB · Gemini · OpenRouter · Hugging Face Transformers · Pydantic 

### Machine Learning & Computer Vision

<p>
  <img src="https://img.shields.io/badge/PyTorch-EE4C2C?style=flat-square&logo=pytorch&logoColor=white"/>
  <img src="https://img.shields.io/badge/TensorFlow-FF6F00?style=flat-square&logo=tensorflow&logoColor=white"/>
  <img src="https://img.shields.io/badge/Keras-D00000?style=flat-square&logo=keras&logoColor=white"/>
  <img src="https://img.shields.io/badge/OpenCV-5C3EE8?style=flat-square&logo=opencv&logoColor=white"/>
  <img src="https://img.shields.io/badge/scikit--learn-F7931E?style=flat-square&logo=scikit-learn&logoColor=white"/>
  <img src="https://img.shields.io/badge/MONAI-4B0082?style=flat-square"/>
</p>

PyTorch · TensorFlow · Keras · OpenCV · scikit-learn · MONAI

### Backend & Deployment

<p>
  <img src="https://img.shields.io/badge/FastAPI-009688?style=flat-square&logo=fastapi&logoColor=white"/>
  <img src="https://img.shields.io/badge/Docker-2496ED?style=flat-square&logo=docker&logoColor=white"/>
  <img src="https://img.shields.io/badge/Git-F05032?style=flat-square&logo=git&logoColor=white"/>
  <img src="https://img.shields.io/badge/SQL-4479A1?style=flat-square&logo=sqlite&logoColor=white"/>
</p>

FastAPI · Docker · Docker Compose · Streamlit · Gradio · pytest · Git · uv · SQL

---

# 👨‍💻 Leadership & AI Builders

## AI Builders

[**AI Builders**](https://github.com/AI-Builders-Iran) is an open-source AI engineering organization focused on building practical systems across **LLM, RAG, AI Agents, Computer Vision, and MLOps**.

### My role

**Co-Founder & Technical Lead**

I contribute to the organization's technical direction, architecture, engineering practices, and development of AI systems.

**LLM Team Lead**

I lead the LLM-focused team working on **LLM applications, RAG pipelines, AI agents, and production-oriented AI workflows**.

My responsibilities include:

- Technical direction and architecture
- LLM/RAG system design
- Technical coordination across projects
- Code and repository review
- Supporting engineering teams
- Leading LLM project development
- Turning AI concepts into working software

> My focus is not only on building models, but on building the systems around them that make AI useful, testable, and deployable.


---

# 📬 Contact

If you are interested in **AI engineering, LLM/RAG systems, collaboration, research, or building practical AI products**, feel free to reach out.

- **GitHub:** [HosseinHeydari2004](https://github.com/HosseinHeydari2004)
- **LinkedIn:** [Hossein Heydari](https://www.linkedin.com/in/hossein-heydari2004)
- **Kaggle:** [mrhosseinheydari](https://www.kaggle.com/mrhosseinheydari)
- **Email:** hosseinheydari992020@gmail.com
- **Telegram:** [@Hossein_h830](https://t.me/Hossein_h830)

---

<p align="center">
  <i>Build deeply. Lead responsibly. Ship useful AI.</i>
</p>
