# 🤖 Telegram AI Personal Assistant

> **A comprehensive AI assistant powered by n8n and Bult.ai that integrates with Google services**

Transform your Telegram bot into a powerful AI assistant that seamlessly manages your digital life. This workflow provides intelligent automation for Gmail, Google Tasks, Calendar, and Contacts - all through natural language commands.

## ✨ Features

- 📧 **Gmail Integration** - Read and compose emails
- ✅ **Google Tasks** - Create and manage your task lists  
- 📅 **Google Calendar** - View and schedule events
- 👥 **Google Contacts** - Search and add contacts
- 🎙️ **Voice Commands** - Process voice messages with automatic transcription
- 🧠 **Smart Routing** - ChatGPT automatically selects the right tool for each request
- ☁️ **Always Online** - Runs 24/7 on cloud infrastructure

## 🚀 Quick Start

### 1. Deploy n8n on Bult.ai

1. Visit [bult.ai](https://bult.ai) and create an account
2. Navigate to **Dashboard** → **New Project** → choose any name
3. Select **Create** → **Templates** → **n8n**
4. Click **Apply** → **Deploy**
5. Open your n8n URL (e.g., `https://your-project.fin1.bult.app/`)
6. Register and verify using the email code

Your cloud-hosted n8n editor is now running! ✅

### 2. Import the Workflow

1. Open the [n8n workflows repository](https://github.com/bultcloud/n8n-workflows)
2. Find and copy the contents of `bult-assistant.json`
3. In n8n: **Create Workflow** → paste (`Ctrl+V`) → **Save**

The workflow is now loaded into your n8n instance! ✅

### 3. Connect Your Telegram Bot

1. Open Telegram and search for `@BotFather`
2. Send the following commands:
   ```
   /start
   /newbot
   ```
3. Follow the prompts and copy the API token
4. In n8n:
   - Open the **Telegram Trigger** node
   - Create a new **Telegram credential**
   - Paste the token and save

Your Telegram bot is connected! ✅

### 4. Set Up Google Integrations (OAuth)

#### Google Cloud Console Setup
1. Go to [Google Cloud Console](https://console.cloud.google.com) and create a project
2. Navigate to **APIs & Services** → **OAuth Consent Screen**
   - Fill required fields and publish
3. Go to **Credentials** → **Create Credentials** → **OAuth Client ID** → **Web Application**
4. Copy the **Client ID** and **Client Secret**

#### n8n OAuth Configuration
1. In n8n, open any Google node
2. Create a new **Google OAuth2 credential**
3. Paste **Client ID** and **Client Secret**
4. Use the Redirect URI shown in n8n: `your-bult-url/rest/oauth2-credential/callback`
5. Click **Connect** → log in → allow permissions

#### Enable Required APIs
Enable these APIs in Google Cloud Console:
- ✅ Gmail API
- ✅ Google Calendar API  
- ✅ Google Tasks API
- ✅ People API (for Contacts)

Google authentication is complete! ✅

## 🧠 What Your Assistant Can Do

### 📧 Gmail: Read & Write Emails
```
"Show me unread emails"
"Send an email to Sarah saying I will be late"
```

### ✅ Google Tasks: List & Create Tasks
```
"What tasks do I have today?"
"Create a task: prepare presentation"
```

### 👥 Google Contacts: View & Add Contacts
```
"Who is Daniel in my contacts?"
"Add a contact: John Smith, john@example.com"
```

### 📅 Google Calendar: View & Create Events
```
"What events do I have tomorrow?"
"Create an event tomorrow at 3 PM: project meeting"
```

### 🎙️ Voice Commands
- Send any voice message
- Automatic transcription → ChatGPT interpretation → action execution

### 🔀 Automatic Tool Selection
The AI intelligently routes your requests to:
- Gmail
- Google Tasks  
- Google Contacts
- Google Calendar
- Or provides a conversational response

*No manual switching required!*

## 🧪 Testing & Activation

1. In n8n: click **Execute Workflow**
2. In Telegram: send a message or voice note
3. The assistant will reply instantly
4. If everything works → **Activate** the workflow for 24/7 operation

## 🔧 Optional Enhancements

Extend functionality by adding nodes for:
- 📝 Task updates & deletions
- 🔄 Calendar event modifications  
- 🔍 Advanced contact filtering
- 📊 Inbox summaries
- ⏰ Smart reminders
- 🔌 Integration with other APIs

n8n provides complete flexibility for customization.

## 📋 Summary

This assistant provides a fully automated, always-available AI secretary that:

- ☁️ Runs in the cloud
- ⚡ Responds instantly on Telegram  
- 🔗 Integrates with Gmail, Calendar, Tasks, and Contacts
- 🎙️ Handles both text and voice commands
- ✍️ Writes emails and creates tasks/events/contacts on command

## 🏁 Quick Setup Checklist

- [ ] Deploy n8n on Bult.ai
- [ ] Import `bult-assistant.json`
- [ ] Connect Telegram bot
- [ ] Configure Google OAuth
- [ ] Test the workflow
- [ ] Activate for 24/7 operation

**That's it! Your AI assistant is ready to work.** 🎉

---

*Built with ❤️ using [n8n](https://n8n.io) and [Bult.ai](https://bult.ai)*
