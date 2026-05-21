🤖 AI-Powered Lead Automation — n8n Workflow

🧩 Problem Statement
Most businesses receive leads through forms but waste hours manually reading, qualifying, and logging them. This project eliminates that manual work entirely using AI automation.

💡 What This Workflow Does
When someone fills a Google Form, this workflow automatically:

Detects the new entry in Google Sheets
Sends the data to Groq AI (Llama 3.1) for analysis
Emails an AI-generated summary to the business owner
Logs the AI summary back into Google Sheets for records

Zero manual work. Fully automated.

🔁 Workflow Architecture
Google Form → Google Sheets Trigger → Groq AI (HTTP Request) → Gmail → Google Sheets Update

🔧 Tools & Technologies
ToolPurposen8nWorkflow automation (self-hosted via Docker)Google SheetsLead data storage & trigger sourceGoogle FormsLead captureGroq API (Llama 3.1-8b-instant)AI lead analysis & summarizationGmail APIAutomated email notificationsDockerLocal self-hosting of n8n

🧠 AI Prompt Used
Analyze this lead and give a 2 line summary:
Name: [Name], Email: [Email], Message: [Message]
The AI returns a concise qualification summary like:

"High priority lead — interested in sales automation, clear use case mentioned. Recommend immediate follow-up."


📈 Business Impact

Eliminates manual lead reading and qualification
Ensures zero leads are missed or forgotten
Gives instant AI-powered priority scoring
Automatically maintains a log of all AI summaries in Google Sheets


🚀 How to Run Locally

Install Docker Desktop
Run n8n:

docker run -it --rm --name n8n -p 5678:5678 -v n8n_data:/home/node/.n8n docker.n8n.io/n8nio/n8n

Open http://localhost:5678
Import the workflow JSON from this repository
Add your credentials — Google Sheets, Gmail, Groq API


👤 Author
Santosh Jaiswal
Data & Business Analyst | Mumbai, India
LinkedIn • GitHub
