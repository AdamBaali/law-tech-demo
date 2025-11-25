# Altus | Sovereign AI Legal Platform (Prototype)

**Current Status:** High-Fidelity Interactive Prototype (MVP Candidate)
**Live Demo:** [Insert your GitHub Pages Link Here]

## 🚀 Executive Summary
Altus is the first AI-native legal workspace designed specifically for the **Sovereign Data requirements** of France, Spain, and Andorra. We solve the "Legal Bottleneck" for SMBs by replacing the billable hour with instant, AI-verified contract drafting and review.

This repository contains a **high-fidelity functional prototype** demonstrating the user experience (UX), business logic, and commercial workflows of the platform.

## 🎯 The Problem
* **Speed:** Simple contracts take days to draft via traditional counsel.
* **Cost:** High hourly rates (€300+) exclude most SMBs from proper legal coverage.
* **Sovereignty:** European firms are hesitant to use US-based AI tools due to GDPR/Data Residency risks.

## 💡 The Solution
A strictly sovereign, EU-hosted platform that combines:

1.  **AI Drafting:** Instant generation of compliant contracts (MSA, NDA, DPA, Employment) tailored to specific Civil Code jurisdictions.
2.  **The "Trinity" Scoring Engine:** Automated analysis for **Legality** (Jurisdiction), **Robustness** (Risk), and **Clarity** (Readability).
3.  **Fairness Engine:** A "Meet in the Middle" negotiation tool that automatically balances terms to resolve counterparty conflicts.
4.  **Partner Marketplace:** A "Human-in-the-loop" marketplace where certified solicitors **monetise** document validation rather than drafting from scratch.

---

## 🛠️ Technical Architecture Strategy
*Note: While this demo runs client-side for portability, the production backend architecture is scoped as follows to meet Enterprise requirements:*

### 1. Sovereign Cloud Strategy
* **Primary Region:** EU-West (Paris/Amsterdam).
* **Provider Agnostic:** Capable of deployment on Scaleway (France), OVH (France), or private on-premise clusters for Enterprise clients.
* **Data Residency:** Guaranteed storage within the EU to comply with strict local regulations.

### 2. AI Pipeline
* **Model:** Fine-tuned 7B/70B models (e.g., Mistral) **specialised** in Civil Code law.
* **RAG (Retrieval-Augmented Generation):** Localised vector stores for legal context without sending data to public APIs.
* **Inference:** Stateless interaction patterns to ensure data is processed in ephemeral memory only.

### 3. Security & Compliance
* **Zero-Retention Policy:** We strictly enforce a policy where input data is never used to train foundation models.
* **Encryption:** AES-256 encryption at rest and TLS 1.3 in transit.
* **GDPR:** Full Article 28 compliance via integrated DPA workflows.

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
    * Click **"Auto-Fix"** to see the text update and the score improve in real-time.

3.  **Negotiation & Upsell:**
    * Click **"Invite Counterparty"**.
    * Observe the "Conflict Detected" state in the sidebar.
    * Use the **"Auto-Balance"** button to resolve the conflict, or click **"Partner Review"** to trigger the commercial upsell loop.

4.  **Partner Portal (Lawyer View):**
    * Navigate to the "Partners" page.
    * View the verification form (including file upload simulation).
    * Enter the **Lawyer Dashboard** to see live job cards with dynamic filters for Jurisdiction and Contract Type.

---
*© 2025 Altus Technologies. Built for the European Legal Market.*
