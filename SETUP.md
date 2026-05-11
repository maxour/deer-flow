songchong@souchuunoMacBook-Air ~ % cd MaxOurC/deer-flow
songchong@souchuunoMacBook-Air deer-flow % make setup
Using CPython 3.12.13
Creating virtual environment at: .venv
Built deerflow-harness @ file:///Users/songchong/MaxOurC/deer-flow/backend/packages/harness
Built forbiddenfruit==0.1.4
Installed 197 packages in 1.61s

Welcome to DeerFlow Setup!
This wizard will help you configure DeerFlow in a few minutes.

╔════════════════════════════════════════════╗
║ Step 1/4 · Choose your LLM provider ║
╚════════════════════════════════════════════╝

Enter choice (↑/↓ move, Enter confirm, number quick-select)
Enter choice: Other OpenAI-compatible (Custom gateway with base_url and model name)

╔════════════════════════════════════════════╗
║ Step 1/4 · Connection details ║
╚════════════════════════════════════════════╝

Base URL (e.g. https://api.openai.com/v1): http://192.168.11.100:4000/v1
Model name [gpt-4o]: ollama-qwen

╔════════════════════════════════════════════╗
║ Step 1/4 · Enter your API Key ║
╚════════════════════════════════════════════╝

OPENAI_API_KEY:
✓ Key will be saved to .env as OPENAI_API_KEY

╔════════════════════════════════════════════╗
║ Step 2/4 · Web Search & Fetch (optional) ║
╚════════════════════════════════════════════╝

Choose a web search provider (↑/↓ move, Enter confirm, number quick-select)
Choose a web search provider: DuckDuckGo (free, no key needed) — No API key required

Choose a web fetch provider (↑/↓ move, Enter confirm, number quick-select)
Choose a web fetch provider: Jina AI Reader — Good default reader, no API key required

╔════════════════════════════════════════════╗
║ Step 3/4 · Execution & Safety ║
╚════════════════════════════════════════════╝

→ Choose how much execution power DeerFlow should have in this workspace.
Execution mode (↑/↓ move, Enter confirm, number quick-select)
Execution mode: Local sandbox — fastest, uses host filesystem paths

! Local sandbox is convenient but not a secure shell isolation boundary.
→ Keep host bash disabled unless this is a fully trusted local workflow.
Enable bash command execution? [Y/N]: Y
Enable file write tools (write_file, str_replace)? [Y/N]: Y

╔════════════════════════════════════════════╗
║ Step 4/4 · Writing configuration ║
╚════════════════════════════════════════════╝

✓ Config written to: config.yaml
✓ API keys written to: .env
✓ frontend/.env created from example

╔════════════════════════════════════════════╗
║ Setup complete! ║
╚════════════════════════════════════════════╝

✓ LLM: Other OpenAI-compatible / ollama-qwen
✓ Web search: DuckDuckGo (free, no key needed)
✓ Web fetch: Jina AI Reader
✓ Execution: Local sandbox
✓ Bash: enabled (host bash)
✓ File write: enabled

Next steps:
make install # Install dependencies (first time only)
make dev # Start DeerFlow

Run make doctor to verify your setup at any time.

songchong@souchuunoMacBook-Air deer-flow %
