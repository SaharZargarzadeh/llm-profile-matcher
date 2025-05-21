# llm-profile-matcher

# AI Profile Matching Agent 🧠✨

This project implements an intelligent AI agent that matches user-defined queries with the most relevant professionals based on structured profile data and unstructured LinkedIn-style resumes.

It was developed as part of the **AI Agent Expert Matching Competition 2025**.

## 🔍 What it Does

The agent analyzes a user's query (e.g. *"Looking for a senior AI engineer with edge computing experience in Chicago"*) and scores the relevance of 40 mock professional profiles using a large language model (Gemini by Google).

It returns the **top-matching candidates**, including:
- Name and job title
- Location
- Contact info
- Availability
- Relevance score (0–10)
- AI-generated explanation of the match

---

## 🧭 Two Approaches Implemented

### 1️⃣ **Dynamic Prompting (LLM-only mode)**
- Sends the full query, Excel metadata, and HTML resume to Gemini
- Gemini handles all reasoning: skills, availability, location
- Best for open-ended, flexible matching

### 2️⃣ **Filtered + Prompting (Hybrid mode)**
- Applies dropdown filters (City, Job Title) to limit the candidate pool
- Sends each candidate’s structured + unstructured data to Gemini for scoring
- Balances precision and performance (quota-safe)

---

## 🚀 Run in Google Colab

To try it yourself, open the notebook below in Google Colab:

[![Open in Colab]([https://colab.research.google.com/assets/colab-badge.svg)](https://colab.research.google.com/github/YOUR_USERNAME/YOUR_REPO/blob/main/your_notebook.ipynb](https://colab.research.google.com/drive/18RX8MvlsUnIVsMS5YnWe6LAWZrmE5zg2?usp=sharing))

---
## 📁 Project Structure

- `mock_profiles_aicompetition.xlsx`: Excel sheet with name, job title, city, contact info, and availability
- `/profiles/*.html`: Mock LinkedIn pages for each candidate
- `*.ipynb`: Notebooks for both matching modes

---

## 🧑‍💻 Developed By

**Sahar Zargarzadeh**  
PhD Student | Machine Learning Researcher  
Built for the AI Matching Agent Challenge 2025

---

