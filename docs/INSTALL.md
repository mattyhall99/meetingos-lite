# Installation Guide

## Prerequisites

- A Claude Pro, Team, or Enterprise account with skills enabled
- For Gmail/Drive integration: Gmail and Google Drive connectors enabled in Claude

## Option 1: Clone from GitHub (recommended)

```bash
git clone https://github.com/mattyhall99/meetingos-lite.git
```

Then copy the skill folder to your Claude skills directory:

**macOS / Linux:**
```bash
cp -r meetingos-lite/.claude/skills/meetingos-lite ~/.claude/skills/
```

**Windows (PowerShell):**
```powershell
Copy-Item -Recurse meetingos-lite\.claude\skills\meetingos-lite $env:USERPROFILE\.claude\skills\
```

## Option 2: Download ZIP

1. Click the green "Code" button on GitHub
2. Select "Download ZIP"
3. Extract the ZIP
4. Copy the `.claude/skills/meetingos-lite` folder to your Claude skills directory (see paths above)

## Option 3: Claude Code

If you use Claude Code, add the skill directly:

```bash
claude skills add https://github.com/mattyhall99/meetingos-lite
```

## Verify Installation

Start a new Claude conversation and say:

> "Summarise my latest meeting notes"

If Claude responds by searching your Gmail or asking which meeting to process, the skill is active.

If Claude doesn't recognise the skill, check that:
- The SKILL.md file is at `~/.claude/skills/meetingos-lite/SKILL.md`
- You started a new conversation after installing (skills load at conversation start)
- Skills are enabled in your Claude account settings

## Enabling Gmail and Drive Integration

MeetingOS Lite can search your Gmail and Google Drive for meeting notes automatically. To enable this:

1. Open Claude settings
2. Go to Connected Apps / Integrations
3. Enable Google Gmail
4. Enable Google Drive
5. Grant the requested permissions

Without these integrations, you can still use MeetingOS Lite by uploading files or pasting text directly.

## Upgrading to MeetingOS Pro

MeetingOS Pro ($49, one-time) adds executive summaries, insights, risks, blockers, decisions, professional .docx output, and full customisation.

Get it at [meetingos.com](https://meetingos.com)
