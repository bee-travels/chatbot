<p align='center'>
<img src='images/logo.png' width='420' alt='Bee Travels logo'>
</p>

# Bee-Travels Chatbot 
> **Note:** Bee Travels Chat Bot is a work in progress. This document will be updated to reflect any changes.

![Bee-Travels Gif](/images/take1.gif)
<!-- <p align='center'>
<img src='images/BT-1.png' width='420' alt='Bee Travels logo'>
</p> -->
## About

Bee Travels is a polyglot microservice demo in the form of a travel agency web application. This repo is home to the implementation of bee travel chatbots. The chatbots crated in this repo are used to demonstrate the key capability of Watson Assistant into the cloud native application. 

To see versions of Bee Travels for other languages, check out the [Bee Travels GitHub org](https://github.com/bee-travels).

## Basic Usage

### Prerequisite

- Register for an [IBM Cloud](https://www.ibm.com/account/reg/us-en/signup?formid=urx-42793&eventid=cfc-2020?cm_mmc=OSocial_Blog-_-Audience+Developer_Developer+Conversation-_-WW_WW-_-cfc-2020-ghub-starterkit-communication_ov75914&cm_mmca1=000039JL&cm_mmca2=10008917) account.

### Set up an instance of Watson Assistant

Log in to IBM Cloud and provision a Watson Assistant instance.

**Step 1.** From the [IBM Cloud catalog](https://cloud.ibm.com/catalog/services/watson-assistant), provision an an instance of **Watson Assistant**.
  ![Watson Assistant Catalog](/images/assistant/WA-Photo1.png)

**Step 2.**  Launch the Watson Assistant service.

**Step 3.** Click **Create assistant** and follow [these detailed instructions](https://cloud.ibm.com/docs/assistant?topic=assistant-assistant-add) for how to create an assistant.
  ![Watson Assistant Photo2 ](/images/assistant/WA-Photo2.png)

**Step 4.** Name the Watson Assistant instance **Bee Travels**
  
**Step 5.** Click **Add Dialog skill** to add this to your assistant. Follow [the documentation](https://cloud.ibm.com/docs/assistant?topic=assistant-skill-dialog-add) if you have questions.


**Step 6.** Click **Import skill > Choose JSON file** and import the [`skill-travelBot.json`](./travelBot/skills/skill-travelBot.json) file.
  ![Watson Assistant Photo5 ](/images/assistant/WA-Photo5.png)

**Step 7.** Go back to the All Assistants page. From the action menu ( **`⋮`** ), open **Settings**.
  

**Step 8.**  On the Settings tab, click **API Details** on the left and make a note of the `Assistant ID` and `Api Key` for future use.
  

**Step 9.** Go back to the All Assistants page and click on the **Skills** link.
  

**Step 10.** On the Skill page, click on the action menu ( **`⋮`** ), open **View API Details**.
 

**Step 11.** On the Skill Details page, make note of the `Skill ID` for future use.
  

**Step 12.**  Go back to your dialog skill and click on the **Preview Link** button on the side to get a link to test and verify your assistant.
  ![Watson Assistant Photo9 ](/images/assistant/WA-Photo91.png)

**Step 13.** Ask the Watson Assistant chatbot some questions about where you will be traveling.
<p align='center'>
<img src='images/BT-1.png' width='420' alt='Bee Travels logo'>
</p>

## Slack Integration 

### Prerequisites

To complete the steps in this tutorial you need:

- A Slack workspace with administrative rights. [Learn how to create your Slack workspace](https://slack.com/help/articles/206845317-Create-a-Slack-workspace).
- A [Watson Assistant Bee Travels Chatbot](https://github.com/Call-for-Code/Solution-Starter-Kit-Communication-2020#getting-started)

Now, I'll show you how to integrate your Slack workspace with your Bee Travels chatbot.

## Integrate Slack and your chatbot

### Step 1. 

Go to your Bee Travels Assistant and click **Add Integration**.

### Step 2.
In the Watson Assistant UI, scroll down to the section for "Third-party integration" and select **Slack**.

### Step 3.
First, you need to create a [Slack App](https://api.slack.com/apps). Click on **Create New App**, name your application, and point to a Slack development workspace. Learn more about creating slack apps [here](https://api.slack.com/start).


### Step 4.
On the Slack app Settings page, go to the **Basic Information** tab and find the **App Credentials** section. Copy your verification token from that section.

Paste the verification token from step 4 and paste it into the appropriate area of Step 2 on Watson Assistant Slack integration page:

(Optional): Upload an App Icon and App Name in the Display information section of the **Basic Information** tab:

### Step 5.
Go to the **OAuth & Permissions tab**. In the **Bot Token Scopes** section, click **Add an Oauth Scope**, and then select the following scopes:`app_mentions:read` `chat:write` `im:history` `im:read` `im:write`.

### Step 6.
On the **OAuth & Permissions** tab, click **Install App to Workspace**, and then click **Allow**. You should be redirected back to the OAuth & Permissions page.

**Note** Make sure you copy your Bot User OAuth access token (`starts with xoxb`)  to both of the fields in **section 3** of Step 2 on Watson Assistant Slack integration page 
 
### Step 7.
On the Slack app settings page, go to the **Event Subscriptions** tab. Switch the **Enable Events** toggle to the On position. Go to Step 3 of the Watson Assistant Slack Integration page, click **Generate Requestt URL**. Paste the requested URL and verify its accuracy on the **Enable Events** page.

### Step 8.
On the Event Subscriptions tab, find the Subscribe to Bot Events section. Click **Add Bot User Event**, and then select the event types you want to subscribe to. You must select at least one of the following types: 

* `message.im`: Listens for message events that are posted in a direct message channel. 
* `app_mention`: Listens for only message events that mention your app or bot.

Make sure you save your changes.

### Step 9.
On the **App Home** tab. Click **Edit** and enter a display name and default username for your virtual assistant. Click **Save**. Enable the **Always Show My Bot as Online** toggle:

### Step 10.
On Watson Assistant Slack Integration page click **Save Changes**.

### Step 11.
Log into your Slack workspace and click on **Browse App**. Find the app you just created and add to your workspace:

### Step 12.
Test your application by asking questions based on intents and entities in your dialog tree! If you recieve answers back you have successfully integrated your Bee Travel chatbot! Congratulations. 
