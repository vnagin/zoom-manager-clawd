---
name: zoom-manager
description: Manage Zoom meetings via OAuth API. Create, list, delete, and update events.
metadata: {
  "clawdbot": {
    "emoji": "📹",
    "requires": {"bins": ["node"]},
    "secrets": ["ZOOM_CLIENT_ID", "ZOOM_CLIENT_SECRET", "ZOOM_ACCOUNT_ID"]
  }
}
---

# Zoom Manager

Manage your Zoom meetings directly from Clawdbot.

## Setup

1. Create a **Server-to-Server OAuth** app in the [Zoom App Marketplace](https://marketplace.zoom.us/).
2. Get your **Client ID**, **Client Secret**, and **Account ID**.
3. Set them as environment variables:
   - `ZOOM_CLIENT_ID`
   - `ZOOM_CLIENT_SECRET`
   - `ZOOM_ACCOUNT_ID`

## Commands

### List Meetings
```bash
node {baseDir}/scripts/zoom-cli.js list
```

### Create a Meeting
```bash
node {baseDir}/scripts/zoom-cli.js create "Meeting Topic" "2026-01-30T10:00:00Z" 60
```

### Update a Meeting
```bash
node {baseDir}/scripts/zoom-cli.js update <meeting_id> <new_start_time> <duration> "New Topic"
```

### Get Meeting Info
```bash
node {baseDir}/scripts/zoom-cli.js info <meeting_id>
```

### Delete a Meeting
```bash
node {baseDir}/scripts/zoom-cli.js delete <meeting_id>
```
