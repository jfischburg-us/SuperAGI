Introduction to SuperAGI
A dev-first open source autonomous AI agent framework enabling developers to build, manage & run useful autonomous agents. You can run concurrent agents seamlessly, extend agent capabilities with tools. The agents efficiently perform a variety of tasks and continually improve their performance with each subsequent run.

Features
Provision, Spawn & Deploy Autonomous AI Agents - Create production-ready & scalable autonomous agents.
Extend Agent Capabilities with Tools - Add various tools/toolkits to your agent workflows.
Graphical User Interface - Access your agents through a graphical user interface.
Action Console - Interact with agents by giving them input and permissions.
Multiple Vector DBs - Connect to multiple Vector DBs to enhance your agent’s performance.
Performance Telemetry - Get insights into your agent’s performance and optimize accordingly.
Optimized Token Usage - Control token usage to manage costs effectively.
Agent Memory Storage - Enable your agents to learn and adapt by storing their memory.

Getting Started
📄️ Prerequisites
You will require an API key for the LLM to get started with your first agent. In this tutorial, you will learn how to obtain the OpenAI's API Key.

📄️ Docker

1. Download the repo using git clone https://github.com/TransformerOptimus/SuperAGI.git in your terminal or directly from GitHub page in a zip format.

📄️ GitHub Codespaces

1. Open the SuperAGI GitHub repository https://github.com/TransformerOptimus/SuperAGI/ and click on Code > Codespaces > Create new codespace

📄️ SuperAGI Cloud

1. Navigate to app.superagi.com

Prerequisites
You will require an API key for the LLM to get started with your first agent. In this tutorial, you will learn how to obtain the OpenAI's API Key.

OpenAI API Key
Go to https://beta.openai.com/signup/ and click on your name on the Top-Right of the Screen. Click on "View API Keys".
Click on "Create new secret key". create-secret-key
Enter a suitable name and click on "Create secret key" to obtain your secret key. create-new-key-page

Docker
Download the repo using git clone https://github.com/TransformerOptimus/SuperAGI.git in your terminal or directly from GitHub page in a zip format.
Navigate to the directory using cd SuperAGI and create a copy of config_template.yaml and name it config.yaml.
Ensure that Docker is installed in your system, if not, Install it from here.
Once you have Docker Desktop running, run command : docker compose up --build in SuperAGI directory. Open your browser and go to localhost:3000 to see SuperAGI running.

Core Components
Agents in SuperAGI are complex systems that leverage the power of LLMs to operate independently, reason, perform tasks, and takes decisions without the constant need for human intervention.

The Agents, plan, reason, interact with toolkits, and execute based on the user's Goals, Instructions, Resources, and Constraints to achieve the expected results.

To dive deeper into how Agents operate, you can explore the sections below:

📄️ Agent Provisioning
Introduction:

📄️ Agent Details
Agent Details provide you with a complete view of the Agent’s Performance and a summary of the details you had given while provisioning an agent.

📄️ Activity Feed
The agent feed page provides you with complete, real-time visibility of the activities performed by the agent.

📄️ Pause & Resume an Agent
You can pause an agent during the middle of a run of resume a paused agent if you would like the agent to continue operating.

📄️ Agent New Run
Agent New Run provides you with the capability to start a New Run of an Agent that has been previously provisioned.

📄️ Run History
The Agent Run History provides you with a view of the runs that the agent has performed. It shows the last time the agent has run and the number of calls it has made

📄️ Action Console
The Action Console is used when you are running a permission-based agent. When the agent is running, you can provide directions to the agent before it proceeds to execute the next action such as approving the action, denying and denying with feedback.

📄️ Agent Scheduling
Agents can now be scheduled to run at a particular time and also run recursively at pre-defined timer intervals and also after ‘n’ number of run completions.

📄️ Agent Type
Agents in SuperAGI currently follow Re-Act architecture, where there is a thinking step that is performed by the LLM and an Execution with the tool that is suggested in the thinking step.

📄️ Agent Performance Monitoring
APM is the analytics dashboard that gives detailed insights into all the agents, models, tokens, runs, etc.

📄️ Delete Agent
You can delete a provisioned agent - the activity feed and the run history associated with the agent.

📄️ Edit Agent Template
You can make changes to an existing template - such as modifying

Agent Provisioning
Introduction:
Agent Provisioning provides you with the Capability of Creating New Agents. You can customize the agent extensively and provision agents that best suit your requirements.

Alt text

Name & Description
You can start by providing a unique name for your Agent and provide a description of the Agent’s Characteristics. This is meant for identification purposes which makes it easier for you to understand the Agent you are working with.

Alt text

Goals:
Goals are the desirable outcomes or objectives you can define for the agent. The goals you define are the overarching targets based on which the behavior of the agent is driven towards.

You can define the goals of your agent to achieve in plain and simple English, step-wise. Feel free to engineer your prompt and experiment with goals so that you can direct the agent towards your desirable outcomes.

An example of goals set for an agent would look like this:

Alt text

Instructions:
Instructions are directives or guidelines that you can prescribe to the agent. With instructions, you can provide actionable information that helps the agent understand how to navigate towards the given goals and make appropriate choices that help the agent progress towards the desired objectives.

It is worth noting that it is not necessary to always give instructions to your Agent. However, with instructions in place, it acts as a catalyst that brings in notable performance improvements of the agent.

Alt text

Models
While creating an agent, you can select the Large Language Model of choice with which you would like to deploy your agent.

As of now, SuperAGI currently supports OpenAI’s GPT 3.5-Turbo, GPT 3.5-Turbo-16k, GPT-4, GPT-4-32k and Google Palm Bison.

Alt text

Tools & Toolkit
You can select your required toolkits or tools which the agent can interact with and perform operations. Using toolkits can help you streamline your agent workflows and achieve better results.

You can select multiple toolkits or tools that suit your specific requirements. To learn more about how SuperAGI’s Toolkits work, you can head to the Toolkit Section.

Alt text

Advanced Options
The advanced options in SuperAGI allows you to get more hands-on in being able to modify your agent’s behavior as per your requirements.

Agent Type
Choosing an agent type allows you to change the agent's thought processs. Such as a ReAct-based agent, Fixed Task and a Dynamic Task-based agent. To learn more about how each of these agent types work, you can navigate to the Agent Type page.

Alt text

Adding Resources
You can add resources in formats such as .txt, .pdf, .csv, .epub, .docx, which the agent would ingest during the run. To learn more about how the Resource Manager works, navigate to the Resource Manager section.

Alt text

Constraints
Constraints are specific guardrails within which the Agent has to operate. These constraints ensure that the agent operates within the set environment and guidelines are met.

Constraints are pre-defined while creating an agent. However, you can change the constraints if required to better optimize the agent’s behavior.

Alt text

Maximum Iterations
Maximum Iterations are pre-defined iteration limits that are set for the agent. Since it can get expensive to run LLMs and it is possible for the Agent to hallucinate, you can set the number of iterations within which the agents have to operate.

Alt text

Permission Type
You can choose between "God Mode" - a truly Autonomous Agent that would independently take decisions and execute based on your goals and instructions and "Restricted" - an agent that would ask for your permission before proceeding with execution of the task.

Alt text

Agent Details
Agent Details provide you with a complete view of the Agent’s Performance and a summary of the details you had given while provisioning an agent.

It provides actionable metrics that show the performance of the agent including the Total Number of API calls made, the number of runs per agent, and the total token consumption.

Along with the metrics, you get complete visibility of the agent settings in terms of the name, description, goals, instructions, tools, constraints, the type of agent, model, time taken between steps, permission type, the maximum iteration limit set for the agent and the schedule details if you have scheduled the agent.

Alt text

Activity Feed
The agent feed page provides you with complete, real-time visibility of the activities performed by the agent.

By looking through the Activity Feed, you can understand the agent’s thought process, the results it is obtaining from tools, and its status whether the interaction was a success.

Alt text

Pause & Resume an Agent
You can pause an agent during the middle of a run of resume a paused agent if you would like the agent to continue operating.

If you wish to pause an agent run, you can do the following:

On the activity feed, click on the triple dotted button besides “New Run” button.
You can click on “Pause Agent” which temporarily pauses the agent.
Alt text

Subsequently, if you wish to resume a paused agent, click on the triple dotted button besides the “New Run” button and click on “Resume Agent” to continue the run.
Alt text

Agent New Run
Agent New Run provides you with the capability to start a New Run of an Agent that has been previously provisioned.

Additionally, you can also modify the Goals and the Instructions which you had given while initially provisioning the agent.

In order to start a new run, select any of the agents you had previously provisioned and click on the “New Run” button. You can change your Goals and Instructions and start a New Run.

Alt text

Run History
The Agent Run History provides you with a view of the runs that the agent has performed. It shows the last time the agent has run and the number of calls it has made

Alt text

Clicking on a run provides you with the visibility of the activity feed of the agent run.

Alt text

Action Console
The Action Console is used when you are running a permission-based agent. When the agent is running, you can provide directions to the agent before it proceeds to execute the next action such as approving the action, denying and denying with feedback.

alt text

You can either choose to approve an action or deny, either by providing feedback or denying the action as it is.

alt text

Agent Scheduling
Agents can now be scheduled to run at a particular time and also run recursively at pre-defined timer intervals and also after ‘n’ number of run completions.

Agents can either be created and scheduled simultaneously or, if they've already been created, they can be scheduled at a later time. However, it's essential to note that each agent can only be assigned one schedule. Currently, the system does not support assigning multiple schedules to a single agent. For those using the local version, it's crucial to ensure that Docker is running for the schedule to execute at the intended time.

Note: It is suggested that while creating a schedule, the agent should be scheduled 5 min before the intended time.

The calendar icon beside the agent name shows when a particular agent is scheduled.

Alt text

Schedule components
Schedule and Run
For a new agent, we get a dropdown at the create and run with the ‘schedule and run’ CTA which on click pops up a modal where the date of schedule, recursion and expiry details can be given.

Alt text

For an existing agent, we have the schedule run option in the three dots beside the new run. This opens up a similar modal.

Alt text

Each schedule’s details are shown in the details section as long as it’s schedule is yet to start. As soon as the last schedule creates a new run, the details are removed from the frontend.

Alt text

Recurring Schedule
Recurring can be enabled while scheduling a run and can be set for days, hours and minutes that is relative to the scheduled date.

Alt text

Schedule Expiry
Schedule can be expired after ‘n’ number of runs or after a specific date.

Alt text

Edit Schedule
The edit schedule option is available in the three dots beside new run. After a schedule is already made, it can be edited such that it overwrites the previous schedule and all the details also get updated.

Stop Schedule
The stop schedule option is available in the three dots beside new run. After a schedule is already made, it can be stopped from executing the following schedules.

Alt text

Agent Type
Agents in SuperAGI currently follow Re-Act architecture, where there is a thinking step that is performed by the LLM and an Execution with the tool that is suggested in the thinking step.

SuperAGI will be launching Chat based agent and S-Re-Act architecture, where the agent will be able to handle a conversation with the user in chat based agent and also sense the occurrence of an event and then think and execute the actions in Sense-Re-Act architecture.

Alt text

Default
Think → Execute

The agent takes the goals that go to the thinking tool which gives a Thought, Plan, Criticism and Tool. The decided tool is then executed which completes 1 call (iteration)

Alt text

Fixed Task Queue
Think → Prioritize → Execute

The agent takes the goals and makes them into a list of tasks and prioritizes them. Each task goes to thinking and then goes to the tool to execute. The Agent finishes all tasks completely when the final task listed is completed.

Alt text

Dynamic Task Queue
Think → Prioritize → Execute → Add Task → Execute

The agent takes the goals and makes them into a list of task and prioritizes them. Each task goes to thinking and then goes to the tool to execute. If the thinking creates another task as a part of the Thought, Plan, Criticism and Tool, then this task also gets added to the task list and reprioritizes. The Agent finishes all tasks completely when the final task listed is completed.

Alt text

Agent Performance Monitoring
APM is the analytics dashboard that gives detailed insights into all the agents, models, tokens, runs, etc.

The KPIs are structured in a way that the user will be able to derive actionable insights. The entire dashboard is interactive and any metric card can be re-ordered or re-sized.

All the KPIs are updated only after run completion.

Organization-Level metrics:
These KPIs give an executive overview of SuperAGI.

Alt text

Total number of agents: The total agents that have run till date irrespective of deletion.

Total tokens consumed: Total Tokens consumed by all the agents that have run till date irrespective of deletion.

Total Runs: Total Runs performed by all the agents that have run till date irrespective of deletion.

Number of Agents per model: How many agents have used a particular model

Number of Runs per model: How many runs have been made using a particular model

Total tokens consumed per model: How many tokens have been consumed while using a particular model

Active Runs: The runs that are currently running

Most used Tools: The number of times a Tool has been called or The number of times an Agent has the tool assigned

Agent-Level metrics:
This shows the model used, tokens consumed, runs made, avg. tokens per run, tools used, calls made, avg. run time for each agent.

Alt text

Model: Each agent can use only one model

Tokens Consumed: The tokens consumed by a particular agent over all its runs for each agent

Runs: Total runs executed in that agent

Average Tokens per run: Total tokens consumed by the agent/Total runs made by the agent

Tools used: Tools that have been used by an agent over all its runs for each agent

Calls made: Number of calls made across all the runs for each agent

Average Run time: The Total time taken/Total runs made

Run
The three plots of run analytics are connected by a single Agent wise filter which give Tokens consumed per run, calls made per run and Average tokens consumed over all calls per run for a particular agent.

Alt text

Tokens consumed per run: Total Tokens consume for a particular run of an agent

Calls made per run: Total calls made for a particular run of an agent

Average tokens consumed in all call per run: The Total Tokens consumed by a Total calls made for a particular run of an agent.

Edit this page
Previous
Agent Type
Next
Delete Agent
Organization-Level metrics:
Agent-Level metrics:
Run

Delete Agent
You can delete a provisioned agent - the activity feed and the run history associated with the agent.

In order to delete an agent, click on the triple dotted button besides the "new run" button and you can find the "delete agent" button in the dropdown. When clicked, the agent gets permanently deleted.

Edit Agent Template
You can make changes to an existing template - such as modifying the goals, instructions, toolkits, the agent type, etc.

When you make changes to an agent template, it does not affect the provisioned agent. However, using the updated agent template, you can start provisioning new agents with the changes you've made to the template.

Alt text

Vector Database
What is a Vector Database?
Vector databases are a type of database that stores data as high-dimensional vectors. These vectors are used to represent the semantic or contextual meaning of data. Vector databases are used for vector search, which is a type of search that finds the most similar or relevant data based on their vector distance or similarity.

How does SuperAGI agent use a Vector Database?
The agent can use the vector database to perform a knowledge search and fetch relevant info from connected knowledge stores to achieve the goal.

Which vector databases are currently supported?
Currently, SuperAGI supports cloud hosted Weaviate, Pinecone and QDrant. Support for other popular vector databases like Milvus, Redis, will be added subsequently.

Navigate to the below sections to learn how to set up your Vector Database.

📄️ Pinecone
Setting up Pinecone with SuperAGI

📄️ Qdrant
Setting up Qdrant with SuperAGI

📄️ Weaviate
Setting up Weaviate with SuperAGI

📄️ Using Marketplace Knowledge
To use Marketplace Knowledge, follow the given steps:

📄️ Using Custom Knowledge
To add custom knowledge select Knowledge in left panel, and click Add Knowledge button

📄️ Update your Vector Database

1. To later update your vector database, select the database you’d like to update

📄️ Delete your Vector Database
Select the vector database to be deleted and click on Uninstall.

Pinecone
Setting up Pinecone with SuperAGI
Login to your account on Pinecone. If you don't have one, you can create an account here
If you are new to Pinecone, you can create an index as follows. If you already have an existing index, you can skip to step 5
alt_text

Input index name and add 1536 in dimensions. For knowledge embeddings, we use OpenAI’s text-embedding-ada-002 model which creates embeddings of 1536 dimensions.
alt_text

Once your index is created, go to Vector Settings in SuperAGI by clicking the settings icon on the top right corner.

In the Vector Database Settings, select Pinecone

alt_text alt_text

To connect Pinecone, add the API Key, environment and index name.
alt_text

Go to Pinecone dashboard and click Indexes to get the index name
alt_text

Go to Pinecone dashboard and click API keys to get API key and environment.
alt_text

Add these in Vector Database settings and click Connect. This will connect your Pinecone index.
alt_text

Qdrant
Setting up Qdrant with SuperAGI
Access your Qdrant Account
If you are new to Qdrant, you can create your account as follows. If you already have an existing index skip to step 5
Create your cluster for Qdrant and get your api-key, and URL.
alt_text alt_text

To create your index, run the following code with your Qdrant Credentials:
alt_text

Once your index is created, go to Vector Settings in SuperAGI by clicking the settings icon on the top right corner.
In the Vector Database Settings, select Qdrant.
alt_text

Add your vector database settings and click connect. This will connect your Qdrant index.
alt_text

Weaviate
Setting up Weaviate with SuperAGI
Access your Weaviate Account
If you are new to Weaviate, you can create your account as follows. If you already have an existing index skip to step 3.
alt_text

Create your cluster for Weaviate and get your api-key, and URL from cluster details.
alt_text

To create your class run the following code with your Weaviate Credentials:
alt_text

Once your class is created, go to Vector Settings in SuperAGI by clicking the settings icon on the top right corner.
In the Vector Database Settings, select Weaviate.
alt_text

Add your vector database settings and click connect. This will connect your Weaviate class.

Using Marketplace Knowledge
To use Marketplace Knowledge, follow the given steps:

Go to Marketplace → Knowledge
alt_text

Click on the install button
It will open a drop down where you can select the index where you want to install the knowledge.
Note: You can only install knowledge in the index which has same dimensions as knowledge and is either empty or only has marketplace knowledge vectors

alt_text

Using Custom Knowledge
To add custom knowledge select Knowledge in left panel, and click Add Knowledge button

alt_text

Enter knowledge name, description and select your index from the dropdown

alt_text

Once done, click update button

alt_text

Your custom knowledge has been added.

Update your Vector Database
To later update your vector database, select the database you’d like to update
alt_text

You can add or remove the indices as per your requirements
alt_text

Delete your Vector Database
Select the vector database to be deleted and click on Uninstall.

alt_text alt_text alt_text alt_text

Resource Manager
Introduction
The SuperAGI Resource Manager facilitates the structured storage and retrieval of files generated by autonomous agents. This component ensures smooth operations of agents, allowing them to read from and save to designated directories based on their unique identification and execution parameters.

Configuration
Local Configuration
For local setups, the configuration is specified through the config.yaml file. In this file, paths are set using the following parameters:

RESOURCES_INPUT_ROOT_DIR: Designates the root directory for agent inputs. It follows the pattern: workspace/input/{agent_id}.
RESOURCES_OUTPUT_ROOT_DIR: Specifies the root directory where agent outputs are saved. Two configurations are available:
Per Execution: workspace/output/{agent_id}/{agent_execution_id}
Per Agent: workspace/output/{agent_id}
Production (Cloud Version) Configuration
In the cloud or production environment, input and output directories configurations are preset and cannot be changed.

Working Mechanism
Concurrent Agent Operation
The SuperAGI infrastructure supports seamless concurrent operations of multiple agents. Each agent, distinguished by its unique agent_id, can run without interference from others.

File Storage and Retrieval
When an agent generates a file during its execution:

The file is saved to its corresponding output directory.
If configured at the execution level, the file will reside under the specific agent_execution_id directory.
Otherwise, it will be stored at the agent level directory.
For reading files, agents access their designated input directory.

User Interface (UI) Representation
In the user interface:

Outputs: Users can view files on a per-execution basis. Each execution's stored files are displayed distinctly, allowing users to track and manage the outputs for each run of an agent.
Inputs: Files are displayed on an agent-wise basis, ensuring clarity in tracking resources used for agent operations.

Toolkits
Toolkits allow SuperAGI Agents to interact with third-party plugins and external systems.

With SuperAGI, you can easily create your own Toolkit or you can provision powerful agents with toolkits that are available in our ecosystem such as GitHub, Jira, Twitter, Slack. Quickly get started by navigating to the below sections:

SuperAGI's Toolkits
With ready-to-use toolkits available out of the box on SuperAGI’s ecosystem, toolkits provide you with the following advantages:

You can provision more powerful and versatile agents.
You can connect your agents to other systems and services.
Learn how you can configure SuperAGI's toolkits and provision powerful agents that interact with these Toolkits:

🗃️ Image Generation
2 items

📄️ Coding Toolkit
The Coding Toolkit lies at the heart of SuperAGI's SuperCoder - providing your agent with the ability to create a codebase from a single prompt.

📄️ DuckDuckGo
The SuperAGI DuckDuckGo Search Tool helps users perform a DuckDuckGo search and extract snippets and webpages.

📄️ Email
The SuperAGI Email Tool lets users send and read emails while providing a foundation for other use cases.

📄️ GitHub
The SuperAGI GitHub Tool enables users to perform various operations on GitHub repositories which include adding files or folders, deleting files, and searching for files or folders within a repository.

📄️ Google Calendar
Introducing the Google Calendar Toolkit, a powerful integration for SuperAGI. With the Google Calendar toolkit, you have the ability to do the following:

📄️ Google Search
The SuperAGI Google Search Tool helps users perform a Google search and extract snippets and webpages.

📄️ Google SERP Search
The SuperAGI Google Search Toolkit helps users perform a Google search and extract snippets and webpages.

📄️ Instagram
The SuperAGI Instagram Tool works with the stable diffusion tool, generates an image & caption based on the goals defined by the user and posts it on their instagram business account. Currently will only work on the Cloud Version

📄️ Jira
The SuperAGI Jira Tool lets users create, edit and search issues while providing a foundation for other great use cases.

📄️ Notion
Introducing Notion Toolkit to increase your productivity via SuperAGI. With Notion toolkit, you can:

📄️ Searx Search
The SuperAGI Searx Search Tool helps users perform a Searx search and extract snippets and webpages. We parse the HTML response pages because most Searx instances do not support the JSON response format without an API key.

📄️ Slack
This SuperAGI Tool lets users send messages to Slack Channels.

📄️ Twitter
Introducing Twitter Toolkit for SuperAGI. With Twitter Integrated into SuperAGI, you can now deploy agents to

📄️ Web Scraper
The SuperAGI Webscraper Tool lets users perform web scraping, extract

Dall-E
The SuperAGI Image Generation Tool helps you generate an image with a prompt using DALL-E.

Features
Customizable Prompts: Users can input their own prompts to guide the image generation process, allowing for a wide range of creative possibilities.

High-quality Image Output: The tool utilizes DALL-E's advanced capabilities to generate high-quality images that match the user's prompts.

If you've put the correct OpenAI key during the installation, you'd be able to use the Image Generation tool as well.

Running SuperAGI Image Generation Tool
You can simply put one of the goals of your agent to create an image and the agent will pick up the Image Generation Tool and will place it in the Output folder of the Resource Manager, from where you'll be able to download it.

Stable Diffusion
Introducing Stable Diffusion Integration with SuperAGI

You can now use SuperAGI agents Stable Diffusion to create true-to-life images which opens up a whole new range of possibilities.

Configuring API from DreamStudio
You can now get your API Key from Dream Studio to use Stable Diffusion by following the instructions below:

Create an Account/Login with DreamStudio.ai
SD_1

Click on the Profile Icon at the top right which will take you to the settings page. Once you have reached the settings page, you can now get your API keys
SD_5

Copy the API Key and save it in a separate file
Configuring Stable Diffusion with SuperAGI
You can configure SuperAGI with Stable Diffusion using the following steps:

Navigate to the “\***\*Toolkit”\*\*** Page in SuperAGI’s Dashboard and select “\***\*Image Generation Toolkit”\*\***
SD_4

Once you’ve clicked Image Generation Toolkit, it will open a page asking you for the API Key and the Model Engine. You can enter the generated API key from Dream Studio here
SD_2

If you would like to go in-depth with the model of Stable Diffusion, you can choose between the following engine IDs:
'stable-diffusion-v1'
'stable-diffusion-v1-5'
'stable-diffusion-512-v2-0'
'stable-diffusion-768-v2-0'
'stable-diffusion-512-v2-1'
’stable-diffusion-768-v2-1'
'stable-diffusion-xl-beta-v2-2-2’
You have now successfully configured Stable Diffusion with SuperAGI!

Coding Toolkit
The Coding Toolkit lies at the heart of SuperAGI's SuperCoder - providing your agent with the ability to create a codebase from a single prompt.

Tools Included
WriteSpecTool: Based on the goal given to the agent, the WriteSpecTool prepares the technical specification required for your project.

WriteTestTool: Using the specifications provided by the WriteSpecTool, the WriteTestTool writes test cases for which the code will have to meet the criteria for acceptance.

WriteCodeTool: The WriteCodeTool takes in the context of the WriteSpecTool and WriteTestTool and starts generating the codebase for your project.

ImproveCodeTool: The ImproveCodeTool can take in the files from your WriteCodeTool or files you upload via the resource manager, analyze the code and improve the code - thus making sure that the code being generated is of qood quality.

You'll be able to use the Coding Tool on the fly once you have setup SuperAGI.

Running SuperAGI Coding Toolkit
You can try the Coding Toolkit through the SuperCoder Template or simply select the "Coding Toolkit" while creating an agent.

DuckDuckGo
The SuperAGI DuckDuckGo Search Tool helps users perform a DuckDuckGo search and extract snippets and webpages.

Running SuperAGI DuckDuckGo Search Tool
You can simply ask your agent about latest information regarding anything in the world and your agent will be able to browse the internet to get that information for you.

Email
The SuperAGI Email Tool lets users send and read emails while providing a foundation for other use cases.

Features
1.Read Emails: With SuperAGI's Email Tool, you can manage your inbox and ensure that you never overlook a critical detail.

Send Emails: SuperAGI's Email Tool uses its comprehensive language model capabilities to create personalised, context-aware emails, sparing you effort and time.

Save Emails to Drafts Folder: By allowing SuperAGI to develop email draughts that you can examine and modify before sending, you'll gain greater control and make sure your messages are tailored to your tastes.

Send Emails with Attachments: Send attachments in emails with ease to expand the scope of your message.

Custom Email Signature: Create a unique signature for each email you send to add a touch of customization and automation.

Auto-Reply and Answer Questions: Allow SuperAGI to read, analyse, and respond to incoming emails with precise answers to streamline your email responses.

Installation
Add Email configuration settings SuperAGI's Dashboard
Config_Page

Add the following configuration in the Email Toolkit Page:

Email address and password:
Set 'EMAIL_ADDRESS' to sender's email address
Set 'EMAIL_PASSWORD' to your Password. If using Gmail, use App Password (Follow the steps given below to obtain your app password.)
Provider-specific settings:
If not using Gmail, modify 'EMAIL_SMTP_HOST', 'EMAIL_SMTP_PORT', AND 'EMAIL_IMAP_HOST' according to your email service provider.
Sending and Drafts:

You can set the EMAIL_DRAFT_MODE to "FALSE" if you'd like your email to be directly sent and "TRUE" if you'd like to save your emails in Draft.
If you're setting Draft Mode to True, Make sure to add the draft folder for your email service provider to prevent it from being sent.
Optional Settings:

Change the 'EMAIL_SIGNATURE' to your personalize signature.
Obtain your App Password
To obtain App password for your Gmail Account follow the steps:

Navigate to the link (https://myaccount.google.com/apppasswords)
app_password

To get the App Password ensure that you have set up 2-Step Verification for your email address.

Generate the password by creating a custom app

password

Copy the password generated and use it for 'EMAIL_PASSWORD'

Also make sure IMAP Access is enabled for your Gmail Address (Settings > See all settings > Forwarding and POP/IMAP > Enable IMAP)

imap_enable

Running SuperAGI Email Tool
Read an email
By default SuperAGI's email tool reads last 10 emails from your inbox, to change the limit you can modify the default limit in read_email.py

Send an email
To send an email to a particular receiver, mention the receiver's ID in your goal. Email will be stored in drafts if in case receiver's email address is not mentioned.

send_email

Send an email with attachment
SuperAGI can send Emails with Attachments if you have uploaded the file in the Resource Manager, or if your file is in the Input or the Output of your SuperAGI Workspace.

GitHub
The SuperAGI GitHub Tool enables users to perform various operations on GitHub repositories which include adding files or folders, deleting files, and searching for files or folders within a repository.

Features
Add Files or Folders: With SuperAGI's GitHub Tool, you can add files or folders to a GitHub repository
Delete Files: Remove files from a GitHub repository using SuperAGI's GitHub Tool.
Search for Files or Folders: Find specific files or folders within a GitHub repository using SuperAGI's GitHub Tool.
Add GitHub Configuration Settings in SuperAGI Dashboard
Add the following configuration settings to the GitHub Toolkit Page:

GitHub Access Token:

Obtain a GitHub access token with the necessary permissions for accessing and modifying repositories.
Go to Settings in your GitHub Account. Then go to Developer Settings.
Click on "Personal access tokens". Then click on "Tokens (classic)". personal-access-token
Click on "Generate new token". Then choose "Generate new token (classic)". generate-new-token
Write a Note about what the token is for and choose an appropriate expiration date. github-permissions
Select all the scopes (In this way, users won't have to create new Access Tokens every time we add new scopes to the code).
Click on Generate New Token.
Copy the token and save it as a separate file.
Github User Name:

You can find your GitHub username on your GitHub Profile.
Configuring in SuperAGI Dashboard: -You can add your Generated Token and your Username to the GitHub Toolkit Page.

Running SuperAGI GitHub Tool
Add Files or Folders:

To add a file or folder to a GitHub repository, specify the repository and the owner's UserName and the path where the file/folder should be added to your goal. SuperAGI will upload it to the repository and automatically raise a PR for it. By default, it'll pick the main branch, if you want to add it to any other branch you have to mention it in the goal.

Delete Files:

To delete a file from a GitHub repository, mention the repository, owner's UserName and provide the path to the file you want to delete in your goal. SuperAGI will handle the deletion process and raise a PR for it. By default, it'll pick the main branch, if you want to delete it to any other branch you have to mention it in the goal.

Search for Files or Folders

To search for files or folders within a GitHub repository, specify the repository, and owner's UserName and provide the name or path of the file/folder you're looking for in your goal. SuperAGI will provide you with the search results. By default, it'll pick the main branch, if you want to search in any other branch you have to mention it in the goal.

Google Calendar
Introducing the Google Calendar Toolkit, a powerful integration for SuperAGI. With the Google Calendar toolkit, you have the ability to do the following:

Features
Create Calendar Events
List your Calendar Events
Fetch an event from your Calendar
Delete Calendar Events
Quickstart Guide:
In order to get started with integrating Google Calendar with SuperAGI, you need to do the following:

API Creation and OAuth Consent Screen
Go to Google Developer Console: https://console.cloud.google.com/ & Create a new project. If you’re having an existing project, you can proceed with that as well:
GC1

After the project is created/you’re in your selected project, head to “APIs and Services”
GC2

Click on “ENABLED APIS AND SERVICES” and search for “Google Calendar”
GC3

GC4

Enable the API
GC5

Once the API is Enabled, go to “OAuth Consent Screen”
GC6

Select your User Type as “External” and click on "Create"
GC7

Fill in the required details such as the App Information, App Domain, Authorized Domain, and Developer contact information. Once filled in, click “Save and Continue”
GC8

On the next page, you don’t need to select the scopes. Proceed to “save and continue” and at the final page, review the process and click “Back to Dashboard”. With this, you’ve created your OAuth Consent Screen for Google Calendar.
You can go ahead and click the “Publish App”
GC9

Configuring endpoints & obtaining Client ID and Client Secret Key
In order to obtain the Client ID and Secret ID, you need to do the following steps:

Go to “Credentials” Page
GC10

Click on “Create Credentials” and click on “OAuth Client ID”
GC11

GC12

Once you click on OAuth Client ID, choose the type of application as “Web Application” and give it a name of your choice
GC13

Create JavaScript Origins and add the following details as shown in the image:
GC14

Go to Authorized redirect URIs and add the following URIs: https://app.superagi.com/api/google/oauth-tokenshttp://localhost:3000/api/google/oauth-tokens
alt_text

Once you’re completed with adding the Authorized redirect URIs, you can click “Create” to obtain the Client ID and Client Secret Key
GC16

Copy the Client ID and Secret Key and save it in a file.
Configuring your Client ID, Secret Key and Authenticating Calendar with SuperAGI
Once the ClientID and Secret Key are obtained, you can configure and authorize Calendar to be used with SuperAGI by following these steps:

Add your Client ID and Client Secret Key on the toolkit page and click on “Update Changes”
GC_17

Click on “Authenticate Tool” - which will now take you to the OAuth Flow.
Once the OAuth Authentication is complete, you can now start using SuperAGI Agents with Google Calendar!

Google Search
The SuperAGI Google Search Tool helps users perform a Google search and extract snippets and webpages.

Features
Google Search: Perform Google searches using the SuperAGI Google Search Tool and obtain relevant results.

Webpages Extraction: Extract webpages from the search results for further analysis and processing.

Installation
If you've put the correct Google API key and Custom Search Engine ID, you'll be able to use the Google Search Tool as well.

Running SuperAGI Google Search Tool
You can simply ask your agent about latest information regarding anything in the world and your agent will be able to browse the internet to get that information for you.

Google SERP Search
The SuperAGI Google Search Toolkit helps users perform a Google search and extract snippets and webpages.

Add Google Serp Search API Key in SuperAGI Dashboard
Register an account at https://serper.dev/ with your Email ID.

Your Private API Key would be made. Copy that and save it in a separate text file.

Serper_Key

Open up the Google SERP Toolkit page in SuperAGI's Dashboard and paste your Private API Key.
Running SuperAGI Google Search Serp Tool
You can simply ask your agent about the latest information regarding anything and your agent will be able to browse the internet to get that information for you.

Instagram
The SuperAGI Instagram Tool works with the stable diffusion tool, generates an image & caption based on the goals defined by the user and posts it on their instagram business account. Currently will only work on the Cloud Version

⚙️ Installation
🔧 Instagram tool requirements
Since the tool uses the official instagram graph API's to post media on user accounts, There are a few requirements:

You will need access to the following:

1. An Instagram Business Account or Instagram Creator Account
2. A Facebook Page connected to that account
3. A Facebook Developer account that can perform Tasks on that Page
4. A registered Facebook App with Basic settings configured

Once everything is set up, add the meta user access token (to be generated from facebook developer account), Facebook page ID (can be found on the facebook page connected to the instagram account under 'Page transparency' in 'About' section of the page ) and the stability API key to the correspponding toolkits.

Follow the steps given in the link to set up meta requirements: (https://developers.facebook.com/docs/instagram-api/getting-started) Follow the link to generate stability API key: (https://dreamstudio.com/api/)

🔧 Configuring in SuperAGI Dashboard:
-You can add your meta user access token and facebook ID to the Instagram Toolkit Page and stability API key to the Image Generation Toolkit Page

Running SuperAGI Instagram Tool
Once everything has been set up just run/schedule an agent with the goal explaining the media to be published and add instagram tool (which will automatically add stable diffusion tool)

Warning
It is advised to run the instagram tool in restricted mode since it allows you to validate the photos generated. You can schedule agent runs (recurring runs are supported as well). Also, only one photo will be posted to your account in a run. To post multiple photos use recurring runs.

Jira
The SuperAGI Jira Tool lets users create, edit and search issues while providing a foundation for other great use cases.

Features
Create Issue: SuperAGI's JIRA tool lets you create new tasks in your project by defining the task's details such as its summary, description, type, and priority.

Edit Issue: Modify existing tasks with SuperAGI's JIRA tool, which allows you to change any task details like summary, description, type, and priority.

Search Issues: Use the 'Search Issues' feature to find specific tasks within your projects by defining your search criteria in terms of project, assignee, or keywords in the task summary.

Get Projects: Discover and access all your projects using the 'Get Projects' feature, providing a bird's eye view of your workload and streamlining project-based searches.

Add Jira configuration settings in SuperAGI Dashboard
Add the following configuration settings in the file:

JIRA API TOKEN:
Login into your Jira Account. Go to "Manage Account".
Go to Security and click on "Create and Manage API Tokens".

Click on "Create API Token" and choose an appropriate label name.
Copy the API Token and save it in a text file.
JIRA INSTANCE URL:
Your instance profile is the section at the start of your URL. It should look something like "https://mycompany.atlassian.net/".
JIRA USERNAME:
Your Jira UserName is the Email Address with which you signed up in Jira.
CONFIGURING JIRA IN SUPERAGI DASHBOARD:
Open the Jira Toolkit Page in SuperAGI Add your Jira API Token, your Instance URL, and your Jira Username and click "Update Changes"
Running SuperAGI Jira Tool
Create an Issue: The SuperAGI JIRA Create Issue tool allows you to create issues in your project. By default, it creates a task with predefined settings. To create a task with different details, modify the relevant fields in the create_issue.py script.

Edit an Issue: To edit a particular issue, specify the issue ID in your goal. The modifications can be made by changing the relevant fields in the edit_issue.py script.

Search for Issues: You can simply search for a particular issue in your agent's goals and your agent performs a search based on the JIRA Query Language (JQL) query you define. Modify the JQL query according to your requirements in the search_issues.py script.

Fetch Project Details: Use the 'Get Projects' feature to retrieve a list of your accessible projects. The get_projects.py script can be modified to adjust the parameters of this operation.

Notion
Introducing Notion Toolkit to increase your productivity via SuperAGI. With Notion toolkit, you can:

Create Pages in a database (Notion Create Tool)
Fetch the contents of a Page (Notion Fetch Tool)
Setting up notion
The notion toolkit can be installed from the marketplace. To setup and use notion toolkit, users need to create a workspace in notion for which the user is the admin.

Notion Integration Token
Step 1
Go to https://www.notion.so/my-integrations and click on “Create new integration”

alt_text

Step 2
Fill in the required details and connect the integration to the appropriate workspace(make sure that you are the admin of that workspace)

alt_text

Step 3
You can get your Integration Token after submitting the previous form. Click show and then copy the Internal Integration Secret.

alt_text

Database ID
Step 1
Create a teamspace and go to one of the pages(database) in that teamspace. Go to the settings of that page and the integration name will be visible in the “+Add connections” section.

alt_text

Step 2
After making the connection, database ID can be found in the URL. The format of the url will be https://www.notion.so/{workspace_name}/{database_id}?v={view_id}. Copy the database_id.

alt_text

Using Notion
Paste the Integration token and the database ID in the tool configurations and the Notion Toolkit will be good to use.

alt_text

Searx Search
The SuperAGI Searx Search Tool helps users perform a Searx search and extract snippets and webpages. We parse the HTML response pages because most Searx instances do not support the JSON response format without an API key.

Running SuperAGI Searx Search Serp Tool
You can simply ask your agent about latest information regarding anything in the world and your agent will be able to browse the internet to get that information for you.

Slack
This SuperAGI Tool lets users send messages to Slack Channels.

Features:
Send Message - This tool gives SuperAGI the ability to send messages to Slack Channels that you have specified
Slack Configuration:
Create an Application on SlackAPI Portal
Slack_1

Select "from scratch"
Slack_2

Add your application's name and the workspace for which you'd like to use your Slack Application
Slack_3

Once the app creation process is done, head to the "OAuth and Permissions" tab
Slack_4

Find the “bot token scopes” and define the following scopes:

"chat:write", and save it

Slack_5

Once you've defined the scope, install the application to your workspace
Slack_6

Post installation, you will get the bot token code
Slack_7

Once the installation is done, you'll get the Bot User OAuth Token, which needs to be added to the Slack Toolkit Page
Slack_8

Once the configuration is complete, you can install the app in the channel of your choice and create an agent on SuperAGI which can now send messages to the Slack Channel.

Twitter
Introducing Twitter Toolkit for SuperAGI. With Twitter Integrated into SuperAGI, you can now deploy agents to

Send Tweets
Send Tweets with Images
Installation
🔐 Obtaining API Key and Secret from Twitter Developer Portal
Log in to your Twitter Developer Portal Account and select your project under the “Projects & Apps” section.
TW1

Proceed with creating a new app. Once you have created the app by adding a name, you will get an API Key and an API Secret, copy that and keep it in a separate text file.
TW2 TW3

🚪 Configuring OAuth
Once you have saved the key and the secret, click on “App Settings”
Once you are on the App Settings Page, start setting up the User Authentication Settings.
TW4

Fill in the details as shown in the below image. Give “Read and Write Permissions” and make it a “Web Application"
TW5

Add the Following Callback URIs and the Website URL as shown in the image below:

https://app.superagi.com/api/twitter/oauth-tokens

http://localhost:3000/api/twitter/oauth-tokens

alt_text

Save the settings. you have now configured OAuth Authentication for Twitter.

✅ Configuring Keys and Authenticating in SuperAGI.
In the SuperAGI’s Dashboard, navigate to the Twitter Toolkit Page, add the API Key and API Secret you’ve saved, and click on ‘Update Changes’

TW7

After you’ve updated the changes, click on Authenticate. This will take you to the OAuth Flow. Authorize the app through the flow.
TW8

Once you have followed the above steps, you have successfully integrated Twitter with SuperAGI.

Edit this page

Web Scraper
The SuperAGI Webscraper Tool lets users perform web scraping, extracting URLs and retrieving the textual content from websites.

Features
URL Extraction: The SuperAGI Web Scraper Tool can extract URLs from web pages, allowing users to collect and analyze links for further processing.

Text Retrieval: The tool is capable of retrieving textual content from websites, enabling users to gather and analyze data from various sources.

You'll be able to use the Web Scraper Tool on the fly once you have setup SuperAGI.

Running SuperAGI Web Scraper Tool
You can simply ask your agent to read or go through a certain website or URL, and it'll be able to retrieve it's textual information from there.

How to add a Custom Toolkit
With a few easy-to-follow steps, you can get started with building and adding your own custom Toolkits to SuperAGI:

Step 1: Set Up Your GitHub Repository.

First things first, you need a place to store and manage your tool's code. For this, you can use GitHub. Create a new repository and make sure it contains the following files:

**init**.py: This file is crucial as it helps Python recognize your repository as a package. It’s usually an empty file.
tool1.py: This is where the code for your first tool should go.
tool2.py: If you have a second tool, this is where its code should reside.
toolname_toolkit.py : This file will have the toolkit name, and description, followed by all tools and config details of that toolkit.
requirements.txt: This file lists all the dependencies needed for your tool to run smoothly.
Your repository structure should look something like this:

Your-Repository-Name
├── **init**.py
├── tool1.py
├── tool2.py
├── toolname_toolkit.py
└── requirements.txt

You can find a sample repo here to understand custom tool building: https://github.com/luciferlinx101/GreetingTool

Step 2: Use the following pip command (https://pypi.org/project/superagi-tools/) to get the required APIs and BaseTool related classes to easily integrate your tool with SuperAGI. Run the following command in your terminal or command prompt:

pip install superagi-tools

This will install the necessary SuperAGI base tool and toolkit class.

Step 3: Start SuperAGI using “Docker compose up” Link Your GitHub Repository to SuperAGI. Next, you need to add your GitHub repository link to SuperAGI’s front-end. This is how SuperAGI will know where to find your tool. When you add the GitHub link, it is stored in a database. Also, make sure to provide a name for your toolkit, which will be used to identify it on the SuperAGI platform. The GitHub link and toolkit name are stored in a file called tools.json like this:

{ "toolkit-name": "your-github-link" }

Step 4: Once your GitHub link is added, the SuperAGI tool manager will take care of installing your tool along with it’s dependencies. It will be placed in a directory named superagi/tools.

Step 5: Once this is added, you have to restart your docker. Now that your tool is installed, it’s time to build and run it. Run the following command:

docker compose down
docker compose up --build

This command restarts your docker, builds it again, and runs it.

During the Docker run, your tool’s dependencies (specified in requirements.txt) will be installed. This is done automatically on startup by a script called install-tool-dependency.sh. It automatically installs all the necessary dependencies for your tool. You'll now be able to use the Toolkit on your local GUI.

Marketplace
📄️ Agent Template Marketplace
The SuperAGI Agent Template Marketplace, offers users a curated selection of agent templates that are pre-approved by SuperAGI. Each template is designed to address specific use cases, ensuring users have a tailored starting point for a variety of tasks. With predefined attributes like Agent Name, Description, Goals, Instructions, Tool, Agent Type, and Models., these templates accelerate the agent creation process.

📄️ Toolkit Marketplace
The SuperAGI Toolkit Marketplace, accessible at marketplace.super

Agent Template Marketplace
The SuperAGI Agent Template Marketplace, offers users a curated selection of agent templates that are pre-approved by SuperAGI. Each template is designed to address specific use cases, ensuring users have a tailored starting point for a variety of tasks. With predefined attributes like Agent Name, Description, Goals, Instructions, Tool, Agent Type, and Models., these templates accelerate the agent creation process.

Untitled

Overview
Each agent template in the marketplace is crafted to cater to specific scenarios and includes:

Agent Name: A unique identifier for each template.
Description: A brief overview detailing the agent's functionality and its intended use case.
Goals: The core objectives that the agent is programmed to achieve.
Instructions: Set of operational guidelines or tasks for the agent to follow.
Tool: Tools or software the agent is designed to work with.
Agent Type: The Type of Agent required for the Template - Task Queue Agent, Dynamic Task Agent or Fixed Action Agent.
Models: The Model the agent is designed to work with. It can work with other models as well, but works best with the model mentioned.
Untitled

Installation Process
Exploring the Marketplace: Begin by browsing through marketplace.superagi.com to inspect all available agent templates.
Template Selection: Upon identifying a suitable template, click on its listing to delve deeper into its details and functionalities.
Installation: Utilize the "Install" option for the chosen agent template. This action incorporates the template into your SuperAGI interface.
Confirmation: Post-installation, users will receive a confirmation message indicating the template's successful addition and its readiness for use.
Using the Installed Templates
Creating a New Agent: Navigate to the "Create Agent" section within the SuperAGI interface.
Choosing a Template: Within the "Choose Templates" segment, users will now find the recently installed agent template(s) available for selection.
Template Customization: After selecting a template, users have the option to modify and tailor the agent's attributes as per their specific requirements, if necessary.
Contributing to Marketplace
We are actively developing a feature allowing users to contribute and add their own agent templates to the marketplace. The specifics of this process are currently being refined.

Coming Soon.

Toolkit Marketplace
The SuperAGI Toolkit Marketplace, accessible at marketplace.superagi.com, serves as a centralized repository of toolkits developed by SuperAGI. It contains a collection of specialized tools that can be integrated into the agents. By browsing the marketplace, users can access, review, and install essential tools to enhance the capabilities of their agents.

Untitled

Toolkit Listings
Each toolkit in the marketplace comes with detailed information, which includes:

Toolkit Name: The unique identifier for each toolkit.
Description: A brief summary outlining the toolkit's primary functions and features.
List of Tools: An itemized breakdown of all the tools contained within the toolkit.
Untitled

Installation Process
Browsing the Marketplace: Navigate to marketplace.superagi.com and explore all available toolkits. Users can delve into the details and functionality of each toolkit.
Toolkit Selection: Once a desired toolkit has been identified, click on its listing to view in-depth information and installation options.
Installation: Click on the "Install" button associated with the toolkit. This will initiate the integration process with the agent.
Confirmation: After a successful installation, a confirmation message will be displayed, confirming that the toolkit is now available for the agent's use.
Usage Considerations
Toolkit Dependency: Agents can only utilize tools from the toolkits that have been installed. Without proper installation, access to these tools will be restricted.
Updates: It's crucial to regularly check the marketplace for toolkit updates to ensure optimal performance and the latest features.
Uninstallation: If a toolkit is no longer required, users can uninstall it from their agent's setup through the marketplace interface.
Contributing to the Marketplace
Currently, we are working on the capability for users to add their own tools to the Toolkit Marketplace. The process and guidelines for contributing Toolkits is coming soon!

Contribute
Contribute to Code
First of all, thank you for taking the time to contribute to this project. We truly appreciate your contributions, whether it's bug reports, feature suggestions, or pull requests. Your time and effort are highly valued in this project. 🚀

This document provides guidelines and best practices to help you to contribute effectively. These are meant to serve as guidelines, not strict rules. We encourage you to use your best judgment and feel comfortable proposing changes to this document through a pull request.

✔️ Code of Conduct:
Please read our Code of Conduct to understand the expectations we have for all contributors participating in this project. By participating, you agree to abide by our Code of Conduct.

🚀 Quick Start
You can quickly get started with contributing by searching for issues with the labels "Good First Issue" or "Help Needed" in the Issues Section. If you think you can contribute, comment on the issue and we will assign it to you.

To set up your development environment, please follow the steps mentioned below :

Fork the repository and create a clone of the fork
Create a branch for a feature or a bug you are working on in your fork
Once you've created your branch, follow the instructions in the README.MD
Contributing Guidelines
🔍 Reporting Bugs
You can start working on an existing bug that has been reported and labeled as "Bug" in the Issues Section, and you can report your bugs in the following manner :

Title describing the issue clearly and concisely with relevant labels
Provide a detailed description of the problem and the necessary steps to reproduce the issue.
Include any relevant logs, screenshots, or other helpful information supporting the issue.
💡 New Feature or Suggesting Enhancements
This section guides you through working on an enhancement Including a completely New Feature & Enhancements to an existing functionality.

Before getting started, Perform a search on Issues to see if the enhancement or feature has already been suggested and picked up. If the feature or enhancement is suggested and not picked up, comment on the issue and assign yourself to it.

If the feature or enhancement is not in the issues, find out whether your idea fits with the scope and aims of the project by looking at the Roadmap. If yes, raise an issue with the label "Feature Request" in the following manner:

Title describing the feature or enhancement in a clear and concise manner
Clearly describe the proposed enhancement, highlighting its benefits and potential drawbacks.
Provide examples and supporting information.
Once you have raised the issue and have gotten yourself assigned, you can start working on the feature or enhancement. Please make sure the feature or enhancement you're working on is placed on the Roadmap.

Testing your Changes
Each method or the function of the code should have a unit test with the maximum coverage possible and on each Pull Request, we have GitHub Actions triggered, which runs all the unit tests where all the tests should pass for merging the Pull Request.

Pull Request
Now that you have worked on your code and tested it thoroughly, you can now go ahead and raise the pull request. Please make sure that the Pull Request adheres to the following guidelines:

The pull request is atomic and focuses on a single change.
You have read the contributing guide and your code conforms to the guidelines.
You have documented your changes clearly and comprehensively.
You have added the required tests.

Benchmarking
Objective Goals Tools Models Expected Output Agent Output Tested Doesn’t work Somewhat Works Works Perfect
Writing Blog Write a 1000-word blog with 2 images. Searx Toolkit, Read File, Write File, Stable Diffusion Toolkit GPT-3.5 900-1000 word blog in a .txt file along with 2 images. 350-word blog in a .txt file along with 2 images Yes No Yes No
Tweeting Do Twitter Marketing by automatically creating 1 tweet every day about a specific theme. Twitter Toolkit, Stable Diffusion Toolkit GPT-4 Tweet with Image Agent tweeted successfully with a relevant image Yes No Yes No
Posting Instagram Do Instagram Marketing by automatically creating 1 post every day about a specific theme. Instagram Toolkit, Stable Diffusion Toolkit GPT-4 Instagram Post with Whey Muscle Protein Powder. Agent posted an image on Instagram with captions and image of generic whey protein from Stable Diffusion Yes No Yes No
Analytics report Collect Weekly Analytics Report from Google Analytics and Mail it every Monday at 8 am. Google Analytics Toolkit, Email Toolkit, Write File GPT-4 .txt report with the collected data, which is mailed to me. To be tested No No No No
Sales prospecting Create a list of sales managers’ contacts from specific companies in a CSV and send personalized mail. Tools not built GPT-4 Maintains a CSV of leads that tracks the mails sent. To be tested No No No No
Google Calendar Analysis Analyze calendar meeting invites for the day and provide an analysis via Email. Google Calendar Toolkit, Email Toolkit, Write File, Read File GPT-4 The agent should provide a rundown of meetings and time availability. The agent got stuck in a loop while making sense of events Yes Yes No No
Investment Research Send personalized mails to potential prospects. Tools not built GPT-4 To be tested No No No No No
Email Summary Provide a summary of unread mails every workday via Scheduled Agent Run and Recurring Run. Email Toolkit, Write File, Read File GPT-4 Mail to me or anyone with a summary of all unread emails. Agent was able to make a summary of at least 5 emails and send it Yes Yes Yes No
Email Automatic Reply Provide automatic draft replies to all unread mails via Scheduled Agent Run and Recurring Run. Email Toolkit, Write File, Read File GPT-4 Generate a draft email with an appropriate reply for all recipients. Agent was able to save three emails as drafts with appropriate replies Yes Yes Yes No
Automatic Jira Ticket Creation Create a Jira ticket automatically when a GitHub Issue is created. Jira Toolkit, GitHub Toolkit GPT-4 To generate a Jira Ticket with the description when a GitHub Issue is created Jira tickets are working, but not connected to GitHub Tool Yes Yes No No
