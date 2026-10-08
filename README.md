<h1 align="center">Hossein Heydari</h1>
<p align="center"><b>Junior AI Engineer · LLM & RAG Systems · Computer Vision</b><br/>
Co-Founder & Technical Lead @ <a href="https://github.com/AI-Builders-Iran">AI Builders Iran</a></p>

<p align="center">
  <a href="https://www.linkedin.com/in/hossein-heydari2004"><img src="https://img.shields.io/badge/LinkedIn-0A66C2?style=for-the-badge&logo=linkedin&logoColor=white"/></a>
  <a href="https://www.kaggle.com/mrhosseinheydari"><img src="https://img.shields.io/badge/Kaggle-20BEFF?style=for-the-badge&logo=kaggle&logoColor=white"/></a>
  <a href="mailto:hosseinheydari992020@gmail.com"><img src="https://img.shields.io/badge/Email-D14836?style=for-the-badge&logo=gmail&logoColor=white"/></a>
  <a href="https://t.me/Hossein_h830"><img src="https://img.shields.io/badge/Telegram-0088CC?style=for-the-badge&logo=telegram&logoColor=white"/></a>
</p>

---

## 👋 About

Computer Engineering (Software) student building **RAG and LLM systems that run end to end**: document ingestion (including scanned PDFs), retrieval, source-grounded answers, an API, a UI, and a container to ship it in.

My background is classical computer vision (OpenCV) and deep learning, so I'm comfortable with the messy input side of AI systems and with putting a model behind a real service. Long-term goal: found an AI company.

**How I learn RAG:** I build it in levels. Each project adds exactly one new concept on top of the previous one, so I understand why every component exists (see the ladder below).

---

## 🪜 The RAG Ladder: one concept per project

| Level | Project | New concept it adds | Status |
|---|---|---|---|
| 1 | [**simple-pdf-rag**](https://github.com/HosseinHeydari2004/simple-pdf-rag) | The baseline: load → chunk → embed → store → retrieve top-k → grounded answer | ✅ Done |
| 2 | [**SmartDocs-RAG**](https://github.com/HosseinHeydari2004/SmartDocs-RAG) | **Metadata-aware retrieval and filtering** | 🔨 Built |
| 3 | [**HybridDocs-RAG**](https://github.com/HosseinHeydari2004/HybridDocs-RAG) | **Hybrid retrieval** | 🚧 In development |

<!-- TODO (Level 3): the repo is EMPTY right now. Push a README + first commit BEFORE publishing this profile and replace "Hybrid retrieval" with exactly what you implemented (which retrievers, how you fuse/rerank). If nothing is pushed yet, delete this row. -->
<!-- TODO (Level 2): the SmartDocs-RAG README did not render when reviewed. Add: which vector DB, which metadata fields you filter on, one example query + result. -->

### Level 1 — [simple-pdf-rag](https://github.com/HosseinHeydari2004/simple-pdf-rag)
Upload PDF/DOCX/TXT/Markdown and chat with them; answers come only from your files, and the app says so when it doesn't know. Recursive chunking, local `bge-small-en-v1.5` embeddings, persisted **ChromaDB**, provider-agnostic LLM layer (**Gemini** primary, **OpenRouter** fallback), **Streamlit** chat UI with source citations, one-command **Docker Compose** run.
`Python` `LangChain` `ChromaDB` `Streamlit` `Docker`

### Level 2 — [SmartDocs-RAG](https://github.com/HosseinHeydari2004/SmartDocs-RAG)
Metadata-aware RAG for document retrieval, filtering and source-grounded question answering, built with **LangChain** and a vector database, with a Dockerfile for reproducible runs.
`Python` `LangChain` `Vector DB` `Docker`

### Level 3 — [HybridDocs-RAG](https://github.com/HosseinHeydari2004/HybridDocs-RAG) *(in development)*
Next step up from SmartDocs-RAG.

---

## 🔥 Applied LLM / RAG Systems

### 📚 [ChemLib-AI](https://github.com/AI-Builders-Iran/ChemLib-AI) — RAG assistant for a university chemistry library
*(formerly DocumentAI · AI Builders Iran · built as a demo for a university chemistry faculty)*

A student asks a scientific question in Persian or English; the answer comes **from the library's own books, with book and page citations**, and the system says "not enough information" instead of guessing.

- **Ingestion:** PDF/DOCX/TXT → cleaning → chunking → **BGE-M3** embeddings (local) → **ChromaDB**; scanned pages are read with **Gemini Vision OCR**
- **Grounded generation:** a similarity-threshold check runs *before* the LLM call, so irrelevant questions get a fixed refusal with no LLM spend; answers return validated **Pydantic** models and only the chunks the model actually used are shown as sources
- **Reliability:** automatic **Gemini → OpenRouter fallback** with a visible notice to the user
- **Product features:** session-only "My documents" mode (never written to the shared DB), admin panel to add/replace/remove books, cross-source **compare** endpoint, REST API (**FastAPI**), right-to-left Persian **Streamlit** UI, **Docker**, mock-based **pytest** suite
- **Also in the repo:** the original structured-extraction pipeline (invoice/contract → validated JSON)

`Python` `RAG` `ChromaDB` `BGE-M3` `Gemini` `OpenRouter` `FastAPI` `Streamlit` `Docker` `pytest`
<!-- TODO: add 1 line on YOUR part (e.g., "I built retrieval + the grounding threshold + tests") and 1 real result (users/queries tested, demo link) -->

### 🦺 [IAI-001 Safety Monitoring System](https://github.com/AI-Builders-Iran/IAI-001-Safety-Monitoring-System) — CV → rules → LLM reports
Worksite video in, management-ready HSE report out. YOLOv8 + ByteTrack feed a rule engine, and a **locally served Qwen2.5** model turns structured alerts into Persian/English daily and weekly reports through Jinja2 prompt templates.
**My role: Lead of the LLM workstream** (prompt engine, local inference with Hugging Face Transformers, Pydantic report schemas, integration behind FastAPI).
`FastAPI` `Docker Compose` `Gradio` `Qwen2.5` `Transformers` `Jinja2`
<!-- TODO: link your PRs / LLM/ folder and one concrete result (how you checked report accuracy) -->

---

## 🎤 Design decisions I can defend (ask me about these)

Each of these is a real trade-off from the projects above:

1. **Refuse before you generate.** In ChemLib-AI, a cheap similarity-threshold check decides whether to call the LLM at all. Why: cost, latency, and the best hallucination fix is not asking the model a question the context can't answer.
2. **Local embeddings, hosted generation.** Embeddings run locally (BGE-M3 for multilingual/Persian in ChemLib-AI, bge-small in the baseline); only generation touches an API.
3. **OCR trade-off.** Tesseract, RapidOCR and PaddleOCR-VL were evaluated for scanned Persian pages and didn't reach acceptable quality or speed; Gemini Vision is used only for pages where digital text extraction fails, which keeps API cost bounded.
4. **Structured outputs over regex parsing.** Answers come back as validated Pydantic models, and the model lists the chunk ids it used, so shown sources are the ones that actually supported the answer.
5. **Provider fallback with transparency.** If the primary LLM fails, the request retries on a second provider and the user is told which model answered.
6. **Privacy boundary for user files.** Session-only documents live in memory and never touch the shared vector store.
7. **Why a ladder.** Adding one concept per project (baseline → metadata filtering → hybrid retrieval) lets me explain what each piece changes in retrieval behavior instead of stacking features blindly.
<!-- TODO: be ready to say which of these YOU designed vs. the team (items 1-6 are from ChemLib-AI, a team project). Interviewers will ask "which part was yours?" -->

**Known gaps I'm working on:** single-turn chat (no follow-up rewriting), tuning the similarity threshold and chunk size on a larger corpus, reranking, and per-user admin accounts.

---

## 👁️ Computer Vision & Medical AI

| Project | What it is | Stack |
|---|---|---|
| [**Brain-MRI-Tumor-Analysis**](https://github.com/HosseinHeydari2004/Brain-MRI-Tumor-Analysis) | Two-stage MRI pipeline: ResNet34 classification, then ResNet34 + UNet3+-style segmentation with bounding boxes, overlays and downloadable reports. Served via FastAPI + Streamlit + Docker. | PyTorch, OpenCV, FastAPI, Docker |
| [**medvision**](https://github.com/HosseinHeydari2004/medvision) | Open-source library for detecting and correcting MRI/CT artifacts (noise, bias field, contrast, motion) before model training. *In progress.* | MONAI, OpenCV |
| [**Data-Science-Laboratory**](https://github.com/HosseinHeydari2004/Data-Science-Laboratory) | Modular Streamlit app covering preprocessing, EDA, feature engineering and model training in one workflow. | scikit-learn, Streamlit |

---

## 🧑‍💼 Leadership

**Co-Founder & Technical Lead, AI Builders Iran** — an open-source AI engineering organization building production-grade Computer Vision, LLM, RAG and AI agent systems.

- **Co-Founder:** helped start the organization and shape its direction
- **Technical Lead:** I own technical operations and the organization's GitHub, make architecture decisions, and review code through pull requests
- **Team Lead, LLM / RAG / AI Agents:** I lead the team that builds the organization's LLM, RAG and agent projects, including the LLM workstream on IAI-001 and the RAG work on ChemLib-AI
<!-- TODO: add 1-2 concrete facts that prove this: team size, number of projects shipped, PR-review process, a repo where your reviews/PRs are visible. For "AI Agents": link the repo/PR that shows an agent you built or led, otherwise interviewers will ask for it -->



---

## 🛠 Tech Stack

**LLM / RAG:** LangChain · ChromaDB · BGE-M3 & bge-small / sentence-transformers · Gemini & OpenRouter APIs · Hugging Face Transformers · Qwen2.5 (local inference) · Pydantic structured outputs · Jinja2 prompt templating
**ML / CV:** Python · PyTorch · OpenCV · scikit-learn · YOLOv8 · MONAI
**Serving & tooling:** FastAPI · Docker / Docker Compose · Streamlit · Gradio · pytest · Git · uv

<sub>Going deeper: reranking, RAG evaluation, agent frameworks (LangGraph) and agent evaluation. I only list tools I have shipped something with.</sub>

---

## 🎯 What I'm looking for

A **Junior AI / LLM Engineer** role (or internship) on a team building RAG or agent products, where I can own a pipeline from retrieval quality to deployment.

<p align="center"><i>Learn deeply. Build consistently. Ship things that work.</i></p>
