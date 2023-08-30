SuperAGI
A dev-first open source autonomous AI agent framework enabling developers to build, manage & run useful autonomous agents. You can run concurrent agents seamlessly, extend agent capabilities with tools. The agents efficiently perform a variety of tasks and continually improve their performance with each subsequent run.

Generate API Key
To use the key in your API call, pass it in the headers as shown below:

To generate a new API key, navigate to the API Keys Dashboard on the Settings page in SuperAGI.

Click on Create key and give a name for your API key.

Copy the key generated and click on OK.

You will be able to view, edit or delete your keys in your SuperAGI dashboard.

Authentication
Authentication to the SuperAGI API is performed by passing X-API-Key in headers.

Plain Text
X-API-Key: yoursuperagiapikey
Cloud API baseurl
Plain Text
Cloud baseurl
https://app.superagi.com
Eg. On SuperAGI cloud, create agent API endpoint would look like
https://app.superagi.com/api/v1/agent
Local API baseurl
Plain Text
Local baseurl
http://localhost:3000
Eg. On SuperAGI local, create agent API endpoint would look like
http://localhost:3000/api/v1/agent
Agent
Agents in SuperAGI are complex systems that leverage the power of LLMs to operate independently, reason, perform tasks, and takes decisions without the constant need for human intervention.

The Agents, plan, reason, interact with toolkits, and execute based on the user's Goals, Instructions, Resources, and Constraints to achieve the expected results.

POST
Create
{{URL}}/api/v1/agent
This endpoint allows users to create agents

Table
Parmeter Type Description Required
name string Name of the agent. yes
description string Desciption of the agent. yes
goals array of strings What the agent is supposed to achieve. yes
agent_workflow string Below are supported values for agent workflow:

Goal Based Workflow
Dynamic Task Workflow
Fixed Task Workflow

These values are case sensitive. yes
constraints array of strings Agent contraints like like use as mininum tokens and interations as possible. See API example to know more. yes
instructions array of strings These are very specific instructions
tools array of maps Supported toolkit names are:
CodingToolkit
Email Toolkit
File Toolkit
GitHub Toolkit
Google Calendar Toolkit
Google Search Toolkit
Google SERP Toolkit
Image Generation Toolkit
Jira Toolkit
Searx Toolkit
Slack Toolkit
Web Scraper Toolkit
Twitter Toolkit
Knowledge Search Toolkit
DuckDuckGo Search Toolkit
Notion Toolkit
Instagram Toolkit

Pass `[]` if you don't want to use any tool.

NOTE: Some tools like Instagram and Notion are required to be installed from marketplace before they can be used in APIs.

In case of a custom toolkit, the value of name property of the toolkit needs to be passed in tools. Check this example toolkit https://github.com/TransformerOptimus/SuperAGI/blob/main/superagi/tools/duck_duck_go/duck_duck_go_search_toolkit.py yes
iteration_interval int Time to wait between each iterations
model string Below are supported values for models:
gpt-4
gpt-3.5-turbo
gpt-3.5-turbo-16k yes
max_iterations int Max number of iterations agent can run for. yes
schedule object Run schudule for an agent no

Schedule object
Parameter Type Description Required
start_time string Start time of agent schedule. yes
recurrence_interval string Time interval after which agent run is triggered. Eg.
3 hours
5 days no
expiry_runs int After how many runs the scheduled agent should stop no
expiry_date string Expiry time of agent schedule. Can be `null` if expiry_data is not required. no
HEADERS
X-API-Key
110e030a-2d27-4d6d-90ba-4f7b7ceee4e2

{
"name": "Aug 17 MS 2606",
"description": "AI assistant to solve complex problems",
"goal": ["create a photo of a cat"],
"agent_workflow": "Goal Based Workflow",
"constraints": [
"~4000 word limit for short term memory.",
"Your short term memory is short, so immediately save important information to files.",
"If you are unsure how you previously did something or want to recall past events, thinking about similar events will help you remember.",
"No user assistance",
"Exclusively use the commands listed in double quotes e.g. \"command name\""
],
"instruction": [],
"tools":[
{
 "name":"Image Generation Toolkit"
},
{
 "name":"DuckDuckGo Search Toolkit"
}
],
"iteration_interval": 500,
"model": "gpt-4",
"max_iterations": 25,
"schedule": { // can be null if for agent without schedule
"start_time": "2023-08-14 21:32:00",
"recurrence_interval": "2 Minutes",
"expiry_runs": 2,
"expiry_date": null
}
}

Example Request
var axios = require('axios');
var data = '{\n "name": "test final 100212dsaCXZCa33",\n "description": "AI assistant to solve complex problems",\n "goal": ["CREATE A PHOTO OF A CAT"],\n "agent_workflow": "Goal Based Workflow", \n "constraints": [\n "~4000 word limit for short term memory.",\n "Your short term memory is short, so immediately save important information to files.",\n "If you are unsure how you previously did something or want to recall past events, thinking about similar events will help you remember.",\n "No user assistance",\n "Exclusively use the commands listed in double quotes e.g. \\"command name\\""\n ],\n "instruction": [],\n "tools":[\n { \n "name":"Image Generation Toolkit"\n },\n { \n "name":"DuckDuckGo Search Toolkit"\n }\n ],\n "iteration_interval": 500,\n "model": "gpt-4",\n "max_iterations": 25,\n "schedule": null // Can be null for an agent without a schedule\n // "schedule": { // Use this to run agent with a schedule\n // "start_time": "2023-08-14 21:32:00",\n // "recurrence_interval": "2 Hours",\n // "expiry_runs": 2,\n // "expiry_date": null\n // }\n}';

var config = {
method: 'post',
maxBodyLength: Infinity,
url: '{{URL}}/api/v1/agent',
headers: {
'X-API-Key': 'bf2b13a0-c5d3-403f-a887-ac8849b8304b'
},
data : data
};

axios(config)
.then(function (response) {
console.log(JSON.stringify(response.data));
})
.catch(function (error) {
console.log(error);
});

Example Response
Body
{
"agent_id": 28
}

Headers
Server
nginx/1.24.0

Date
Wed, 16 Aug 2023 14:13:22 GMT

Content-Type
application/json

Content-Length
15

Connection
keep-alive

POST
Pause
{{URL}}/api/v1/agent/{agent_id}/pause
This endpoint allows users to pause agent runs

Parameter Type Description Required
agent_id path param: int Id of the agent to pause the runs for. yes
run_ids array of ints Array of agent run_ids to pause. If you pass run_ids as empty array [] , all runs for the agent_id will be paused. no
HEADERS
X-API-Key
576d4db5-03c4-4a2c-92ca-29550eee4180

Body
raw (json)
json
{
"run_ids":[102]
}
Example Request
var axios = require('axios');
var data = '{\n "run_ids":[18]\n}';

var config = {
method: 'post',
maxBodyLength: Infinity,
url: '{{URL}}/api/v1/agent/{agent_id}/pause',
headers: {
'X-API-Key': 'bf2b13a0-c5d3-403f-a887-ac8849b8304b'
},
data : data
};

axios(config)
.then(function (response) {
console.log(JSON.stringify(response.data));
})
.catch(function (error) {
console.log(error);
});

Example Response
Body
{
"result": "success"
}
Headers (5)
Server
nginx/1.24.0

Date
Wed, 16 Aug 2023 14:04:33 GMT

Content-Type
application/json

Content-Length
20

Connection
keep-alive

POST
Resume
{{URL}}/api/v1/agent/{agent_id}/resume
This endpoint allows users to resume agent runs

Parameter Type Description Required
agent_id path param: int Id of the agent for runs to resume. yes
run_ids array of ints Array of agent run_ids to resume. If you pass run_ids as empty array [] to all agent runs will be resumed. no
HEADERS
X-API-Key
e3347a48-c4f0-4fcc-b444-7a375473c712

Body
raw (json)
json
{
"run_ids":[98,100,102]
}

var axios = require('axios');
var data = '{\n "run_ids":[25]\n} ';

var config = {
method: 'post',
maxBodyLength: Infinity,
url: '{{URL}}/api/v1/agent/{agent_id}/resume',
headers: {
'X-API-Key': 'bf2b13a0-c5d3-403f-a887-ac8849b8304b'
},
data : data
};

axios(config)
.then(function (response) {
console.log(JSON.stringify(response.data));
})
.catch(function (error) {
console.log(error);
});

Example Response
Body
{
"result": "success"
}
Headers (5)
Server
nginx/1.24.0

Date
Wed, 16 Aug 2023 14:13:36 GMT

Content-Type
application/json

Content-Length
20

Connection
keep-alive

PUT
Update
{{URL}}/api/v1/agent/{agent_id}
This endpoint allows users to update an existing agent.

Note:

Users can't add schedule to an existing agent using the update end point.
Table
Parmeter Type Description Required
agent_id path param: int Id of the agent to update. yes
name string Name of the agent. no
description string Desciption of the agent. no
goals array of strings What the agent is supposed to achieve. yes
agent_workflow string Below are supported values for agent workflow:

Goal Based Workflow
Dynamic Task Workflow
Fixed Task Workflow

These values are case sensitive. yes
constraints array of strings Agent contraints like like use as mininum tokens and interations as possible. See API example to know more. yes
instruction array of strings Specific instructions given to agent to complete the goal in a pre-defined way.
tools array of maps Supported toolkit names are:
CodingToolkit
Email Toolkit
File Toolkit
GitHub Toolkit
Google Calendar Toolkit
Google Search Toolkit
Google SERP Toolkit
Image Generation Toolkit
Jira Toolkit
Searx Toolkit
Slack Toolkit
Web Scraper Toolkit
Twitter Toolkit
Knowledge Search Toolkit
DuckDuckGo Search Toolkit
Notion Toolkit
Instagram Toolkit

Pass `[]` if you don't want to use any tool.

NOTE: Some tools like Instagram and Notion are required to be installed from marketplace before they can be used in APIs

In case of a custom toolkit, the value of name property of the toolkit needs to be passed in tools. Check this example toolkit https://github.com/TransformerOptimus/SuperAGI/blob/main/superagi/tools/duck_duck_go/duck_duck_go_search_toolkit.py yes
iteration_interval int Time to wait between each iteration. yes
model string Below are supported values for models:
gpt-4
gpt-3.5-turbo
gpt-3.5-turbo-16k yes
max_iterations int Max number of iterations agent can run for. yes

HEADERS
X-API-Key
e3347a48-c4f0-4fcc-b444-7a375473c712

Body
raw (json)
{
"name": "Aug 17 0626",
"description": "AI assistant to solve complex problems",
"goal": ["compare iphone 15 and iphone 14 base variant"],
"agent_workflow": "Don't Maintain Task Queue",
"constraints": [
"~4000 word limit for short term memory.",
"Your short term memory is short, so immediately save important information to files.",
"If you are unsure how you previously did something or want to recall past events, thinking about similar events will help you remember.",
"No user assistance",
"Exclusively use the commands listed in double quotes e.g. \"command name\""
],
"instruction": [],
"tools":[
{
 "name":"Image Generation Toolkit"
},
{
 "name":"DuckDuckGo Search Toolkit"
}
],
"iteration_interval": 500,
"model": "gpt-4",
"max_iterations": 25
}

Example Request
var axios = require('axios');
var data = '{\n "name": "dasdas test_100dasdrreterterteasffffffffffffffffffffff1_updated",\n "org_id": 1,\n "description": "AI assistant to solve complex problems",\n "goal": ["compare iphone 15 and iphone 14 base variant"],\n "agent_workflow": "Don\'t Maintain Task Queue", \n "constraints": [\n "~4000 word limit for short term memory.",\n "Your short term memory is short, so immediately save important information to files.",\n "If you are unsure how you previously did something or want to recall past events, thinking about similar events will help you remember.",\n "No user assistance",\n "Exclusively use the commands listed in double quotes e.g. \\"command name\\""\n ],\n "instruction": [],\n "tools":[\n { \n "name":"Image Generation Toolkit"\n },\n { \n "name":"DuckDuckGo Search Toolkit"\n }\n ],\n "iteration_interval": 500,\n "model": "gpt-4",\n "max_iterations": 25\n // "schedule": { \n // "start_time": "2023-07-07 06:15:00",\n // "recurrence_interval": "5 Minutes",\n // "expiry_runs": 2,\n // "expiry_date": null\n // }\n\n}';

var config = {
method: 'put',
maxBodyLength: Infinity,
url: '{{URL}}/api/v1/agent/72',
headers: {
'X-API-Key': 'c6c2a6b3-3bba-41eb-a031-c767a645e9e9'
},
data : data
};

axios(config)
.then(function (response) {
console.log(JSON.stringify(response.data));
})
.catch(function (error) {
console.log(error);
});

Example Response
Body
{
"agent_id": 72
}

Headers
Server
nginx/1.24.0

Date
Fri, 18 Aug 2023 05:55:07 GMT

Content-Type
application/json

Content-Length
15

Connection
keep-alive

Run
An agent run is the end-to-end execution of the goals and instructions that has been assigned to the agent, operating within the set constraints with the necessary tools and resources.

POST
Create
{{URL}}/api/v1/agent/{agent_id}/run
This endpoint allows users to create an agent run

Parameter Type Description Required
agent_id path param: int Id of the agent to create runs for. yes
HEADERS
X-API-Key
776022a2-159e-40b5-8bd6-d733de2ade98

PARAMS
Body
raw (json)

{}

Example Request
var axios = require('axios');
var data = '{}';

var config = {
method: 'post',
maxBodyLength: Infinity,
url: '{{URL}}/api/v1/agent/{agent_id}/run',
headers: {
'X-API-Key': 'bf2b13a0-c5d3-403f-a887-ac8849b8304b'
},
data : data
};

axios(config)
.then(function (response) {
console.log(JSON.stringify(response.data));
})
.catch(function (error) {
console.log(error);
});

Example Response
Body
{
"run_id": 40
}
Headers (5)
{
"run_id": 40
}

POST
Retrieve Agent Runs
{{URL}}/api/v1/agent/{agent_id}/run-status
This endpoint allows users to retrieve an agent runs
Table
Parameter Type Description Required
agent_id path param: int Id of the agent to retrieve agent runs for yes
run_status_filter string Below are the supported values for run_status_filter:
RUNNING
PAUSED
COMPLETED

Only one value for run_status_filter should be passed at a time.

If this param is NOT passed in the request body, api will return statuses of all agent runs no
run_ids array of int List of agent run_ids to fetch run status for.

If this param is NOT passed in the request body, api will return statuses of all agent runs no

HEADERS
X-API-Key
e3347a48-c4f0-4fcc-b444-7a375473c712

PARAMS
run_ids
[78,79]

Body
raw (json)
json
{
"run_status_filter":"RUNNING" // run_status_filter could be values like RUNNING, PAUSED, COMPLETED
}

Example Request
var axios = require('axios');
var data = '{\n "run_status_filter":"RUNNING" // run_status_filter could be values like RUNNING, PAUSED, COMPLETED\n}\n';

var config = {
method: 'post',
maxBodyLength: Infinity,
url: '{{URL}}/api/v1/agent/{agent_id}/run-status',
headers: {
'X-API-Key': 'bf2b13a0-c5d3-403f-a887-ac8849b8304b'
},
data : data
};

axios(config)
.then(function (response) {
console.log(JSON.stringify(response.data));
})
.catch(function (error) {
console.log(error);
});

Example Response
Body
json
[
{
"run_id": 39,
"status": "RUNNING"
}
]

Headers (5)
Server
nginx/1.24.0

Date
Wed, 16 Aug 2023 14:05:09 GMT

Content-Type
application/json

Content-Length
34

Connection
keep-alive

Resources
Resources are the input/output files used or generated by the agent during its run.

POST
Retrieve Run Resources
{{URL}}/api/v1/agent/resources/output
This endpoint allows users to retrieve resources of an agent run

Parameter Type Description Required
run_ids array of int List of agent run_ids to fetch resources for. yes
HEADERS
X-API-Key
426436df-e4cb-428d-af9f-65b162d3ada3

Body
raw (json)
json
{
"run_ids":[97,98,99,100,101,102]
}

Example Request
var axios = require('axios');
var data = '{\n "run_ids":[38]\n}';

var config = {
method: 'post',
maxBodyLength: Infinity,
url: '{{URL}}/api/v1/agent/resources/output',
headers: {
'X-API-Key': 'bf2b13a0-c5d3-403f-a887-ac8849b8304b'
},
data : data
};

axios(config)
.then(function (response) {
console.log(JSON.stringify(response.data));
})
.catch(function (error) {
console.log(error);
});

Example Response
Body
json
{
"38": [
"https://superagi-instagram-tool.s3.amazonaws.com/public_resources/run_id38/cat_image_running.png",
"https://superagi-instagram-tool.s3.amazonaws.com/public_resources/run_id38/cat_image_jumping.png"
],
"39": [
"https://superagi-instagram-tool.s3.amazonaws.com/public_resources/run_id38/cat_image_small.png"
]
}

Headers
Server
nginx/1.24.0

Date
Wed, 16 Aug 2023 14:15:16 GMT

Content-Type
application/json

Content-Length
99

Connection
keep-alive
