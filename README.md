# 🚀 YouTube Shorts Autopilot: Agentic Video Pipeline

**[🎥 Watch the AI-Generated Result](https://youtu.be/58r4kNkrQtQ)**

---

<div align="center">
  <img src="https://raw.githubusercontent.com/Muneeb20019/n8n/main/YouTube%20short.png" width="100%" alt="Final YouTube Result Preview"/>
</div>

---

## 🚀 Project Overview
Developed for digital content automation, this system is a **"Zero-Touch" Video Production House**. It automates the entire creative lifecycle—from **Agentic Brainstorming (Phase 1)** to **Automated YouTube Distribution (Phase 2)**. 

The system utilizes **Veo 3** for high-fidelity video generation and **Groq** for near-instant reasoning, producing professional social media content without human intervention.

---

## 🖼️ System Architecture & Workflow Preview

| ⚙️ n8n Agentic Orchestrator | 📺 Final YouTube Publication |
| :---: | :---: |
| <img src="https://raw.githubusercontent.com/Muneeb20019/n8n/main/Video%20Generation%20for%20youtube.png" width="450" alt="n8n Workflow"/> | <img src="https://raw.githubusercontent.com/Muneeb20019/n8n/main/YouTube%20short.png" width="400" alt="YouTube Result"/> |

---

## 🧠 Core Technical Pillars

### 1. 🤖 Multi-Agent Production Briefing
The system utilizes a dual-agent architecture powered by **Groq (LPU Inference)** for lightning-fast reasoning. 
- **The Strategist:** Uses a **"Think" tool** (Chain-of-Thought) to storyboard viral ideas.
- **The Prompt Engineer:** Performs **Contextual Expansion**, transforming raw ideas into technical "Production Briefs" (lighting, camera motion, and cinematic instructions) optimized for the **Veo 3** API.

### 2. ⏳ Asynchronous Polling Lifecycle
Since video generation is compute-intensive, I implemented a robust **Recursive Polling Loop**. The workflow captures a `taskId`, enters a controlled **Wait state**, and queries the API status until the render is verified. This ensures 100% reliability for high-fidelity 4K assets.

### 3. 💾 Persistence & Audit Trail (Google Sheets)
Using **Google Sheets** as a lightweight **Production CRM**, the workflow logs every generated concept. Utilizing dynamic primary keys (`=ROW()-1`), the system maintains a "Single Source of Truth," allowing human staff to audit or edit prompts before the final video render begins.

### 4. 📂 Binary Media Management
Unlike simple link-sharing automations, this system performs full **Binary Data Handling**. It downloads the raw MP4 buffer from the AI server into n8n's memory, allowing for direct, secure uploads to the **YouTube Data API v3** via **OAuth2**.

---

## ✨ Advanced Features (Production Grade)
- **🐍 Python Data Transformation:** Utilized custom **Python nodes** to sanitize AI-generated prompts, escaping special characters to ensure a valid JSON payload for the Veo 3 endpoint.
- **🛡️ Schema Enforcement:** Integrated **Structured Output Parsers** to guarantee that Agentic brainstorming always follows a strict data schema, eliminating model "hallucination."
- **🌍 Dynamic Metadata Mapping:** Automatically assigns YouTube **Region Codes (PK)** and Categories based on the cultural context identified by the AI during the strategy phase.

---

## 🛠️ Technical Stack
| Layer | Technology |
| :--- | :--- |
| **🔄 Automation** | n8n Orchestration (Agentic Workflow) |
| **🧠 AI Brain** | Groq Llama 3 & Gemini 1.5 Flash |
| **📹 Video Model** | Google Veo 3.0 (via KIE.AI) |
| **💻 Backend Code** | **Python** & JavaScript |
| **🗄️ Database** | Google Sheets API |
| **🎥 Distribution** | YouTube Data API v3 |

---

## 📝 How to Use
1.  **Trigger** the workflow via the **Schedule Trigger** for automated daily posting.
2.  **Monitor** the Google Sheet as the AI brainstorms "Vlogger in Lahore" concepts.
3.  **The System** automatically polls the Veo 3 API until the video is successfully rendered.
4.  **Check** your YouTube Studio to see the private/public upload with all metadata attached.

---

## ✍️ Author
**Muneeb Ali Khan**
- **GitHub:** [@Muneeb20019](https://github.com/Muneeb20019)
- **LinkedIn:** [Muneeb Ali Khan](https://www.linkedin.com/in/muneeb-ali-khan-2a1675365)
