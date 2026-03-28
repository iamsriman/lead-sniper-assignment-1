# Lead Sniper - Assignment 1

## What it does
Monitors GitHub stargazers of n8n-io/n8n repo and automatically 
sends high-value leads to Discord using n8n automation.

## Workflow Steps
1. Schedule Trigger - runs every minute
2. Fetches stargazers from GitHub API
3. Enriches each user profile via GitHub /users/{username}
4. Filters users with 100+ followers OR 50+ public repos
5. Generates AI sales pitch using Groq LLM (llama-3.3-70b)
6. Sends formatted lead to Discord webhook

## Logic Log - API Rate Limit Handling
- Used GitHub PAT token (5000 requests/hour limit)
- Added Wait nodes (2-3 sec delays) between API calls
- Used $workflow.staticData to prevent duplicate processing

## Files
- `My workflow.json` - n8n workflow export
- `Screenshot discord.png` - successful Discord output
- `logic_log.txt` - rate limit handling explanation

## Demo
[Watch Demo Recording] https://drive.google.com/file/d/1vOzVSHKDzHszTWPOQAtZwJTcI7xkFqb2/view?usp=sharing
