# AI-Powered Penetration Testing Tools & Frameworks
A collection of open-source AI-powered penetration testing frameworks, autonomous agents, MCP-based security tools, code analysis solutions, and AI copilots.

## Family 1: Autonomous AI Penetration Testing Agents
These frameworks use AI agents to perform penetration testing tasks with varying levels of autonomy. They can coordinate multiple agents, execute security tools, analyze results, identify vulnerabilities, and generate proof-of-concept (PoC) code.
### 1. Raptor
- **Purpose:** AI-powered security analysis and vulnerability research.
- **Key Capabilities:**
  - Analyzes vulnerabilities.
  - Generates proof-of-concept code and patches.
- **GitHub:** https://github.com/gadievron/raptor
### 2. PentAGI
- **Purpose:** Multi-agent autonomous penetration testing framework.
- **Key Capabilities:**
  - Uses a team of cooperating AI agents.
  - Includes an orchestrator, researcher, developer, and executor.
  - Runs agents inside isolated Kali Linux containers.
- **GitHub:** https://github.com/vxcontrol/pentagi
### 3. PentestGPT
- **Purpose:** LLM-guided penetration testing agent.
- **Key Capabilities:**
  - Uses large language models to guide penetration testing.
  - Helps testers understand security findings and determine next steps.
  - Commonly used as a teaching and learning baseline.
- **GitHub:** https://github.com/GreyDGL/PentestGPT
### 4. Strix
- **Purpose:** Autonomous AI-powered application security testing.
- **Key Capabilities:**
  - Uses autonomous agents that behave like attackers.
  - Dynamically executes application code.
  - Identifies weaknesses and validates findings with working PoC exploits.
- **GitHub:** https://github.com/usestrix/strix
### 5. NeuroSploit
- **Purpose:** Multi-agent AI penetration testing framework.
- **Key Capabilities:**
  - Deploys specialized AI agent personas.
  - Runs agents inside isolated Kali containers.
  - Supports Claude, OpenAI, Gemini, Grok, and local models through Ollama.
- **GitHub:** https://github.com/CyberSecurityUP/NeuroSploit
### 6. Deadend CLI
- **Purpose:** Self-correcting AI agent designed for black-box testing.
- **Key Capabilities:**
  - Analyzes responses when an attack is blocked.
  - Generates custom Python code to adapt testing approaches.
  - Fully self-hosted.
  - Supports almost any model.
- **GitHub:** https://github.com/xoxruns/deadend-cli
### 7. CAI (Cybersecurity AI)
- **Purpose:** Modular framework for offensive and defensive AI agents.
- **Key Capabilities:**
  - Supports hundreds of model backends.
  - Provides modular agent development.
  - Can operate fully offline.
  - Suitable for air-gapped security laboratories.
- **GitHub:** https://github.com/aliasrobotics/CAI
### 8. PentestAgent
- **Purpose:** AI agent framework focused on black-box penetration testing.
- **Key Capabilities:**
  - Built-in browser tools.
  - Terminal integration.
  - Note-taking capabilities.
- **GitHub:** https://github.com/GH05TCREW/pentestagent
### 9. LLM4Pentest
- **Purpose:** LLM-powered penetration testing framework.
- **Key Capabilities:**
  - Wraps more than 200 security tools.
  - Includes a built-in browser agent.
  - Supports testing modern single-page applications (SPAs).
- **GitHub:** https://github.com/simon-p-j-r/LLM4Pentest
### 10. Watchtower
- **Purpose:** Command-line penetration testing orchestration tool.
- **Key Capabilities:**
  - Orchestrates approximately two dozen security tools.
  - Automates security testing workflows.
  - Automatically generates assessment reports.
- **GitHub:** https://github.com/fzn0x/watchtower
### 11. Pentest Copilot
- **Purpose:** AI assistant connected to a Kali Linux attack machine.
- **Key Capabilities:**
  - Executes security tools through a Kali attack box.
  - Analyzes command output.
  - Determines subsequent testing steps.
- **GitHub:** https://github.com/bugbasesecurity/pentest-copilot
### 12. BlacksmithAI
- **Purpose:** AI-powered penetration testing framework.
- **Key Capabilities:**
  - Uses a lead orchestrator agent.
  - Coordinates multiple specialized agents.
  - Maps agents to different stages of a penetration testing assessment.
- **Article:** https://www.helpnetsecurity.com/2026/03/02/blacksmithai-open-source-ai-powered-penetration-testing-framework/

## Family 2: MCP-Based Security Tool Integration
These projects do not necessarily provide their own intelligence or reasoning engine. Instead, they expose large collections of security tools through the **Model Context Protocol (MCP)**.
**How MCP-Based AI Pentesting Works:**
1. Connect an AI assistant, such as Claude or a coding copilot, to an MCP server.
2. The MCP server exposes security tools to the assistant.
3. The AI model selects and invokes tools.
4. The model analyzes results and determines subsequent actions.
**Important Distinction:** Most of these bridges expose a broad collection of tools without necessarily providing a strong, predefined testing methodology. Our approach will be different: expose focused capabilities and guide the AI using a well-researched methodology rather than simply giving it access to every available tool.
### 1. HexStrike AI
- **Purpose:** MCP-based security tool integration for AI agents.
- **Key Capabilities:**
  - Exposes more than 150 security tools.
  - Allows AI agents to interact with a broad security toolkit.
  - Demonstrates the dual-use nature of autonomous security tools.
  - Has also been abused by real attackers.
- **GitHub:** https://github.com/0x4m4/hexstrike-ai
### 2. AutoPentest AI
- **Purpose:** Agentic penetration testing server.
- **Key Capabilities:**
  - Includes dozens of security tools.
  - Provides more than 100 web security test cases.
  - Supports browser automation.
  - Includes a quality assurance agent to review testing results.
- **GitHub:** https://github.com/bhavsec/autopentest-ai
### 3. Pentest AI Agents
- **Purpose:** Turns Claude Code into a collection of offensive security helpers.
- **Key Capabilities:**
  - Provides AI-assisted penetration testing workflows.
  - Includes a companion server.
  - Provides more than 150 tool wrappers.
- **GitHub:** https://github.com/0xSteph/pentest-ai-agents
### 4. Kali Pentest Skill
- **Purpose:** Gives AI agents access to Kali Linux security tools.
- **Key Capabilities:**
  - Supports more than 200 Kali tools.
  - Includes 15 scenario-based playbooks.
  - Provides approval gates.
  - Pauses for human sign-off before risky actions.
- **GitHub:** https://github.com/x-glacier/kali-pentest
### 5. Transilience Community Tools
- **Purpose:** Collection of community-developed AI security skills.
- **Key Capabilities:**
  - Open security skills.
  - AI-powered pentesting commands.
  - Bug bounty workflows.
- **GitHub:** https://github.com/transilienceai/communitytools

## Family 3: AI-Powered Code Analysis
This family focuses on analyzing source code instead of directly testing live targets. The AI model examines application code, follows data flows, and identifies weaknesses that simple pattern-matching scanners might miss.
**Core Methodology:** Follow the data from the original user input to the dangerous function (Source-to-Sink Analysis).
This approach is closer to the analysis philosophy behind Raptor.
### 1. Vulnhuntr
- **Purpose:** AI-powered source code vulnerability discovery.
- **Key Capabilities:**
  - Uses language models to trace complete data flows.
  - Follows user input through application code.
  - Identifies potentially dangerous function calls.
  - Focuses on Python applications.
  - Has reportedly discovered more than a dozen previously unknown vulnerabilities in major open-source projects.
- **GitHub:** https://github.com/protectai/vulnhuntr

## Family 4: AI Copilots and Assistants
Unlike fully autonomous penetration testing agents, these tools keep a human in control. The AI observes what the security tester is doing, analyzes command output, explains findings, and suggests the next steps.
### 1. Nebula
- **Purpose:** AI assistant integrated directly into the command line.
- **Key Capabilities:**
  - Brings an LLM into the terminal.
  - Suggests the next steps during penetration testing.
  - Explains security tool output.
  - Helps testers understand their findings.
- **GitHub:** https://github.com/berylliumsec/nebula

## The Bigger Picture: Generic AI Frameworks vs. Focused AI Skills
Most frameworks follow the **"Wrap a Model Around Every Tool"** approach.
They provide:
- Large collections of security tools.
- Multiple AI agents.
- Automated execution.
- Tool orchestration.
- Browser and terminal integration.
These are powerful demonstrations of what AI-powered penetration testing can achieve. However, **broad automation is not necessarily the same as deep vulnerability discovery.**
**Our Focused Approach:**
| Generic AI Frameworks | Our Focused Approach |
|---|---|
| Expose hundreds of tools | Expose focused capabilities |
| General-purpose execution | Methodology-driven testing |
| Broad automated workflows | Deep vulnerability research |
| Tool-oriented intelligence | Research-oriented intelligence |
| Generic attack strategies | Target-specific testing strategies |
| General-purpose agents | Specialized AI skills |
**Goal:** Build focused skills grounded in real security methodologies and supported by deep research. These skills should help identify vulnerabilities that generic frameworks might overlook, especially on targets that matter to us.
Learn these existing tools to understand the capabilities and limitations of the easy path. Then build something more specialized and effective.

## Where to Keep Tracking This Space
AI-powered penetration testing is evolving quickly. These two curated resources are useful for following new projects, comparing frameworks, and discovering emerging tools.
### 1. AI Pentesting Agents – 2026
- **Description:** A tested comparison of more than 30 AI penetration testing agents.
- **URL:** https://appsecsanta.com/research/ai-pentesting-agents-2026
### 2. Ostorlab – Open-Source AI Pentest Tools
- **Description:** A focused roundup covering eight open-source AI penetration testing tools in 2026.
- **URL:** https://blog.ostorlab.co/8-open-source-ai-pentest-tools-2026.html

## Quick Reference: All Projects
| Family | Project | Primary Focus |
|---|---|---|
| Autonomous Agents | Raptor | AI security analysis and PoCs |
| Autonomous Agents | PentAGI | Multi-agent pentesting |
| Autonomous Agents | PentestGPT | LLM-guided pentesting |
| Autonomous Agents | Strix | Autonomous application testing |
| Autonomous Agents | NeuroSploit | Multi-agent Kali testing |
| Autonomous Agents | Deadend CLI | Black-box testing |
| Autonomous Agents | CAI | Modular security agents |
| Autonomous Agents | PentestAgent | Black-box testing |
| Autonomous Agents | LLM4Pentest | 200+ security tools |
| Autonomous Agents | Watchtower | Tool orchestration and reporting |
| Autonomous Agents | Pentest Copilot | Kali AI assistant |
| Autonomous Agents | BlacksmithAI | Specialized agent orchestration |
| MCP Integration | HexStrike AI | 150+ security tools |
| MCP Integration | AutoPentest AI | Automated web security testing |
| MCP Integration | Pentest AI Agents | Claude Code security helpers |
| MCP Integration | Kali Pentest Skill | 200+ Kali tools and playbooks |
| MCP Integration | Transilience Community Tools | Security skills and commands |
| Code Analysis | Vulnhuntr | Source-to-sink analysis |
| AI Copilots | Nebula | AI-powered terminal assistance |

**Note:** Project descriptions and numerical capabilities are preserved from the supplied material and have not been independently verified. Check individual repositories for current maintenance status, dependencies, and features.
