# Jira MCP Server Usage Examples

## Getting Started

Once your Jira MCP server is configured, you can interact with Jira using natural language commands through Claude Code.

## Basic Operations

### Search and List Tickets

```
Show me all open tickets in project MBA
```

```
Find all bugs assigned to me
```

```
List all tickets with "authentication" in the title
```

```
Show me tickets created in the last week
```

### Get Ticket Details

```
Get details of ticket MBA-123
```

```
Show me the description and comments for MBA-456
```

```
What are the requirements for ticket MBA-789?
```

### Create New Tickets

```
Create a new bug ticket: "Login form doesn't validate email format"
```

```
Create a story for implementing dark mode in the application
```

```
Create a task ticket for updating the user documentation
```

### Update Existing Tickets

```
Update MBA-123 status to In Progress
```

```
Add a comment to MBA-456: "Fixed the validation issue, ready for testing"
```

```
Assign ticket MBA-789 to john.doe@company.com
```

## Development Workflow Integration

### Creating Development Plans

```
Create a development plan for implementing the feature described in MBA-123
```

```
Analyze ticket MBA-456 and suggest the files that need to be modified
```

```
Break down the epic MBA-100 into smaller development tasks
```

### Linking Code to Tickets

```
I'm working on MBA-123, help me implement the authentication feature
```

```
Create a PR description based on the requirements in MBA-456
```

```
Generate commit messages that reference ticket MBA-789
```

## Advanced Queries

### Project Management

```
Show me the sprint burndown for project MBA
```

```
List all tickets in the current sprint
```

```
Find blocked tickets in project MBA
```

### Reporting and Analysis

```
Show me all high-priority bugs in the last month
```

```
List tickets that are overdue
```

```
Find tickets without assignees in project MBA
```

## Development Planning Examples

### Feature Implementation

When you have a ticket describing a feature, you can ask:

```
"I have ticket MBA-124 about implementing user profiles. Can you:
1. Get the ticket details
2. Create a development plan
3. Identify the components that need to be created/modified
4. Suggest the implementation approach"
```

### Bug Fixing

For bug tickets:

```
"Help me fix the bug described in MBA-125:
1. Get the bug details and reproduction steps
2. Analyze the codebase to find potential causes
3. Create a plan to fix the issue
4. Update the ticket with progress"
```

## Best Practices

1. **Reference Ticket Numbers**: Always include the ticket number (e.g., MBA-123) for specific operations
2. **Use Natural Language**: The MCP server understands conversational requests
3. **Be Specific**: Include project keys when working with multiple projects
4. **Combine Operations**: You can ask for multiple actions in a single request

## Troubleshooting Commands

```
Test the Jira connection
```

```
Show me my Jira permissions
```

```
List all projects I have access to
```

```
Verify the MCP server is working
```