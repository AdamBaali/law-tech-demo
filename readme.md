# Altus | Sovereign AI Legal Platform (Prototype)

**Project Status:** High-Fidelity Interactive Prototype (MVP Candidate)

**Project Name:** Altus (Working Title / Codename)

**Live Demo:** https://adambaali.github.io/law-tech-demo

**Slides:** https://adambaali.github.io/law-tech-demo/slides


## 🚀 Executive Summary
**Altus** (working title) is the first AI-native legal workspace designed specifically for the **Sovereign Data requirements** of France, Spain, and Andorra. We solve the "Legal Bottleneck" for SMBs by replacing the billable hour with instant, AI-verified contract drafting and review.

This repository contains a functional prototype demonstrating the user experience (UX), business logic, and commercial workflows of the platform.

## 🎯 The Problem
* **Speed:** Simple contracts take days to draft via traditional counsel.
* **Cost:** High hourly rates (€300+) exclude most SMBs from proper legal coverage.
* **Sovereignty:** European firms are hesitant to use US-based AI tools due to GDPR/Data Residency risks.

## 💡 The Solution
A strictly sovereign, EU-hosted SaaS platform that combines:

1.  **AI Drafting:** Instant generation of compliant contracts (MSA, NDA, DPA, Employment) tailored to specific Civil Code jurisdictions.
2.  **The "Trinity" Scoring Engine:** Automated analysis for **Legality** (Jurisdiction), **Robustness** (Risk), and **Clarity** (Readability).
3.  **Fairness Engine:** A "Meet in the Middle" negotiation tool that automatically balances terms to resolve counterparty conflicts.
4.  **Partner Marketplace:** A "Human-in-the-loop" marketplace where certified solicitors **monetise** document validation rather than drafting from scratch.

---

## 🛠️ Technical Architecture: Sovereign & Cost-Effective
*Note: This is a centralised SaaS platform built for SMBs. We manage the infrastructure to guarantee sovereignty, ensuring clients do not need their own IT resources.*

### 1. Cascading AI Strategy (Cost Optimisation)
To keep subscription costs competitive for SMBs, we do not rely on expensive "frontier models" for every task. We utilise a **Model Routing Architecture**:

* **Deterministic Diffing (Zero-Cost):** We do not use LLMs to compare document versions. Background Python workers (using libraries like `diff-pdf-visually` or `difflib`) handle document comparison deterministically.
* **The Router:** A lightweight classifier determines the complexity of a user request.
    * *Simple Tasks:* Routed to fast, cost-effective models (e.g., Mistral Small) or local vector lookups.
    * *Complex Reasoning:* Only high-stakes legal analysis is routed to larger, more expensive models.
* **Multimodal Efficiency:** We utilise Multimodal AI (Vision + Text) only for scanned documents. Digital-native PDFs are processed via standard text extraction to save tokens.

### 2. Sovereign Cloud Infrastructure
* **Region Strategy:** All data is strictly pinned to **EU-West (Paris)**.
* **Hosting Partners:** We utilise sovereign European cloud providers (Scaleway / OVH) to ensure data never falls under non-EU jurisdiction (e.g., US CLOUD Act).
* **No Data Transfers:** We enforce a strict technical policy that prevents data egress outside of the European Economic Area (EEA).

### 3. Security & Compliance
* **Stateless Processing:** Contracts are processed in ephemeral memory. Once the session is closed, the inference context is wiped.
* **Zero-Retention:** We strictly enforce a policy where client input data is **never** used to train our foundation models.
* **Encryption:** Industry-standard AES-256 encryption at rest and TLS 1.3 in transit.

---

## ⭐️ Demo Walkthrough
To experience the full flow of the prototype:

1.  **Drafting (Customer View):**
    * Select a contract type (e.g., SaaS MSA).
    * Choose a Jurisdiction (France, Spain, or Andorra) to see the flag and legal context update.
    * Click "Generate Draft Workspace".

2.  **Analysis & Gamification:**
    * Open the Editor. Note the "Trinity" score bars (Legality, Robustness, Clarity).
    * Click on the coloured clauses (e.g., **2. Payment Terms**) to see the AI analyse the risk.
    * Click **"Auto-Fix Clause"** to see the text update and the score improve in real-time.

3.  **Negotiation & Upsell:**
    * Click **"Invite Counterparty"**.
    * Observe the "Conflict Detected" state in the sidebar.
    * Use the **"Auto-Balance"** button to resolve the conflict, or click **"Partner Review"** to trigger the commercial upsell loop.

4.  **Partner Portal (Lawyer View):**
    * Navigate to the "For Lawyers" page.
    * View the verification form (including file upload simulation).
    * Enter the **Lawyer Dashboard** to see live job cards with dynamic filters for Jurisdiction and Contract Type (Note the "Pages" count impacting price).

---
*© 2025 Altus Technologies (Working Title). Built for the European Legal Market.*
