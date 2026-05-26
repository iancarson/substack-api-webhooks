# How Narrareach Fits

Narrareach is the production distribution layer for newsletter writers who want the outcome behind **substack api webhooks** without maintaining the full integration stack.

## What Narrareach Handles

- Cloud scheduling for Substack Notes and social posts.
- Cross-posting from newsletter ideas into LinkedIn, Medium, X, Bluesky, and Threads.
- Platform-specific formatting and post previews.
- Retry handling and delivery status.
- Writer-friendly workflows that do not require maintaining an MCP server or REST API.
- Analytics and attribution loops after publishing.

## Best Entry Point

Start with [Substack API Webhooks on Narrareach](https://www.narrareach.com/features/content-scheduling-api).

## Related Workflows

- [Narrareach solution for substack api webhooks](https://www.narrareach.com/features/content-scheduling-api)
- [Schedule Substack Notes](https://www.narrareach.com/features/schedule-substack-notes)
- [Substack automation guide](https://www.narrareach.com/features/substack-automation-guide)

## Practical Split

Use your own MCP server or REST API for internal drafts, custom agent workflows, and proprietary business logic. Use Narrareach for the parts that need reliability: scheduling, account connections, publishing, retries, and performance feedback.
