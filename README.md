# Microsoft-Copilot-Agent-Spectrum
Microsoft Copilot Agent Spectrum: From Retrieval to Autonomous Systems

# AI Agent Spectrum Demo

A practical demo project that shows how to build three types of AI agents using Microsoft Copilot, Copilot Studio, SharePoint, Power Automate, and external business systems.

This project is based on a simple idea: **AI becomes valuable when it automates real business workflows**.

Instead of building one generic chatbot, this repo demonstrates a progression from:

1. **Retrieval Agent** – answers questions from trusted documents
2. **Task Agent** – reads and writes data to business systems
3. **Autonomous Agent** – runs on triggers and performs work independently

---

## Project Overview

This repo explains and demonstrates a three-level AI agent model:

### 1. Retrieval-Based Agent
A grounded agent that answers questions using documents provided by the organization.

**Example use case:**
- HR benefits assistant that answers questions about 401k, medical benefits, PTO, and employee reviews

**Key capability:**
- Reads documents
- Summarizes information
- Responds with grounded answers

**Typical tools:**
- Microsoft 365 Copilot
- Agent Builder
- SharePoint knowledge sources

---

### 2. Task-Based Agent
An agent that goes beyond answering questions and can take actions in connected systems.

**Example use case:**
- HR assistant that checks vacation balances and books PTO in ServiceNow

**Key capability:**
- Reads business data
- Writes updates back to systems
- Automates repetitive workflows

**Typical tools:**
- Copilot Studio
- Power Automate
- ServiceNow connector
- SharePoint knowledge sources

---

### 3. Autonomous Agent
An agent that works independently when a trigger occurs.

**Example use case:**
- Inbox assistant that watches for new emails, drafts responses using company documentation, and saves drafts for human review

**Key capability:**
- Watches for triggers
- Executes actions automatically
- Supports human-in-the-loop review

**Typical tools:**
- Copilot Studio
- Trigger-based workflows
- Outlook / email integration
- Connected documentation sources

---

## Why This Project Matters

Most AI demos are fluff. This one is not.

This project focuses on **real business value**:
- reducing repetitive manual work
- improving response speed
- connecting AI to actual business systems
- supporting secure and governed AI adoption

Two concrete examples:
- Instead of telling an employee where the PTO policy is, the agent can **book PTO**.
- Instead of waiting for support staff to answer repeated email questions, the agent can **draft responses automatically**.

---

## Architecture Summary

```text
User / Trigger
   |
   v
AI Agent Layer
   |
   +--> Retrieval from SharePoint / Docs
   +--> Actions through Copilot Studio
   +--> Flows through Power Automate
   +--> Read/Write operations in external systems (ex: ServiceNow)
   |
   v
Business Outcome
```

---

## Included Agent Patterns

### Agent 1: HR Knowledge Assistant
**Type:** Retrieval Agent  
**Purpose:** Answer employee questions using HR policy documents

**Example prompts:**
- What does the 401k plan include?
- What is the employee review process?

**Input source:**
- SharePoint HR documents

**Output:**
- Grounded summaries and cited document responses

---

### Agent 2: HR PTO Assistant
**Type:** Task Agent  
**Purpose:** Retrieve vacation balances and update PTO requests

**Example prompts:**
- How many vacation hours does Michael have?
- Book 15 hours of PTO for Taylor

**Input sources:**
- SharePoint HR policies
- ServiceNow vacation data

**Actions:**
- Read records from ServiceNow
- Update PTO balance using Power Automate flow

---

### Agent 3: Inbox Auto-Reply Assistant
**Type:** Autonomous Agent  
**Purpose:** Monitor incoming email and draft responses automatically

**Example triggers:**
- New email arrives in inbox
- Customer asks a product or support question

**Actions:**
- Read email
- Search documentation
- Generate draft response
- Save result for human review

---

## Tech Stack

- **Microsoft 365 Copilot**
- **Microsoft Copilot Studio**
- **Agent Builder**
- **SharePoint**
- **Power Automate**
- **ServiceNow**
- **Outlook / Exchange**
- **Microsoft Teams**

---

## Core Concepts Demonstrated

### Grounding
The agent should respond using approved enterprise documents instead of random model guesses.

**Examples:**
- HR policy documents in SharePoint
- Internal product documentation for support replies

### Actions
The agent becomes useful when it can do more than talk.

**Examples:**
- Create or update PTO entries
- Trigger workflows in external systems

### Triggers
Autonomy starts when the agent no longer waits for a user prompt.

**Examples:**
- New email received
- New ticket created

### Human-in-the-loop
Autonomous does not mean uncontrolled.

**Examples:**
- Save draft replies for review before sending
- Require approval before updating a sensitive system

---

## Security and Responsible AI Considerations

This project is designed with enterprise constraints in mind.

Important considerations include:
- data privacy
- least-privilege access
- secure connector configuration
- responsible use of generated outputs
- accessibility
- auditability
- governance over agent publishing and usage

Two examples of what should be controlled:
- A vacation agent should **not** let every employee view everyone else’s PTO balance.
- An autonomous email agent should **not** send replies directly without review in high-risk scenarios.

---

## Example Business Use Cases

This pattern can be adapted across departments.

### HR
- Benefits Q&A assistant
- PTO booking assistant

### IT
- Help desk agent for common support requests
- Password reset or onboarding workflow agent

### Customer Service
- Auto-draft support email responses
- Ticket triage assistant

### Finance
- Policy retrieval for expense rules
- Invoice or approval workflow assistant

---

## Repository Structure

```text
.
├── README.md
├── docs/
│   ├── architecture-overview.md
│   ├── agent-spectrum.md
│   └── security-and-governance.md
├── demos/
│   ├── retrieval-agent-demo.md
│   ├── task-agent-demo.md
│   └── autonomous-agent-demo.md
├── flows/
│   └── power-automate-notes.md
├── screenshots/
└── examples/
    ├── prompts.md
    └── sample-use-cases.md
```

---

## How to Use This Repo

1. Review the three agent patterns
2. Start with the retrieval agent first
3. Add business actions through connectors and flows
4. Add triggers only when the workflow is stable and safe
5. Keep a human approval step where risk is high

That order matters.

Two examples of bad implementation:
- Building an autonomous agent first without grounding or guardrails
- Letting an agent write to live business systems before testing read-only behavior

---

## Suggested Demo Flow

If you are presenting this project, use this sequence:

1. Show a grounded retrieval agent answering HR questions
2. Show a task agent checking and booking PTO
3. Show an autonomous inbox agent reacting to incoming emails
4. Explain why each level adds more value and more responsibility

---

## What I Built / What This Demonstrates

This project demonstrates my approach to AI solution design:

- start with a clear business workflow
- ground the agent in trusted enterprise data
- connect the agent to real systems when action is needed
- use triggers carefully for autonomy
- keep security, governance, and human review built into the design

This is not just prompt engineering. It is workflow automation with AI in the loop.

---

## Future Improvements

Possible next steps for this project:
- add architecture diagrams
- include sample Power Automate flow screenshots
- add demo videos
- publish sanitized example prompts
- document connector setup steps
- add governance checklist for enterprise deployment

---

## Disclaimer

This repository is intended for demonstration and educational purposes. Any sample business data, employee names, or workflows should be sanitized before sharing publicly.

---

## Contact

If you are reviewing this project as part of a hiring process, I’d be glad to walk through:
- the business problem being solved
- the architecture decisions
- the tradeoffs between retrieval, task, and autonomous agents
- the security and governance considerations

---

## License

This project is shared as a portfolio/demo artifact unless otherwise specified.
