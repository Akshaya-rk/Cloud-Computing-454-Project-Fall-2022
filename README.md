# Cloud-Computing-454-Project-Fall-2022

##Slack Bot using Google Dialog Flow

This simple bot is setup to act as a intermediate between a Slack "Bot" User, and a DialogFlow Agent. By simply setting the appropriate APIAI_KEY and SLACK_API_KEY in the development/deployment environment, you can get started chatting with your "Bot Users" powered by a DialogFlow agent.  If you don't already have a Dialogflow agent, you may create one or add a prebuilt agent.

#Requirements
A Slack account
A Slack Workspace
A Slack Application downloaded on Desktop. 
A free-tier Google Cloud account with the Dialog Flow service. 
Node.js (for scripts) 

#Getting Started

1. Have admin privileges for a Slack channel and your development system.
2.Set your APIAI_KEY and SLACK_API_KEY environment variables to their corresponding values. You can get them from Slack's Bot Users interface for creating a Bot users in a Slack workspace you are the admin for, and in the settings area for the DialogFlow agent you wish to use.
node app.js to start the development server, which will run on port 5000 by default. 

#GCP Setup
## Log in or Sign up for GCP
1. Log in or sign up to google cloud console using a credit or debit card for a free trial. Create a project and enable billing for that project.
2. For deploying with App Engine, go to App Engine and enable the API. 

## Service Account Setup (GCP)
1. For the integration to function properly, it is necessary to create a Service Account in your agent’s GCP Project. Refer to documentation. 
2. For the service account, fill in the details, and give it the "Dialogflow Client API" role. This allows users to gain access to converse with the chatbot. 
3. Download the resulting JSON key file.
4. Save the JSON key file as dialogflowcx.json inside the functions/config directory of the cloned repo, else set the GOOGLE_APPLICATION_CREDENTIALS env variable on the deployment environment to the absolute path of Service Account JSON key file. See this guide for details. If JSON key is saved inside the repo, then uncomment CREDENTIALS_PATH in this file.

# Slack Integration
1. Create a workspace in Slack, or use an existing workspace.

2. To enable Slack integration with Dialogflow, choose "Integrations" on the left, then enable Slack. Follow the instructions and give permission to Dialogflow to operate a bot on your workspace.

3. When you enable the test bot, it should appear as an app in your Slack workspace with the name "Dialogflow Bot". You can direct message this bot to get translations.
