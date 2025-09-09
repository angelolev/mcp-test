# CLAUDE.md

This file provides guidance to Claude Code (claude.ai/code) when working with code in this repository.

## Commands

### Development
- `pnpm dev` or `npm run dev` - Start development server with HMR
- `pnpm build` or `npm run build` - Build for production (TypeScript compilation + Vite build)
- `pnpm preview` or `npm run preview` - Preview production build locally
- `pnpm lint` or `npm run lint` - Run ESLint on the codebase

### Package Manager
This project uses `pnpm` as indicated by the presence of `pnpm-lock.yaml`. Use `pnpm` commands when possible.

## Architecture

This is a React + TypeScript + Vite project with a component-based architecture:

### Project Structure
- `src/` - Source code
  - `components/` - Reusable React components organized by feature
    - Each component has its own folder with `index.tsx` and CSS modules
  - `App.tsx` - Main application component
  - `main.tsx` - Application entry point

### Key Technologies
- **React 19** - UI library
- **TypeScript** - Type safety
- **Vite** - Build tool and dev server
- **ESLint** - Code linting with React-specific rules
- **CSS Modules** - Scoped styling (pattern: `ComponentName.module.css`)

### Component Conventions
- Components are placed in `src/components/[ComponentName]/`
- Each component folder contains:
  - `index.tsx` - Main component file
  - `ComponentName.module.css` - CSS module for styling
- Components use CSS modules imported as `styles` object
- Default exports are used for components

### TypeScript Configuration
- Uses project references with separate configs for app (`tsconfig.app.json`) and Node (`tsconfig.node.json`)
- Main `tsconfig.json` only contains references to these configs

## MCP (Model Context Protocol) Integration

This project is configured with both Jira and GitHub MCP server integration for seamless project management:

### GitHub MCP Integration
**IMPORTANT**: Always prefer GitHub MCP tools over bash/git commands for GitHub operations:
- Use `mcp__github__create_branch` instead of `git checkout -b`
- Use `mcp__github__create_pull_request` instead of `gh pr create`
- Use `mcp__github__merge_pull_request` instead of `gh pr merge`
- Use `mcp__github__get_pull_request` instead of `gh pr view`
- Use `mcp__github__update_pull_request` instead of `gh pr edit`

### Jira MCP Integration

### Configuration Files
- `.mcp.json` - MCP server configuration for Claude Code
- `.env` - Environment variables for Jira authentication (not committed)
- `.env.example` - Template for environment variables
- `JIRA_SETUP.md` - Complete setup instructions

### Jira Integration Capabilities
- Fetch ticket descriptions and requirements
- Create development plans based on Jira issues
- Search and filter tickets by project, status, assignee
- Create new tickets and update existing ones
- Link development work to specific Jira tickets

### Environment Variables Required
- `JIRA_HOST` - Your Jira instance URL
- `JIRA_EMAIL` - Your Jira account email
- `JIRA_API_TOKEN` - API token from Atlassian account
- `JIRA_PROJECT_KEY` - Default project key (optional)

### Usage Examples
- "Show me all open tickets in project MBA"
- "Create a ticket for implementing dark mode feature"
- "Get details of ticket MBA-123"
- "Create a development plan for fixing the login bug in MBA-456"