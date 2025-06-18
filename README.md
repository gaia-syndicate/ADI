# ADI
🧠 ADI — Advanced Data Intelligence (Deep Research)

ADI (Advanced Data Intelligence) is a local AI research assistant designed to analyze large-scale files, documents, and databases with contextual depth. This Deep Research version enables ADI to scan, interpret, and reason across full research directories in real-time—ideal for academic research, novel writing, scientific analysis, or cybersecurity investigations.

🔐 Runs fully on local infrastructure. No internet required.

🚀 Features
Deep File Analysis: ADI can scan all files in the /mnt/deep_research directory during inference.

Context-Aware Reasoning: Maintains memory of previous queries and adapts to long-term research goals.

Secure & Local: No cloud, no API keys, no external calls—runs on your local Ollama LLM stack.

Markdown & Report Generation: Outputs well-formatted summaries, citations, and breakdowns.

MariaDB + Filesystem Awareness: Can cross-reference relational data with unstructured text.

🧩 Use Cases
Technical research assistance

AI-supported writing companion (for novels, reports, whitepapers)

Deep document review (legal, academic, etc.)

Reverse engineering document trails or investigation logs

Offline intelligence for air-gapped systems

🛠️ Setup
Prerequisites
Ubuntu Server (recommended)

PHP + Apache

MariaDB

Ollama (running your chosen local LLM, e.g. mistral, llama3, or custom)

Shared folder: /mnt/deep_research


1. Clone the Repository
bash
Copy
Edit
git clone https://github.com/gaia-syndicate/adi-deep-research.git
cd adi-deep-research
2. Configure Database
Edit config.php to match your MariaDB credentials.

php
Copy
Edit
// config.php
$db_host = "localhost";
$db_user = "your_db_user";
$db_pass = "your_db_password";
$db_name = "adi_llm_chat_db";
Create the necessary tables using schema.sql included in the repo.

3. Set Up Ollama Integration
Ensure ollama is installed and running your chosen model:

bash
Copy
Edit
ollama run llama3
Edit the PHP backend to point to your local AI Node (default: http://localhost:11434).

4. Mount Research Directory
Ensure /mnt/deep_research/ is accessible and populated with your documents, text files, PDFs, etc.

bash
Copy
Edit
sudo mount -t cifs //192.168.1.X/deep_research /mnt/deep_research -o username=...,password=...
5. Launch the Web App
Serve with Apache or your preferred stack:

arduino
Copy
Edit
http://localhost/deep_research.php
📁 Folder Structure
bash
Copy
Edit
/
├── deep_research.php       # Main dashboard
├── ollama.php              # Handles LLM requests
├── config.php              # DB & LLM settings
├── schema.sql              # MariaDB setup
├── /mnt/deep_research/     # Your raw research files
└── /responses/             # Saved AI responses
🧠 AI Capabilities
ADI is prompt-engineered to:

Ingest large file sets

Search for named entities, facts, contradictions

Generate hypothesis summaries and back them with evidence

Ask follow-up questions automatically to refine its own understanding

🔒 Security Considerations
Fully offline. Designed for air-gapped or research-sensitive environments.

Access controlled via internal Apache/PHP authentication (can be expanded to SSO or 2FA).

File uploads and database queries are sandboxed and logged.

📅 Roadmap
 Document tagging & annotation system

 Interactive file graph visualization

 Multi-model support (switch between LLMs)

 Research memory timeline mode

 Export to PDF / DOCX

🤖 Built With
PHP / Apache

MariaDB

Ollama (local LLM runtime)

Markdown renderer (for clean AI output)

✨ Screenshots
Add a few screenshots or screen recordings of the dashboard here.

🤝 Contributing
Pull requests are welcome. If you want to extend ADI’s research capabilities, feel free to fork and customize.

📜 License
MIT License — do what you want, but don’t remove attribution.
