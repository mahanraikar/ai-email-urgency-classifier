# AI Email Urgency Classifier & Gmail Automation Agent

An AI-driven email automation agent built using n8n and OpenAI that classifies incoming Gmail messages by urgency, applies labels automatically, and sends notifications for time-critical emails.
This project demonstrates a production-style AI agent workflow combining LLM reasoning, memory, and API-based automation.

---

## Overview

Email overload often leads to missed priorities. This agent continuously monitors incoming Gmail messages, evaluates their urgency using an AI model, and performs predefined actions based on the classification. Once configured, the system operates fully autonomously.

---

## Key Capabilities

* Continuous Gmail monitoring via triggers
* AI-based urgency classification with concise reasoning
* Automatic Gmail label assignment
* Notification email for urgent messages
* Thread-level context handling using memory
* Modular and extensible agent architecture

---

## Urgency Classification

Each email is classified into one of the following categories:

* Urgent – Requires immediate attention (within hours)
* High Priority – Action required within one business day
* Normal – No immediate deadline
* Low Priority – Informational or optional follow-up

Classification is based on tone, intent, deadlines, and urgency-related keywords.

---

## Technology Stack

* n8n – Workflow orchestration and automation
* OpenAI (GPT-5 Mini) – Natural language reasoning
* LangChain Agent (n8n) – AI agent execution framework
* Gmail API – Email read, label, and send operations

---

## Workflow Architecture

1. Gmail Trigger detects new incoming emails
2. Email content is passed to the AI Agent
3. The AI model determines urgency and reasoning
4. Gmail labels are applied automatically
5. A notification email is sent for urgent cases

---

## Repository Structure

ai-email-urgency-agent/
├── AI Email Urgency Classifier & Gmail Labeler.json
└── README.md

---

## Setup Instructions

1. Set up an n8n instance (cloud or self-hosted)
2. Import the provided workflow JSON file
3. Configure credentials:

   * Gmail OAuth (read, modify, send permissions)
   * OpenAI API key
4. Activate the workflow
5. Send test emails to verify classification and automation

---

## Operational Notes

* Gmail API scopes must allow label modification
* Gmail label IDs can be customized as needed
* The AI prompt can be adapted to organization-specific rules
* Suitable for personal, startup, or enterprise inbox automation

---

## Future Enhancements

* Confidence scoring for urgency classification
* Multi-label or topic-based categorization
* Slack, Microsoft Teams, or WhatsApp notifications
* Integration with CRM or ticketing systems
* Fine-tuned models for domain-specific email workflows

---

## Author

Mahan Raikar
AI Automation • LLM Agents • Workflow Engineering

---

## License

This project is provided for educational and demonstration purposes.
