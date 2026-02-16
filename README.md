# n8n
# 🚀 YouTube Shorts Autopilot: Agentic Video Pipeline

**[🎥 View Sample Output](https://www.youtube.com/watch?v=your-video-id)** 

---

<div align="center">
  <!-- Replace this link with your actual video raw link or a high-res GIF -->
  <img src="https://github.com/Muneeb20019/Sales-AI-Agent-n8n/raw/main/YouTube_Preview.png" width="100%" alt="Final AI Video Output Preview"/>
</div>

---

## 🚀 Project Overview
Developed for **Digital Media Agencies**, this system is a "Zero-Touch" production house. It automates the complete lifecycle of short-form video creation—from **Agentic Brainstorming (Phase 1)** to **Automated Distribution (Phase 2)**. 

The system leverages **Veo 3** for cinematic video generation and **Groq** for near-instant reasoning, producing high-fidelity social media content without human intervention.

---

## 🖼️ System Architecture & Workflow Preview

| ⚙️ n8n Agentic Orchestrator | 📺 Final YouTube Publication |
| :---: | :---: |
| <img src="https://github.com/Muneeb20019/Sales-AI-Agent-n8n/raw/main/video_gen_workflow.png" width="450" alt="n8n Workflow"/> | <img src="https://github.com/Muneeb20019/Sales-AI-Agent-n8n/raw/main/youtube_result.png" width="400" alt="YouTube Result"/> |

---

## 🧠 Core Technical Pillars

### 1. 🤖 Multi-Agent Production Briefing
The system utilizes a dual-agent architecture powered by **Groq (LPU Inference)**. 
- **The Strategist:** Uses a **"Think" tool** (Chain-of-Thought) to storyboard viral ideas.
- **The Prompt Engineer:** Performs **Contextual Expansion**, transforming raw ideas into technical "Production Briefs" (lighting, camera motion, and physics instructions) optimized for the **Veo 3** API.

### 2. ⏳ Asynchronous Polling Lifecycle
Since high-fidelity video generation is compute-intensive, I implemented a robust **Recursive Polling Loop**. The workflow captures a `taskId`, enters a controlled **Wait state**, and queries the API status until the render is verified. This ensures 100% reliability in data transfer for 4K assets.

### 3. 💾 Persistence & Audit Trail (Google Sheets)
Using **Google Sheets** as a lightweight **Production CRM**, the workflow logs every generated concept. Utilizing dynamic primary keys (`=ROW()-1`), the system maintains a "Single Source of Truth," allowing human staff to audit or edit prompts before the final video render begins.

### 4. 📂 Binary Media Management
Unlike simple link-sharing automations, this system performs full **Binary Data Handling**. It downloads the raw MP4 buffer from the AI server into n8n's memory, allowing for direct, secure uploads to the **YouTube Data API v3** via **OAuth2**.

---

## ✨ Advanced Features (Production Grade)
- **🐍 Python Data Transformation:** Utilized custom **Python nodes** to sanitize AI-generated prompts, escaping special characters to ensure a valid JSON payload for the Veo 3 endpoint.
- **🛡️ Schema Enforcement:** Integrated **Structured Output Parsers** to guarantee that Agentic brainstorming always follows a strict data schema, eliminating model "hallucination."
- **🌍 Dynamic Metadata Mapping:** Automatically assigns YouTube **Region Codes (PK)** and Categories based on the cultural context identified by the AI during the strategy phase.

<div align="center">
  <img src="https://github.com/Muneeb20019/Sales-AI-Agent-n8n/raw/main/api_payload.png" width="600" alt="API Payload"/>
  <p><i>🚀 Technical Production Brief mapped to the Veo 3 REST API</i></p>
</div>

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
2.  **Monitor** the Google Sheet as the AI brainstorms "Vlogger" concepts.
3.  **The System** automatically polls the Veo 3 API until the video is successfullly rendered.
4.  **Check** your YouTube Studio to see the private/public upload with all metadata attached.

---

## ✍️ Author
**Muneeb Ali Khan**
- **GitHub:** [@Muneeb20019](https://github.com/Muneeb20019)
- **LinkedIn:** [Muneeb Ali Khan](https://www.linkedin.com/in/muneeb-ali-khan-2a1675365)
