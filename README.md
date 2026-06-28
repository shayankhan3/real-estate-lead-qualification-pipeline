# Autonomous Real Estate Lead Qualification & Routing Pipeline 🚀

An enterprise-grade backend automation pipeline designed to capture unstructured real estate property inquiries, dynamically qualify intent using LLM orchestration, and synchronize validated leads into database/CRM structures instantly.

Built entirely using **n8n**, **Groq (Llama 3.3)**, and **custom API/Webhook gateways**.

---

## 🛠️ System Architecture & Workflow

The architecture is built on structured asynchronous data ingestion and robust stateful dialog logic:

```mermaid
flowchart LR
    A[WhatsApp/Webhook Ingress] --> B{Traffic Triage Gateway}
    B -- Static FAQ --> C[Dynamic Q&A Knowledge Node]
    B -- Intent / Lead --> D[Conversational AI Agent Node]
    D --> E[Structured JSON Parser]
    E --> F[Google Sheets CRM Sync]
    E --> G[Agent Route Notification]
