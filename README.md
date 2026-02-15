AI EMAIL AUTOMATION PROJECT
===========================

Project Overview
----------------
This project is an automated email system built using n8n, Google Sheets, and the Gmail API.  
It sends personalized bulk emails automatically using data stored in Google Sheets.

The system is designed to save time and automate repetitive email tasks such as confirmations, notifications, and marketing emails.


Key Features
------------
- Reads recipient name and email from Google Sheets
- Sends personalized HTML emails
- Processes multiple records automatically
- Adds 2-second wait between emails to avoid spam detection
- Supports manual and scheduled triggers
- Integrates with Gmail API and Google Sheets API


Use Cases
---------
This workflow can be used for:

- Workshop or event confirmation emails
- Bulk personalized email notifications
- Automated onboarding emails
- Marketing campaigns
- Newsletter distribution


Technology Used
---------------
Automation Platform: n8n  
APIs: Google Sheets API, Gmail API  
Email Format: HTML  
Triggers: Manual and Scheduled (Daily 10 AM)


How the Workflow Works
----------------------
1. Workflow starts using manual trigger or scheduled trigger.
2. Google Sheets node reads all rows containing Email and firstName.
3. Split in Batches processes one row at a time.
4. Wait node adds 2 seconds delay to avoid rate limiting.
5. Gmail node sends personalized email.
6. Loop continues until all rows are processed.


Project Folder Structure
------------------------
ai-email-automation/

- workflows/
  - Mail_Trigger.json (n8n workflow file)

- README.md (documentation)

- .gitignore (ignores credentials and sensitive files)


Setup Instructions
------------------

Prerequisites:
- n8n installed (cloud or local)
- Google account
- Gmail account for sending emails

Import Workflow:
1. Open n8n dashboard.
2. Click Workflows.
3. Select Import.
4. Upload Mail_Trigger.json file.

Connect Credentials:
- Connect Google Sheets OAuth2 account.
- Connect Gmail OAuth2 account.

Configure Google Sheet:
Create a sheet with the following columns:

Email | firstName  
john@example.com | John  
sarah@example.com | Sarah  

Customize Email Template:
Edit the email content inside the Gmail node.
Change workshop details, message, or branding as needed.

Test Workflow:
1. Click Execute Workflow to test manually.
2. Turn on Active mode to enable scheduled automation.


Email Template Example
----------------------
Hello firstName,

Your registration for the AI-Powered Digital Marketing Workshop
has been successfully confirmed.

Workshop Details:
Date: March 15, 2024  
Time: 10:00 AM - 4:00 PM  
Venue: Online  

Best regards  
Your Team


Security Notes
--------------
- Do not upload credentials or API keys to GitHub.
- Workflow JSON does not store sensitive data.
- Credentials are stored securely inside n8n.
- Use .gitignore to exclude secret files.


Learning Outcomes
-----------------
- Understanding workflow automation using n8n
- API integration with Google services
- Batch processing and looping logic
- Rate limiting using wait nodes
- Scheduled automation workflows
- Real-world SaaS automation practice




Created using n8n automation
