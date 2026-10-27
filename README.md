\# 👻 GhostTrace



\*\*A local AI-powered system log investigator using Gemma 3 4B, Ollama, and Flask.\*\*



GhostTrace investigates system logs and generates structured AI reports to help developers understand errors, identify possible causes, and decide what to investigate next.



The project explores the idea of a \*Ghost in the Machine\*: using open-weight AI to investigate problems locally, without relying on a hosted AI API.



\## ✨ Features



\- \*\*Local AI inference:\*\* Runs Gemma 3 4B through Ollama.

\- \*\*Log investigation:\*\* Analyzes supplied log text and identifies relevant errors and warning patterns.

\- \*\*Structured reports:\*\* Organizes findings, possible causes, and recommended investigation steps.

\- \*\*Fallback analysis:\*\* Provides basic keyword-based analysis when AI inference is unavailable.

\- \*\*Evidence-focused prompting:\*\* Encourages the model to distinguish observed log evidence from hypotheses.

\- \*\*Local web interface:\*\* Provides a browser-based interface powered by Flask.

\- \*\*Safer output rendering:\*\* Escapes HTML before rendering AI-generated report content.



\## 🛠️ Tech Stack



\- Python

\- Flask

\- Ollama

\- Gemma 3 4B

\- HTML, CSS, JavaScript



\## ⚙️ Prerequisites



\- Python 3.10+

\- \[Ollama](https://ollama.com/)

\- The `gemma3:4b` model



\## 🚀 Getting Started



\### 1. Clone the repository



```bash

git clone https://github.com/Yadnu14/GhostTrace.git

cd GhostTrace

```



\### 2. Create and activate a virtual environment



\*\*Windows PowerShell:\*\*



```powershell

python -m venv .venv

.\\.venv\\Scripts\\Activate.ps1

```



\### 3. Install dependencies



```powershell

python -m pip install -r requirements.txt

```



\### 4. Download the model



```powershell

ollama pull gemma3:4b

```



Make sure Ollama is running.



\### 5. Start GhostTrace



```powershell

python app.py

```



Open \*\*http://127.0.0.1:5000\*\* in your browser.



\## 🔍 How It Works



1\. The user supplies system log text through the web interface.

2\. GhostTrace sends the logs to the locally running application.

3\. The application requests an investigation from Gemma 3 4B through Ollama.

4\. The model generates a structured report based on the supplied evidence.

5\. If AI inference is unavailable, the application can fall back to basic keyword-based analysis.



\## 🔐 Privacy and Safety



GhostTrace is designed for local inference. In the default configuration, prompts are sent to the local Ollama endpoint rather than a hosted AI service.



\- No automatic system-command execution.

\- No automatic modification of system files.

\- AI-generated conclusions should be verified against the original logs.

\- Avoid submitting passwords, access tokens, or other sensitive information.



\## 🌍 Why Open Innovation?



Open-weight models and local inference make AI experimentation more accessible. Developers can explore AI-assisted troubleshooting, inspect their workflows, and build useful tools without depending entirely on external AI APIs.



GhostTrace is a small example of how open-source software and open-weight AI can support practical developer tools.



\## ⚠️ Limitations



GhostTrace is a prototype, not a production incident-response platform. Its findings may be incomplete or incorrect, and keyword-based fallback analysis is limited. It does not replace professional monitoring, forensic investigation, or human verification.



\## 📁 Project Structure



```text

GhostTrace/

├── app.py

├── requirements.txt

├── .gitignore

└── README.md

```
