# Mohammed Jabir Hussain Shaik

MSc Artificial Intelligence, Queen's University Belfast · AI engineer

I build AI systems that run in production — retrieval-augmented generation, clinical decision support, document understanding, autonomous testing — and I measure whether they can be trusted. Those two halves feed each other: building a system is how I find the failure worth studying, and studying it changes what I build next.

---

## Research

**Character accuracy conceals numerical error** — [code](https://github.com/thejabirhussain/silent-corruption-clinical-ai) · preprint under screening at Research Square

I built a retrieval-based clinical decision support system, then measured it on the kind of document photographs real clinics produce. At 100 dpi, character accuracy was still **88.9%** — the figure a standard OCR benchmark reports — while **32.3% of extracted laboratory values were wrong**. Of those corrupted values, **47.3% carried the same abnormality flag as the truth**, so the error passed the alerting layer unseen.

The point isn't that OCR is imperfect. It's that the metric everyone reports cannot see the failure that matters, and thresholding hides it rather than catching it. Presented as a poster at the Vision and Language Symposium, Queen's University Belfast, October 2026.

**Does predictive multiplicity grow as the training set shrinks?** — [code](https://github.com/thejabirhussain/multiplicity-small-n) · manuscript in preparation

Models that score identically can still disagree about which individual patients they flag. Every study I could find measures this at one fixed sample size. Across **30 public datasets**, holding the size of the near-optimal model set fixed, disagreement was higher at the smallest training size than the largest in **28 of them**.

My first design was confounded: the ε-ball rule standard in the literature admits a number of models that itself varies with *n*. Finding that out was worth more than the result, and it implies published ambiguity figures aren't comparable across papers unless Rashomon set size is reported — which it usually isn't. The failed design is in the repository alongside the one that worked.

---

## What I build

| Project | What it is | Stack |
|---|---|---|
| [**AI Clinical Decision Support**](https://github.com/thejabirhussain/AI-CLINICAL-DECISION-SUPPORT-SYSTEM) | RAG service and clinical dashboard returning **verifiable citations** from trusted medical guidelines for every answer, with OCR-based patient data ingestion | FastAPI · Qdrant · React |
| [**Autonomous QA Intelligence (ReQon)**](https://github.com/thejabirhussain/Autonomous_QA_Intelligence_Platform) | Self-driving crawler running 20+ detectors across functional, UI, performance, accessibility, SEO and security; LLM-based false-positive elimination and a **knowledge graph** of defects | FastAPI · Neo4j · React |
| [**Enterprise AI Copilot**](https://github.com/thejabirhussain/Enterprise-AI-Copilot) | Production-grade RAG platform with semantic search, role-based access control and data governance, on a **fully local LLM stack** | FastAPI · Qdrant · Ollama · TypeScript |
| [**Arabic → English OCR**](https://github.com/thejabirhussain/ARABIC-ENGLISH-OCR) | Arabic OCR over scanned PDFs with layout preservation, then neural translation — **entirely open models, no API keys** | Tesseract · Helsinki-NLP opus-mt · FastAPI |
| [**Legal Intake Platform**](https://github.com/thejabirhussain/legal-intake-platform) | WhatsApp-based client intake with AI triage and a workflow dashboard for legal professionals | Python · Meta Cloud API |
| [**Imaginary Hub AI Labs**](https://github.com/thejabirhussain/Imaginary-Hub-AI-Labs) | Open AI curriculum I write and teach: mathematical foundations alongside production engineering builds | Python · Markdown |

---

## What I'm reading and thinking about

**AI for health.** Most of the difficulty in clinical AI isn't the model. It's fragmented patient records, missing labels, and the fact that a recommendation is worthless unless a clinician can see why it was made. I'm interested in multimodal and self-supervised models for decision support — systems that make assessment and planning faster and better evidenced, rather than systems that try to replace clinical judgement.

**World models and spatial intelligence.** Language models are remarkable on text and close to helpless in three dimensions; they have no grounded representation of space, position or movement. Models that can simulate and navigate the physical world seem to me the more interesting frontier, and the one robotics, autonomous systems and surgical technology all depend on.

**Foundations.** Linear algebra, probability and optimisation read properly rather than skimmed — most engineering intuitions about deep learning turn out to be downstream of a handful of theorems.

**Evaluation.** The thread running through both studies above: a headline metric that moves in the right direction while the thing you actually care about gets worse. I'd like to get better at designing evaluations that can fail honestly.

---

## Skills

**Machine learning** — PyTorch · transformers · RAG architectures · vector databases (Qdrant) · embeddings and semantic search · OCR pipelines · LLM evaluation · experiment design

**Engineering** — Python · TypeScript · FastAPI · React · Node.js · Neo4j · MongoDB · Docker · REST APIs

**Mathematics** — linear algebra · probability & statistics · optimisation · information theory

**Currently learning** — knowledge representation and ontology engineering · knowledge graphs with LLMs · computer vision · multimodal foundation models

---

## Teaching

I run [**Imaginary Hub**](https://www.youtube.com/@ImaginaryHub), where I teach AI and computer science to students in India — free, structured, and built on the idea that explaining something clearly is the fastest way to understand it yourself.

---

[Google Scholar](https://scholar.google.com/citations?user=f4gX2kgAAAAJ) · [LinkedIn](https://www.linkedin.com/in/thejabirhussain) · `mshaik01@qub.ac.uk`

*Belfast, Northern Ireland*
