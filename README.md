# Agentic Web
A concise introduction to the Agentic Web and how it differs from the World Wide Web we know today.

## What is the Agentic Web?
The Agentic Web is an evolution of the current World Wide Web where autonomous software agents — not just human users or passive servers — act as first-class participants. These agents can discover information, make decisions, negotiate, transact, and coordinate on behalf of users or organizations. They interact with services, APIs, and other agents across the network to accomplish multi-step goals with varying degrees of autonomy.

Key characteristics:
- Autonomous behavior: agents can execute tasks and make decisions without continuous human direction.
- Goal-driven workflows: agents accept goals or intents and plan multi-step interactions to achieve them.
- Inter-agent coordination: agents can communicate, negotiate, and form temporary collaborations.
- Programmatic trust & governance: strong emphasis on verifiable identities, permissions, and policy enforcement.

## How the Agentic Web differs from the traditional World Wide Web
While the current World Wide Web focuses on humans navigating information and services (browsers, links, and user-driven interactions), the Agentic Web shifts toward automated, goal-oriented agents interacting on behalf of humans or organizations. The differences include:

- Roles and actors:
  - WWW: Human users browse, click, and consume content. Servers provide resources. APIs augment interactivity.
  - Agentic Web: Autonomous agents are active participants alongside humans and servers. Agents can initiate interactions, aggregate data, and take actions.

- Interaction model:
  - WWW: Mostly request/response and UI-driven flows.
  - Agentic Web: Programmatic conversations, multi-step protocols, background planning, and stateful workflows across services.

- Intent and agency:
  - WWW: Actions are typically explicit and user-initiated.
  - Agentic Web: Agents carry intent, pursue goals, and make local decisions within policy constraints.

- Trust, safety, and governance:
  - WWW: Relies on user consent, access controls, and centralized platform policies.
  - Agentic Web: Requires richer, machine-readable policies, verifiable agent identities, audit trails, and runtime governance to manage autonomous actions.

- Scale and dynamics:
  - WWW: Human scale and interactive latency expectations.
  - Agentic Web: Higher throughput of automated interactions, asynchronous task execution, and long-running collaborations.

## Why it matters
The Agentic Web promises higher automation, personalized services that proactively act for users, and faster composition of complex tasks across distributed services. It can boost productivity, enable new business models, and power more capable consumer and enterprise applications.

## Risks & safeguards
Because agents act autonomously, the Agentic Web raises important risks: unintended or harmful actions, privacy leaks, deceptive behaviors, and emergent coordination that violates norms. Mitigations include strict identity and capability controls, policy-as-code, transparent audit logs, human-in-the-loop controls for high-risk actions, and standardized safety protocols.

## Learn more
This README is a brief overview. For deeper study, look for resources on autonomous agents, policy-as-code, decentralized identity (DID), agent communication languages, and research on safe multi-agent systems.

# Agentic Web protocols
The Agentic Web builds on a set of existing standards and protocols that enable agent identity, secure messaging, credentialing, and agent-to-agent interaction. Below are short introductions to widely recognized protocols and specifications that play a role in agentic systems.

## Decentralized Identifiers (DIDs)
Brief: DIDs provide a standard, blockchain-agnostic way to create and resolve unique identifiers for agents (human or software). They let agents own identifiers that can be cryptographically controlled without central registries.

Reference: W3C Decentralized Identifiers (DID) Core — https://www.w3.org/TR/did-core/

## Verifiable Credentials (VCs)
Brief: Verifiable Credentials are machine-readable credentials (claims) that can be issued to, stored by, and presented by agents. VCs enable agents to prove attributes or claims about themselves in a privacy-preserving, verifiable way.

Reference: W3C Verifiable Credentials Data Model — https://www.w3.org/TR/vc-data-model/

## DIDComm Messaging
Brief: DIDComm defines secure, private, end-to-end encrypted messaging patterns for peer-to-peer agent communication using DIDs for addressing. It includes message packaging, routing, and transport-agnostic formats suitable for agent-to-agent protocols.

Reference: Decentralized Identity Foundation — DIDComm Messaging Spec — https://identity.foundation/didcomm-messaging/

## ActivityPub
Brief: ActivityPub is a decentralized social networking protocol that defines actor-to-actor messaging, activity streams, and federation. While originally designed for social applications, its activity-centric, actor-based model is useful for agent interactions across federated services.

Reference: W3C ActivityPub Recommendation — https://www.w3.org/TR/activitypub/

## FIPA ACL (Agent Communication Language)
Brief: FIPA ACL is a standardized agent communication language developed for multi-agent systems. It defines communicative acts (performatives), message structure, and semantics for agent interaction patterns in distributed systems.

Reference: FIPA ACL Message Structure Specification — https://www.fipa.org/specs/fipa00061/

## KQML (Knowledge Query and Manipulation Language)
Brief: KQML is an early, influential agent communication language and message-oriented protocol that introduced performatives (e.g., ask, tell, achieve) used by agents to exchange knowledge and requests. KQML influenced later ACLs and agent messaging designs.

Reference: Finin, Tim, et al., "KQML — An Overview" and related KQML resources (original papers and archives) — see academic archives and project pages for the canonical publications.

### Additional links & resources
Below are key specifications, implementations, and resources referenced in this README and commonly used when building Agentic Web systems. Where possible I included authoritative sources (W3C, DIF, standards bodies).

- W3C Decentralized Identifiers (DID) Core: https://www.w3.org/TR/did-core/
- W3C Verifiable Credentials Data Model: https://www.w3.org/TR/vc-data-model/
- DIDComm Messaging (Decentralized Identity Foundation): https://identity.foundation/didcomm-messaging/
- W3C ActivityPub: https://www.w3.org/TR/activitypub/
- FIPA ACL (Agent Communication Language) specification: https://www.fipa.org/specs/fipa00061/
- KQML — original papers and archives (search academic archives for canonical KQML publications)
- Interledger (payments interoperability): https://interledger.org/
- ISO 20022 (financial messaging standards): https://www.iso20022.org/
- Model Cards for Model Reporting (useful background for model metadata / MCP foundations): https://arxiv.org/abs/1810.03993
- Hyperledger Aries (agent frameworks and DID implementations): https://www.hyperledger.org/use/aries

# Agentic Protocols Definitions
## MCP (Model Context Protocol)
Brief: The Model Context Protocol (MCP) defines how agents advertise, request, and share contextual model information and runtime model capabilities. MCP enables agents to discover model endpoints, exchange model metadata (version, capabilities, input/output contract), and negotiate model usage policies and constraints that affect planning and execution.

Reference: See research and working drafts on model metadata and model cards for foundations (e.g., "Model Cards for Model Reporting" by Mitchell et al.) and emerging MCP drafts from agentic standards efforts. If you have a canonical MCP spec, add that link here for a direct authoritative reference.

## A2A (Agent-to-Agent Communication)
Brief: A2A covers the collection of standards and patterns for direct agent-to-agent messaging, including addressing, message envelopes, performatives, and conversation management. A2A systems rely on secure addressing (DIDs), message privacy (DIDComm or similar), and agreed semantic performatives (ACL/KQML-style).

Reference: Relevant authoritative sources include the FIPA ACL specification (for performatives/semantics) and DIDComm (for secure peer-to-peer messaging):
- FIPA ACL: https://www.fipa.org/specs/fipa00061/
- DIDComm (DIF): https://identity.foundation/didcomm-messaging/

## ANP (Agent Network Protocol)
Brief: ANP refers to networking and discovery protocols that let agents find, advertise, and route requests through an agent overlay or federation. ANP covers discovery, routing, and federation semantics so agents can operate across organizational boundaries.

Reference: ANP ideas draw from federation and activity-stream protocols such as ActivityPub (actor/discovery semantics) and routing concepts from DIDComm routing overlays:
- ActivityPub (federation model): https://www.w3.org/TR/activitypub/
- DIDComm routing patterns: https://identity.foundation/didcomm-messaging/

## ACP (Agentic Commerce Protocol)
Brief: ACP defines commerce-specific message flows, offers, order negotiation, digital contract formation, and verifiable commercial claims between agents (buyer agents, seller agents, escrow agents). It ties credentialing (VCs), payments (AP2/ILP), and policy-driven negotiation into commerce workflows.

Reference: Standards that inform ACP include verifiable credentials for claims and commercial messaging conventions and financial messaging standards such as ISO 20022. For payment rails and interoperability, see Interledger and ISO work:
- W3C Verifiable Credentials: https://www.w3.org/TR/vc-data-model/
- ISO 20022 (financial messaging): https://www.iso20022.org/
- Interledger (payments interoperability): https://interledger.org/

## AP2 (Agent Payments Protocol)
Brief: AP2 specifies how agents execute, authorize, and settle payments. AP2 includes payment request/authorization messages, receipt/settlement flows, and links to payment rails or interledger mechanisms. It is designed so agent payments can be atomic, auditable, and tied to verifiable receipts and credentials.

Reference: Foundational payment and interoperability specs include Interledger (for cross-ledger payments), ISO 20022 (messaging), and work around programmable on-chain/off-chain payments. See:
- Interledger Protocol: https://interledger.org/
- ISO 20022: https://www.iso20022.org/

## NLWeb Protocol
Brief: The NLWeb protocol is an open-source framework developed by Microsoft to enable conversational interfaces for websites. It simplifies the integration of natural language processing (NLP) capabilities, allowing users to interact with websites using everyday language. This protocol bridges structured website data with AI models, making it accessible to both humans and AI agents. 

NLWeb leverages Model Context Protocol (MCP), which acts as a standard for enabling AI agents and chatbots to interact with websites. MCP is to NLWeb what HTTP is to HTML, providing a foundational layer for conversational AI on the web. The protocol uses Schema.org and other semi-structured formats like RSS to organize and share data, ensuring compatibility with millions of websites.

NLWeb is platform-agnostic, supporting major operating systems (Windows, macOS, Linux) and AI models (OpenAI, Anthropic, Gemini, etc.). It is lightweight and scalable, capable of running on anything from data center clusters to laptops.

Reference: Introducing NLWeb: Brining conversational interfaces directly to the web.
- https://news.microsoft.com/source/features/company-news/introducing-nlweb-bringing-conversational-interfaces-directly-to-the-web/?msockid=35ff00aff67f621f0a4114dcf7546395

## Agent-user Interaction Protocol
Brief: AG-UI is an open, lightweight, event-based protocol that standardizes how AI agents connect to user-facing applications.

Reference: Agent-User Interaction Protocol (AG-UI)
- https://docs.ag-ui.com/introduction

### Links and additional resources
Below are the links and labels you provided (included verbatim):

- W3C AI Agent Protocol (AAP)
  - https://www.w3.org/community/agentprotocol/
  - https://w3c-cg.github.io/ai-agent-protocol/

- OpenAI Agentic Commerce Protocol (ACP)
  - https://developers.openai.com/commerce
  - https://github.com/agentic-commerce-protocol/agentic-commerce-protocol

- Anthropic Model Context Protocol (MCP)
  - https://www.anthropic.com/news/model-context-protocol
  - https://modelcontextprotocol.io/docs/getting-started/intro

- IBM Agent Communication Protocol (ACP)
  - https://research.ibm.com/projects/agent-communication-protocol

- Google Agent 2 Agent Protocol (A2A)
  - https://a2a-protocol.org/dev/

- Google Agent Payments Protocol (AP2)
  - https://cloud.google.com/blog/products/ai-machine-learning/announcing-agents-to-payments-ap2-protocol
  - https://a2a-protocol.org/latest/

- Agent Network Protocol (ANP)
  - https://agentnetworkprotocol.com/en/
  - https://github.com/agent-network-protocol

- NLWeb Protocol
  - https://github.com/nlweb-ai/NLWeb

- Agent-User Interaction Protocol (AG-UI)
  - https://docs.ag-ui.com/introduction

# Agentic Stacks
In addition to frameworks and protocols, there are several ongoing projects geared towards building the next tecnology stack that powers the agentic web. 

- AGNTCY
  - https://agntcy.org/

# Agentic Patterns
Multi-agent systems follow a typical pattern. These have been identified as follows. 

- Microsoft
  - https://microsoft.github.io/multi-agent-reference-architecture/index.html
  - https://learn.microsoft.com/en-us/azure/architecture/ai-ml/guide/ai-agent-design-patterns

- AWS
  - https://strandsagents.com/latest/documentation/docs/user-guide/concepts/multi-agent/multi-agent-patterns/

- Google
  - https://docs.cloud.google.com/architecture/choose-design-pattern-agentic-ai-system

# Agentic Frameworks
Agent Building Frameworks that enable you to build multiagent systems. Here are the few well known in the industry. 

- Google Agent Development Kit (ADK)
  - https://google.github.io/adk-docs/get-started/

- AWS Strands Agents SDK
  - https://strandsagents.com/latest/

- Microsoft Agent Framework (MAF)
  - https://learn.microsoft.com/en-us/agent-framework/overview/agent-framework-overview
  - https://github.com/microsoft/agent-framework

- OpenAI Agents SDK
  - https://platform.openai.com/docs/guides/agents-sdk

- Anthropic Agent SDK
  - https://www.anthropic.com/engineering/building-agents-with-the-claude-agent-sdk

- CrewAI
  - https://github.com/crewAIInc/crewAI

- LangChain
  - https://www.langchain.com/

# Agentic for Beginners
Learn how to develop AI Agents

- Microsoft Agent Framework Quick Start guide (Python)
  - https://learn.microsoft.com/en-us/agent-framework/tutorials/quick-start?pivots=programming-language-python


- Microsoft GenAI for Beginners
  - https://github.com/microsoft/generative-ai-for-beginners

- Microsoft AI Agents for Beginners
  - https://microsoft.github.io/ai-agents-for-beginners/14-microsoft-agent-framework/