

# 🕵️ AI-Assisted Bug Bounty Pipeline  

> **Automate recon & vulnerability analysis with AI** – powered by `llm` + GPT or local models.  

This project helps Bug Bounty hunters speed up:  
✅ **Reconnaissance & scan analysis**  
✅ **JavaScript secret extraction**  
✅ **Payload generation & exploitation tips**  
✅ **Report-ready summaries**  

---

## 🚀 Quick Setup  

We’ll only install `llm` (AI CLI) and connect it to GPT or a local model.  

### 1️⃣ Install `llm`  

```bash
pip install llm


##Check if it’s installed:

  llm --version



2️⃣ Add OpenAI API Key

    Get your key from OpenAI API Keys

    Save it for llm:

llm keys set openai
# Enter your key, e.g.:
# sk-xxxxxxxxxxxxxxxxxxxxxx

✅ Done! Now you can use GPT models like gpt-4o-mini or gpt-4.1.
(Optional) Use Local AI (No API Needed)
-----------------------------------------------------------------------------------------------------------------------------------------------------------------------

If you prefer running local models, install Ollama:

curl --http1.1 -fsSL https://ollama.com/install.sh | sh
ollama pull llama3



Then chat with:

llm chat -m ollama:llama3

---------------------------------------------------------------------------------------------------------------------------------------------------------------

🛠️ Usage Examples
🔹 1. Analyze Nmap or Nuclei scan results

cat nmap_results.txt | llm -m gpt-4o-mini "Analyze these Nmap results. Identify critical services and suggest exploitation paths."



Combine both scans:

cat nmap_results.txt nuclei_results.txt | llm -m gpt-4o-mini "Summarize & prioritize vulnerabilities. Suggest top 3 attack paths."



🔹 2. Extract API keys & secrets from JavaScript

cat app.js | llm -m gpt-4o-mini "Extract API endpoints, tokens, secrets, and hidden debug parameters from this JS file."



🔹 3. Generate Payloads:

llm "Parameter id in /product?id=123 may have SQLi. Give me top payloads & bypass techniques."

#Or for XSS:

llm "I found /search?q= vulnerable to XSS. Suggest 10 best payloads."



🔹 4. Get Recon Strategy

llm "I have target.com for Bug Bounty. Suggest a recon plan with best tools & commands."


✅ Why use this?

✔️ Fast triage → AI instantly summarizes huge scan outputs
✔️ Find hidden attack vectors
✔️ Save time writing payloads & reports
✔️ Works online (GPT) or offline (Ollama)
📜 Copyright

Created by: sadiQ-hashim & ChatGPT
For ethical Bug Bounty & security research only.
