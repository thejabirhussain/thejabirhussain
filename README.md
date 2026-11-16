# Mohammed Jabir Hussain Shaik

MSc Artificial Intelligence, Queen's University Belfast · AI engineer

I ship AI systems into production, and I measure whether they deserve to be trusted. Those are the same job done twice: building a system at scale is how I find the failure that is worth studying, and studying it properly changes what I build next. The work below is split that way — what I measured, and what I shipped — because neither half is interesting without the other.

---

## Research

**Character accuracy conceals numerical error** — [code](https://github.com/thejabirhussain/silent-corruption-clinical-ai) · preprint under screening at Research Square

I built a retrieval-based clinical decision support system, then measured it on the kind of document photographs real clinics produce. At 100 dpi, character accuracy was still **88.9%** — the figure a standard OCR benchmark reports — while **32.3% of extracted laboratory values were wrong**. Of those corrupted values, **47.3% carried the same abnormality flag as the truth**, so the error passed the alerting layer unseen.

The point isn't that OCR is imperfect. It's that the metric everyone reports cannot see the failure that matters, and thresholding hides it rather than catching it. Presented as a poster at the Vision and Language Symposium, Queen's University Belfast, October 2026.

**Does predictive multiplicity grow as the training set shrinks?** — [code](https://github.com/thejabirhussain/multiplicity-small-n) · manuscript in preparation

Models that score identically can still disagree about which individual patients they flag. Every study I could find measures this at one fixed sample size. Across **30 public datasets**, holding the size of the near-optimal model set fixed, disagreement was higher at the smallest training size than the largest in **28 of them**.

My first design was confounded: the ε-ball rule standard in the literature admits a number of models that itself varies with *n*. Finding that out was worth more than the result, and it implies published ambiguity figures aren't comparable across papers unless Rashomon set size is reported — which it usually isn't. The failed design is in the repository alongside the one that worked.

---

## Shipped

Production work as an AI engineer at XIT Solutions, and for its clients through AxeGenAI.

**A real-time voice tutor** teaching English to Urdu-speaking schoolchildren, for Developing in Literacy, Pakistan. The hard bug was not the model: the Gemini Live path never signalled end of turn, so roughly **27% of conversational turns timed out**. Diagnosing and fixing it took that to **zero**. I then rebuilt voice-activity detection with adaptive thresholds and validated it against **100+ simulated room profiles**, because a classroom in Karachi is not a recording studio. Shipped to the Play Store on Android 16.

**A multi-agent workflow system** for a US real-estate group. A transaction event triggers router, asset and template agents on Azure AI Foundry, which fill Canva templates, store the renders, create Publer drafts and notify staff in Teams. Runs end to end across both residential and commercial divisions.

**Document intelligence for financial records** — scanned Arabic PDFs to English with layout preserved, built entirely on open models (OCRmyPDF/Tesseract, Helsinki-NLP opus-mt) so nothing leaves the customer's infrastructure. This pipeline is where I first saw numerically wrong output that looked perfectly correct, which became the research above.

**TRACE**, an agentic SDLC framework I designed at management's request: one agent per lifecycle stage, Azure DevOps as the state machine, schema-checked handoffs and three human approval gates. Tests are written before the code and blind to it, so a passing test is independent evidence rather than a tautology. Backed by a 164-page sourced review of industry practice.

---

## Open source

| Project | What it actually does | Stack |
|---|---|---|
| [**AI Clinical Decision Support**](https://github.com/thejabirhussain/AI-CLINICAL-DECISION-SUPPORT-SYSTEM) | 11,000 MedQuAD passages in Qdrant (HNSW). 40 candidates retrieved, similarity-filtered, cross-encoder reranked to 3; **every answer cites its sources, and it abstains** when nothing clears the cutoff rather than answering from memory. Runs fully local, so patient documents never leave the machine | FastAPI · Qdrant · Llama 3.2 · React |
| [**Autonomous QA Intelligence (ReQon)**](https://github.com/thejabirhussain/Autonomous_QA_Intelligence_Platform) | Self-driving crawler running **29 defect detectors** across functional, UI, performance, accessibility, SEO and security; an LLM pass removes false positives and a Neo4j graph links pages, features and defects | FastAPI · Neo4j · Playwright · Celery |
| [**Enterprise AI Copilot**](https://github.com/thejabirhussain/Enterprise-AI-Copilot) | RAG where **retrieval itself is filtered by each user's access level** — not just the answer. Request audit logging, streamed responses, and a step-by-step trace of the retrieval pipeline. No API keys anywhere | FastAPI · Qdrant · Ollama · TypeScript |
| [**Arabic → English OCR**](https://github.com/thejabirhussain/ARABIC-ENGLISH-OCR) | Layout-preserving Arabic OCR over scanned PDFs, then neural translation — **entirely open models** | Tesseract · opus-mt · FastAPI |
| [**Legal Intake Platform**](https://github.com/thejabirhussain/legal-intake-platform) | WhatsApp Cloud API state machine gathering client, case and incident details; switches between GPT-4 and a local model; feeds a lawyer dashboard with AI case summaries | Python · Meta Cloud API |
| [**Imaginary Hub AI Labs**](https://github.com/thejabirhussain/Imaginary-Hub-AI-Labs) | The curriculum I teach from — e.g. PCA implemented from scratch in NumPy and checked against scikit-learn | Python · NumPy |

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

I founded [**Imaginary Hub**](https://www.youtube.com/@ImaginaryHub) in my second undergraduate year and have taught AI and computer science through it since: **6,000+ learners**, **1,600+ students** trained through government-partnered programmes, 10+ workshops in schools and colleges, and **148 videos** on mathematics for ML, LLM internals and system design. I also built the platform it runs on (React, Node.js, MongoDB, AWS, payments, video delivery).

I keep doing it because explaining something clearly is the fastest way to find out whether you actually understand it.

---

[Google Scholar](https://scholar.google.com/citations?user=f4gX2kgAAAAJ) · [LinkedIn](https://www.linkedin.com/in/thejabirhussain) · `mshaik01@qub.ac.uk`

*Belfast, Northern Ireland*
