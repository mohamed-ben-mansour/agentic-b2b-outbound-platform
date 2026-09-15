# Nudge AI Outbound : agentic-b2b-outbound-platform
Production-grade multi-agent platform for autonomous B2B outbound, from ICP discovery and lead qualification to multi-source enrichment, personalized sequence generation, human validation, message generation, adaptive sequence execution, and outbound message sending.



##  Architecture & Core Stack: 
The Nudge AI Outbound platform is built on a production-grade Multi-Repo Architecture powered by LangGraph.Instead of a monolithic codebase, each agent of our autonomous B2B outbound workflow is isolated into its own dedicated repository as a specialized LangGraph subgraph. This ensures:
### Reusability & Standalone Utility : 
Each agent can function as a completely standalone service. For example, the Multi-Source Enrichment Agent can be plugged directly into an internal data pipeline or CRM workflow completely independent of the broader outbound platform.
### Domain Isolation :
Teams can deploy, version, and update individual agents without rebuilding the entire pipeline.
### Stateful Orchestration:
LangGraph statefully routes data across these distributed repositories, allowing seamless human-in-the-loop (HITL) validation.
## Agents: 
Each agent below operates as an independent LangGraph microservice. Click the icons below to view the specific codebases for each pipeline stage:

[![Intelligence Sourcer](https://img.shields.io/badge/Agent-Intelligence%20Sourcer-2ea44f?style=for-the-badge)](https://github.com/mohamed-ben-mansour/nudge-intelligence-sourcer)
Finds and gathers new leads.

[![Qualifier Engine](https://img.shields.io/badge/Agent-Qualifier%20Engine-2ea44f?style=for-the-badge)](https://github.com/mohamed-ben-mansour/nudge-qualifier-engine)
Checks each lead, and keeps the good ones.

[![Personalization Engine](https://img.shields.io/badge/Agent-Personalization%20Engine-2ea44f?style=for-the-badge)](https://github.com/mohamed-ben-mansour/nudge-personalization-engine)
Writes personalized outreach for each lead.

[![Orchestrator](https://img.shields.io/badge/Agent-Orchestrator-2ea44f?style=for-the-badge)](https://github.com/mohamed-ben-mansour/nudge_ai_outbound_orchestrator)
Runs every agent in order, and passes leads between them.

[![Dashboard](https://img.shields.io/badge/View-Dashboard-007ec6?style=for-the-badge)](https://github.com/mohamed-ben-mansour/nudge-ai-outbound-dashboard)
Shows the full pipeline, live.
