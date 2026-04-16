# AI Resume Architect 🚀

**An Enterprise-Grade, AI-Powered Resume Generation & ATS Optimization Engine**

AI Resume Architect is a robust, full-stack platform designed to autonomously generate perfectly formatted, highly compressed LaTeX resumes. By intelligently parsing target job descriptions and matching them against a candidate's GitHub portfolio, it serves as a high-conversion engine for software engineers navigating automated resume screeners.

By leveraging specialized AI Agents working in concert and employing algorithmic data pruning, the platform ensures that the generated document strips away noisy data and injects high-confidence keywords, maximizing Applicant Tracking System (ATS) selection rates.

***

## 🌟 Key Technical Features

- **🧠 Intelligent JD Extraction Model:** Semantically parses raw Job Descriptions to extract absolute prerequisite skills, core domain knowledge, and exact tooling requirements into a structured JSON payload.
- **🔍 Algorithmic Project Pruning:** Hooks into candidate GitHub repositories and algorithmically selects the **top 3 optimal, highly-correlated projects** based strictly upon the Parsed JD parameters.
- **⚙️ Strict 1-Page Constraints:** Employs advanced Prompt Engineering constraints forcing the LLM to output exactly 2 ultra-concise bullet points per project (max 1-2 lines), ensuring guaranteed 1-page PDF compilation.
- **💯 ATS Pre-Calculation Scoring:** Evaluates the overlap between the selected candidate data and the target JD to provide a hard ATS projection score, natively alerting the user of critical missing skills.
- **🛠️ Dynamic Base Templates:** Features an interactive frontend Template Manager allowing users to securely hot-swap the underlying `.tex` LaTeX architecture via API injection.

***

## 💻 Tech Stack Overview

- **Backend Core:** `Python`, `FastAPI`, `Pydantic` (Strict Data Validation)
- **AI/LLM Architecture:** `Groq API` (LLaMa 3.3 70B Versatile), `Prompt Engineering`
- **Frontend UI Engine:** `React`, `Vite`, `Tailwind CSS v4`, `Lucide Icons`
- **Data Transport:** `Axios`, `RESTful JSON APIs`

***

## 🚀 Getting Started: Complete Installation Guide

Follow these comprehensive steps to download, install dependencies, and boot the multi-agent orchestration locally.

### 📋 Prerequisites
- **Git**: To clone the repository.
- **Node.js (v18+)**: To run the Vite React server.
- **Python (v3.9+)**: To isolate the backend server.
- **Groq API Key**: Obtain a free API key from the [Groq Cloud Console](https://console.groq.com/keys).

### 1️⃣ Clone the Repository
```bash
git clone https://github.com/prakhar383/AI-JD-Analyzer-and-Resume-Maker.git
cd AI-JD-Analyzer-and-Resume-Maker
```

### 2️⃣ Configure the AI Backend (FastAPI)
Establish an isolated Python virtual environment inside the `backend` directory.

**For Windows:**
```cmd
cd backend
python -m venv venv
.\venv\Scripts\activate
pip install -r requirements.txt
```

**For macOS / Linux:**
```bash
cd backend
python3 -m venv venv
source venv/bin/activate
pip3 install -r requirements.txt
```

**Environment Setup:**
1. Create a new file named `.env` inside the `backend` directory.
2. Add your Groq API key securely:
   ```env
   GROQ_API_KEY=your_actual_groq_api_key_here
   ```

**Start the Server (Port 8000):**
*Note for Windows users: Prepending the UTF-8 flag prevents character encoding crashes during AI generation.*
```cmd
# Windows CMD
set PYTHONIOENCODING=utf-8
python main.py

# PowerShell
$env:PYTHONIOENCODING="utf-8"
python main.py

# Mac / Linux
python main.py
```

### 3️⃣ Configure the Frontend (React + Vite)
Leave the backend terminal running. Open a **new** terminal window.

```bash
cd frontend
npm install
npm run dev
```

### 4️⃣ Application Usage

1. 🌐 Open your web browser and navigate to **[http://localhost:5173/](http://localhost:5173/)**.
2. 👤 Input a target **GitHub Username**.
3. 📝 Paste the complete text of your desired **Job Description**.
4. ⚙️ *(Optional)* Use the **Template Configuration** box to paste your own custom LaTeX template. Ensuring it contains `{{DYNAMIC_OBJECTIVE_PLACEHOLDER}}` and `{{DYNAMIC_PROJECTS_PLACEHOLDER}}`, click **Overwrite Template** to re-wire the backend on the fly.
5. ✨ Click **Generate LaTeX Resume** to instantly trigger the multi-agent AI pipeline and receive your custom-tailored ATS resume code.

---
*Created dynamically to streamline rigorous technical job application workflows.*
