# Lessons Learned

## Plugin Customization
- Skills are just markdown files — edit SKILL.md directly to tune prompts for specific workflow needs
- Commands in commands/*.md load specific skills; update the skill reference if you rename a skill dir
- MCP servers in .mcp.json are optional — commands degrade gracefully to Claude's training knowledge without them

## MCP Setup
- When adding API keys, use environment variables rather than hardcoding in .mcp.json
- Test each MCP connection individually before relying on it in a command workflow
