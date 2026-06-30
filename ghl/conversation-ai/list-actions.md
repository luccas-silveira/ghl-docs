---
title: "List Actions for an Agent"
source_url: https://marketplace.gohighlevel.com/docs/ghl/conversation-ai/list-actions
version: v3
method: GET
endpoint: https://services.leadconnectorhq.com/conversation-ai/agents/:agentId/actions/list
---
# List Actions for an Agent

```
GET https://services.leadconnectorhq.com/conversation-ai/agents/:agentId/actions/list
```


List for actions for an agent

### Requirements

#### Scope(s)

`conversation-ai.readonly`

#### Auth Method(s)

`OAuth Access Token``Private Integration Token`

#### Token Type(s)

`Sub-Account Token`

## Request [​](https://marketplace.gohighlevel.com/docs/ghl/conversation-ai/list-actions/\#request "Direct link to Request")

### Header Parameters

**Version** stringrequired

**Possible values:** \[`v3`\]

API Version

### Path Parameters

**agentId** stringrequired

## Responses [​](https://marketplace.gohighlevel.com/docs/ghl/conversation-ai/list-actions/\#responses "Direct link to Responses")

- 200
- 400
- 401
- 422

Success

- application/json

- Schema
- Example (auto)

**Schema**

**data** object\[\]required

Grouped actions by type

Array \[\
\
**id** stringrequired\
\
Unique identifier for the action\
\
Example:`actionId123`\
\
**name** stringrequired\
\
Name of the action\
\
Example:`Trigger Workflow`\
\
**type** stringrequired\
\
Type of the action\
\
**Possible values:** \[`triggerWorkflow`, `updateContactField`, `appointmentBooking`, `stopBot`, `humanHandOver`, `advancedFollowup`, `transferBot`\]\
\
Example:`triggerWorkflow`\
\
**agentId** string\
\
Agent ID where the action belongs\
\
Example:`agentId123`\
\
**details** objectrequired\
\
Action-specific details. The structure depends on the action type. For TRIGGER\_WORKFLOW use triggerWorkflowDto, for UPDATE\_CONTACT\_FIELD use updateContactFieldDto, for APPOINTMENT\_BOOKING use appointmentBookingDto, for STOP\_BOT use stopBotDto, for HUMAN\_HAND\_OVER use humanHandOverDto, for ADVANCED\_FOLLOWUP use advancedFollowupDto, and for TRANSFER\_BOT use transferBotDto.\
\
oneOf\
\
- triggerWorkflowDto\
- updateContactFieldDto\
- appointmentBookingDto\
- stopBotDto\
- humanHandOverDto\
- advancedFollowupDto\
- transferBotDto\
\
**workflowIds** string\[\]required\
\
Array of workflow IDs to trigger\
\
Example:`["workflow123","workflow456"]`\
\
**triggerCondition** stringrequired\
\
Condition that triggers the workflow\
\
Example:`When user requests appointment`\
\
**triggerMessage** string\
\
Optional message to send when triggering the workflow\
\
Example:`Workflow triggered successfully`\
\
**contactFieldId** stringrequired\
\
ID of the contact field in Contacts Table\
\
Example:`123`\
\
**description** stringrequired\
\
Description of the contact field in Contacts Table\
\
Example:`Business Name`\
\
**contactUpdateExamples** string\[\]\
\
Contact update examples in Contacts Table. Not required when using standard fields, Monetory or Date Custom fields.\
\
**Default value:**`[]`\
\
Example:`["Example 1"]`\
\
**actionId** string\
\
Optional action ID reference\
\
Example:`action123`\
\
**calendarId** stringrequired\
\
Calendar ID for appointment booking\
\
Example:`calendar123`\
\
**onlySendLink** booleanrequired\
\
If true, only sends the appointment link without booking\
\
Example:`false`\
\
**triggerWorkflow** booleanrequired\
\
Whether to trigger a workflow after booking (cannot be true when onlySendLink is true)\
\
Example:`true`\
\
**workflowIds** string\[\]\
\
Workflow IDs to trigger after booking (required when triggerWorkflow is true)\
\
Example:`["workflow123"]`\
\
**sleepAfterBooking** booleanrequired\
\
Whether to put the agent to sleep after booking (cannot be true when onlySendLink is true)\
\
Example:`true`\
\
**sleepTimeUnit** string\
\
Unit for sleep time (required when sleepAfterBooking is true)\
\
**Possible values:** \[`days`, `hours`, `minutes`\]\
\
Example:`hours`\
\
**sleepTime** number\
\
Sleep duration (required when sleepAfterBooking is true)\
\
Example:`24`\
\
**transferBot** booleanrequired\
\
Whether to transfer to another agent after booking (cannot be true when onlySendLink is true)\
\
Example:`false`\
\
**transferAgent** string\
\
Agent ID to transfer to (required when transferBot is true)\
\
Example:`employee456`\
\
**rescheduleEnabled** booleanrequired\
\
Whether to allow appointment rescheduling (cannot be true when onlySendLink is true)\
\
**Default value:** `false`\
\
Example:`true`\
\
**cancelEnabled** booleanrequired\
\
Whether to allow appointment cancellation (cannot be true when onlySendLink is true)\
\
**Default value:** `false`\
\
Example:`true`\
\
**stopBotDetectionType** stringrequired\
\
Type of stop bot detection - Goodbye or Custom\
\
**Possible values:** \[`Goodbye`, `Custom`\]\
\
Example:`Custom`\
\
**stopBotTriggerCondition** stringrequired\
\
Condition that triggers stopping the bot\
\
Example:`When the user says they no longer need assistance or want to end the conversation`\
\
**reactivateEnabled** booleanrequired\
\
Whether the bot can be reactivated after being stopped\
\
Example:`true`\
\
**sleepTimeUnit** string\
\
Time unit for reactivation delay (required when reactivateEnabled is true)\
\
**Possible values:** \[`days`, `hours`, `minutes`\]\
\
Example:`hours`\
\
**sleepTime** number\
\
Time duration before reactivation (required when reactivateEnabled is true)\
\
Example:`24`\
\
**enabled** booleanrequired\
\
Whether this action is enabled for the agent\
\
Example:`true`\
\
**stopBotExamples** string\[\]required\
\
Example phrases that trigger stop bot action (minimum 2 required)\
\
Example:`["goodbye","thank you","no more questions"]`\
\
**finalMessage** stringrequired\
\
Final message sent when stopping the bot\
\
Example:`Thank you for contacting us. Have a great day!`\
\
**tags** string\[\]\
\
Tags to apply when stopping the bot\
\
Example:`["resolved","no-response"]`\
\
**enabled** booleanrequired\
\
Whether human handover action is enabled\
\
Example:`true`\
\
**triggerCondition** stringrequired\
\
Condition that triggers human handover\
\
Example:`When the user requests to speak with a human agent or expresses frustration`\
\
**examples** string\[\]\
\
Example phrases that trigger human handover (required when handoverType is custom or contactRequest)\
\
Example:`["speak to human","talk to agent","need help from person"]`\
\
**assignToUserId** string\
\
ID of the user to assign the conversation to\
\
Example:`user123`\
\
**skipAssignToUser** boolean\
\
Whether to skip assigning to a specific user\
\
Example:`false`\
\
**createTask** boolean\
\
Whether to create a task when handing over\
\
Example:`true`\
\
**reactivateEnabled** booleanrequired\
\
Whether the agent can be reactivated after handover\
\
Example:`true`\
\
**sleepTimeUnit** string\
\
Time unit for reactivation delay (required when reactivateEnabled is true)\
\
**Possible values:** \[`days`, `hours`, `minutes`\]\
\
Example:`hours`\
\
**sleepTime** number\
\
Time duration before reactivation (required when reactivateEnabled is true)\
\
Example:`24`\
\
**finalMessage** stringrequired\
\
Final message sent when handing over to human\
\
Example:`I am transferring you to a human agent who will assist you shortly.`\
\
**tags** string\[\]\
\
Tags to apply during handover\
\
Example:`["escalated","human-requested"]`\
\
**handoverType** stringrequired\
\
Type of human handover detection\
\
**Possible values:** \[`contactRequest`, `lackOfInformation`, `failedToResolveIssue`, `custom`\]\
\
Example:`contactRequest`\
\
**enabled** booleanrequired\
\
Whether advanced followup is enabled\
\
Example:`true`\
\
**scenarioId** stringrequired\
\
ID of the followup scenario\
\
**Possible values:** \[`contactStoppedReplying`, `contactIsBusy`, `contactRequested`\]\
\
Example:`contactIsBusy`\
\
**followupSequence** object\[\]required\
\
Sequence of followup actions to perform\
\
Array \[\
\
**id** numberrequired\
\
Unique identifier for this followup step\
\
Example:`1`\
\
**followupTimeUnit** stringrequired\
\
Time unit for followup delay\
\
**Possible values:** \[`days`, `hours`, `minutes`\]\
\
Example:`hours`\
\
**followupTime** numberrequired\
\
Time duration before followup (max: 60 minutes, 24 hours, or 180 days depending on unit)\
\
Example:`2`\
\
**aiEnabledMessage** boolean\
\
Whether to use AI to generate the followup message\
\
**Default value:** `true`\
\
Example:`true`\
\
**triggerWorkflow** boolean\
\
Whether to trigger a workflow during this followup\
\
**Default value:** `false`\
\
Example:`false`\
\
**customMessage** string\
\
Custom message to send (when aiEnabledMessage is false)\
\
Example:`Hi! Just following up on our previous conversation. Do you have any questions?`\
\
**workflowId** string\
\
Workflow ID to trigger (when triggerWorkflow is true)\
\
Example:`workflow789`\
\
**contactRequested** boolean\
\
Whether contact was requested in this followup\
\
Example:`false`\
\
\]\
\
**followupSettings** object\
\
Additional settings for followup behavior\
\
**dynamicChannelSwitching** booleanrequired\
\
Whether to dynamically switch channels for followups\
\
**Default value:** `true`\
\
Example:`true`\
\
**followUpHours** boolean\
\
Whether to respect working hours for followups\
\
Example:`true`\
\
**workingHours** object\[\]\
\
Working hours configuration for followups\
\
Array \[\
\
**dayOfTheWeek** numberrequired\
\
Day of the week (0=Sunday, 1=Monday, etc.)\
\
Example:`1`\
\
**intervals** object\[\]\
\
Time intervals for this day\
\
Array \[\
\
**startHour** numberrequired\
\
Start hour (24-hour format)\
\
Example:`9`\
\
**startMinute** numberrequired\
\
Start minute\
\
Example:`0`\
\
**endHour** numberrequired\
\
End hour (24-hour format)\
\
Example:`17`\
\
**endMinute** numberrequired\
\
End minute\
\
Example:`30`\
\
\]\
\
\]\
\
**timezoneToUse** string\
\
Timezone to use for followups, contact or location\
\
**Possible values:** \[`contact`, `business`\]\
\
**transferBotType** stringrequired\
\
Type of transfer - Default or Custom\
\
**Possible values:** \[`Default`, `Custom`\]\
\
Example:`Custom`\
\
**transferToBot** stringrequired\
\
ID of the bot/agent to transfer to\
\
Example:`employee789`\
\
**enabled** booleanrequired\
\
Whether this transfer action is enabled\
\
Example:`true`\
\
**transferBotTriggerCondition** string\
\
Condition that triggers the transfer (required for Custom type)\
\
Example:`When the user asks to speak with sales or needs pricing information`\
\
**transferBotExamples** string\[\]\
\
Example phrases that trigger transfer (required for Custom type, minimum 2)\
\
Example:`["talk to sales","pricing information","speak to specialist"]`\
\
\]

**success** booleanrequired

Success status of the request

Example:`true`

```json
{
  "data": [\
    {\
      "id": "actionId123",\
      "name": "Trigger Workflow",\
      "type": "triggerWorkflow",\
      "agentId": "agentId123",\
      "details": {\
        "workflowIds": [\
          "workflow123",\
          "workflow456"\
        ],\
        "triggerCondition": "When user requests appointment",\
        "triggerMessage": "Workflow triggered successfully"\
      }\
    }\
  ],
  "success": true
}
```

Bad Request

- application/json

- Schema
- Example (auto)

**Schema**

**statusCode** number

Example:`400`

**message** string

Example:`Bad Request`

```json
{
  "statusCode": 400,
  "message": "Bad Request"
}
```

Unauthorized

- application/json

- Schema
- Example (auto)

**Schema**

**statusCode** number

Example:`401`

**message** string

Example:`Invalid token: access token is invalid`

**error** string

Example:`Unauthorized`

```json
{
  "statusCode": 401,
  "message": "Invalid token: access token is invalid",
  "error": "Unauthorized"
}
```

Unprocessable Entity

- application/json

- Schema
- Example (auto)

**Schema**

**statusCode** number

Example:`422`

**message** string\[\]

Example:`["Unprocessable Entity"]`

**error** string

Example:`Unprocessable Entity`

```json
{
  "statusCode": 422,
  "message": [\
    "Unprocessable Entity"\
  ],
  "error": "Unprocessable Entity"
}
```

## Share your feedback

★★★★★

#### Authorization: Authorization

```
name: Authorizationtype: httpscopes: conversation-ai.readonlyscheme: bearerbearerFormat: JWTin: headerdescription: Use the Access Token generated with user type as Sub-Account (OR) Private Integration Token of Sub-Account.
```

- curl
- nodejs
- python
- php
- java
- go
- ruby
- powershell

- CURL

```bash
curl -L 'https://services.leadconnectorhq.com/conversation-ai/agents/:agentId/actions/list' \
-H 'Accept: application/json' \
-H 'Authorization: Bearer <TOKEN>'
```

Request Collapse all

Base URL

Edit

https://services.leadconnectorhq.com

Auth

Bearer Token

Parameters

agentId — pathrequired

Version — headerrequired

\-\-\-v3

Send API Request

ResponseClear

Click the `Send API Request` button above and see the response here!