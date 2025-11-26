# 📘 **FactLens: Intelligent Fake News Verification System**

FactLens is a hybrid **AI-powered fake news verification system** that goes beyond traditional machine-learning classifiers.  
Instead of relying only on trained data, FactLens performs **dynamic fact-checking** by retrieving real-time evidence from the web, evaluating source credibility, and using advanced **Natural Language Inference (NLI)** models to determine whether a claim is *Supported*, *Refuted*, or *Unverified*.

---

## 🚀 **Project Overview**

Traditional fake news classifiers can only predict based on previously seen patterns.  
FactLens solves this limitation by combining:

- **NLP Claim Extraction**
- **Web Search & Evidence Retrieval**
- **Source Reliability Analysis**
- **NLI-Based Fact Verification**
- **Deep Learning Fake News Classification**
- **(Optional) Multi-Modal Verification for Images & Videos**

This provides a **robust, real-world truth assessment engine** suitable for modern misinformation challenges.

---

## 🎯 **Key Features**

### ✅ **1. Claim Extraction**
Extracts the core claim from raw text using summarization models (BART/T5).

### ✅ **2. Web Search Integration**
Fetches real-time news data via:
- NewsAPI  
- SerpAPI (Google Search)  
- GDELT / EventRegistry  

### ✅ **3. Source Reliability Check**
Includes a customizable credibility database with:
- Trustworthy outlets  
- Known misinformation sources  
- Satire/hoax websites  

### ✅ **4. Fact Verification Using NLI**
Uses state-of-the-art NLI models to determine:
- **Supported**
- **Refuted**
- **Not Enough Evidence**

### ✅ **5. Deep Learning Classifier (RoBERTa)**
Fine-tuned on curated real/fake datasets + synthetic absurd/satire claims for generalization.

### ✅ **6. Multi-Modal Verification (Optional)**
Image and video fact-checking via:
- Reverse image search  
- Google Vision API  
- Deepfake detection models  

### ✅ **7. Final Truth Scoring**
Combines:
- Classifier score  
- Source credibility score  
- Cross-verification result  

And produces a final verdict:
- **Likely Real**
- **Likely Fake**
- **Needs Verification**

---

## 🏗️ **System Architecture**

         ┌──────────────────────────┐
         │        User Input         │
         │  (Text / Image / Video)   │
         └─────────────┬────────────┘
                       │
           ┌───────────▼────────────┐
           │   Claim Extraction      │
           └───────────┬────────────┘
                       │
        ┌──────────────▼───────────────┐
        │   Web Search & Evidence Fetch │
        └──────────────┬───────────────┘
                       │
     ┌─────────────────▼──────────────────┐
     │        Source Credibility Check     │
     └─────────────────┬──────────────────┘
                       │
  ┌────────────────────▼────────────────────┐
  │      NLI-Based Evidence Verification     │
  └────────────────────┬────────────────────┘
                       │
┌──────────────────────▼──────────────────────┐
│     RoBERTa Fake News Classification Model   │
└──────────────────────┬──────────────────────┘
                       │
  ┌────────────────────▼─────────────────────┐
  │         Final Truth Decision Engine       │
  └───────────────────────────────────────────┘


