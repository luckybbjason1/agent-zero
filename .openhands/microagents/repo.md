# Agent Zero Repository

## Project Description

Agent Zero is a personal, organic agentic framework designed to grow and learn with you. Unlike predefined agentic frameworks, Agent Zero is dynamic, fully transparent, and completely customizable. It uses the computer as a tool to accomplish tasks, featuring persistent memory, multi-agent cooperation, and the ability to create its own tools as needed. The framework is guided entirely by prompts and can be extended or modified by users without any hard-coded limitations.

## File Structure Overview

```
agent-zero/
├── agent.py                 # Main agent implementation
├── models.py               # Model configurations and providers
├── initialize.py           # Agent initialization logic
├── run_ui.py              # Web UI launcher
├── run_cli.py             # Command-line interface
├── run_tunnel.py          # Remote access functionality
├── requirements.txt       # Python dependencies
├── python/                # Core Python modules
│   ├── tools/            # Default tools (search, memory, code execution, etc.)
│   ├── api/              # API interfaces
│   ├── helpers/          # Utility functions
│   └── extensions/       # Extension framework
├── prompts/              # System prompts and message templates
│   ├── default/          # Default agent behavior prompts
│   └── reflection/       # Reflection and self-improvement prompts
├── webui/               # Web interface files (HTML, CSS, JS)
├── docs/                # Comprehensive documentation
├── instruments/         # Custom functions and procedures
├── knowledge/           # Knowledge base and RAG tools
├── memory/              # Persistent memory storage
├── logs/                # Session logs and outputs
└── docker/              # Docker configuration files
```

## Running Tests and Commands

**Quick Start (Docker - Recommended):**
```bash
docker pull frdel/agent-zero-run
docker run -p 50001:80 frdel/agent-zero-run
# Visit http://localhost:50001
```

**Development Setup:**
```bash
# Install dependencies
pip install -r requirements.txt

# Run Web UI
python run_ui.py

# Run CLI interface
python run_cli.py

# Run with tunnel for remote access
python run_tunnel.py
```

**Environment Setup:**
- Copy `example.env` to `.env` and configure your API keys
- Supports multiple LLM providers (OpenAI, Anthropic, Groq, Ollama, etc.)
- Docker Desktop required for containerized runtime

## Developer Information

Agent Zero is highly customizable through its prompt-based architecture. Key customization points include:

- **System Prompts**: Modify `prompts/default/agent.system.md` to change agent behavior
- **Tools**: Extend functionality by adding tools in `python/tools/`
- **Instruments**: Create custom functions in `instruments/`
- **Knowledge**: Add domain-specific knowledge in `knowledge/`

The framework supports multi-agent cooperation where agents can create subordinates to handle subtasks. All agent communication and tool usage is transparent and logged. The Web UI provides real-time streaming output with the ability to intervene at any point during execution.

For detailed setup instructions, usage examples, and architecture details, refer to the comprehensive documentation in the `docs/` folder.