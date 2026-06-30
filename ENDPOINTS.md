# GoHighLevel API — Endpoint Manifest

Every documented endpoint, grouped by resource. 529 endpoints.

## ghl

| Method | Path | Endpoint | Scope | File |
|---|---|---|---|---|
| GET | `/affiliate-manager/:locationId/affiliates/:affiliateId` | Get Affiliate | affiliate-manager.readonly | [get-affiliate.md](ghl/affiliate-manager/get-affiliate.md) |
| GET | `/affiliate-manager/:locationId/affiliates` | List Affiliates | affiliate-manager.readonly | [list-affiliates.md](ghl/affiliate-manager/list-affiliates.md) |
| GET | `/affiliate-manager/:locationId/commissions` | List Commissions | affiliate-manager.readonly | [list-commissions.md](ghl/affiliate-manager/list-commissions.md) |
| GET | `/affiliate-manager/:locationId/payouts` | List Payouts | affiliate-manager.readonly | [list-payouts.md](ghl/affiliate-manager/list-payouts.md) |
| POST | `/agent-studio/agent` | Create Agent | agent-studio.write | [create-agent.md](ghl/agent-studio/create-agent.md) |
| DELETE | `/agent-studio/agent/:agentId` | Delete Agent | agent-studio.write | [delete-agent.md](ghl/agent-studio/delete-agent.md) |
| POST | `/agent-studio/public-api/agents/:agentId/execute` | Execute Agent (Deprecated) | agent-studio.write | [execute-agent-deprecated.md](ghl/agent-studio/execute-agent-deprecated.md) |
| POST | `/agent-studio/agent/:agentId/execute` | Execute Agent | agent-studio.write | [execute-agent.md](ghl/agent-studio/execute-agent.md) |
| GET | `/agent-studio/public-api/agents/:agentId` | Get Agent (Deprecated) | agent-studio.readonly | [get-agent-by-id-deprecated.md](ghl/agent-studio/get-agent-by-id-deprecated.md) |
| GET | `/agent-studio/agent/:agentId` | Get Agent | agent-studio.readonly | [get-agent-by-id.md](ghl/agent-studio/get-agent-by-id.md) |
| GET | `/agent-studio/public-api/agents` | List Agents (Deprecated) | agent-studio.readonly | [get-agents-deprecated.md](ghl/agent-studio/get-agents-deprecated.md) |
| GET | `/agent-studio/agent` | List Agents | agent-studio.readonly | [get-agents.md](ghl/agent-studio/get-agents.md) |
| POST | `/agent-studio/agent/versions/:versionId/publish` | Promote to Production | agent-studio.write | [promote-and-publish.md](ghl/agent-studio/promote-and-publish.md) |
| PATCH | `/agent-studio/agent/:agentId` | Update Agent Metadata | agent-studio.write | [update-agent-metadata.md](ghl/agent-studio/update-agent-metadata.md) |
| PATCH | `/agent-studio/agent/versions/:versionId` | Update Agent | agent-studio.write | [update-agent-version.md](ghl/agent-studio/update-agent-version.md) |
| POST | `/associations` | Create Association | associations.write | [create-association.md](ghl/associations/create-association.md) |
| POST | `/associations/relations` | Create Relation for you associated entities. | associations/relation.write | [create-relation.md](ghl/associations/create-relation.md) |
| DELETE | `/associations/:associationId` | Delete Association | associations.write | [delete-association.md](ghl/associations/delete-association.md) |
| DELETE | `/associations/relations/:relationId` | Delete Relation | associations/relation.write | [delete-relation.md](ghl/associations/delete-relation.md) |
| GET | `/associations` | Get all associations for a sub-account / location | associations.readonly | [find-associations.md](ghl/associations/find-associations.md) |
| GET | `/associations/:associationId` | Get association by ID | associations.readonly | [get-association-by-id.md](ghl/associations/get-association-by-id.md) |
| GET | `/associations/objectKey/:objectKey` | Get association by object keys | associations.readonly | [get-association-by-object-keys.md](ghl/associations/get-association-by-object-keys.md) |
| GET | `/associations/key/:key_name` | Get association key by key name | associations.readonly | [get-association-key-by-key-name.md](ghl/associations/get-association-key-by-key-name.md) |
| GET | `/associations/relations/:recordId` | Get all relations By record Id | associations/relation.readonly | [get-relations-by-record-id.md](ghl/associations/get-relations-by-record-id.md) |
| PUT | `/associations/:associationId` | Update Association By Id | associations.write | [update-association.md](ghl/associations/update-association.md) |
| GET | `/blogs/posts/url-slug-exists` | Check url slug | blogs/check-slug.readonly | [check-url-slug-exists.md](ghl/blogs/check-url-slug-exists.md) |
| POST | `/blogs/posts` | Create Blog Post | blogs/post.write | [create-blog-post.md](ghl/blogs/create-blog-post.md) |
| GET | `/blogs/authors` | Get all authors | blogs/author.readonly | [get-all-blog-authors-by-location.md](ghl/blogs/get-all-blog-authors-by-location.md) |
| GET | `/blogs/categories` | Get all categories | blogs/category.readonly | [get-all-categories-by-location.md](ghl/blogs/get-all-categories-by-location.md) |
| GET | `/blogs/posts/all` | Get Blog posts by Blog ID | blogs/posts.readonly | [get-blog-post.md](ghl/blogs/get-blog-post.md) |
| GET | `/blogs/site/all` | Get Blogs by Location ID | blogs/list.readonly | [get-blogs.md](ghl/blogs/get-blogs.md) |
| PUT | `/blogs/posts/:postId` | Update Blog Post | blogs/post-update.write | [update-blog-post.md](ghl/blogs/update-blog-post.md) |
| POST | `/brand-boards` | Create a new brand board | brand-boards/design-kit.write | [create-brand-board.md](ghl/brand-boards/create-brand-board.md) |
| POST | `/brand-boards/locations/:locationId/brand-voices` | Create Brand Voice |  | [create-brand-voice.md](ghl/brand-boards/create-brand-voice.md) |
| DELETE | `/brand-boards/:locationId/:id` | Delete a Brand Board | brand-boards/design-kit.write | [delete-brand-board.md](ghl/brand-boards/delete-brand-board.md) |
| DELETE | `/brand-boards/locations/:locationId/brand-voices/:brandVoiceId` | Delete Brand Voice |  | [delete-brand-voice.md](ghl/brand-boards/delete-brand-voice.md) |
| GET | `/brand-boards/:locationId/:id` | Get Brand Board | brand-boards/design-kit.readonly | [get-brand-board-by-id.md](ghl/brand-boards/get-brand-board-by-id.md) |
| GET | `/brand-boards/:locationId` | Get Brand Boards | brand-boards/design-kit.readonly | [get-brand-boards-by-location.md](ghl/brand-boards/get-brand-boards-by-location.md) |
| GET | `/brand-boards/locations/:locationId/brand-voices/:brandVoiceId` | Get Brand Voice |  | [get-brand-voice.md](ghl/brand-boards/get-brand-voice.md) |
| GET | `/brand-boards/locations/:locationId/brand-voices` | List Brand Voices |  | [list-brand-voices.md](ghl/brand-boards/list-brand-voices.md) |
| POST | `/brand-boards/locations/:locationId/brand-voices/:brandVoiceId/default` | Set Default Brand Voice |  | [set-default-brand-voice.md](ghl/brand-boards/set-default-brand-voice.md) |
| PATCH | `/brand-boards/:locationId/:id` | Update a Brand Board | brand-boards/design-kit.write | [update-brand-board.md](ghl/brand-boards/update-brand-board.md) |
| PATCH | `/brand-boards/locations/:locationId/brand-voices/:brandVoiceId` | Update Brand Voice |  | [update-brand-voice.md](ghl/brand-boards/update-brand-voice.md) |
| POST | `/businesses` | Create Business | businesses.write | [create-business.md](ghl/businesses/create-business.md) |
| DELETE | `/businesses/:businessId` | Delete Business | businesses.write | [delete-business.md](ghl/businesses/delete-business.md) |
| GET | `/businesses/:businessId` | Get Business | businesses.readonly | [get-business.md](ghl/businesses/get-business.md) |
| GET | `/businesses` | Get Businesses by Location | businesses.readonly | [get-businesses-by-location.md](ghl/businesses/get-businesses-by-location.md) |
| PUT | `/businesses/:businessId` | Update Business | businesses.write | [update-business.md](ghl/businesses/update-business.md) |
| PUT | `/calendars/schedules/:id/associations/:calendarId` | Apply user availability schedule to a calendar | calendars.write | [add-calendar-to-schedule.md](ghl/calendars/add-calendar-to-schedule.md) |
| POST | `/calendars/appointments/:appointmentId/notes` | Create Note | calendars/events.write | [create-appointment-note.md](ghl/calendars/create-appointment-note.md) |
| POST | `/calendars/events/appointments` | Create appointment | calendars/events.write | [create-appointment.md](ghl/calendars/create-appointment.md) |
| POST | `/calendars/events/block-slots` | Create Block Slot | calendars/events.write | [create-block-slot.md](ghl/calendars/create-block-slot.md) |
| POST | `/calendars/groups` | Create Calendar Group | calendars/groups.write | [create-calendar-group.md](ghl/calendars/create-calendar-group.md) |
| POST | `/calendars/resources/:resourceType` | Create Calendar Resource | calendars/resources.write | [create-calendar-resource.md](ghl/calendars/create-calendar-resource.md) |
| POST | `/calendars/schedules/event-calendar/:calendarId` | Create event calendar availability schedule | calendars.write | [create-calendar-schedule.md](ghl/calendars/create-calendar-schedule.md) |
| POST | `/calendars` | Create Calendar | calendars.write | [create-calendar.md](ghl/calendars/create-calendar.md) |
| POST | `/calendars/:calendarId/notifications` | Create notification | calendars/events.write | [create-event-notification.md](ghl/calendars/create-event-notification.md) |
| POST | `/calendars/schedules` | Create user availability schedule | calendars.write | [create-schedule.md](ghl/calendars/create-schedule.md) |
| POST | `/calendars/services/bookings` | Create Service Booking | calendars/events.write | [create-service-booking.md](ghl/calendars/create-service-booking.md) |
| POST | `/calendars/services/catalog` | Create Service | calendars.write | [create-service-catalog.md](ghl/calendars/create-service-catalog.md) |
| POST | `/calendars/services/locations` | Create Service Location | calendars.write | [create-service-location.md](ghl/calendars/create-service-location.md) |
| DELETE | `/calendars/appointments/:appointmentId/notes/:noteId` | Delete Note | calendars/events.write | [delete-appointment-note.md](ghl/calendars/delete-appointment-note.md) |
| DELETE | `/calendars/resources/:resourceType/:id` | Delete Calendar Resource | calendars/resources.write | [delete-calendar-resource.md](ghl/calendars/delete-calendar-resource.md) |
| DELETE | `/calendars/:calendarId` | Delete Calendar | calendars.write | [delete-calendar.md](ghl/calendars/delete-calendar.md) |
| DELETE | `/calendars/:calendarId/notifications/:notificationId` | Delete Notification | calendars/events.write | [delete-event-notification.md](ghl/calendars/delete-event-notification.md) |
| DELETE | `/calendars/events/:eventId` | Delete Event | calendars/events.write | [delete-event.md](ghl/calendars/delete-event.md) |
| DELETE | `/calendars/groups/:groupId` | Delete Group | calendars/groups.write | [delete-group.md](ghl/calendars/delete-group.md) |
| DELETE | `/calendars/schedules/:id` | Delete user availability schedule | calendars.write | [delete-schedule.md](ghl/calendars/delete-schedule.md) |
| DELETE | `/calendars/services/bookings/:bookingId` | Delete Service Booking | calendars/events.write | [delete-service-booking.md](ghl/calendars/delete-service-booking.md) |
| DELETE | `/calendars/services/catalog/:serviceId` | Delete Service | calendars.write | [delete-service-catalog.md](ghl/calendars/delete-service-catalog.md) |
| DELETE | `/calendars/services/locations/:serviceLocationId` | Delete Service Location | calendars.write | [delete-service-location.md](ghl/calendars/delete-service-location.md) |
| PUT | `/calendars/groups/:groupId/status` | Disable Group | calendars/groups.write | [disable-group.md](ghl/calendars/disable-group.md) |
| PUT | `/calendars/events/appointments/:eventId` | Update Appointment | calendars/events.write | [edit-appointment.md](ghl/calendars/edit-appointment.md) |
| PUT | `/calendars/events/block-slots/:eventId` | Update Block Slot | calendars/events.write | [edit-block-slot.md](ghl/calendars/edit-block-slot.md) |
| PUT | `/calendars/groups/:groupId` | Update Group | calendars/groups.write | [edit-group.md](ghl/calendars/edit-group.md) |
| GET | `/calendars/resources/:resourceType` | List Calendar Resources | calendars/resources.readonly | [fetch-calendar-resources.md](ghl/calendars/fetch-calendar-resources.md) |
| GET | `/calendars/:calendarId/notifications/:notificationId` | Get notification | calendars/events.readonly | [find-event-notification.md](ghl/calendars/find-event-notification.md) |
| GET | `/calendars/schedules/search` | List user availability schedule | calendars.readonly | [get-all-schedules.md](ghl/calendars/get-all-schedules.md) |
| GET | `/calendars/appointments/:appointmentId/notes` | Get Notes | calendars/events.readonly | [get-appointment-notes.md](ghl/calendars/get-appointment-notes.md) |
| GET | `/calendars/events/appointments/:eventId` | Get Appointment | calendars/events.readonly | [get-appointment.md](ghl/calendars/get-appointment.md) |
| GET | `/calendars/blocked-slots` | Get Blocked Slots | calendars/events.readonly | [get-blocked-slots.md](ghl/calendars/get-blocked-slots.md) |
| GET | `/calendars/events` | Get Calendar Events | calendars/events.readonly | [get-calendar-events.md](ghl/calendars/get-calendar-events.md) |
| GET | `/calendars/resources/:resourceType/:id` | Get Calendar Resource | calendars/resources.readonly | [get-calendar-resource.md](ghl/calendars/get-calendar-resource.md) |
| GET | `/calendars/schedules/event-calendar/:calendarId` | Get event calendar availability schedule | calendars.readonly | [get-calendar-schedule.md](ghl/calendars/get-calendar-schedule.md) |
| GET | `/calendars/:calendarId` | Get Calendar | calendars.readonly | [get-calendar.md](ghl/calendars/get-calendar.md) |
| GET | `/calendars` | Get Calendars | calendars.readonly | [get-calendars.md](ghl/calendars/get-calendars.md) |
| GET | `/calendars/:calendarId/notifications` | Get notifications | calendars/events.readonly | [get-event-notification.md](ghl/calendars/get-event-notification.md) |
| GET | `/calendars/groups` | Get Groups | calendars/groups.readonly | [get-groups.md](ghl/calendars/get-groups.md) |
| GET | `/calendars/schedules/:id` | Get user availability schedule | calendars.readonly | [get-schedule-by-id.md](ghl/calendars/get-schedule-by-id.md) |
| GET | `/calendars/services/bookings/:bookingId` | Get Service Booking by ID | calendars/events.readonly | [get-service-booking-by-id.md](ghl/calendars/get-service-booking-by-id.md) |
| GET | `/calendars/services/bookings` | Get Service Bookings | calendars/events.readonly | [get-service-bookings.md](ghl/calendars/get-service-bookings.md) |
| GET | `/calendars/services/catalog/:serviceId` | Get Service by ID | calendars.readonly | [get-service-catalog-by-id.md](ghl/calendars/get-service-catalog-by-id.md) |
| GET | `/calendars/services/locations/:serviceLocationId` | Get Service Location by ID | calendars.readonly | [get-service-location-by-id.md](ghl/calendars/get-service-location-by-id.md) |
| GET | `/calendars/services/locations` | Get Service Locations | calendars.readonly | [get-service-locations.md](ghl/calendars/get-service-locations.md) |
| GET | `/calendars/services/catalog` | Get Services | calendars.readonly | [get-services-catalog.md](ghl/calendars/get-services-catalog.md) |
| GET | `/calendars/:calendarId/free-slots` | Get Free Slots | calendars.readonly | [get-slots.md](ghl/calendars/get-slots.md) |
| DELETE | `/calendars/schedules/:id/associations/:calendarId` | Remove user availability schedule from a calendar | calendars.write | [remove-calendar-from-schedule.md](ghl/calendars/remove-calendar-from-schedule.md) |
| PUT | `/calendars/appointments/:appointmentId/notes/:noteId` | Update Note | calendars/events.write | [update-appointment-note.md](ghl/calendars/update-appointment-note.md) |
| PUT | `/calendars/resources/:resourceType/:id` | Update Calendar Resource | calendars/resources.write | [update-calendar-resource.md](ghl/calendars/update-calendar-resource.md) |
| PUT | `/calendars/schedules/event-calendar/:calendarId` | Update event calendar availability schedule | calendars.write | [update-calendar-schedule.md](ghl/calendars/update-calendar-schedule.md) |
| PUT | `/calendars/:calendarId` | Update Calendar | calendars.write | [update-calendar.md](ghl/calendars/update-calendar.md) |
| PUT | `/calendars/:calendarId/notifications/:notificationId` | Update notification | calendars/events.write | [update-event-notification.md](ghl/calendars/update-event-notification.md) |
| PUT | `/calendars/schedules/:id` | Update user availability schedule | calendars.write | [update-schedule.md](ghl/calendars/update-schedule.md) |
| PUT | `/calendars/services/bookings/:bookingId` | Update Service Booking | calendars/events.write | [update-service-booking.md](ghl/calendars/update-service-booking.md) |
| PUT | `/calendars/services/catalog/:serviceId` | Update Service | calendars.write | [update-service-catalog.md](ghl/calendars/update-service-catalog.md) |
| PUT | `/calendars/services/locations/:serviceLocationId` | Update Service Location | calendars.write | [update-service-location.md](ghl/calendars/update-service-location.md) |
| POST | `/calendars/groups/validate-slug` | Validate group slug | calendars/groups.write | [validate-groups-slug.md](ghl/calendars/validate-groups-slug.md) |
| GET | `/campaigns` | Get Campaigns | campaigns.readonly | [get-campaigns.md](ghl/campaigns/get-campaigns.md) |
| POST | `/chat-widget/clone` | Clone Chat Widget | chat-widget.write | [clone-chat-widget.md](ghl/chat-widget/clone-chat-widget.md) |
| POST | `/chat-widget` | Create Chat Widget | chat-widget.write | [create-chat-widget.md](ghl/chat-widget/create-chat-widget.md) |
| DELETE | `/chat-widget/:locationId/:id` | Delete Chat Widget | chat-widget.write | [delete.md](ghl/chat-widget/delete.md) |
| GET | `/chat-widget/data/:locationId/:id` | Get Chat Widget | chat-widget.readonly | [get-chat-widget.md](ghl/chat-widget/get-chat-widget.md) |
| GET | `/chat-widget/public/config/:id` | Get Widget Config |  | [get-widget.md](ghl/chat-widget/get-widget.md) |
| GET | `/chat-widget/list` | List Chat Widgets | chat-widget.readonly | [list-chat-widget.md](ghl/chat-widget/list-chat-widget.md) |
| PATCH | `/chat-widget/data/:locationId/:id` | Patch Chat Widget | chat-widget.write | [patch-chat-widget.md](ghl/chat-widget/patch-chat-widget.md) |
| PUT | `/chat-widget/data/:locationId/:id` | Update Chat Widget | chat-widget.write | [update-chat-widget.md](ghl/chat-widget/update-chat-widget.md) |
| GET | `/companies/:companyId` | Get Company | companies.readonly | [get-company.md](ghl/companies/get-company.md) |
| POST | `/contacts/:contactId/campaigns/:campaignId` | Add Contact to Campaign | contacts.write | [add-contact-to-campaign.md](ghl/contacts/add-contact-to-campaign.md) |
| POST | `/contacts/:contactId/workflow/:workflowId` | Add Contact to Workflow | contacts.write | [add-contact-to-workflow.md](ghl/contacts/add-contact-to-workflow.md) |
| POST | `/contacts/:contactId/followers` | Add Followers | contacts.write | [add-followers-contact.md](ghl/contacts/add-followers-contact.md) |
| POST | `/contacts/bulk/business` | Add/Remove Contacts From Business |  | [add-remove-contact-from-business.md](ghl/contacts/add-remove-contact-from-business.md) |
| POST | `/contacts/:contactId/tags` | Add Tags | contacts.write | [add-tags.md](ghl/contacts/add-tags.md) |
| POST | `/contacts/bulk/tags/update/:type` | Update Contacts Tags |  | [create-association.md](ghl/contacts/create-association.md) |
| POST | `/contacts` | Create Contact | contacts.write | [create-contact.md](ghl/contacts/create-contact.md) |
| POST | `/contacts/:contactId/notes` | Create Note | contacts.write | [create-note.md](ghl/contacts/create-note.md) |
| POST | `/contacts/:contactId/tasks` | Create Task | contacts.write | [create-task.md](ghl/contacts/create-task.md) |
| DELETE | `/contacts/:contactId/workflow/:workflowId` | Delete Contact from Workflow | contacts.write | [delete-contact-from-workflow.md](ghl/contacts/delete-contact-from-workflow.md) |
| DELETE | `/contacts/:contactId` | Delete Contact | contacts.write | [delete-contact.md](ghl/contacts/delete-contact.md) |
| DELETE | `/contacts/:contactId/notes/:id` | Delete Note | contacts.write | [delete-note.md](ghl/contacts/delete-note.md) |
| DELETE | `/contacts/:contactId/tasks/:taskId` | Delete Task | contacts.write | [delete-task.md](ghl/contacts/delete-task.md) |
| GET | `/contacts/:contactId/notes` | Get All Notes | contacts.readonly | [get-all-notes.md](ghl/contacts/get-all-notes.md) |
| GET | `/contacts/:contactId/tasks` | Get all Tasks | contacts.readonly | [get-all-tasks.md](ghl/contacts/get-all-tasks.md) |
| GET | `/contacts/:contactId/appointments` | Get Appointments for Contact | contacts.readonly | [get-appointments-for-contact.md](ghl/contacts/get-appointments-for-contact.md) |
| GET | `/contacts/:contactId` | Get Contact | contacts.readonly | [get-contact.md](ghl/contacts/get-contact.md) |
| GET | `/contacts/business/:businessId` | Get Contacts By BusinessId | contacts.readonly | [get-contacts-by-business-id.md](ghl/contacts/get-contacts-by-business-id.md) |
| GET | `/contacts/search/duplicate` | Get Duplicate Contact | contacts.readonly | [get-duplicate-contact.md](ghl/contacts/get-duplicate-contact.md) |
| GET | `/contacts/:contactId/notes/:id` | Get Note | contacts.readonly | [get-note.md](ghl/contacts/get-note.md) |
| GET | `/contacts/:contactId/tasks/:taskId` | Get Task | contacts.readonly | [get-task.md](ghl/contacts/get-task.md) |
| DELETE | `/contacts/:contactId/campaigns/:campaignId` | Remove Contact From Campaign | contacts.write | [remove-contact-from-campaign.md](ghl/contacts/remove-contact-from-campaign.md) |
| DELETE | `/contacts/:contactId/campaigns/remove-all` | Remove Contact From Every Campaign | contacts.write | [remove-contact-from-every-campaign.md](ghl/contacts/remove-contact-from-every-campaign.md) |
| DELETE | `/contacts/:contactId/followers` | Remove Followers | contacts.write | [remove-followers-contact.md](ghl/contacts/remove-followers-contact.md) |
| DELETE | `/contacts/:contactId/tags` | Remove Tags | contacts.write | [remove-tags.md](ghl/contacts/remove-tags.md) |
| POST | `/contacts/search` | Search Contacts | contacts.readonly | [search-contacts-advanced.md](ghl/contacts/search-contacts-advanced.md) |
| PUT | `/contacts/:contactId` | Update Contact | contacts.write | [update-contact.md](ghl/contacts/update-contact.md) |
| PUT | `/contacts/:contactId/notes/:id` | Update Note | contacts.write | [update-note.md](ghl/contacts/update-note.md) |
| PUT | `/contacts/:contactId/tasks/:taskId/completed` | Update Task Completed | contacts.write | [update-task-completed.md](ghl/contacts/update-task-completed.md) |
| PUT | `/contacts/:contactId/tasks/:taskId` | Update Task | contacts.write | [update-task.md](ghl/contacts/update-task.md) |
| POST | `/contacts/upsert` | Upsert Contact | contacts.write | [upsert-contact.md](ghl/contacts/upsert-contact.md) |
| POST | `/conversation-ai/agents/:agentId/actions` | Attach Action to Agent | conversation-ai.write | [create-action.md](ghl/conversation-ai/create-action.md) |
| POST | `/conversation-ai/agents` | Create an Agent | conversation-ai.write | [create-agent.md](ghl/conversation-ai/create-agent.md) |
| DELETE | `/conversation-ai/agents/:agentId/actions/:actionId` | Remove Action from Agent | conversation-ai.write | [delete-action.md](ghl/conversation-ai/delete-action.md) |
| DELETE | `/conversation-ai/agents/:agentId` | Delete Agent | conversation-ai.write | [delete-agent.md](ghl/conversation-ai/delete-agent.md) |
| GET | `/conversation-ai/agents/:agentId/actions/:actionId` | Get Action by ID | conversation-ai.readonly | [get-action-by-id.md](ghl/conversation-ai/get-action-by-id.md) |
| GET | `/conversation-ai/agents/:agentId` | Get Agent | conversation-ai.readonly | [get-agent.md](ghl/conversation-ai/get-agent.md) |
| GET | `/conversation-ai/generations` | Get the generation details | conversation-ai.readonly | [get-generation-details.md](ghl/conversation-ai/get-generation-details.md) |
| GET | `/conversation-ai/agents/:agentId/actions/list` | List Actions for an Agent | conversation-ai.readonly | [list-actions.md](ghl/conversation-ai/list-actions.md) |
| GET | `/conversation-ai/agents/search` | Search Agents | conversation-ai.readonly | [search-agent.md](ghl/conversation-ai/search-agent.md) |
| PUT | `/conversation-ai/agents/:agentId/actions/:actionId` | Update Action | conversation-ai.write | [update-action.md](ghl/conversation-ai/update-action.md) |
| PUT | `/conversation-ai/agents/:agentId` | Update Agent | conversation-ai.write | [update-agent.md](ghl/conversation-ai/update-agent.md) |
| PATCH | `/conversation-ai/agents/:agentId/followup-settings` | Update Followup Settings | conversation-ai.write | [update-followup-settings.md](ghl/conversation-ai/update-followup-settings.md) |
| POST | `/conversations/messages/inbound` | Add an inbound message | conversations/message.write | [add-an-inbound-message.md](ghl/conversations/add-an-inbound-message.md) |
| POST | `/conversations/messages/outbound` | Add an external outbound call | conversations/message.write | [add-an-outbound-message.md](ghl/conversations/add-an-outbound-message.md) |
| PUT | `/conversations/messages/:messageId/attachments` | Add message attachments | conversations/message.write | [add-message-attachments.md](ghl/conversations/add-message-attachments.md) |
| DELETE | `/conversations/messages/email/:emailMessageId/schedule` | Cancel a scheduled email message. | conversations/message.write | [cancel-scheduled-email-message.md](ghl/conversations/cancel-scheduled-email-message.md) |
| DELETE | `/conversations/messages/:messageId/schedule` | Cancel a scheduled message. | conversations/message.write | [cancel-scheduled-message.md](ghl/conversations/cancel-scheduled-message.md) |
| POST | `/conversations` | Create Conversation | conversations.write | [create-conversation.md](ghl/conversations/create-conversation.md) |
| DELETE | `/conversations/:conversationId` | Delete Conversation | conversations.write | [delete-conversation.md](ghl/conversations/delete-conversation.md) |
| GET | `/conversations/locations/:locationId/messages/:messageId/transcription/download` | Download transcription by Message ID |  | [download-message-transcription.md](ghl/conversations/download-message-transcription.md) |
| GET | `/conversations/messages/export` | Export messages by location ID | conversations/message.readonly | [export-messages-by-location.md](ghl/conversations/export-messages-by-location.md) |
| GET | `/conversations/:conversationId` | Get Conversation | conversations.readonly | [get-conversation.md](ghl/conversations/get-conversation.md) |
| GET | `/conversations/messages/email/:id` | Get email by Id | conversations/message.readonly | [get-email-by-id.md](ghl/conversations/get-email-by-id.md) |
| GET | `/conversations/messages/:messageId/locations/:locationId/recording` | Get Recording by Message ID |  | [get-message-recording.md](ghl/conversations/get-message-recording.md) |
| GET | `/conversations/locations/:locationId/messages/:messageId/transcription` | Get transcription by Message ID |  | [get-message-transcription.md](ghl/conversations/get-message-transcription.md) |
| GET | `/conversations/messages/:id` | Get message by message id | conversations/message.readonly | [get-message.md](ghl/conversations/get-message.md) |
| GET | `/conversations/:conversationId/messages` | Get messages by conversation id | conversations/message.readonly | [get-messages.md](ghl/conversations/get-messages.md) |
| POST | `/conversations/providers/live-chat/typing` | Agent/Ai-Bot is typing a message indicator for live chat | conversations/livechat.write | [live-chat-agent-typing.md](ghl/conversations/live-chat-agent-typing.md) |
| GET | `/conversations/search` | Search Conversations | conversations.readonly | [search-conversation.md](ghl/conversations/search-conversation.md) |
| POST | `/conversations/messages` | Send a new message | conversations/message.write | [send-a-new-message.md](ghl/conversations/send-a-new-message.md) |
| PUT | `/conversations/:conversationId` | Update Conversation | conversations.write | [update-conversation.md](ghl/conversations/update-conversation.md) |
| PUT | `/conversations/messages/email/:emailMessageId/status` | Update email message status | conversations/message.write | [update-email-message-status.md](ghl/conversations/update-email-message-status.md) |
| PUT | `/conversations/messages/:messageId/status` | Update message status | conversations/message.write | [update-message-status.md](ghl/conversations/update-message-status.md) |
| POST | `/conversations/messages/upload` | Upload file attachments | conversations/message.write | [upload-file-attachments.md](ghl/conversations/upload-file-attachments.md) |
| POST | `/courses/courses-exporter/public/import` | Import Courses |  | [import-courses.md](ghl/courses/import-courses.md) |
| POST | `/custom-fields/folder` | Create Custom Field Folder | locations/customFields.write | [create-custom-field-folder.md](ghl/custom-fields/create-custom-field-folder.md) |
| POST | `/custom-fields` | Create Custom Field | locations/customFields.write | [create-custom-field.md](ghl/custom-fields/create-custom-field.md) |
| DELETE | `/custom-fields/folder/:id` | Delete Custom Field Folder | locations/customFields.write | [delete-custom-field-folder.md](ghl/custom-fields/delete-custom-field-folder.md) |
| DELETE | `/custom-fields/:id` | Delete Custom Field By Id | locations/customFields.write | [delete-custom-field.md](ghl/custom-fields/delete-custom-field.md) |
| GET | `/custom-fields/:id` | Get Custom Field / Folder By Id | locations/customFields.readonly | [get-custom-field-by-id.md](ghl/custom-fields/get-custom-field-by-id.md) |
| GET | `/custom-fields/object-key/:objectKey` | Get Custom Fields By Object Key | locations/customFields.readonly | [get-custom-fields-by-object-key.md](ghl/custom-fields/get-custom-fields-by-object-key.md) |
| PUT | `/custom-fields/folder/:id` | Update Custom Field Folder Name | locations/customFields.write | [update-custom-field-folder.md](ghl/custom-fields/update-custom-field-folder.md) |
| PUT | `/custom-fields/:id` | Update Custom Field By Id | locations/customFields.write | [update-custom-field.md](ghl/custom-fields/update-custom-field.md) |
| POST | `/custom-menus` | Create Custom Menu Link | custom-menu-link.write | [create-custom-menu.md](ghl/custom-menus/create-custom-menu.md) |
| DELETE | `/custom-menus/:customMenuId` | Delete Custom Menu Link | custom-menu-link.write | [delete-custom-menu.md](ghl/custom-menus/delete-custom-menu.md) |
| GET | `/custom-menus/:customMenuId` | Get Custom Menu Link | custom-menu-link.readonly | [get-custom-menu-by-id.md](ghl/custom-menus/get-custom-menu-by-id.md) |
| GET | `/custom-menus` | Get Custom Menu Links | custom-menu-link.readonly | [get-custom-menus.md](ghl/custom-menus/get-custom-menus.md) |
| PUT | `/custom-menus/:customMenuId` | Update Custom Menu Link | custom-menu-link.write | [update-custom-menu.md](ghl/custom-menus/update-custom-menu.md) |
| POST | `/email/verify` | Email Verification | lc-email.readonly | [verify-email.md](ghl/email-isv/verify-email.md) |
| POST | `/emails/locations/:locationId/campaigns/emails` | Create Email Campaign | emails/campaigns.write | [create-email-campaign.md](ghl/emails/create-email-campaign.md) |
| POST | `/emails/locations/:locationId/templates` | Create an email template | emails/templates.write | [create-email-template.md](ghl/emails/create-email-template.md) |
| POST | `/emails/locations/:locationId/templates/folders` | Create a template folder | emails/templates.write | [create-template-folder.md](ghl/emails/create-template-folder.md) |
| DELETE | `/emails/locations/:locationId/campaigns/emails/:campaignId` | Delete Campaign | emails/campaigns.write | [delete-campaign.md](ghl/emails/delete-campaign.md) |
| DELETE | `/emails/locations/:locationId/templates/:templateId` | Delete a template | emails/templates.write | [delete-email-template.md](ghl/emails/delete-email-template.md) |
| GET | `/emails/locations/:locationId/campaigns/bulk-actions/:campaignId` | Get Bulk Action Campaign by ID | emails/campaigns.readonly | [get-bulk-action-campaign.md](ghl/emails/get-bulk-action-campaign.md) |
| GET | `/emails/locations/:locationId/campaigns/stats/:source/:sourceId` | Get Campaign Statistics | emails/stats.readonly | [get-campaign-stats.md](ghl/emails/get-campaign-stats.md) |
| GET | `/emails/locations/:locationId/campaigns/emails/:campaignId` | Get Email Campaign by ID | emails/campaigns.readonly | [get-email-campaign.md](ghl/emails/get-email-campaign.md) |
| GET | `/emails/locations/:locationId/templates/:templateId` | Get Email Template by ID | emails/templates.readonly | [get-email-template.md](ghl/emails/get-email-template.md) |
| GET | `/emails/locations/:locationId/campaigns/workflows/:campaignId` | Get Workflow Campaign by ID | emails/campaigns.readonly | [get-workflow-campaign.md](ghl/emails/get-workflow-campaign.md) |
| POST | `/emails/locations/:locationId/templates/import` | Import an email template | emails/templates.write | [import-email-template.md](ghl/emails/import-email-template.md) |
| GET | `/emails/locations/:locationId/campaigns/bulk-actions` | List Bulk Action Campaigns | emails/campaigns.readonly | [list-bulk-action-campaigns.md](ghl/emails/list-bulk-action-campaigns.md) |
| GET | `/emails/locations/:locationId/campaigns/emails` | List Email Campaigns | emails/campaigns.readonly | [list-email-campaigns.md](ghl/emails/list-email-campaigns.md) |
| GET | `/emails/locations/:locationId/templates` | List templates | emails/templates.readonly | [list-email-templates.md](ghl/emails/list-email-templates.md) |
| GET | `/emails/locations/:locationId/campaigns/workflows` | List Workflow Campaigns | emails/campaigns.readonly | [list-workflow-campaigns.md](ghl/emails/list-workflow-campaigns.md) |
| POST | `/emails/locations/:locationId/campaigns/emails/:campaignId/schedule` | Schedule Campaign | emails/campaigns.write | [schedule-campaign.md](ghl/emails/schedule-campaign.md) |
| PATCH | `/emails/locations/:locationId/campaigns/emails/:campaignId` | Update Email Campaign | emails/campaigns.write | [update-email-campaign.md](ghl/emails/update-email-campaign.md) |
| PATCH | `/emails/locations/:locationId/templates/:templateId` | Update an email template | emails/templates.write | [update-email-template.md](ghl/emails/update-email-template.md) |
| GET | `/forms/submissions` | Get Forms Submissions | forms.readonly | [get-forms-submissions.md](ghl/forms/get-forms-submissions.md) |
| GET | `/forms` | Get Forms | forms.readonly | [get-forms.md](ghl/forms/get-forms.md) |
| POST | `/forms/upload-custom-files` | Upload files to custom fields | forms.write | [upload-to-custom-fields.md](ghl/forms/upload-to-custom-fields.md) |
| POST | `/funnels/lookup/redirect` | Create Redirect | funnels/redirect.write | [create-redirect.md](ghl/funnels/create-redirect.md) |
| DELETE | `/funnels/lookup/redirect/:id` | Delete Redirect By Id | funnels/redirect.write | [delete-redirect-by-id.md](ghl/funnels/delete-redirect-by-id.md) |
| GET | `/funnels/lookup/redirect/list` | Fetch List of Redirects | funnels/redirect.readonly | [fetch-redirects-list.md](ghl/funnels/fetch-redirects-list.md) |
| GET | `/funnels/funnel/list` | Fetch List of Funnels |  | [get-funnels.md](ghl/funnels/get-funnels.md) |
| GET | `/funnels/page` | Fetch list of funnel pages |  | [get-pages-by-funnel-id.md](ghl/funnels/get-pages-by-funnel-id.md) |
| GET | `/funnels/page/count` | Fetch count of funnel pages |  | [get-pages-count-by-funnel-id.md](ghl/funnels/get-pages-count-by-funnel-id.md) |
| PATCH | `/funnels/lookup/redirect/:id` | Update Redirect By Id | funnels/redirect.write | [update-redirect-by-id.md](ghl/funnels/update-redirect-by-id.md) |
| POST | `/invoices/schedule/:scheduleId/auto-payment` | Manage Auto payment for an schedule invoice | invoices/schedule.write | [auto-payment-invoice-schedule.md](ghl/invoices/auto-payment-invoice-schedule.md) |
| POST | `/invoices/schedule/:scheduleId/cancel` | Cancel an scheduled invoice | invoices/schedule.write | [cancel-invoice-schedule.md](ghl/invoices/cancel-invoice-schedule.md) |
| POST | `/invoices/estimate/template` | Create Estimate Template | invoices/estimate.write | [create-estimate-template.md](ghl/invoices/create-estimate-template.md) |
| POST | `/invoices/estimate/:estimateId/invoice` | Create Invoice from Estimate | invoices/estimate.write | [create-invoice-from-estimate.md](ghl/invoices/create-invoice-from-estimate.md) |
| POST | `/invoices/schedule` | Create Invoice Schedule | invoices/schedule.write | [create-invoice-schedule.md](ghl/invoices/create-invoice-schedule.md) |
| POST | `/invoices/template` | Create template | invoices/template.write | [create-invoice-template.md](ghl/invoices/create-invoice-template.md) |
| POST | `/invoices` | Create Invoice | invoices.write | [create-invoice.md](ghl/invoices/create-invoice.md) |
| POST | `/invoices/estimate` | Create New Estimate | invoices/estimate.write | [create-new-estimate.md](ghl/invoices/create-new-estimate.md) |
| DELETE | `/invoices/estimate/template/:templateId` | Delete Estimate Template | invoices/estimate.write | [delete-estimate-template.md](ghl/invoices/delete-estimate-template.md) |
| DELETE | `/invoices/estimate/:estimateId` | Delete Estimate | invoices/estimate.write | [delete-estimate.md](ghl/invoices/delete-estimate.md) |
| DELETE | `/invoices/schedule/:scheduleId` | Delete schedule | invoices/schedule.write | [delete-invoice-schedule.md](ghl/invoices/delete-invoice-schedule.md) |
| DELETE | `/invoices/template/:templateId` | Delete template | invoices/template.write | [delete-invoice-template.md](ghl/invoices/delete-invoice-template.md) |
| DELETE | `/invoices/:invoiceId` | Delete invoice | invoices.write | [delete-invoice.md](ghl/invoices/delete-invoice.md) |
| GET | `/invoices/estimate/number/generate` | Generate Estimate Number | invoices/estimate.readonly | [generate-estimate-number.md](ghl/invoices/generate-estimate-number.md) |
| GET | `/invoices/generate-invoice-number` | Generate Invoice Number | invoices.readonly | [generate-invoice-number.md](ghl/invoices/generate-invoice-number.md) |
| GET | `/invoices/schedule/:scheduleId` | Get an schedule | invoices/schedule.readonly | [get-invoice-schedule.md](ghl/invoices/get-invoice-schedule.md) |
| GET | `/invoices/settings` | Get Invoice Settings | invoices.readonly | [get-invoice-settings.md](ghl/invoices/get-invoice-settings.md) |
| GET | `/invoices/template/:templateId` | Get an template | invoices/template.readonly | [get-invoice-template.md](ghl/invoices/get-invoice-template.md) |
| GET | `/invoices/:invoiceId` | Get invoice | invoices.readonly | [get-invoice.md](ghl/invoices/get-invoice.md) |
| GET | `/invoices/estimate/template` | List Estimate Templates | invoices/estimate.readonly | [list-estimate-templates.md](ghl/invoices/list-estimate-templates.md) |
| GET | `/invoices/estimate/list` | List Estimates | invoices/estimate.readonly | [list-estimates.md](ghl/invoices/list-estimates.md) |
| GET | `/invoices/schedule` | List schedules | invoices/schedule.readonly | [list-invoice-schedules.md](ghl/invoices/list-invoice-schedules.md) |
| GET | `/invoices/template` | List templates | invoices/template.readonly | [list-invoice-templates.md](ghl/invoices/list-invoice-templates.md) |
| GET | `/invoices` | List invoices | invoices.readonly | [list-invoices.md](ghl/invoices/list-invoices.md) |
| GET | `/invoices/estimate/template/preview` | Preview Estimate Template | invoices/estimate.readonly | [preview-estimate-template.md](ghl/invoices/preview-estimate-template.md) |
| POST | `/invoices/:invoiceId/record-payment` | Record a manual payment for an invoice | invoices.write | [record-invoice.md](ghl/invoices/record-invoice.md) |
| POST | `/invoices/schedule/:scheduleId/schedule` | Schedule an schedule invoice | invoices/schedule.write | [schedule-invoice-schedule.md](ghl/invoices/schedule-invoice-schedule.md) |
| POST | `/invoices/estimate/:estimateId/send` | Send Estimate | invoices/estimate.write | [send-estimate.md](ghl/invoices/send-estimate.md) |
| POST | `/invoices/:invoiceId/send` | Send invoice | invoices.write | [send-invoice.md](ghl/invoices/send-invoice.md) |
| POST | `/invoices/text2pay` | Create & Send | invoices.write | [text-2-pay-invoice.md](ghl/invoices/text-2-pay-invoice.md) |
| POST | `/invoices/schedule/:scheduleId/updateAndSchedule` | Update scheduled recurring invoice | invoices/schedule.write | [update-and-schedule-invoice-schedule.md](ghl/invoices/update-and-schedule-invoice-schedule.md) |
| PATCH | `/invoices/estimate/stats/last-visited-at` | Update estimate last visited at |  | [update-estimate-last-visited-at.md](ghl/invoices/update-estimate-last-visited-at.md) |
| PUT | `/invoices/estimate/template/:templateId` | Update Estimate Template | invoices/estimate.write | [update-estimate-template.md](ghl/invoices/update-estimate-template.md) |
| PUT | `/invoices/estimate/:estimateId` | Update Estimate | invoices/estimate.write | [update-estimate.md](ghl/invoices/update-estimate.md) |
| PATCH | `/invoices/stats/last-visited-at` | Update invoice last visited at |  | [update-invoice-last-visited-at.md](ghl/invoices/update-invoice-last-visited-at.md) |
| PATCH | `/invoices/:invoiceId/late-fees-configuration` | Update invoice late fees configuration |  | [update-invoice-late-fees-configuration.md](ghl/invoices/update-invoice-late-fees-configuration.md) |
| PATCH | `/invoices/template/:templateId/payment-methods-configuration` | Update template late fees configuration |  | [update-invoice-payment-methods-configuration.md](ghl/invoices/update-invoice-payment-methods-configuration.md) |
| PUT | `/invoices/schedule/:scheduleId` | Update schedule |  | [update-invoice-schedule.md](ghl/invoices/update-invoice-schedule.md) |
| PATCH | `/invoices/template/:templateId/late-fees-configuration` | Update template late fees configuration |  | [update-invoice-template-late-fees-configuration.md](ghl/invoices/update-invoice-template-late-fees-configuration.md) |
| PUT | `/invoices/template/:templateId` | Update template | invoices/template.write | [update-invoice-template.md](ghl/invoices/update-invoice-template.md) |
| PUT | `/invoices/:invoiceId` | Update invoice | invoices.write | [update-invoice.md](ghl/invoices/update-invoice.md) |
| POST | `/invoices/:invoiceId/void` | Void invoice | invoices.write | [void-invoice.md](ghl/invoices/void-invoice.md) |
| POST | `/knowledge-bases` | Create a new knowledge base (max 15 knowledge bases per location) |  | [create-knowledge-base.md](ghl/knowledge-base/create-knowledge-base.md) |
| POST | `/knowledge-bases/faqs` | Create a new FAQ inside knowledge base |  | [create.md](ghl/knowledge-base/create.md) |
| DELETE | `/knowledge-bases/:knowledgeBaseId` | Delete a knowledge base |  | [delete-knowledge-base.md](ghl/knowledge-base/delete-knowledge-base.md) |
| DELETE | `/knowledge-bases/crawler` | Delete trained pages |  | [delete-trained-urls-for-knowledge-base.md](ghl/knowledge-base/delete-trained-urls-for-knowledge-base.md) |
| DELETE | `/knowledge-bases/faqs/:id` | Delete an existing knowledge base FAQ |  | [delete.md](ghl/knowledge-base/delete.md) |
| POST | `/knowledge-bases/crawler` | Start crawling and discover pages for training |  | [discover-website.md](ghl/knowledge-base/discover-website.md) |
| GET | `/knowledge-bases/crawler` | Get all trained page links by knowledge base |  | [get-all-website-urls-data-by-knowledge-base.md](ghl/knowledge-base/get-all-website-urls-data-by-knowledge-base.md) |
| GET | `/knowledge-bases/crawler/status` | Get crawling status for the latest operation |  | [get-crawling-status-for-latest-operation.md](ghl/knowledge-base/get-crawling-status-for-latest-operation.md) |
| GET | `/knowledge-bases/:knowledgeBaseId` | Get knowledge base by ID |  | [get-knowledge-base-by-id.md](ghl/knowledge-base/get-knowledge-base-by-id.md) |
| GET | `/knowledge-bases` | Get all knowledge bases for a location by location Id (paginated) |  | [list-all-knowledge-bases-paginated.md](ghl/knowledge-base/list-all-knowledge-bases-paginated.md) |
| GET | `/knowledge-bases/faqs` | Get all FAQs by knowledge base with pagination support |  | [list.md](ghl/knowledge-base/list.md) |
| POST | `/knowledge-bases/crawler/train` | Train discovered website pages and ingest into the knowledge base |  | [train-discovered-urls.md](ghl/knowledge-base/train-discovered-urls.md) |
| PUT | `/knowledge-bases/:id` | Update a knowledge base |  | [update-knowledge-base.md](ghl/knowledge-base/update-knowledge-base.md) |
| PUT | `/knowledge-bases/faqs/:id` | Update an existing knowledge base FAQ |  | [update.md](ghl/knowledge-base/update.md) |
| POST | `/links` | Create Link | links.write | [create-link.md](ghl/links/create-link.md) |
| DELETE | `/links/:linkId` | Delete Link | links.write | [delete-link.md](ghl/links/delete-link.md) |
| GET | `/links/id/:linkId` | Get Link by ID | links.readonly | [get-link-by-id.md](ghl/links/get-link-by-id.md) |
| GET | `/links` | Get Links | links.readonly | [get-links.md](ghl/links/get-links.md) |
| GET | `/links/search` | Search Trigger Links | links.readonly | [search-trigger-links.md](ghl/links/search-trigger-links.md) |
| PUT | `/links/:linkId` | Update Link | links.write | [update-link.md](ghl/links/update-link.md) |
| POST | `/locations/:locationId/customFields` | Create Custom Field | locations/customFields.write | [create-custom-field.md](ghl/locations/create-custom-field.md) |
| POST | `/locations/:locationId/customValues` | Create Custom Value | locations/customValues.write | [create-custom-value.md](ghl/locations/create-custom-value.md) |
| POST | `/locations` | Create Sub-Account (Formerly Location) | locations.write | [create-location.md](ghl/locations/create-location.md) |
| POST | `/locations/:locationId/recurring-tasks` | Create Recurring Task |  | [create-recurring-task.md](ghl/locations/create-recurring-task.md) |
| POST | `/locations/:locationId/tags` | Create Tag | locations/tags.write | [create-tag.md](ghl/locations/create-tag.md) |
| DELETE | `/locations/:locationId/templates/:id` | DELETE an email/sms template |  | [delete-an-email-sms-template.md](ghl/locations/delete-an-email-sms-template.md) |
| DELETE | `/locations/:locationId/customFields/:id` | Delete Custom Field |  | [delete-custom-field.md](ghl/locations/delete-custom-field.md) |
| DELETE | `/locations/:locationId/customValues/:id` | Delete Custom Value |  | [delete-custom-value.md](ghl/locations/delete-custom-value.md) |
| DELETE | `/locations/:locationId` | Delete Sub-Account (Formerly Location) | locations.internal-access-only | [delete-location.md](ghl/locations/delete-location.md) |
| DELETE | `/locations/:locationId/recurring-tasks/:id` | Delete Recurring Task |  | [delete-recurring-task.md](ghl/locations/delete-recurring-task.md) |
| DELETE | `/locations/:locationId/tags/:tagId` | Delete tag |  | [delete-tag.md](ghl/locations/delete-tag.md) |
| GET | `/locations/:locationId/templates` | GET all or email/sms templates | locations/templates.readonly | [get-all-or-email-sms-templates.md](ghl/locations/get-all-or-email-sms-templates.md) |
| GET | `/locations/:locationId/conversationChannels/:type` | Get Conversation Channel | locations.readonly | [get-conversation-channel.md](ghl/locations/get-conversation-channel.md) |
| GET | `/locations/:locationId/customFields/:id` | Get Custom Field |  | [get-custom-field.md](ghl/locations/get-custom-field.md) |
| GET | `/locations/:locationId/customFields` | Get Custom Fields | locations/customFields.readonly | [get-custom-fields.md](ghl/locations/get-custom-fields.md) |
| GET | `/locations/:locationId/customValues/:id` | Get Custom Value |  | [get-custom-value.md](ghl/locations/get-custom-value.md) |
| GET | `/locations/:locationId/customValues` | Get Custom Values | locations/customValues.readonly | [get-custom-values.md](ghl/locations/get-custom-values.md) |
| GET | `/locations/:locationId/permissions` | Get Permissions | locations/write | [get-location-permissions.md](ghl/locations/get-location-permissions.md) |
| GET | `/locations/:locationId/tags` | Get Tags | locations/tags.readonly | [get-location-tags.md](ghl/locations/get-location-tags.md) |
| GET | `/locations/:locationId` | Get Sub-Account (Formerly Location) | locations.readonly | [get-location.md](ghl/locations/get-location.md) |
| GET | `/locations/:locationId/recurring-tasks/:id` | Get Recurring Task By Id |  | [get-recurring-task-by-id.md](ghl/locations/get-recurring-task-by-id.md) |
| GET | `/locations/:locationId/tags/:tagId` | Get tag by id |  | [get-tag-by-id.md](ghl/locations/get-tag-by-id.md) |
| GET | `/locations/:locationId/timezones` | Fetch Timezones | locations.readonly | [get-timezones.md](ghl/locations/get-timezones.md) |
| PUT | `/locations/:locationId` | Put Sub-Account (Formerly Location) | locations.write | [put-location.md](ghl/locations/put-location.md) |
| GET | `/locations/search` | Search | locations.readonly | [search-locations.md](ghl/locations/search-locations.md) |
| POST | `/locations/:locationId/tasks/search` | Task Search Filter | locations/tasks.readonly | [task-search.md](ghl/locations/task-search.md) |
| PUT | `/locations/:locationId/customFields/:id` | Update Custom Field |  | [update-custom-field.md](ghl/locations/update-custom-field.md) |
| PUT | `/locations/:locationId/customValues/:id` | Update Custom Value |  | [update-custom-value.md](ghl/locations/update-custom-value.md) |
| PUT | `/locations/:locationId/permissions` | Update Permissions | locations/write | [update-location-permissions.md](ghl/locations/update-location-permissions.md) |
| PUT | `/locations/:locationId/recurring-tasks/:id` | Update Recurring Task |  | [update-recurring-task.md](ghl/locations/update-recurring-task.md) |
| PUT | `/locations/:locationId/tags/:tagId` | Update tag |  | [update-tag.md](ghl/locations/update-tag.md) |
| POST | `/locations/:locationId/customFields/upload` | Uploads File to customFields | locations/customFields.write | [upload-file-custom-fields.md](ghl/locations/upload-file-custom-fields.md) |
| POST | `/marketplace/billing/charges` | Create a new wallet charge | charges.write | [charge.md](ghl/marketplace/charge.md) |
| DELETE | `/marketplace/billing/charges/:chargeId` | Delete a wallet charge | charges.write | [delete-charge.md](ghl/marketplace/delete-charge.md) |
| GET | `/marketplace/billing/charges` | Get all wallet charges | charges.readonly | [get-charges.md](ghl/marketplace/get-charges.md) |
| GET | `/marketplace/app/:appId/installations` | Get Installer Details | marketplace-installer-details.readonly | [get-installer-details.md](ghl/marketplace/get-installer-details.md) |
| GET | `/marketplace/app/:appId/rebilling-config/location/:locationId` | Get rebilling config for an app subscription and usage plans | oauth.readonly | [get-rebilling-config-for-app.md](ghl/marketplace/get-rebilling-config-for-app.md) |
| GET | `/marketplace/billing/charges/:chargeId` | Get specific wallet charge details | charges.readonly | [get-specific-charge.md](ghl/marketplace/get-specific-charge.md) |
| GET | `/marketplace/billing/charges/has-funds` | Check if account has sufficient funds | charges.readonly | [has-funds.md](ghl/marketplace/has-funds.md) |
| POST | `/marketplace/external-auth/migration` | Migrate external authentication connection | marketplace-external-auth-migration.write | [migrate-connection.md](ghl/marketplace/migrate-connection.md) |
| DELETE | `/marketplace/app/:appId/installations` | Uninstall an application | oauth.write | [uninstall-application.md](ghl/marketplace/uninstall-application.md) |
| PUT | `/medias/delete-files` | Bulk Delete / Trash Files or Folders |  | [bulk-delete-media-objects.md](ghl/medias/bulk-delete-media-objects.md) |
| PUT | `/medias/update-files` | Bulk Update Files/ Folders |  | [bulk-update-media-objects.md](ghl/medias/bulk-update-media-objects.md) |
| POST | `/medias/folder` | Create Folder |  | [create-media-folder.md](ghl/medias/create-media-folder.md) |
| DELETE | `/medias/:id` | Delete File or Folder | medias.write | [delete-media-content.md](ghl/medias/delete-media-content.md) |
| GET | `/medias/files` | Get List of Files/ Folders | medias.readonly | [fetch-media-content.md](ghl/medias/fetch-media-content.md) |
| POST | `/medias/:id` | Update File/ Folder |  | [update-media-object.md](ghl/medias/update-media-object.md) |
| POST | `/medias/upload-file` | Upload File into Media Storage | medias.write | [upload-media-content.md](ghl/medias/upload-media-content.md) |
| POST | `/oauth/token` | Get Access Token |  | [get-access-token.md](ghl/oauth/get-access-token.md) |
| GET | `/oauth/installed-locations` | Get Location where app is installed | oauth.readonly | [get-installed-location.md](ghl/oauth/get-installed-location.md) |
| POST | `/oauth/location-token` | Get Location Access Token from Agency Token | oauth.write | [get-location-access-token.md](ghl/oauth/get-location-access-token.md) |
| POST | `/objects` | Create Custom Object | objects/schema.write | [create-custom-object-schema.md](ghl/objects/create-custom-object-schema.md) |
| POST | `/objects/:schemaKey/records` | Create Record | objects/record.write | [create-object-record.md](ghl/objects/create-object-record.md) |
| DELETE | `/objects/:schemaKey/records/:id` | Delete Record |  | [delete-object-record.md](ghl/objects/delete-object-record.md) |
| GET | `/objects` | Get all objects for a location | objects/schema.readonly | [get-object-by-location-id.md](ghl/objects/get-object-by-location-id.md) |
| GET | `/objects/:key` | Get Object Schema by key / id | objects/schema.readonly | [get-object-schema-by-key.md](ghl/objects/get-object-schema-by-key.md) |
| GET | `/objects/:schemaKey/records/:id` | Get Record By Id |  | [get-record-by-id.md](ghl/objects/get-record-by-id.md) |
| POST | `/objects/:schemaKey/records/search` | Search Object Records | objects/record.readonly | [search-object-records.md](ghl/objects/search-object-records.md) |
| PUT | `/objects/:key` | Update Object Schema By Key / Id | objects/schema.write | [update-custom-object.md](ghl/objects/update-custom-object.md) |
| PUT | `/objects/:schemaKey/records/:id` | Update Record |  | [update-object-record.md](ghl/objects/update-object-record.md) |
| POST | `/opportunities/:id/followers` | Add Followers | opportunities.write | [add-followers-opportunity.md](ghl/opportunities/add-followers-opportunity.md) |
| POST | `/opportunities` | Create Opportunity | opportunities.write | [create-opportunity.md](ghl/opportunities/create-opportunity.md) |
| DELETE | `/opportunities/:id` | Delete Opportunity | opportunities.write | [delete-opportunity.md](ghl/opportunities/delete-opportunity.md) |
| GET | `/opportunities/lost-reason` | Get lost reason | opportunities.readonly | [get-lost-reason.md](ghl/opportunities/get-lost-reason.md) |
| GET | `/opportunities/:id` | Get Opportunity | opportunities.readonly | [get-opportunity.md](ghl/opportunities/get-opportunity.md) |
| GET | `/opportunities/pipelines` | Get Pipelines | opportunities.readonly | [get-pipelines.md](ghl/opportunities/get-pipelines.md) |
| DELETE | `/opportunities/:id/followers` | Remove Followers | opportunities.write | [remove-followers-opportunity.md](ghl/opportunities/remove-followers-opportunity.md) |
| POST | `/opportunities/search` | Search Opportunities | opportunities.readonly | [search-opportunities-advanced.md](ghl/opportunities/search-opportunities-advanced.md) |
| GET | `/opportunities/search` | Search Opportunity | opportunities.readonly | [search-opportunity.md](ghl/opportunities/search-opportunity.md) |
| PUT | `/opportunities/:id/status` | Update Opportunity Status | opportunities.write | [update-opportunity-status.md](ghl/opportunities/update-opportunity-status.md) |
| PUT | `/opportunities/:id` | Update Opportunity | opportunities.write | [update-opportunity.md](ghl/opportunities/update-opportunity.md) |
| POST | `/opportunities/upsert` | Upsert Opportunity | opportunities.write | [upsert-opportunity.md](ghl/opportunities/upsert-opportunity.md) |
| POST | `/payments/custom-provider/connect` | Create new provider config | payments/custom-provider.write | [create-config.md](ghl/payments/create-config.md) |
| POST | `/payments/coupon` | Create Coupon | payments/coupons.write | [create-coupon.md](ghl/payments/create-coupon.md) |
| POST | `/payments/integrations/provider/whitelabel` | Create White-label Integration Provider | payments/integration.write | [create-integration-provider.md](ghl/payments/create-integration-provider.md) |
| POST | `/payments/custom-provider/provider` | Create new integration | payments/custom-provider.write | [create-integration.md](ghl/payments/create-integration.md) |
| POST | `/payments/orders/:orderId/fulfillments` | Create order fulfillment | payments/orders.write | [create-order-fulfillment.md](ghl/payments/create-order-fulfillment.md) |
| PUT | `/payments/custom-provider/capabilities` | Custom-provider marketplace app update capabilities | payments/custom-provider.write | [custom-provider-marketplace-app-update-capabilities.md](ghl/payments/custom-provider-marketplace-app-update-capabilities.md) |
| DELETE | `/payments/coupon` | Delete Coupon | payments/coupons.write | [delete-coupon.md](ghl/payments/delete-coupon.md) |
| DELETE | `/payments/custom-provider/provider` | Deleting an existing integration | payments/custom-provider.write | [delete-integration.md](ghl/payments/delete-integration.md) |
| POST | `/payments/custom-provider/disconnect` | Disconnect existing provider config | payments/custom-provider.write | [disconnect-config.md](ghl/payments/disconnect-config.md) |
| GET | `/payments/custom-provider/connect` | Fetch given provider config | payments/custom-provider.readonly | [fetch-config.md](ghl/payments/fetch-config.md) |
| GET | `/payments/coupon` | Fetch Coupon | payments/coupons.readonly | [get-coupon.md](ghl/payments/get-coupon.md) |
| GET | `/payments/orders/:orderId` | Get Order by ID | payments/orders.readonly | [get-order-by-id.md](ghl/payments/get-order-by-id.md) |
| GET | `/payments/subscriptions/:subscriptionId` | Get Subscription by ID | payments/subscriptions.readonly | [get-subscription-by-id.md](ghl/payments/get-subscription-by-id.md) |
| GET | `/payments/transactions/:transactionId` | Get Transaction by ID | payments/transactions.readonly | [get-transaction-by-id.md](ghl/payments/get-transaction-by-id.md) |
| GET | `/payments/coupon/list` | List Coupons | payments/coupons.readonly | [list-coupons.md](ghl/payments/list-coupons.md) |
| GET | `/payments/integrations/provider/whitelabel` | List White-label Integration Providers | payments/integration.readonly | [list-integration-providers.md](ghl/payments/list-integration-providers.md) |
| GET | `/payments/orders/:orderId/fulfillments` | List fulfillment | payments/orders.readonly | [list-order-fulfillment.md](ghl/payments/list-order-fulfillment.md) |
| GET | `/payments/orders/:orderId/notes` | List Order Notes |  | [list-order-notes.md](ghl/payments/list-order-notes.md) |
| GET | `/payments/orders` | List Orders | payments/orders.readonly | [list-orders.md](ghl/payments/list-orders.md) |
| GET | `/payments/subscriptions` | List Subscriptions | payments/subscriptions.readonly | [list-subscriptions.md](ghl/payments/list-subscriptions.md) |
| GET | `/payments/transactions` | List Transactions | payments/transactions.readonly | [list-transactions.md](ghl/payments/list-transactions.md) |
| POST | `/payments/orders/:orderId/record-payment` | Record Order Payment | payments/orders.collectPayment | [record-order-payment.md](ghl/payments/record-order-payment.md) |
| PUT | `/payments/coupon` | Update Coupon | payments/coupons.write | [update-coupon.md](ghl/payments/update-coupon.md) |
| GET | `/phone-system/numbers/location/:locationId` | List active numbers | phonenumbers.read | [active-numbers.md](ghl/phone-system/active-numbers.md) |
| GET | `/phone-system/number-pools` | List number pools | numberpools.read | [get-number-pool-list.md](ghl/phone-system/get-number-pool-list.md) |
| GET | `/phone-system/numbers/location/:locationId/available` | List available phone numbers | phonenumbers.read | [list-available-numbers-for-a-country.md](ghl/phone-system/list-available-numbers-for-a-country.md) |
| POST | `/phone-system/numbers/location/:locationId/purchase` | Purchase number for location | phonenumbers.write | [purchase-number-for-location.md](ghl/phone-system/purchase-number-for-location.md) |
| POST | `/products/bulk-update/edit` | Bulk Edit Products and Prices |  | [bulk-edit.md](ghl/products/bulk-edit.md) |
| POST | `/products/reviews/bulk-update` | Update Product Reviews | products.write | [bulk-update-product-review.md](ghl/products/bulk-update-product-review.md) |
| POST | `/products/bulk-update` | Bulk Update Products | products.write | [bulk-update.md](ghl/products/bulk-update.md) |
| POST | `/products/:productId/price` | Create Price for a Product | products/prices.write | [create-price-for-product.md](ghl/products/create-price-for-product.md) |
| POST | `/products/collections` | Create Product Collection | products/collection.write | [create-product-collection.md](ghl/products/create-product-collection.md) |
| POST | `/products` | Create Product | products.write | [create-product.md](ghl/products/create-product.md) |
| DELETE | `/products/:productId/price/:priceId` | Delete Price by ID for a Product | products/prices.write | [delete-price-by-id-for-product.md](ghl/products/delete-price-by-id-for-product.md) |
| DELETE | `/products/:productId` | Delete Product by ID | products.write | [delete-product-by-id.md](ghl/products/delete-product-by-id.md) |
| DELETE | `/products/collections/:collectionId` | Delete Product Collection | products/collection.write | [delete-product-collection.md](ghl/products/delete-product-collection.md) |
| DELETE | `/products/reviews/:reviewId` | Delete Product Review | products.write | [delete-product-review.md](ghl/products/delete-product-review.md) |
| GET | `/products/inventory` | List Inventory | products/prices.readonly | [get-list-inventory.md](ghl/products/get-list-inventory.md) |
| GET | `/products/:productId/price/:priceId` | Get Price by ID for a Product | products/prices.readonly | [get-price-by-id-for-product.md](ghl/products/get-price-by-id-for-product.md) |
| GET | `/products/:productId` | Get Product by ID | products.readonly | [get-product-by-id.md](ghl/products/get-product-by-id.md) |
| GET | `/products/collections/:collectionId` | Get Details about individual product collection | products/collection.readonly | [get-product-collection-id.md](ghl/products/get-product-collection-id.md) |
| GET | `/products/collections` | Fetch Product Collections | products/collection.readonly | [get-product-collection.md](ghl/products/get-product-collection.md) |
| GET | `/products/reviews` | Fetch Product Reviews | products.readonly | [get-product-reviews.md](ghl/products/get-product-reviews.md) |
| GET | `/products/store/:storeId/stats` | Fetch Product Store Stats | products.readonly | [get-product-store-stats.md](ghl/products/get-product-store-stats.md) |
| GET | `/products/reviews/count` | Fetch Review Count as per status | products.readonly | [get-reviews-count.md](ghl/products/get-reviews-count.md) |
| GET | `/products` | List Products | products.readonly | [list-invoices.md](ghl/products/list-invoices.md) |
| GET | `/products/:productId/price` | List Prices for a Product | products/prices.readonly | [list-prices-for-product.md](ghl/products/list-prices-for-product.md) |
| POST | `/products/store/:storeId/priority` | Update product display priorities in store |  | [update-display-priority.md](ghl/products/update-display-priority.md) |
| POST | `/products/inventory` | Update Inventory | products/prices.write | [update-inventory.md](ghl/products/update-inventory.md) |
| PUT | `/products/:productId/price/:priceId` | Update Price by ID for a Product | products/prices.write | [update-price-by-id-for-product.md](ghl/products/update-price-by-id-for-product.md) |
| PUT | `/products/:productId` | Update Product by ID | products.write | [update-product-by-id.md](ghl/products/update-product-by-id.md) |
| PUT | `/products/collections/:collectionId` | Update Product Collection | products/collection.write | [update-product-collection.md](ghl/products/update-product-collection.md) |
| PUT | `/products/reviews/:reviewId` | Update Product Reviews | products.write | [update-product-review.md](ghl/products/update-product-review.md) |
| POST | `/products/store/:storeId` | Action to include/exclude the product in store | products.write | [update-store-status.md](ghl/products/update-store-status.md) |
| GET | `/proposals/templates` | List templates |  | [list-documents-contracts-templates.md](ghl/proposals/list-documents-contracts-templates.md) |
| GET | `/proposals/document` | List documents |  | [list-documents-contracts.md](ghl/proposals/list-documents-contracts.md) |
| POST | `/proposals/templates/send` | Send template |  | [send-documents-contracts-template.md](ghl/proposals/send-documents-contracts-template.md) |
| POST | `/proposals/document/send` | Send document |  | [send-documents-contracts.md](ghl/proposals/send-documents-contracts.md) |
| POST | `/saas/allow-attach-rebilling/:locationId` | Allow Attach Rebilling | saas/company.read | [allow-attach-rebilling.md](ghl/saas/allow-attach-rebilling.md) |
| POST | `/saas-api/public-api/bulk-disable-saas/:companyId` | Disable SaaS for locations |  | [bulk-disable-saas-deprecated.md](ghl/saas/bulk-disable-saas-deprecated.md) |
| POST | `/saas/bulk-disable-saas/:companyId` | Disable SaaS for locations |  | [bulk-disable-saas.md](ghl/saas/bulk-disable-saas.md) |
| POST | `/saas-api/public-api/bulk-enable-saas/:companyId` | Bulk Enable SaaS |  | [bulk-enable-saas-deprecated.md](ghl/saas/bulk-enable-saas-deprecated.md) |
| POST | `/saas/bulk-enable-saas/:companyId` | Bulk Enable SaaS |  | [bulk-enable-saas.md](ghl/saas/bulk-enable-saas.md) |
| POST | `/saas-api/public-api/enable-saas/:locationId` | Enable SaaS for Sub-Account (Formerly Location) |  | [enable-saas-location-deprecated.md](ghl/saas/enable-saas-location-deprecated.md) |
| POST | `/saas/enable-saas/:locationId` | Enable SaaS for Sub-Account (Formerly Location) |  | [enable-saas-location.md](ghl/saas/enable-saas-location.md) |
| PUT | `/saas-api/public-api/update-saas-subscription/:locationId` | Update SaaS subscription |  | [generate-payment-link-deprecated.md](ghl/saas/generate-payment-link-deprecated.md) |
| PUT | `/saas/update-saas-subscription/:locationId` | Update SaaS subscription |  | [generate-payment-link.md](ghl/saas/generate-payment-link.md) |
| GET | `/saas-api/public-api/agency-plans/:companyId` | Get Agency Plans |  | [get-agency-plans-deprecated.md](ghl/saas/get-agency-plans-deprecated.md) |
| GET | `/saas/agency-plans/:companyId` | Get Agency Plans |  | [get-agency-plans.md](ghl/saas/get-agency-plans.md) |
| GET | `/saas-api/public-api/get-saas-subscription/:locationId` | Get Location Subscription Details |  | [get-location-subscription-deprecated.md](ghl/saas/get-location-subscription-deprecated.md) |
| GET | `/saas/get-saas-subscription/:locationId` | Get Location Subscription Details |  | [get-location-subscription.md](ghl/saas/get-location-subscription.md) |
| GET | `/saas-api/public-api/companies/:companyId/locations/:locationId/wallet-balance` | Get Location Wallet Balance | saas/company.read | [get-location-wallet-balance.md](ghl/saas/get-location-wallet-balance.md) |
| GET | `/saas-api/public-api/saas-locations/:companyId` | Get SaaS Locations |  | [get-saas-locations-deprecated.md](ghl/saas/get-saas-locations-deprecated.md) |
| GET | `/saas/saas-locations/:companyId` | Get SaaS Locations |  | [get-saas-locations.md](ghl/saas/get-saas-locations.md) |
| GET | `/saas-api/public-api/saas-plan/:planId` | Get SaaS Plan |  | [get-saas-plan-deprecated.md](ghl/saas/get-saas-plan-deprecated.md) |
| GET | `/saas/saas-plan/:planId` | Get SaaS Plan |  | [get-saas-plan.md](ghl/saas/get-saas-plan.md) |
| GET | `/saas-api/public-api/locations` | Get locations by stripeId with companyId |  | [locations-deprecated.md](ghl/saas/locations-deprecated.md) |
| GET | `/saas/locations` | Get locations by stripeId with companyId |  | [locations.md](ghl/saas/locations.md) |
| POST | `/saas-api/public-api/pause/:locationId` | Pause location |  | [pause-location-deprecated.md](ghl/saas/pause-location-deprecated.md) |
| POST | `/saas/pause/:locationId` | Pause location |  | [pause-location.md](ghl/saas/pause-location.md) |
| POST | `/saas-api/public-api/companies/:companyId/locations/:locationId/wallet-balance/complimentary-credits` | Update Location Wallet Balance | saas/company.write | [update-location-wallet-balance.md](ghl/saas/update-location-wallet-balance.md) |
| POST | `/saas-api/public-api/update-rebilling/:companyId` | Update Rebilling |  | [update-rebilling-deprecated.md](ghl/saas/update-rebilling-deprecated.md) |
| POST | `/saas/update-rebilling/:companyId` | Update Rebilling |  | [update-rebilling.md](ghl/saas/update-rebilling.md) |
| POST | `/snapshots/share/link` | Create Snapshot Share Link |  | [create-snapshot-share-link.md](ghl/snapshots/create-snapshot-share-link.md) |
| GET | `/snapshots` | Get Snapshots |  | [get-custom-snapshots.md](ghl/snapshots/get-custom-snapshots.md) |
| GET | `/snapshots/snapshot-status/:snapshotId/location/:locationId` | Get Last Snapshot Push |  | [get-latest-snapshot-push.md](ghl/snapshots/get-latest-snapshot-push.md) |
| GET | `/snapshots/snapshot-status/:snapshotId` | Get Snapshot Push between Dates |  | [get-snapshot-push.md](ghl/snapshots/get-snapshot-push.md) |
| POST | `/social-media-posting/oauth/:locationId/:platform/accounts/:accountId` | Connect Account (Step 3 of 3) |  | [attach-oauth-accounts.md](ghl/social-planner/attach-oauth-accounts.md) |
| POST | `/social-media-posting/:locationId/posts/bulk-delete` | Bulk Delete Social Planner Posts |  | [bulk-delete-social-planner-posts.md](ghl/social-planner/bulk-delete-social-planner-posts.md) |
| POST | `/social-media-posting/category/queues/:queueId/items/:itemId/clone` | Clone a queue item | socialplanner/category.write | [clone-queue-item.md](ghl/social-planner/clone-queue-item.md) |
| POST | `/social-media-posting/comments/:platform` | Create a comment or reply |  | [create-comment.md](ghl/social-planner/create-comment.md) |
| POST | `/social-media-posting/comments/:platform/:id/like` | Like a comment |  | [create-like.md](ghl/social-planner/create-like.md) |
| POST | `/social-media-posting/:locationId/posts` | Create post | socialplanner/post.write | [create-post.md](ghl/social-planner/create-post.md) |
| POST | `/social-media-posting/category/queues/:queueId/create/item` | Create a new item in the queue |  | [create-queue-item.md](ghl/social-planner/create-queue-item.md) |
| POST | `/social-media-posting/category/queues` | Create a new category queue | socialplanner/category.write | [create-queue.md](ghl/social-planner/create-queue.md) |
| DELETE | `/social-media-posting/:locationId/accounts/:id` | Delete Account |  | [delete-account.md](ghl/social-planner/delete-account.md) |
| DELETE | `/social-media-posting/:locationId/csv/:csvId/post/:postId` | Delete CSV Post |  | [delete-csv-post.md](ghl/social-planner/delete-csv-post.md) |
| DELETE | `/social-media-posting/:locationId/csv/:id` | Delete CSV |  | [delete-csv.md](ghl/social-planner/delete-csv.md) |
| DELETE | `/social-media-posting/category/queues/:postId/active-post` | Delete an active post and schedule the next one | socialplanner/category.write | [delete-current-active-post-and-schedule-next.md](ghl/social-planner/delete-current-active-post-and-schedule-next.md) |
| DELETE | `/social-media-posting/comments/:platform/:id/like` | Unlike a comment |  | [delete-like.md](ghl/social-planner/delete-like.md) |
| DELETE | `/social-media-posting/:locationId/posts/:id` | Delete Post |  | [delete-post.md](ghl/social-planner/delete-post.md) |
| DELETE | `/social-media-posting/category/queues/:queueId/items/:itemId` | Delete an item from a queue | socialplanner/category.write | [delete-queue-item.md](ghl/social-planner/delete-queue-item.md) |
| POST | `/social-media-posting/category/queues/:queueId/edit/discard` | Discard edit session changes | socialplanner/category.write | [discard-edit-session.md](ghl/social-planner/discard-edit-session.md) |
| PUT | `/social-media-posting/:locationId/posts/:id` | Edit post |  | [edit-post.md](ghl/social-planner/edit-post.md) |
| GET | `/social-media-posting/category/queues/available-categories` | Get all categories with their queue status | socialplanner/category.readonly | [fetch-available-categories.md](ghl/social-planner/fetch-available-categories.md) |
| POST | `/social-media-posting/category/queues/list/calendar` | Get scheduled posts calendar view |  | [fetch-calendar-list.md](ghl/social-planner/fetch-calendar-list.md) |
| POST | `/social-media-posting/category/queues/:queueId/edit/calendar` | Fetch calendar view for an edit session |  | [fetch-edit-session-calendar.md](ghl/social-planner/fetch-edit-session-calendar.md) |
| GET | `/social-media-posting/category/queues/:queueId` | Fetch a category queue by ID | socialplanner/category.readonly | [fetch-queue-by-id.md](ghl/social-planner/fetch-queue-by-id.md) |
| POST | `/social-media-posting/category/queues/:queueId/items` | Fetch items from a queue | socialplanner/category.readonly | [fetch-queue-items.md](ghl/social-planner/fetch-queue-items.md) |
| POST | `/social-media-posting/category/queues/list` | Fetch category queues for a location | socialplanner/category.readonly | [fetch-queues.md](ghl/social-planner/fetch-queues.md) |
| POST | `/social-media-posting/category/queues/:queueId/slots` | Fetch slot information for queue items | socialplanner/category.readonly | [fetch-slots.md](ghl/social-planner/fetch-slots.md) |
| GET | `/social-media-posting/:locationId/accounts` | Get Accounts | socialplanner/account.readonly | [get-account.md](ghl/social-planner/get-account.md) |
| GET | `/social-media-posting/:locationId/categories/:id` | Get categories by id |  | [get-categories-id.md](ghl/social-planner/get-categories-id.md) |
| GET | `/social-media-posting/:locationId/categories` | Get categories by location id | socialplanner/category.readonly | [get-categories-location-id.md](ghl/social-planner/get-categories-location-id.md) |
| POST | `/social-media-posting/comments/:platform/list` | List comments for a post or thread |  | [get-comment-list.md](ghl/social-planner/get-comment-list.md) |
| GET | `/social-media-posting/:locationId/csv/:id` | Get CSV Post |  | [get-csv-post.md](ghl/social-planner/get-csv-post.md) |
| GET | `/social-media-posting/oauth/:locationId/:platform/accounts/:accountId` | Get Available Accounts (Step 2 of 3) |  | [get-oauth-accounts.md](ghl/social-planner/get-oauth-accounts.md) |
| GET | `/social-media-posting/:locationId/posts/:id` | Get post |  | [get-post.md](ghl/social-planner/get-post.md) |
| POST | `/social-media-posting/:locationId/posts/list` | Get posts |  | [get-posts.md](ghl/social-planner/get-posts.md) |
| POST | `/social-media-posting/statistics` | Get Social Media Statistics | socialplanner/statistics.readonly | [get-statistics.md](ghl/social-planner/get-statistics.md) |
| POST | `/social-media-posting/:locationId/tags/details` | Get tags by ids |  | [get-tags-by-ids.md](ghl/social-planner/get-tags-by-ids.md) |
| GET | `/social-media-posting/:locationId/tags` | Get tags by location id |  | [get-tags-location-id.md](ghl/social-planner/get-tags-location-id.md) |
| GET | `/social-media-posting/:locationId/csv` | Get Upload Status |  | [get-upload-status.md](ghl/social-planner/get-upload-status.md) |
| PUT | `/social-media-posting/category/queues/:queueId/items/:itemId/reset` | Reset an item in a queue |  | [reset-queue-item.md](ghl/social-planner/reset-queue-item.md) |
| POST | `/social-media-posting/category/queues/:queueId/edit/save` | Save edit session changes | socialplanner/category.write | [save-edit-session.md](ghl/social-planner/save-edit-session.md) |
| POST | `/social-media-posting/:locationId/set-accounts` | Set Accounts | socialplanner/csv.write | [set-accounts.md](ghl/social-planner/set-accounts.md) |
| PATCH | `/social-media-posting/:locationId/csv/:id` | Start CSV Finalize |  | [start-csv-finalize.md](ghl/social-planner/start-csv-finalize.md) |
| POST | `/social-media-posting/category/queues/:queueId/edit/start` | Start or resume an edit session | socialplanner/category.write | [start-edit-session.md](ghl/social-planner/start-edit-session.md) |
| GET | `/social-media-posting/oauth/:platform/start` | Start OAuth Flow (Step 1 of 3) |  | [start-oauth.md](ghl/social-planner/start-oauth.md) |
| PUT | `/social-media-posting/category/queues/:queueId/items/:itemId` | Update an item in a queue |  | [update-queue-item.md](ghl/social-planner/update-queue-item.md) |
| PUT | `/social-media-posting/category/queues/:queueId` | Update queue settings or status | socialplanner/category.write | [update-queue.md](ghl/social-planner/update-queue.md) |
| POST | `/social-media-posting/:locationId/csv` | Upload CSV | socialplanner/csv.write | [upload-csv.md](ghl/social-planner/upload-csv.md) |
| POST | `/store/shipping-carrier` | Create Shipping Carrier |  | [create-shipping-carrier.md](ghl/store/create-shipping-carrier.md) |
| POST | `/store/shipping-zone/:shippingZoneId/shipping-rate` | Create Shipping Rate |  | [create-shipping-rate.md](ghl/store/create-shipping-rate.md) |
| POST | `/store/shipping-zone` | Create Shipping Zone |  | [create-shipping-zone.md](ghl/store/create-shipping-zone.md) |
| POST | `/store/store-setting` | Create/Update Store Settings |  | [create-store-setting.md](ghl/store/create-store-setting.md) |
| DELETE | `/store/shipping-carrier/:shippingCarrierId` | Delete shipping carrier |  | [delete-shipping-carrier.md](ghl/store/delete-shipping-carrier.md) |
| DELETE | `/store/shipping-zone/:shippingZoneId/shipping-rate/:shippingRateId` | Delete shipping rate |  | [delete-shipping-rate.md](ghl/store/delete-shipping-rate.md) |
| DELETE | `/store/shipping-zone/:shippingZoneId` | Delete shipping zone |  | [delete-shipping-zone.md](ghl/store/delete-shipping-zone.md) |
| POST | `/store/shipping-zone/shipping-rates` | Get available shipping rates |  | [get-available-shipping-zones.md](ghl/store/get-available-shipping-zones.md) |
| GET | `/store/shipping-carrier/:shippingCarrierId` | Get Shipping Carrier |  | [get-shipping-carriers.md](ghl/store/get-shipping-carriers.md) |
| GET | `/store/shipping-zone/:shippingZoneId/shipping-rate/:shippingRateId` | Get Shipping Rate |  | [get-shipping-rates.md](ghl/store/get-shipping-rates.md) |
| GET | `/store/shipping-zone/:shippingZoneId` | Get Shipping Zone |  | [get-shipping-zones.md](ghl/store/get-shipping-zones.md) |
| GET | `/store/store-setting` | Get Store Settings |  | [get-store-settings.md](ghl/store/get-store-settings.md) |
| GET | `/store/shipping-carrier` | List Shipping Carriers |  | [list-shipping-carriers.md](ghl/store/list-shipping-carriers.md) |
| GET | `/store/shipping-zone/:shippingZoneId/shipping-rate` | List Shipping Rates |  | [list-shipping-rates.md](ghl/store/list-shipping-rates.md) |
| GET | `/store/shipping-zone` | List Shipping Zones |  | [list-shipping-zones.md](ghl/store/list-shipping-zones.md) |
| PUT | `/store/shipping-carrier/:shippingCarrierId` | Update Shipping Carrier |  | [update-shipping-carrier.md](ghl/store/update-shipping-carrier.md) |
| PUT | `/store/shipping-zone/:shippingZoneId/shipping-rate/:shippingRateId` | Update Shipping Rate |  | [update-shipping-rate.md](ghl/store/update-shipping-rate.md) |
| PUT | `/store/shipping-zone/:shippingZoneId` | Update Shipping Zone |  | [update-shipping-zone.md](ghl/store/update-shipping-zone.md) |
| GET | `/surveys/submissions` | Get Surveys Submissions | surveys.readonly | [get-surveys-submissions.md](ghl/surveys/get-surveys-submissions.md) |
| GET | `/surveys` | Get Surveys | surveys.readonly | [get-surveys.md](ghl/surveys/get-surveys.md) |
| POST | `/users` | Create User | users.write | [create-user.md](ghl/users/create-user.md) |
| DELETE | `/users/:userId` | Delete User | users.write | [delete-user.md](ghl/users/delete-user.md) |
| POST | `/users/search/filter-by-email` | Filter Users by Email | users.readonly | [filter-users-by-email.md](ghl/users/filter-users-by-email.md) |
| GET | `/users/:userId` | Get User | users.readonly | [get-user.md](ghl/users/get-user.md) |
| GET | `/users/search` | Search Users | users.readonly | [search-users.md](ghl/users/search-users.md) |
| PUT | `/users/:userId` | Update User | users.write | [update-user.md](ghl/users/update-user.md) |
| POST | `/voice-ai/actions` | Create Agent Action | voice-ai-agent-goals.write | [create-action.md](ghl/voice-ai/create-action.md) |
| POST | `/voice-ai/agents` | Create Agent | voice-ai-agents.write | [create-agent.md](ghl/voice-ai/create-agent.md) |
| DELETE | `/voice-ai/actions/:actionId` | Delete Agent Action | voice-ai-agent-goals.write | [delete-action.md](ghl/voice-ai/delete-action.md) |
| DELETE | `/voice-ai/agents/:agentId` | Delete Agent | voice-ai-agents.write | [delete-agent.md](ghl/voice-ai/delete-agent.md) |
| GET | `/voice-ai/actions/:actionId` | Get Agent Action | voice-ai-agent-goals.readonly | [get-action.md](ghl/voice-ai/get-action.md) |
| GET | `/voice-ai/agents/:agentId` | Get Agent | voice-ai-agents.readonly | [get-agent.md](ghl/voice-ai/get-agent.md) |
| GET | `/voice-ai/agents` | List Agents | voice-ai-agents.readonly | [get-agents.md](ghl/voice-ai/get-agents.md) |
| GET | `/voice-ai/dashboard/call-logs/:callId` | Get Call Log | voice-ai-dashboard.readonly | [get-call-log.md](ghl/voice-ai/get-call-log.md) |
| GET | `/voice-ai/dashboard/call-logs` | List Call Logs | voice-ai-dashboard.readonly | [get-call-logs.md](ghl/voice-ai/get-call-logs.md) |
| PATCH | `/voice-ai/agents/:agentId` | Patch Agent | voice-ai-agents.write | [patch-agent.md](ghl/voice-ai/patch-agent.md) |
| PUT | `/voice-ai/actions/:actionId` | Update Agent Action | voice-ai-agent-goals.write | [update-action.md](ghl/voice-ai/update-action.md) |
| GET | `/workflows` | Get Workflow | workflows.readonly | [get-workflow.md](ghl/workflows/get-workflow.md) |

