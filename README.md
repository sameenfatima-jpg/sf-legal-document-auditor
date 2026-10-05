# sf-legal-document-auditor
An AI-assisted parsing engine for Australian RMBS and ABS Information Memorandums built with strict credit risk data governance guardrails.
# AI-Assisted Structured Finance Legal Document Auditor

## 📌 Project Overview
This project is an open-source, prototype analytical engine designed to automate the structural review of **Australian Residential Mortgage-Backed Securities (RMBS)** and **Asset-Backed Securities (ABS)** Information Memorandums. 

By leveraging a Retrieval-Augmented Generation (RAG) framework paired with large language models, this tool automatically extracts critical credit triggers, subordination structures, and structural risks from 300+ page legal transaction documents.

---

## 🔒 Credit Risk Data Governance Guardrails
Designed explicitly to mirror institutional compliance standards and S&P Global's core value of **Responsible AI use**, this system eliminates reliance on LLM creativity by enforcing three strict architectural guardrails:

*   **Deterministic Output Framework:** Configured with a temperature of `0.0` to force rigid, rule-based data extraction and completely prevent model hallucinations.
*   **Traceable Source Citations:** The engine maps structural variables directly to physical anchors in the raw string, outputting the exact page number and text quote for seamless validation.
*   **Human-in-the-Loop Integration:** Built fundamentally as an analytical enabler rather than an automated decision-maker, requiring human verification and sign-off before outputs can be utilized.

---

## 🛠️ Core Analytical Capabilities
The model scans and audits transaction documents for the following Australian market parameters:
*   **Clean-up Call Options:** Validates the outstanding pool percentage threshold allowing early redemption.
*   **Sequential Pay Triggers:** Identifies specific cumulative loss or 90+ day delinquency thresholds that shift the deal from pro-rata allocation to sequential notes payoff.
*   **Commingling & Servicer Risks:** Evaluates transaction structures for backup servicer names and operational transition timelines.
*   **Credit Enhancement Mapping:** Structures baseline credit support and subordination layers across all tranches (Class A through Equity).

---

## 🚀 Technical Architecture & Stack
*   **Language:** Python
*   **Document Ingestion:** PyPDF (Preserves string-mapping data)
*   **Orchestration:** Google GenAI SDK (Interfaced via Gemini 1.5 Flash)
*   **Database (Planned Front-End):** ChromaDB local vector storage & Streamlit UI dashboard framework
