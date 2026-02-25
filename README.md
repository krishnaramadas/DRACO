# 🐉 DRACO — DataOps Response And Cost Optimization

> A Snowflake-native AI platform for DataOps incident response and cost intelligence — built entirely on Snowflake Cortex, Cortex Search, and Streamlit in Snowflake. No external APIs. No hosting. Pure Snowflake.

![Status](https://img.shields.io/badge/Status-In%20Development-orange)
![Platform](https://img.shields.io/badge/Platform-Snowflake%20Native-29B5E8?logo=snowflake)
![AI](https://img.shields.io/badge/AI-Snowflake%20Cortex-blue)
![UI](https://img.shields.io/badge/UI-Streamlit%20in%20Snowflake-red?logo=streamlit)

---

## 🧩 What is DRACO?

DRACO is a unified DataOps intelligence platform with two core capabilities:

### 🔧 Tab 1 — DataOps Incident Assistant (DoRRA)
An AI-powered L1/L2 shift assistant that helps on-call engineers during production incidents — without guessing or hallucinating fixes.

Given an incident, DRACO can answer:
- *"What are the documented troubleshooting steps for this pipeline?"*
- *"Has this error happened before? What was the resolution?"*
- *"Is this expected behaviour?"*
- *"Who do I escalate to for a P2 bridge call?"*

DRACO **only surfaces what developers have explicitly documented** in runbooks or historical incident records. If the answer isn't documented — it says so and provides escalation contacts. No hallucinated fixes on production systems.

### 💰 Tab 2 — Cost Intelligence Assistant
A Snowflake-native cost dashboard powered by `SNOWFLAKE.ACCOUNT_USAGE` with an embedded AI chat assistant — giving engineers visibility into warehouse spend, query costs, and storage usage without leaving Snowflake.

---

## 🏗️ Architecture

<img width="840" height="620" alt="ChatGPT Image Feb 25, 2026, 07_00_15 PM" src="https://github.com/user-attachments/assets/4063525a-48c1-473a-b435-509f0329e2de" />



---

## ⚙️ Tech Stack

| Layer | Technology |
|---|---|
| Database | Snowflake |
| AI Search | Snowflake Cortex Search |
| LLM | Snowflake Cortex (Mistral / Llama) |
| Orchestration | Snowflake Tasks + Streams |
| UI | Streamlit in Snowflake |
| Data Ingestion | Snowpipe, External Stages |
| Cost Data | SNOWFLAKE.ACCOUNT_USAGE (native) |

**Zero external dependencies. 100% Snowflake native.**

---

## 🚀 Project Status

- [x] Architecture design
- [x] Mock runbooks (5 pipelines, varied formats)
- [x] Mock incident archive schema
- [ ] Snowflake DDL + table setup
- [ ] Cortex Search service configuration
- [ ] Streamlit app — DataOps tab
- [ ] Streamlit app — Cost tab
- [ ] End-to-end testing
- [ ] Demo video

---

## 💡 Design Decisions

**Why strict docs-only responses?**
DRACO is designed for production DataOps environments. Hallucinated troubleshooting steps on live pipelines are dangerous. The system prompt explicitly prohibits the LLM from suggesting fixes that aren't documented by the development team.

**Why fully Snowflake-native?**
No external hosting, no API keys, no infra to manage. Everything — data, AI, and UI — lives inside Snowflake. This makes DRACO portable, secure, and easy to demo from a single Snowflake account.

---

## 👤 Author

**Krishna Ramadas** — Senior Data Engineer
4+ years building production DataOps systems for Fortune 500 clients.

[![LinkedIn](https://img.shields.io/badge/LinkedIn-Krishna%20Ramadas-blue?logo=linkedin)](https://www.linkedin.com/in/krishna-ramadas-0807121b0/)
[![GitHub](https://img.shields.io/badge/GitHub-krishnaramadas-black?logo=github)](https://github.com/krishnaramadas)

---

## 📄 License

MIT License — see [LICENSE](LICENSE) for details.
