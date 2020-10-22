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
