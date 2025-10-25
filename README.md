# MCP and A2A Protocols - Multi-Agent Systems Assignment

## Assignment Overview

This assignment explores advanced AI agent architectures using **MCP (Model Context Protocol)** and **A2A (Agent-to-Agent Protocol)**. Through three progressive codelabs, we implement multi-agent systems where AI agents communicate with each other and integrate with external tools to solve complex tasks.

## What Are MCP and A2A?

### MCP (Model Context Protocol)
A standardized protocol that allows AI agents to connect to external resources such as databases, APIs, file systems, and tools. Think of it as a universal adapter that lets agents access any data source or service.

**Example Use Cases:**
- Agent accessing a database
- Agent calling external APIs
- Agent reading/writing files
- Agent using specialized tools

### A2A (Agent-to-Agent Protocol)
A communication protocol that enables multiple AI agents to interact, share information, delegate tasks, and collaborate to achieve common goals. It's like giving agents a common language to work together.

**Example Use Cases:**
- Main agent delegating to specialist agents
- Agents sharing context and information
- Multi-step workflows across agents
- Collaborative problem-solving

### Codelab 1: Multi-Agent System with ADK & A2A
**Focus:** Agent-to-agent communication and deployment

Build a multi-agent system where specialized agents work together using the A2A protocol, then deploy to Google's Agent Engine.

**Key Learning:**
- Multi-agent architecture design
- A2A protocol implementation
- Agent delegation patterns
- Production deployment on Agent Engine

### Codelab 2: Currency Agent with MCP & A2A
**Focus:** External tool integration with agent collaboration

Create a currency conversion agent that uses MCP to access exchange rate APIs while coordinating with other agents via A2A.

**Key Learning:**
- MCP protocol for external data
- Combining MCP and A2A
- Real-world API integration
- Currency conversion use case

### Codelab 3: Purchasing Concierge with Action Engine
**Focus:** Complex multi-agent workflows

Build a sophisticated shopping assistant with multiple specialized agents (search, compare, recommend) orchestrated by Action Engine.

**Key Learning:**
- Action Engine for workflow management
- Complex agent orchestration
- Multi-step agent collaboration
- Production-grade architectures

### Environment Setup
```bash
# Set up Google Cloud
gcloud config set project YOUR_PROJECT_ID

# Enable required APIs
gcloud services enable \
    aiplatform.googleapis.com \
    run.googleapis.com \
    cloudbuild.googleapis.com

# Create workspace
mkdir mcp-a2a-assignment
cd mcp-a2a-assignment
```

### Installation
```bash
# Install ADK
pip install google-adk

# Install MCP dependencies
pip install mcp-core mcp-server

# Verify installation
adk --version
```

## Running the Projects

Each codelab has specific run instructions in its README, but generally:
```bash
# Navigate to codelab directory
cd codelab-X-name/

# Activate environment
source .venv/bin/activate

# Run locally
adk run agent-name

# Or use web UI
adk web agent-name

# Deploy to Agent Engine
adk deploy agent-name
```

## Key Differences from Previous Assignments

| Aspect | Previous Assignment | This Assignment |
|--------|-------------------|-----------------|
| **Focus** | Single agents with tools | Multi-agent collaboration |
| **Protocols** | Basic tool calling | MCP + A2A protocols |
| **Architecture** | Simple agent-tool | Complex multi-agent systems |
| **Deployment** | Local only | Agent Engine production |
| **Communication** | Agent → Tool | Agent ↔ Agent |

