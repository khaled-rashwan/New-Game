# Claude Code GitHub Workflow Setup

## Overview

This repository is configured to use Claude Code via GitHub Actions. You can assign issues or tasks to Claude by mentioning `@claude` in issues, pull requests, or comments.

## Setup Instructions

### 1. Add ANTHROPIC_API_KEY Secret

To enable Claude Code, you need to add your Anthropic API key as a GitHub secret:

1. Go to your repository settings: `https://github.com/khaled-rashwan/New-Game/settings/secrets/actions`
2. Click **"New repository secret"**
3. Name: `ANTHROPIC_API_KEY`
4. Value: Your Anthropic API key (get it from https://console.anthropic.com/)
5. Click **"Add secret"**

### 2. Workflow Configuration

The workflow is already configured in `.github/workflows/claude.yml` with:

- ✅ Proper permissions (contents, issues, pull-requests)
- ✅ Trigger events for issues and PRs
- ✅ Support for issue comments and PR review comments
- ✅ GitHub token and API key configuration

## How to Use

### In Issues

Simply mention Claude in an issue:

```
@claude Please help implement the user authentication feature
```

### In Pull Requests

Mention Claude in PR descriptions or comments:

```
@claude Please review this code and suggest improvements
```

### In Comments

You can also use Claude in issue or PR comments:

```
@claude Can you help debug this error?
```

## Workflow Triggers

The Claude Code workflow runs automatically when:

- An issue is opened or edited
- A pull request is opened, edited, or synchronized
- A comment is created on an issue
- A review comment is created on a pull request

## Workflow Permissions

The workflow has the following permissions:

- **contents: write** - To make code changes and commits
- **issues: write** - To comment on and update issues
- **pull-requests: write** - To comment on and update pull requests

## Troubleshooting

### Claude is not responding

1. **Check API Key**: Ensure `ANTHROPIC_API_KEY` is set in repository secrets
2. **Check Workflow**: Go to Actions tab and check if the workflow ran
3. **Check Permissions**: Ensure the workflow has necessary permissions
4. **Check Syntax**: Ensure you're using `@claude` (not `@Claude` or other variants)

### Workflow failed

1. Go to the **Actions** tab in your repository
2. Click on the failed workflow run
3. Check the logs for error messages
4. Common issues:
   - Missing or invalid API key
   - Rate limits reached
   - Network issues

## Best Practices

1. **Be Specific**: Provide clear, detailed instructions to Claude
2. **Context**: Include relevant context and links in your requests
3. **One Task**: Focus on one task per mention for better results
4. **Review**: Always review Claude's changes before merging

## Features

- 🤖 Automated code assistance
- 💬 Natural language interaction
- 🔄 Automatic PR creation and updates
- 📝 Code reviews and suggestions
- 🐛 Bug fixes and debugging help
- 📚 Documentation generation

## Example Use Cases

### Feature Implementation
```
@claude Please implement a dark mode toggle feature with these requirements:
1. Add a toggle button in the header
2. Save preference to localStorage
3. Apply dark theme classes when enabled
```

### Code Review
```
@claude Please review this PR and check for:
- Security vulnerabilities
- Performance issues
- Best practices
```

### Bug Fix
```
@claude There's a bug where users can't submit the contact form. 
The form data is not being sent to the backend. Can you investigate and fix?
```

### Documentation
```
@claude Please add JSDoc comments to all functions in src/utils.js
```

## Additional Resources

- [Claude Code Documentation](https://github.com/anthropics/claude-code-action)
- [Anthropic API Documentation](https://docs.anthropic.com/)
- [GitHub Actions Documentation](https://docs.github.com/en/actions)

## Status

✅ Workflow configured and ready to use  
⚠️ Requires ANTHROPIC_API_KEY secret to be set  

---

**Last Updated**: 2024  
**Workflow File**: `.github/workflows/claude.yml`  
**Version**: 1.0
