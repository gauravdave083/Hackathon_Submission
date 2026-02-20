# FLX Genie: Where Intelligence Takes Flight

Welcome to the documentation for **FLX Genie**, an LLM-native enterprise intelligence layer purpose-built for airline retailing and NDC operations.

The airline retailing ecosystem, heavily powered by NDC APIs, has grown highly complex and fragmented. FLX Genie addresses this by serving as an intelligent, adaptive, context-aware system capable of interpreting NDC schemas, debugging complex flows, and contextualizing large XML/JSON payloads directly within an organization's secure infrastructure.

---

# 🚨 The Core Problem & Business Impact

Modern airline retail complexity impacts every function across the enterprise, creating heavy dependence on tribal knowledge.

| Problem | Business Impact |
|----------|----------------|
| Knowledge scattered across tools | Slow decision-making |
| Employees depend on SMEs | Bottlenecks |
| Third Party enterprise tools to empower AI use | High operational cost |
| Long onboarding time | Productivity loss |
| External AI tools blocked due to security | Innovation slowdown |

> Your employees already want AI — they’re just not allowed to use it safely.

---

# 📸 Interface Overview

FLX Genie integrates seamlessly into the daily workflow of enterprise teams.

- **User Profile & Authentication**
- **Chat Interface** – Context-aware inquiry for NDC APIs
- **Saved Prompts & Tools** – Quick access to document summarization and data extraction
- **File Upload** – Drag-and-drop support for PDF, DOCX, CSV, TXT
- **Agent Selection** – Dynamic switching between specialized agents
- **Global Search** – Intelligent search across past conversations

---

# 🏗 High-Level Architecture (HLD)

FLX Genie is designed on AWS Well-Architected principles, ensuring private, secure, and observable AI adoption.

![Chat Interface](Images/AWS.png)


## Architecture Components

### 1️⃣ Edge & Routing
- AWS WAF secures incoming traffic
- CloudFront optimizes delivery
- Application Load Balancer routes traffic internally

### 2️⃣ Backend Services
- FastAPI backend running in private subnet
- Secure request handling

### 3️⃣ AI Orchestration
- LangChain coordinates workflows
- Context memory management
- Agent routing

### 4️⃣ Inference Layer
- Private LLM/SLM endpoints
- Hosted natively on Amazon SageMaker
- Supports GPT-OSS / LLaMA-class models

### 5️⃣ Knowledge Retrieval (RAG)
- Embedding model converts enterprise documents into vectors
- Stored in:
  - OpenSearch
  - Pinecone
- Enables contextual intelligence

### 6️⃣ Storage & Security
- Amazon S3 (encrypted with AWS KMS)
- AWS Cognito for authentication
- IAM & Secrets Manager for RBAC
- Region-specific deployment

### 7️⃣ Observability
- CloudWatch monitoring
- AWS X-Ray tracing

---

# 🚀 Key Use Cases & Capabilities

FLX Genie is not a standalone chatbot; it is the central operating system of an extensible AI ecosystem.

---

## 1️⃣ NDC Offer & Order Intelligence

- Explains offers and pricing logic
- Detects airline-specific inconsistencies
- Validates schema deviations
- Debugs complex XML/JSON payloads

---

## 2️⃣ Autonomous QA Agent

- Validates NDC schemas automatically
- Generates automated test cases from schema changes
- Performs semantic & business-aware validation
- Analyzes XML payloads, trace logs, API responses

---

## 3️⃣ Reshop & Exchange AI Copilot

- Explains complex reshop logic
- Suggests optimal exchange routes
- Compares Reshop types:
  - Even
  - AddCollect
  - Residual
- Auto-fixes direct channel requests

---

## 4️⃣ Smart Documentation Engine

- Generates airline-specific NDC documentation
- Creates Jira tickets and technical comments
- Instantly updates documentation when schemas change

---

## 5️⃣ Architect & Business Consultant Companion

- Translates business requirements into technical specs
- Designs High-Level Documents (HLDs)
- Recommends scalable AWS architectures
- Generates solution diagrams
- Performs data-driven impact analysis
- Creates BRDs, PRDs, wireframes

---

# 🔐 Enterprise-Grade Security & Compliance

FLX Genie is built for organizations where data privacy is critical.

### Privacy by Design
- Data never leaves your controlled environment
- No external training on enterprise data

### Access Control
- Strict role-based access control
- Secure authentication via Cognito

### Full Auditability
- Complete audit logs
- Region-specific deployments
- Data sovereignty compliance

---

# ❓ Why Not Just Use Public AI Tools?

| Feature | FLX Genie | Public AI Tools |
|----------|------------|----------------|
| Uses internal enterprise data | ✅ | ❌ |
| Data stays completely private | ✅ | ❌ |
| Cost predictability | ✅ | ❌ |
| Role-based access control | ✅ | ❌ |
| Compliance friendly | ✅ | ❌ |
| Custom airline retail workflows | ✅ | ❌ |

---

# 💰 AWS Costing Model (Resilient, Multi-Region)

Designed for predictable scaling across 100–500 enterprise users.

## Assumptions

- Primary Region: ap-south-1 (Mumbai)
- DR Region: ap-southeast-1 (Singapore)
- LLM hosted privately (GPT-OSS / LLaMA-class)
- High Availability across Multi-AZ
- DR = Warm Standby

---

## Core Compute – LLM Inference Layer (Primary Cost Center)

| Component | Instance Type | Primary | DR |
|------------|---------------|----------|------|
| EC2 for LLM | GPU (g5.xlarge / p4d) | Scaled to Load | Warm Standby |
| Vector DB | OpenSearch Serverless / Managed | Auto-scaling | Replicated |
| Backend API | Fargate / EKS | Auto-scaling | Warm Standby |

---

# 📊 Cost Efficiency

At **under $15 per employee per year**, FLX Genie unlocks massive productivity gains while keeping all enterprise data fully private.

---

# 🌍 The Vision

FLX Genie is more than an AI assistant.

It is the intelligent layer powering the future of airline retail —  
where intelligence takes flight.
