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

# songchong@souchuunoMacBook-Air deer-flow % make check

# Checking Required Dependencies

Checking Node.js...
OK Node.js 22.11.0 (>= 22 required)

Checking pnpm...
INFO Unable to determine pnpm version

Checking uv...
OK uv 0.11.12

Checking nginx...
FAIL nginx not found
macOS: brew install nginx
Ubuntu: sudo apt install nginx
Windows: use WSL for local mode or use Docker mode
Or visit: https://nginx.org/en/download.html

==========================================
FAIL Some dependencies are missing
==========================================

Please install the missing tools and run 'make check' again.
make: \*\*\* [check] Error 1
songchong@souchuunoMacBook-Air deer-flow % brew install nginx
==> Auto-updating Homebrew...
Adjust how often this is run with `$HOMEBREW_AUTO_UPDATE_SECS` or disable with
`$HOMEBREW_NO_AUTO_UPDATE=1`. Hide these hints with `$HOMEBREW_NO_ENV_HINTS=1` (see `man brew`).
==> Auto-updated Homebrew!
Updated 3 taps (mongodb/brew, homebrew/core and homebrew/cask).
==> New Formulae
committed: Nitpicking commit history since beabf39
crit: Your feedback loop with the agent: review plans and code locally
cutadapt: Removes adapter sequences from sequencing reads
dexter-lsp: Elixir LSP optimized for large codebases
freesasa: Solvent Accessible Surface Area calculations
ginkgo: High-performance numerical linear algebra software package
go-hass-agent: Native Home Assistant agent for desktop/laptop devices
hermes-agent: Self-improving AI agent that creates skills from experience
hexapoda: Colorful modal hex editor
iqtree3: Phylogenetics by maximum likelihood
lavinmq: Message broker implementing the AMQP 0-9-1 and MQTT protocols
marmot: Open-source data catalog exposing metadata to AI agents
nettle@3: Low-level cryptographic library
opendoor: CLI for web reconnaissance, directory discovery, and exposure assessment
paml: Phylogenetic analyses of DNA or protein sequences using maximum likelihood
plutosvg: Tiny SVG rendering library in C
smlnj: Compiler and programming system for Standard ML
sol2: C++ <-> Lua API wrapper with advanced features and top notch performance
vtzero: Minimalist vector tile decoder and encoder in C++
zapp: Flash ZSA keyboards from your terminal

You have 111 outdated formulae installed.

==> Fetching downloads for: nginx
✔︎ Bottle Manifest nginx (1.29.8) Downloaded 11.8KB/ 11.8KB
✔︎ Bottle Manifest pcre2 (10.47_1) Downloaded 11.7KB/ 11.7KB
✔︎ Bottle pcre2 (10.47_1) Downloaded 2.4MB/ 2.4MB
✔︎ Bottle nginx (1.29.8) Downloaded 1.5MB/ 1.5MB
==> Installing nginx dependency: pcre2
==> Pouring pcre2--10.47_1.arm64_tahoe.bottle.tar.gz
🍺 /opt/homebrew/Cellar/pcre2/10.47_1: 244 files, 7.3MB
==> Pouring nginx--1.29.8.arm64_tahoe.bottle.tar.gz
==> Caveats
Docroot is: /opt/homebrew/var/www

The default port has been set in /opt/homebrew/etc/nginx/nginx.conf to 8080 so that
nginx can run without sudo.

nginx will load all files in /opt/homebrew/etc/nginx/servers/.

To start nginx now and restart at login:
brew services start nginx
Or, if you don't want/need a background service you can just run:
/opt/homebrew/opt/nginx/bin/nginx -g daemon\ off\;
==> Summary
🍺 /opt/homebrew/Cellar/nginx/1.29.8: 27 files, 2.7MB
==> Running `brew cleanup nginx`...
Disable this behaviour by setting `HOMEBREW_NO_INSTALL_CLEANUP=1`.
Hide these hints with `HOMEBREW_NO_ENV_HINTS=1` (see `man brew`).
==> Caveats
==> nginx
Docroot is: /opt/homebrew/var/www

The default port has been set in /opt/homebrew/etc/nginx/nginx.conf to 8080 so that
nginx can run without sudo.

nginx will load all files in /opt/homebrew/etc/nginx/servers/.

To start nginx now and restart at login:
brew services start nginx
Or, if you don't want/need a background service you can just run:
/opt/homebrew/opt/nginx/bin/nginx -g daemon\ off\;
songchong@souchuunoMacBook-Air deer-flow % make install
Installing backend dependencies...
Resolved 217 packages in 17ms
Checked 197 packages in 23ms
Installing frontend dependencies...
/bin/sh: pnpm: command not found
make: **_ [install] Error 127
songchong@souchuunoMacBook-Air deer-flow % make install
Installing backend dependencies...
Resolved 217 packages in 17ms
Checked 197 packages in 23ms
Installing frontend dependencies...
/bin/sh: pnpm: command not found
make: _** [install] Error 127
songchong@souchuunoMacBook-Air deer-flow % brew install pnpm
==> Fetching downloads for: pnpm
✔︎ Bottle Manifest pnpm (11.0.9) Downloaded 7.5KB/ 7.5KB
✔︎ Bottle pnpm (11.0.9) Downloaded 3.7MB/ 3.7MB
==> Pouring pnpm--11.0.9.arm64_tahoe.bottle.tar.gz
==> Caveats
pnpm requires a Node installation to function. You can install one with:
brew install node
==> Summary
🍺 /opt/homebrew/Cellar/pnpm/11.0.9: 461 files, 16.3MB
==> Running `brew cleanup pnpm`...
Disable this behaviour by setting `HOMEBREW_NO_INSTALL_CLEANUP=1`.
Hide these hints with `HOMEBREW_NO_ENV_HINTS=1` (see `man brew`).
==> Caveats
zsh completions have been installed to:
/opt/homebrew/share/zsh/site-functions
songchong@souchuunoMacBook-Air deer-flow %

# songchong@souchuunoMacBook-Air deer-flow % make dev

# Checking Required Dependencies

Checking Node.js...
OK Node.js 22.11.0 (>= 22 required)

Checking pnpm...
INFO Unable to determine pnpm version

Checking uv...
OK uv 0.11.12

Checking nginx...
OK nginx 1.29.8

==========================================
FAIL Some dependencies are missing
==========================================

Please install the missing tools and run 'make check' again.
make: \*\*\* [dev] Error 1
songchong@souchuunoMacBook-Air deer-flow % pnpm -v
ERROR: This version of pnpm requires at least Node.js v22.13
The current version of Node.js is v22.11.0
Visit https://r.pnpm.io/comp to see the list of past pnpm versions with respective Node.js version support.
songchong@souchuunoMacBook-Air deer-flow % node -v
v22.11.0
songchong@souchuunoMacBook-Air deer-flow % nvm install --lts

Installing latest LTS version.
Downloading and installing node v24.15.0...
Downloading https://nodejs.org/dist/v24.15.0/node-v24.15.0-darwin-arm64.tar.xz...
##################################################################################################################### 100.0%
Computing checksum with sha256sum
Checksums matched!
Now using node v24.15.0 (npm v11.12.1)
songchong@souchuunoMacBook-Air deer-flow %

make dev

==========================================
Checking Required Dependencies
==========================================

Checking Node.js...
OK Node.js 24.15.0 (>= 22 required)

Checking pnpm...
OK pnpm 11.0.9

Checking uv...
OK uv 0.11.12

Checking nginx...
OK nginx 1.29.8

==========================================
OK All dependencies are installed!
==========================================

You can now run:
make install - Install project dependencies
make setup - Create a minimal working config (recommended)
make config - Copy the full config template (manual setup)
make doctor - Verify config and dependency health
make dev - Start development server
make start - Start production server
Stopping all services...
Cleaning up sandbox containers with prefix: deer-flow-sandbox
Docker not found, skipping...
Apple Container not found, skipping...
✓ Container cleanup complete
✓ All services stopped
OK config.yaml is already up to date (version 9).
Syncing dependencies...
✓ Dependencies synced

==========================================
Starting DeerFlow
==========================================

Mode: DEV (Gateway runtime, hot-reload enabled)

Services:
Gateway → localhost:8001 (REST API + agent runtime)
Frontend → localhost:3000 (Next.js)
Nginx → localhost:2026 (reverse proxy)

Starting Gateway...
✓ Gateway started on localhost:8001  
Starting Frontend...
✓ Frontend started on localhost:3000  
Starting Nginx...
✓ Nginx started on localhost:2026

==========================================
✓ DeerFlow is running! [DEV (Gateway runtime, hot-reload enabled)]
==========================================

🌐 http://localhost:2026

Routing: Frontend → Nginx → Gateway
API: /api/langgraph/_ → Gateway agent runtime
/api/_ → Gateway REST API (8001)

📋 Logs: logs/{gateway,frontend,nginx}.log

Press Ctrl+C to stop all services

# 禁用块超时限制（推荐设为 0 或 None）

export LANGCHAIN_OPENAI_STREAM_CHUNK_TIMEOUT_S=0

# 或者设置一个更长的时间，比如 10 分钟

export LANGCHAIN_OPENAI_STREAM_CHUNK_TIMEOUT_S=600

export DEER_FLOW_HOME="~/MaxOurC/deer-flow/"

Ubuntu

songc@agent-windows:/mnt/c/Users/songc/GitHub/deer-flow$ curl -fsSL https://get.pnpm.io/install.sh | sh -
==> Downloading pnpm binaries 11.0.9

[WARN] using --force I sure hope you know what you are doing
Installing pnpm CLI globally from /tmp/tmp.8kqnLmOa1E
Packages: +1

- Progress: resolved 1, reused 0, downloaded 0, added 0
  (node:1278) [MODULE_TYPELESS_PACKAGE_JSON] Warning: Module type of file:///tmp/tmp.8kqnLmOa1E/dist/worker.js is n
  ot specified and it doesn't parse as CommonJS.
  Reparsing as ES module because module syntax was detected. This incurs a performance overhead.
  To eliminate this warning, add "type": "module" to /tmp/tmp.8kqnLmOa1E/package.json.
  Progress: resolved 1, reused 1, downloaded 0, added 1, donewas created)

global:

- @pnpm/exe 11.0.9

Done in 6.1s using pnpm v11.0.9
Appended new lines to /home/songc/.bashrc

Next configuration changes were made:
export PNPM*HOME="/home/songc/.local/share/pnpm"
case ":$PATH:" in
  *":$PNPM_HOME/bin:"*) ;;
\_) export PATH="$PNPM_HOME/bin:$PATH" ;;
esac

To start using pnpm, run:
source /home/songc/.bashrc
songc@agent-windows:/mnt/c/Users/songc/GitHub/deer-flow$
songc@agent-windows:/mnt/c/Users/songc/GitHub/deer-flow$ source /home/songc/.bashrc
