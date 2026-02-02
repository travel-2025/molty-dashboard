# 🔥 Molty Dashboard

Personal dashboard tracking projects, tasks, and activity for Molty (AI assistant) and Juli.

## Features

- **Projects** — View active projects with status
- **Tasks** — Track todos, in-progress, and completed work
- **Activity Feed** — See recent actions and updates

## How It Works

1. Molty updates JSON files in `data/` when tasks change
2. Dashboard reads the JSON and renders it
3. Auto-refreshes every 60 seconds

## Files

```
molty-dashboard/
├── index.html          # Main dashboard
├── data/
│   ├── projects.json   # Project list
│   ├── tasks.json      # Task board
│   └── activity.json   # Activity log
└── README.md
```

## Deployment

Deploy to GitHub Pages, Vercel, or any static host.

For GitHub Pages:
1. Go to repo Settings → Pages
2. Set source to main branch, root folder
3. Dashboard will be at `https://username.github.io/molty-dashboard`

## Data Formats

### Project
```json
{
  "id": "project-id",
  "name": "Project Name",
  "status": "active",
  "description": "Description",
  "color": "#hex",
  "created_at": "2026-01-01"
}
```

### Task
```json
{
  "id": "task-id",
  "project_id": "project-id",
  "title": "Task title",
  "description": "Details",
  "status": "todo|in_progress|done",
  "priority": "high|medium|low",
  "created_at": "ISO8601",
  "due_date": "ISO8601|null"
}
```

### Activity
```json
{
  "id": "act-id",
  "timestamp": "ISO8601",
  "action": "action_type",
  "description": "What happened",
  "project_id": "project-id"
}
```
