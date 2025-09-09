# Jira MCP Server Setup Guide

## Prerequisites

1. **Jira Cloud Account**: You need access to a Jira Cloud instance
2. **Node.js**: Required for running the MCP server

## Step 1: Create Jira API Token

1. Go to [Atlassian Account Settings](https://id.atlassian.com/manage-profile/security/api-tokens)
2. Click **Create API token**
3. Give it a label (e.g., "Claude MCP Server")
4. Copy the generated token (you won't see it again)

## Step 2: Configure Environment Variables

1. Copy `.env.example` to `.env`:
   ```bash
   cp .env.example .env
   ```

2. Fill in your values in `.env`:
   ```
   JIRA_HOST=https://yourcompany.atlassian.net
   JIRA_EMAIL=your-email@company.com
   JIRA_API_TOKEN=your-api-token-here
   JIRA_PROJECT_KEY=PROJ
   ```

## Step 3: Install MCP Server

The MCP server will be automatically installed when Claude Code first tries to use it, thanks to the `npx` command in `.mcp.json`.

## Step 4: Test the Connection

1. Restart Claude Code
2. Try a command like: "Show me all open tickets in Jira"
3. Or: "Create a new ticket for fixing the login bug"

## Troubleshooting

- **Authentication Error**: Verify your API token and email are correct
- **Host Error**: Ensure your JIRA_HOST includes https:// and is your actual Jira URL
- **Permission Error**: Check that your Jira account has appropriate permissions for the project

## Security Notes

- Never commit your `.env` file to version control
- API tokens should be treated as passwords
- Consider using project-specific tokens with limited permissions