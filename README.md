n8n AI Customer Feedback AgentAn automated, end-to-end workflow built in n8n that uses an Advanced AI Agent (OpenAI) to capture, analyze, categorize, and route customer feedback in real-time.🎯 Purpose & ScopeCore Objective: Eliminate manual feedback triage by automatically segregating incoming submissions and routing them to the correct department.Success Metric: Designed to reduce manual administrative sorting efforts by at least 30%.⚡ Trigger & FlowTrigger: Initiated instantly via an On Form Submission trigger.Analysis: Raw form text is processed by an AI Agent / OpenAI Chat Model to determine user intent and sentiment contextually.Categorization & Branching: A Switch Node routes the classified data into three distinct paths:🔴 Complaint: Logs record to Airtable $\rightarrow$ Alerts the team via Slack $\rightarrow$ Triggers an automated follow-up email via Gmail.✨ Compliment: Logs record to Airtable $\rightarrow$ Routes to the owners'/management Slack channel.💡 Feature Addition: Logs record to Airtable $\rightarrow$ Routes to the product/feature development Slack channel.🗺️ Architectural BlueprintPlaintext[Form Submission] 
       │
       ▼
[AI Agent (OpenAI)] ──> [Merge Node] ──> [Switch Node]
                                              │
       ┌──────────────────┬───────────────────┴───────────────────┐
       ▼                  ▼                                       ▼
  [Complain]         [Compliment]                       [Feature Addition]
       │                  │                                       │
       ├─> Airtable       ├─> Airtable                            ├─> Airtable
       ├─> Slack Alert    └─> Slack (Owners Channel)              └─> Slack (Dev Channel)
       └─> Gmail (Customer Reply)
🧰 Tech Stack & ToolsWorkflow Engine: n8nAI Model: OpenAI (Advanced AI Agent Node)Logic Routing: Switch NodeDatabase / Logging: AirtableNotifications & Messaging: SlackEmail Automation: Gmail🚀 Getting StartedImport the provided workflow JSON file into your n8n instance.Configure your credentials for:OpenAI APIAirtableSlack WorkspaceGmail AccountConnect your frontend form tool to the n8n webhook endpoint.Activate the workflow and test an end-to-end submission!
