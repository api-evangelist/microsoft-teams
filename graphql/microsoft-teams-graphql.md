# Microsoft Teams GraphQL Schema

## Overview

This GraphQL schema provides a conceptual representation of the Microsoft Teams API surface exposed through Microsoft Graph. It maps the core Teams resources — teams, channels, messages, meetings, call records, apps, members, and notifications — into a typed GraphQL schema suitable for tooling, documentation, and exploratory graph queries.

The schema is derived from the Microsoft Graph Teams API documented at:
- https://learn.microsoft.com/en-us/graph/api/resources/teams-api-overview
- https://learn.microsoft.com/en-us/graph/api/resources/communications-api-overview

## Source

**Provider:** Microsoft Teams
**Underlying API:** Microsoft Graph (REST)
**Base URL:** https://graph.microsoft.com/v1.0
**GitHub:** https://github.com/microsoftgraph

## Schema File

[microsoft-teams-schema.graphql](microsoft-teams-schema.graphql)

## Type Coverage

The schema defines 68 named GraphQL types organized across the following domains:

### Team and Channel Management
- `Team` — Core team resource with settings, members, channels, and installed apps
- `Channel` — A channel within a team (standard, private, or shared)
- `PrimaryChannel` — The default General channel for a team
- `SharedChannel` — A channel shared across multiple tenants
- `SharedChannelTeamInfo` — Metadata about a team hosting a shared channel
- `SharedChannelInvitation` — Invitation to join a shared channel from an external tenant
- `IncomingChannel` — A shared channel incoming to a team from another tenant
- `TeamSettings` — Top-level settings container for a team
- `FunSettings` — Controls for GIFs, stickers, and memes in a team
- `GuestSettings` — Controls for what guests can do in a team
- `MessagingSettings` — Controls for messaging permissions in a team
- `DiscoverySettings` — Controls for team discoverability

### Messaging
- `ChannelMessage` — A message posted in a channel
- `MessageContent` — The body content of a message (text or HTML)
- `MessageAttachment` — A file, card, or reference attached to a message
- `Mention` — An @mention of a user, team, channel, application, or tag
- `Reaction` — An emoji reaction on a message
- `Reply` — A reply to a channel message

### Membership
- `ConversationMember` — Base type for a member of a chat or channel
- `TeamMember` — A member of a team
- `ChannelMembership` — Membership record for a channel (used for private/shared channels)
- `AssignedLabel` — A sensitivity label assigned to a team

### Apps and Tabs
- `TeamsApp` — An application available in the Teams app catalog
- `TeamsAppDefinition` — A specific version of a Teams app
- `TeamsAppInstallation` — An app installed within a team or chat
- `TeamsTab` — A tab pinned in a channel or chat

### Meetings and Communications
- `Meeting` — A scheduled Teams meeting
- `OnlineMeeting` — An online meeting with join URL and participant details
- `MeetingPolicy` — Policy settings governing meeting capabilities
- `MeetingTranscript` — A transcript resource for a completed meeting
- `MeetingAttendance` — Attendance report for a meeting
- `AttendanceRecord` — A single attendee's attendance record
- `AttendanceInterval` — A time interval during which an attendee was present

### Call Records
- `CallRecord` — A record of a completed Teams call
- `Segment` — A segment within a call session
- `Session` — A peer-to-peer or group session within a call record
- `Endpoint` — A participant endpoint in a call (device/user)
- `CallerInfo` — Identity and device information for the caller
- `ParticipantInfo` — Identity information for a call participant

### Tags
- `TeamworkTag` — A tag that can be applied to members in a team
- `TeamworkTagMember` — A member associated with a teamwork tag

### Operations and Notifications
- `TeamsAsyncOperation` — A long-running asynchronous operation on a team resource
- `SendActivityNotification` — Input for sending an activity notification to a user
- `ActivityNotification` — A notification delivered to a user's Teams activity feed
- `ActivityTemplate` — Template describing the type of activity notification
- `Invitation` — An invitation sent to a user to join a team
- `Webhook` — A change notification subscription for Teams resources
- `ResourceSpecificPermission` — A resource-specific consent permission for an app

### Scalar and Enum Types
- `DateTime`, `JSON`, `URL` — common scalars
- `ChannelMembershipType`, `CallDirection`, `CallType`, `MeetingChatMode`, `OnlineMeetingRole`, `TeamVisibilityType`, `TeamworkTagType`, `TeamsAsyncOperationStatus`, `TeamsAsyncOperationType`, `MediaDirection`, `Modality`, `ChannelMessageType`, `ChannelMessageImportance` — domain enums

## Usage Notes

This schema is a conceptual mapping. Microsoft Graph does not natively expose a GraphQL endpoint; this schema represents the equivalent resource graph derived from the REST API surface. It is intended for:

- Documentation and developer education
- Schema-driven tooling (linters, mocking, test data generation)
- Graph exploration and query planning
- Integration mapping with GraphQL gateway layers (e.g., Hasura, Apollo Federation, StepZen)

## References

- Microsoft Graph Teams API Overview: https://learn.microsoft.com/en-us/graph/api/resources/teams-api-overview
- Microsoft Graph Communications API: https://learn.microsoft.com/en-us/graph/api/resources/communications-api-overview
- Microsoft Graph SDKs: https://learn.microsoft.com/en-us/graph/sdks/sdks-overview
- Microsoft Graph GitHub: https://github.com/microsoftgraph
