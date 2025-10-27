# SSoT-Lite

## Project Overview
SSoT-Lite is a proof-of-concept (PoC) MVP, currently in the bootstrap phase, developed within the Coretex Hub initiative. The goal: to provide scalable operational infrastructure and workflow automation for micro-SMBs or self-employed professionals who face operational complexity but lack resources to manage it themselves.

Coretex acts as both operator and technology partner, handling processes for client companies through proprietary solutions and intellectual capital (Coretex IP). An expert network can be engaged on-demand for projects requiring specialized knowledge or advanced complexity.

The project is built on a Single Source of Truth (SSoT) architecture – one consistent truth across all processes, tools, and business decisions. This architecture eliminates inter-layer data errors, synchronizes everything in real-time, and maintains a full process chronology.

***

## Key Components
Google Forms – Used for collecting consultation data from clients.

Google Sheets – Aggregate and synchronize operational data across system layers.

HubSpot CRM – Master Record; authoritative register for clients, projects, experts.

Jira – Logic engine and task execution; contains performance metrics (TS-ROI).

Trello – Coretex team management and project documentation (exclusive to staff).

Obsidian – Stores versioned business logic (Coretex IP), readable for AI agents and used for operations validation, access by single trusted maintainer.

***

## How It Works
Consultation data flows from Google Forms to CRM, where an AI model analyses project details and matches experts using profile data.

The model is continuously trained and validated for skills performance and alignment.

Expert credentialing involves verification and documentation collection. AI agents validate completeness and consistency.

The first expert who accepts a project gets a full Jira brief; production launches after readiness confirmation.

One AI agent routinely exports Jira metadata (to CSV/XML) for auditing, historical integrity, and cloud archiving. This data adds to the client's portfolio for transparent, traceable project records.

***

## AI Agent System
Each dataflow stage is supervised by a defined network of cooperating AI agents. Each agent’s role and logic is precisely encoded (Obsidian process files), and their communication uses RAG (Retrieval Augmented Generation) to prevent cascading errors.

A supervising AI agent actively monitors data consistency across layers. Any issue pauses the workflow and auto-generates a diagnostic report identifying and tracing the problem for swift debugging. This keeps SSoT integrity intact and restores operations quickly.

***

## Core Features
Single source of truth across the entire project lifecycle.

Skill matching and validation using AI models.

Continuous export and archiving of Jira metadata in the client’s portfolio/cloud.

Validation of project documents in Trello referencing CRM and Jira.

Ongoing data verification by AI agents, with built-in state self-checking.

RAG-based mechanisms to prevent cascading errors or information leaks.

Obsidian-based, controlled versioning of business logic for LLM-readability and validation.

Full support for TS-ROI (Time Savings ROI) calculation.

***

## Scalability & Adaptability
The system is both vertically scalable (supports increased projects/processes) and technically adaptable. Its modular architecture allows for seamless migration to platforms like Airtable, Notion, Make, or n8n. Any update propagates deterministically and securely, maintaining data integrity and historical records.

***

## License
© 2025 Coretex / InnovatiffPL – All rights reserved. This project is in MVP stage for research and validation only. Commercial usage or secondary process/code reuse requires IP holder's written permission. Public information is for educational/conceptual purposes only.
