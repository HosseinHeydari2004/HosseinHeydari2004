<h1 align="center">Hossein Heydari</h1>

<p align="center">
  <strong>AI Engineer · LLM, RAG & Agentic Systems · Computer Vision</strong>
</p>

<p align="center">
  Co-Founder & Technical Lead at Vexonova · LLM Team Lead
</p>

<p align="center">
  I build AI systems that turn documents, code, and visual data into grounded, observable, deployable products.
</p>

<p align="center">
  <a href="https://github.com/HosseinHeydari2004"><img src="https://img.shields.io/badge/GitHub-181717?style=for-the-badge&logo=github&logoColor=white" alt="GitHub" /></a>
  <a href="https://www.linkedin.com/in/hossein-heydari2004"><img src="https://img.shields.io/badge/LinkedIn-0A66C2?style=for-the-badge&logo=linkedin&logoColor=white" alt="LinkedIn" /></a>
  <a href="https://www.kaggle.com/mrhosseinheydari"><img src="https://img.shields.io/badge/Kaggle-20BEFF?style=for-the-badge&logo=kaggle&logoColor=white" alt="Kaggle" /></a>
  <a href="mailto:hosseinheydari992020@gmail.com"><img src="https://img.shields.io/badge/Email-D14836?style=for-the-badge&logo=gmail&logoColor=white" alt="Email" /></a>
  <a href="https://t.me/Hossein_h830"><img src="https://img.shields.io/badge/Telegram-0088CC?style=for-the-badge&logo=telegram&logoColor=white" alt="Telegram" /></a>
</p>

---

## About me

I am a Computer Engineering student and AI Engineer focused on building reliable AI software—not isolated model demos. My work spans document ingestion, retrieval, grounded generation, agent workflows, APIs, testing, and containerized deployment.

At **Vexonova**, I help shape technical direction and lead the LLM workstream across RAG, LLM applications, and AI-agent systems. My background in machine learning, computer vision, and data science helps me work across structured data, documents, images, and real operational constraints.

> **Build deeply. Measure honestly. Ship useful AI.**

## What I build

- **RAG systems** — retrieval pipelines with citations, refusal behavior, evaluation, and document lifecycle considerations.
- **Document intelligence** — PDF, DOCX, Markdown, source code, web content, OCR, and Persian/English documents.
- **Agentic systems** — bounded tool use, routing, retrieval agents, GitHub-aware workflows, and human-controlled actions.
- **Applied LLM products** — structured outputs, provider fallbacks, APIs, user interfaces, and Dockerized services.
- **Computer vision & medical AI** — practical image-analysis pipelines and model-serving workflows.

## Featured work

### [TeamDocs AI](https://github.com/HosseinHeydari2004/TeamDocs-AI) — Agentic engineering knowledge assistant

An AI assistant for teams to search their documents and inspect GitHub repositories, issues, and pull requests with verifiable sources.

- Hybrid retrieval: dense embeddings + BM25, fused with weighted reciprocal-rank fusion.
- Ingests PDF, DOCX, PPTX, Markdown, text, source code, and approved web pages.
- Main agent routes requests to RAG and read-only GitHub agents; runs are bounded by tool-call, recursion, and timeout limits.
- Citations, insufficient-evidence responses, incremental indexing, model fallback, FastAPI, Docker Compose, and a browser UI.
- Security-minded design: SSRF-safe URL import, secret handling, read-only GitHub tools, and untrusted-content treatment.
- Evaluation artifacts and a pytest suite cover retrieval, ingestion, configuration, agents, APIs, and web loading.

**Current focus:** improving retrieval quality with measured experiments, reranking, and regression evaluation rather than adding features blindly.

**Stack:** Python · FastAPI · LangChain · ChromaDB · BM25 · OpenRouter · Ollama · GitHub MCP · Docker · pytest · DeepEval

### [ChemLib AI](https://github.com/AI-Builders-Iran/ChemLib-AI) — Multilingual library RAG

A document-intelligence assistant for a university chemistry library. Students can ask Persian or English questions over the library’s own documents and receive grounded answers with book and page citations.

- Handles digital and scanned documents through extraction plus OCR fallback.
- Uses local BGE-M3 embeddings and persistent ChromaDB storage.
- Refuses before generation when retrieval evidence is insufficient.
- Supports document-scoped chat, cross-source comparison, private session documents, and library-admin ingestion workflows.
- Includes structured extraction, provider fallback, FastAPI, Docker, pytest, and a RAGAS evaluation workflow.

**My contribution:** LLM Team Lead; contributing to the LLM/RAG architecture, engineering workflow, structured outputs, and application integration.

**Stack:** Python · LangChain · BGE-M3 · ChromaDB · OCR · FastAPI · NiceGUI · OpenRouter · Pydantic · pytest · Docker · RAGAS

### [SmartDocs-RAG](https://github.com/HosseinHeydari2004/SmartDocs-RAG) — Metadata-aware document search

A deployable document RAG application that combines semantic search with metadata-aware filtering. It supports OCR for scanned Persian and English documents, local embeddings, persistent indexing, a FastAPI backend, Streamlit UI, Docker, and tests for ingestion and API behavior.

**Stack:** Python · FastAPI · Streamlit · LangChain · ChromaDB · sentence-transformers · Tesseract · Docker · pytest

### [simple-pdf-rag](https://github.com/HosseinHeydari2004/simple-pdf-rag) — Clean RAG baseline

A compact end-to-end RAG application for PDF, DOCX, TXT, and Markdown. It demonstrates the essentials clearly: loading, chunking, local embeddings, persistent vector search, grounded answers with source citations, provider-agnostic generation, Streamlit, FastAPI, and Docker Compose.

### [RAG: From Zero to Advanced](https://github.com/HosseinHeydari2004/RAG-Tutorial-From-Zero-to-Advanced) — Engilish/Persian-first learning path

An open, hands-on tutorial series that progresses from first-principles RAG to ingestion, cleaning, metadata, chunking, embeddings, vector databases, indexing, and retrieval. The next modules focus on evaluation, hybrid retrieval, reranking, agentic RAG, and production systems.

## RAG engineering progression

| Stage | Project | Engineering focus |
|---|---|---|
| Foundation | [simple-pdf-rag](https://github.com/HosseinHeydari2004/simple-pdf-rag) | End-to-end RAG, citations, UI, API, and Docker |
| Retrieval control | [SmartDocs-RAG](https://github.com/HosseinHeydari2004/SmartDocs-RAG) | Metadata-aware filtering and OCR-aware ingestion |
| Domain application | [ChemLib AI](https://github.com/AI-Builders-Iran/ChemLib-AI) | Multilingual, OCR, refusal logic, admin workflows, and evaluation |
| Advanced retrieval & agents | [TeamDocs AI](https://github.com/HosseinHeydari2004/TeamDocs-AI) | Hybrid retrieval, agent routing, GitHub MCP, security, and evaluation |

## Engineering principles

1. **Retrieve before generating.** If the evidence is weak, the system should say so instead of guessing.
2. **Measure retrieval separately from generation.** A good-looking answer can still be based on poor retrieval.
3. **Make outputs structured.** Pydantic schemas turn LLM responses into reliable application contracts.
4. **Treat external content as untrusted.** Documents, web pages, and tool results are data—not instructions.
5. **Bound agent behavior.** Tool limits, timeouts, scoped permissions, and user approval matter more than unconstrained autonomy.
6. **Build incrementally.** Add complexity only when it solves a measurable product or reliability problem.

## AI-agent direction

I am expanding from RAG systems into reliable AI-agent engineering. My focus is on workflow-first agents that can retrieve, reason, use scoped tools, and report their work transparently—not agents that act without controls.

Areas I am actively developing:

- Agent routing and multi-agent coordination
- Tool design, permission boundaries, and human-in-the-loop approvals
- Stateful workflows, retries, timeouts, and idempotent operations
- Tracing, evaluation, and failure analysis for agent systems
- Retrieval quality improvements: reranking, query transformation, and regression testing

## Applied AI beyond RAG

| Project | Description | Stack |
|---|---|---|
| [Brain-MRI-Tumor-Analysis](https://github.com/HosseinHeydari2004/Brain-MRI-Tumor-Analysis) | Deep-learning MRI tumor analysis with an interactive web interface and deployment-oriented workflow. | PyTorch · OpenCV · FastAPI · Docker |
| [MedArtifact](https://github.com/HosseinHeydari2004/MedArtifact) | Toolkit for detecting and correcting common MRI/CT image artifacts before model training. | MONAI · OpenCV |
| [Data-Science-Laboratory](https://github.com/HosseinHeydari2004/Data-Science-Laboratory) | Modular application for preprocessing, EDA, feature engineering, training, and evaluation. | scikit-learn · Streamlit |
| [IAI-001 Safety Monitoring System](https://github.com/AI-Builders-Iran/IAI-001-Safety-Monitoring-System) | Computer-vision-to-LLM system for structured workplace HSE reporting. | YOLOv8 · Qwen2.5 · FastAPI · Docker · Gradio |

## Technology

**LLM, RAG & agents:** Python · LangChain · ChromaDB · BM25 · BGE-M3 · Hugging Face · OpenRouter · Ollama · GitHub MCP · Pydantic · DeepEval · RAGAS

**Backend & delivery:** FastAPI · Streamlit · NiceGUI · Gradio · Docker · Docker Compose · pytest · Git · SQL

**Machine learning & vision:** PyTorch · TensorFlow · Keras · OpenCV · scikit-learn · MONAI

## Leadership

### Vexonova

At Vexonova, I contribute to technical direction, system architecture, repository review, engineering practice, and delivery across LLM/RAG, agentic AI, computer vision, and applied AI products.

As **LLM Team Lead**, I focus on turning model capabilities into reliable software: designing retrieval systems, defining integration boundaries, supporting team implementation, and guiding projects from prototype to deployable product.

## Contact

- GitHub: [HosseinHeydari2004](https://github.com/HosseinHeydari2004)
- LinkedIn: [Hossein Heydari](https://www.linkedin.com/in/hossein-heydari2004)
- Kaggle: [mrhosseinheydari](https://www.kaggle.com/mrhosseinheydari)
- Email: [hosseinheydari992020@gmail.com](mailto:hosseinheydari992020@gmail.com)
- Telegram: [@Hossein_h830](https://t.me/Hossein_h830)

<p align="center"><i>Build deeply. Measure honestly. Ship useful AI.</i></p>
