Telegram AI Personal Assistant (n8n + Bult.ai)

This workflow turns your Telegram bot into a full AI assistant that can:

Read and write Gmail emails

List and create Google Tasks

View and create Google Calendar events

View and create Google Contacts

Process both text and voice messages

Think with ChatGPT and route actions automatically

The entire system runs on n8n deployed on Bult.ai, so it’s always online.

 1. Deploy n8n on Bult.ai

Go to https://bult.ai
 → create an account.

Dashboard → New Project → choose any name.

Inside the project → Create → Templates → n8n.

Click Apply → Deploy.

When ready, open your n8n URL, e.g.:

https://your-project.fin1.bult.app/


Register → verify using the email code.

Your cloud-hosted n8n editor is now running.

 2. Import the Workflow from GitHub

Open the repo:
https://github.com/bultcloud/n8n-workflows

Find bult-assistant.json.

Copy the entire file contents.

In n8n → Create Workflow → paste (Ctrl+V).

Save.

The workflow is now loaded into your n8n instance.

 3. Connect Your Telegram Bot

Open Telegram → search @BotFather.

Send:

/start
/newbot


Follow the prompts → copy the API token.

In n8n:

Open the Telegram Trigger node

Create a new Telegram credential

Paste the token

Save

Your Telegram bot is now connected and ready to receive messages.

 4. Set Up Google Integrations (OAuth)

The workflow uses Gmail, Calendar, Tasks, and Contacts (People API).
You only need to set up OAuth once.

Steps:

Go to Google Cloud Console → create a project.

Go to:
APIs & Services → OAuth Consent Screen
Fill required fields and publish.

Go to:
Credentials → Create Credentials → OAuth Client ID → Web Application

Copy Client ID and Client Secret.

In n8n, open any Google node → create a new Google OAuth2 credential.

Paste Client ID + Client Secret.

Use the Redirect URI shown in n8n (your Bult URL + /rest/oauth2-credential/callback).

Click Connect → log in → allow permissions.

Enable APIs:

Search and enable:

Gmail API

Google Calendar API

Google Tasks API

People API

Google authentication is now complete.

 5. What Your Assistant Can Do
 Gmail: Read & Write Emails

“Show me unread emails.”

“Send an email to Sarah saying I will be late.”

 Google Tasks: List & Create Tasks

“What tasks do I have today?”

“Create a task: prepare presentation.”

 Google Contacts: View & Add Contacts

“Who is Daniel in my contacts?”

“Add a contact: John Smith, john@example.com
.”

 Google Calendar: View & Create Events

“What events do I have tomorrow?”

“Create an event tomorrow at 3 PM: project meeting.”

 Voice Commands

Send any voice message

It gets transcribed → ChatGPT interprets → action executed

 Automatic Tool Selection

The AI decides internally whether your request requires:

Gmail

Google Tasks

Google Contacts

Google Calendar

Or just a normal chat response

No manual switching needed.

 6. Test the Workflow

In n8n → click Execute Workflow.

In Telegram → send a message or voice note.

The assistant will reply instantly.

If everything works correctly → Activate the workflow so it runs automatically 24/7.

 7. Optional Enhancements

You can easily extend this project by adding nodes for:

Task updates & deletions

Calendar event modifications

Contact lookups with filters

Automatic summaries of inboxes

Smart reminders

Integration with other APIs or databases

n8n gives you full flexibility.

 Summary

This assistant gives you a fully automated, always-available AI secretary that:

Runs in the cloud

Responds instantly on Telegram

Uses your Gmail, Calendar, Tasks, and Contacts

Handles both text and voice

Writes emails and creates tasks/events/contacts on command

All you need to do is:

Deploy n8n on Bult.ai

Import bult-assistant.json

Connect Telegram

Connect Google OAuth

Done.
