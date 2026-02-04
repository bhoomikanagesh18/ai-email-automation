# ai-email-automation
AI-powered email automation using OpenAI and Gmail API
📧 AI-Powered Email Automation Workflow

This project is an AI-assisted automated email system built using n8n, Google Sheets, and Gmail API.
It reads user data from a Google Sheet and sends personalized confirmation emails automatically at scale with delay control and scheduling.

🚀 Features

📊 Reads recipient data (name & email) from Google Sheets

✉️ Sends personalized HTML email confirmations

🔁 Loops through multiple records automatically

⏳ Adds wait intervals to prevent email throttling

🕒 Can be triggered manually or on a schedule

🔗 Integrates with Gmail API and Google Sheets API

🧠 Use Case

This workflow can be used for:

Workshop or event registration confirmations

Bulk personalized email notifications

Automated onboarding or follow-up emails

Marketing or customer communication workflows

🛠️ Tech Stack

Automation Platform: n8n

APIs Used:

Google Sheets API

Gmail API

Email Format: HTML

Trigger Types: Manual trigger / Scheduled trigger

⚙️ How It Works

Trigger starts manually or via schedule

Google Sheets node fetches rows containing user data

Data is processed in batches

A wait timer controls the sending frequency

Gmail API sends a personalized email to each recipient

Loop continues until all rows are processed

📁 Files

Mail Trigger.json → n8n workflow file

📌 Setup Instructions

Install and run n8n

Import the Mail Trigger.json workflow

Connect your:

Google Sheets account

Gmail account

Update the Google Sheet with:

firstName

Email

Customize the email template (HTML supported)

Run manually or schedule execution

🧩 Example Email Content
Hello {{ firstName }},

Your registration for the AI-powered workshop is confirmed.
We will send joining details soon.

📈 Learning Outcomes

Learned workflow automation using n8n

Integrated multiple APIs into a single pipeline

Implemented batch processing and scheduling logic

Designed scalable communication workflows

Understood practical automation use cases in SaaS
