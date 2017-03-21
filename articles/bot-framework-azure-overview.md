---
title: Azure Bot Service overview | Microsoft Docs
description: Learn about Azure Bot Service.
keywords: Bot Framework, Azure Bot Service, Overview
author: Toney001
manager: rstand
ms.topic: bot-service-article
ms.prod: botframework
ms.service: Azure Bot Service
ms.date: 3/20/2017
ms.reviewer:
#ROBOTS: Index
---

# Overview

Use the Azure Bot Service to accelerate your bot’s development by working in an integrated environment that’s purpose-built for bot development. This integrated environment lets you build, connect, deploy and manage intelligent bots that interact naturally wherever your users are talking, whether it's with an app or website, Text/SMS, Skype, Slack, Facebook Messenger, Kik, Office 365 mail, and other popular services. You can also increase the value of your bots with a few lines of code by plugging into <a href="https://www.microsoft.com/cognitive-services/en-US/sign-up?ReturnUrl=/cognitive-services/en-us/subscriptions" target="_blank">Cognitive Services</a> to enable your bots to see, hear, interpret and interact in more human ways.

Azure Bot Service is powered by Microsoft Bot Framework and Azure Functions. By using Azure Functions, your bot will run in a serverless environment on Azure that will scale based on demand.

You can write your bot in C# or Node.js directly in the browser using the Azure editor without any need for a tool chain (local editor and source control). The integrated chat window sits side-by-side with the Azure editor, which lets you test your bot on the fly as you write the code in the browser.

The Azure editor does not allow you to manage the files by adding new files or renaming or deleting existing files. If you need to manage the files, you should set up continuous integration, which would let you use the IDE and source control of your choice (for example, Visual Studio Team, GitHub, and Bitbucket). Continuous integration will automatically deploy to Azure the changes that you commit to source control. 

> [!NOTE]
> After configuring continuous integration, you will no longer be able to update the bot in the Azure editor.

Once you have setup continuous integration, you can debug your bot locally by following these instructions.

The following are the Bot App templates that you can create.

* Basic—A simple bot that uses dialogs to respond to user input. See Basic bot template. Read [Create a bot with the Azure Bot Service](../articles/bot-framework-azure-getstarted.md) to learn how to build a basic bot.
* Form—A bot that uses a guided conversation to collect user input. The C# template uses FormFlow to collect user input, and the Node.js template uses waterfalls. See  [Form bot template](../articles/bot-framework-azure-forbottemplate.md).
* Language understanding—A bot that uses natural language models (LUIS) to understand user intent. See [Natural langugae bot template]. (../articles/bot-framework-azure-naturallanguagebottemplate.md).
* Proactive—A bot that uses Azure Functions to alert bot users of events. See [Proactive bot template](../articles/bot-framework-azure-proactivebottemplate.md).
* Question and answer—A bot that creates question and answer pairs based upon your company's FAQ. See [Question and Answer template](../articles/bot-framework-azure-questionandanswer.md).

For a walkthrough that shows creating a bot using Azure Bot Service, see [Create a bot with the Azure Bot Service](../articles/bot-framework-azure-getstarted.md).

## What's include with bots made with Azure Bot Service
Azure Bot Service is powered by the serveless infrastructure of Azure Functions, and it shares its runtime concepts, which you should become familiar with.

All Azure Bot Service bots include the following files

### C #

| File | Description |
|------|-------------|
| Bot.sln | The Microsoft Visual Studio solutions file. Used locally if you set up < a "https://docs.botframework.com/en-us/azure-bot-service/manage/setting-up-continuous-integration/" target="_blank">Continuous Integration</a>. |
|Commands.json | This file contains the commands that start debughost in Task Runner Explorer when you open the Bot.sln file. If you don't install Task Runner Explorer, you can delete this file.
| debughost.cmd | This file contains the commands to load and run your bot. Used locally if you set up continuous integration and want to debug your bot locally. For more information, see Debugging C# bots built using the Azure Bot Service on Windows. The file also contains your app ID and password. You would set the ID and password if you want to debug authentication. If you set these, you must provide the ID and password in the emulator, too. |
| function.json | This file contains the function’s bindings. You should not modify this file. |
| host.json | A metadata file that contains the global configuration options affecting the function. |
| project.json | This file contains the project’s NuGet references. You should only have to change this file if you add a new reference. |
| readme.md | This file contains notes that you should read before using or modifying the bot. |


###Node.js

| File | Description |
|------|-------------|
| function.json | This file contains the function’s bindings. You should not modify this file. |
| host.json | A metadata file that contains the global configuration options affecting the function |
| package.json | This file contains the project’s NuGet references. You should only have to change this file if you add a new reference. |