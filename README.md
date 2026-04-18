# Microsoft Teams (microsoft-teams)
Microsoft Teams is a collaboration platform that combines workplace chat, meetings, file storage, and application integration. It provides APIs for building custom integrations, managing teams and channels, sending messages, scheduling meetings, and initiating calls through Microsoft Graph.

**URL:** [Visit APIs.json URL](https://raw.githubusercontent.com/api-evangelist/microsoft-teams/refs/heads/main/apis.yml)

**Run:** [Capabilities Using Naftiko](https://github.com/naftiko/fleet?utm_source=api-evangelist&utm_medium=readme&utm_campaign=company-api-evangelist&utm_content=repo)

## Tags:

 - Chat, Collaboration, Communication, Microsoft 365, Productivity, Video Conferencing

## Timestamps

- **Created:** 2024
- **Modified:** 2026-04-18

## APIs

### Microsoft Graph Teams API
Core REST API for accessing Teams data including teams, channels, messages, tabs, apps, members, online meetings, and calls through Microsoft Graph.

**Human URL:** [https://learn.microsoft.com/en-us/graph/api/resources/teams-api-overview](https://learn.microsoft.com/en-us/graph/api/resources/teams-api-overview)

#### Tags:

 - Channels, Messages, Microsoft Graph, REST API, Teams

#### Properties

- [Documentation](https://learn.microsoft.com/en-us/graph/api/resources/teams-api-overview)
- [OpenAPI](openapi/microsoft-teams-graph-api.yaml)
- [Authentication](https://learn.microsoft.com/en-us/graph/auth/)
- [SDK](https://learn.microsoft.com/en-us/graph/sdks/sdks-overview)
- [RateLimits](https://learn.microsoft.com/en-us/graph/throttling)

### Microsoft Teams Bot Framework API
API for building conversational bots that interact with users in Microsoft Teams through the Bot Framework.

**Human URL:** [https://learn.microsoft.com/en-us/microsoftteams/platform/bots/what-are-bots](https://learn.microsoft.com/en-us/microsoftteams/platform/bots/what-are-bots)

#### Tags:

 - Bot Framework, Bots, Conversational AI, Messaging

#### Properties

- [Documentation](https://learn.microsoft.com/en-us/microsoftteams/platform/bots/how-to/conversations/conversation-basics)
- [Quickstart](https://learn.microsoft.com/en-us/microsoftteams/platform/build-your-first-app/build-bot)
- [CodeExamples](https://github.com/microsoft/BotBuilder-Samples)
- [APIReference](https://learn.microsoft.com/en-us/azure/bot-service/rest-api/bot-framework-rest-connector-api-reference)

### Microsoft Teams Webhook and Connector API
APIs for creating incoming webhooks and Office 365 connectors to post messages and notifications to Teams channels.

**Human URL:** [https://learn.microsoft.com/en-us/microsoftteams/platform/webhooks-and-connectors/what-are-webhooks-and-connectors](https://learn.microsoft.com/en-us/microsoftteams/platform/webhooks-and-connectors/what-are-webhooks-and-connectors)

#### Tags:

 - Connectors, Incoming Webhooks, Notifications, Webhooks

#### Properties

- [Documentation](https://learn.microsoft.com/en-us/microsoftteams/platform/webhooks-and-connectors/how-to/add-incoming-webhook)

### Microsoft Teams Real-Time Communication APIs
APIs for building calling and meeting experiences in Teams including VoIP calls, group calls, IVR flows, and online meetings.

**Human URL:** [https://learn.microsoft.com/en-us/graph/api/resources/communications-api-overview](https://learn.microsoft.com/en-us/graph/api/resources/communications-api-overview)

#### Tags:

 - Audio, Calling, Meetings, Real-Time, Video

#### Properties

- [Documentation](https://learn.microsoft.com/en-us/graph/api/resources/communications-api-overview)
- [APIReference](https://learn.microsoft.com/en-us/graph/api/resources/call)

## Common Properties

- [DeveloperPortal](https://developer.microsoft.com/en-us/microsoft-teams)
- [GettingStarted](https://learn.microsoft.com/en-us/microsoftteams/platform/get-started/get-started-overview)
- [SDK](https://learn.microsoft.com/en-us/microsoftteams/platform/toolkit/teams-toolkit-fundamentals)
- [Blog](https://techcommunity.microsoft.com/t5/microsoft-teams-blog/bg-p/MicrosoftTeamsBlog)
- [Support](https://learn.microsoft.com/en-us/answers/products/office-teams)
- [GitHubOrganization](https://github.com/OfficeDev/Microsoft-Teams-Samples)
- [StatusPage](https://status.teams.microsoft.com/)
- [TermsOfService](https://www.microsoft.com/en-us/legal/terms-of-use)
- [PrivacyPolicy](https://privacy.microsoft.com/en-us/privacystatement)

## Features

| Name | Description |
|------|-------------|
| Team Lifecycle Management | Create, archive, and delete teams programmatically. |
| Channel Management | Create and manage standard, private, and shared channels. |
| Messaging | Send and receive chat messages in channels and chats. |
| Member Management | Add, remove, and update team members and roles. |
| Online Meetings | Create and manage online meetings with join URLs. |
| Calling | Initiate calls, answer, reject, transfer, and manage IVR flows. |
| App Installation | Install and manage apps in teams and channels. |
| Activity Feed Notifications | Send activity feed notifications to engage users. |

## Use Cases

| Name | Description |
|------|-------------|
| Team Provisioning | Automate creation and configuration of teams for projects. |
| Messaging Automation | Send automated notifications and updates to channels. |
| Meeting Scheduling | Programmatically create and manage online meetings. |
| Customer Service Bots | Build conversational bots for customer support in Teams. |
| Workforce Management | Manage shifts and schedules for frontline workers. |

## Integrations

| Name | Description |
|------|-------------|
| Microsoft Power Automate | Automate Teams workflows with Power Automate connectors. |
| SharePoint | Teams channels with SharePoint document libraries. |
| OneDrive | Share and collaborate on files in Teams via OneDrive. |
| Azure Bot Service | Build and deploy bots using Azure Bot Service. |
| Adaptive Cards | Rich interactive cards for messaging and notifications. |

## Artifacts

Machine-readable API specifications organized by format.

### OpenAPI

- [Microsoft Graph Teams API](openapi/microsoft-teams-graph-api.yaml)

### JSON Schema

- [Team](json-schema/teams-graph-api-team-schema.json)
- [Channel](json-schema/teams-graph-api-channel-schema.json)
- [ChatMessage](json-schema/teams-graph-api-chat-message-schema.json)
- [ConversationMember](json-schema/teams-graph-api-conversation-member-schema.json)
- [OnlineMeeting](json-schema/teams-graph-api-online-meeting-schema.json)
- [Call](json-schema/teams-graph-api-call-schema.json)

### JSON Structure

- [Team](json-structure/teams-graph-api-team-structure.json)
- [Channel](json-structure/teams-graph-api-channel-structure.json)
- [ChatMessage](json-structure/teams-graph-api-chat-message-structure.json)
- [ConversationMember](json-structure/teams-graph-api-conversation-member-structure.json)
- [OnlineMeeting](json-structure/teams-graph-api-online-meeting-structure.json)
- [Call](json-structure/teams-graph-api-call-structure.json)

### JSON-LD

- [Microsoft Teams Graph API Context](json-ld/microsoft-teams-graph-api-context.jsonld)

### Examples

- [Team](examples/teams-graph-api-team-example.json)
- [Channel](examples/teams-graph-api-channel-example.json)
- [ChatMessage](examples/teams-graph-api-chat-message-example.json)
- [ConversationMember](examples/teams-graph-api-conversation-member-example.json)
- [OnlineMeeting](examples/teams-graph-api-online-meeting-example.json)
- [Call](examples/teams-graph-api-call-example.json)

## Capabilities

Naftiko capabilities organized as shared per-API definitions composed into customer-facing workflows.

### Shared Per-API Definitions

- [Microsoft Graph Teams API](capabilities/shared/teams-graph-api.yaml) -- 10 operations for team collaboration

### Workflow Capabilities

| Workflow | APIs Combined | Tools | Persona |
|----------|--------------|-------|---------|
| [Team Collaboration](capabilities/team-collaboration.yaml) | Teams Graph API | 10 | IT Administrator, Team Lead, Developer |

## Vocabulary

- [Microsoft Teams Vocabulary](vocabulary/microsoft-teams-vocabulary.yaml) -- Unified taxonomy mapping 8 resources, 12 actions, 1 workflow, and 3 personas across operational (OpenAPI) and capability (Naftiko) dimensions

## Rules

- [Microsoft Teams Spectral Rules](rules/microsoft-teams-spectral-rules.yml) -- 22 rules across 9 categories enforcing Microsoft Teams API conventions

## Maintainers

**FN:** Kin Lane

**Email:** kin@apievangelist.com
