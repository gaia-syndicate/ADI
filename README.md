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


📁 Folder Structure
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
