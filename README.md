# Automated SaaS Customer Ticket Routing Pipeline

An automated backend data pipeline that ingests unstructured customer support text logs, maps them into high-dimensional vector spaces, clusters them into specialized engineering domains, and applies algorithmic triage logic to produce structured JSON webhooks.

## System Architecture Overview

The system processes incoming unstructured telemetry through four major layers:

1. **Ingestion & Sanitization:** Streams data directly via the Hugging Face API, structures the raw fields into an enterprise database layout, and strips structural formatting irregularities in-place to ensure absolute index alignment.
2. **Semantic Representation:** Leverages a GPU-accelerated dense vector encoder (`all-MiniLM-L6-v2`) to transform chaotic string records into 384-dimensional numerical feature spaces in parallel.
3. **Unsupervised Partitioning:** Evaluates structural variance using K-Means and an Elbow Curve optimization matrix to segment text clusters into four core operational company domains.
4. **Contextual Tag Extraction:** Utilizes KeyBERT with bounded N-Gram constraints to extract multi-word technical phrases directly from the complaints.
5. **Deterministic Triage Logic:** Computes a composite priority value (1–100) based on input text length metrics, explicit high-risk string triggers, and core domain premiums.
6. **Confidence Guardrails & SLA Gateway:** Calculates distance vectors to active cluster centroids to derive alignment confidence percentages. Tickets dropping below a 70% threshold are systematically rerouted to a manual triage queue. High-priority payloads trigger automated critical SLA flags targeting rapid infrastructure response teams.

## Diagnostic Highlights

The pipeline saves high-yield diagnostic metrics natively to verify production readiness:
* **nlp_elbow_curve.png:** Visual confirmation of optimal cluster mapping via WCSS stabilization.
* **system_confidence_distribution.png:** Distribution tracking showing the density profile of incoming ticket alignment alongside the automated manual triage cutoff line.

## Getting Started

### Prerequisites
Ensure your local environment or container has the necessary software dependencies deployed:
```bash
pip install -r requirements.txt
