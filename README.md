# ClaudeCode_vs_ClaudeCodeWeb
- I wanted to understand the difference between "Claude Code (local)" and "Claude Code Web".  
- I had a chat session with Claude.ai, asking about the differences.  
- It generated two PDF docs comparing/contrasting Claude Code (local) and Claude Code Web

## Anthropic is Promoting Claude Code web
- Anthropic recently sent emails offering free credits ($250 or $1000)
  - applicable to Claude Code Web only
  - Expires Nov 18, 2025
 
## Caveats
- My queries were done in a hurry
- The two PDF docs have some overlap & repetition
  - Nevertheless, I found them useful & informative
  - Take it as-is, no warranties implied or expressed
- I hope this helps someone

## TLDR Summary

### Strongest Similarities
Both Claude Code (local) and Claude Code Web use identical Claude models (Sonnet 4.5, etc.) with the same 200K token context window, support the same core agentic capabilities (multi-file editing, bash command execution, codebase understanding with extended thinking visible), and both fully support custom agents (subagents) and skills stored in .claude/agents/ and .claude/skills/ directories while respecting CLAUDE.md for project context and leveraging GitHub for version control workflows.

### Middle Ground:  only small differences
Both environments provide similar capabilities but through different mechanisms: Local offers native slash commands (/compact, /clear, /plan) while Web requires defining commands as instructions in CLAUDE.md; Local installs tools directly via system package managers (apt, pip, npm) while Web uses SessionStart hooks in CLAUDE.md to automate installations; Local implements sandboxing through OS-level primitives (Seatbelt on macOS, Bubblewrap on Linux) while Web uses container-level isolation with configurable network environments; and Local stores sessions permanently in ~/.claude/ for indefinite resumption while Web maintains active sessions with 24-hour/8-hour timeouts but preserves conversation history and GitHub-committed work beyond the container's destruction.

### Strongest Differences
Claude Code Local executes on your actual machine with permanent filesystem persistence where all your files, tools, configurations, and sessions remain exactly as you left them indefinitely with full IDE integration and the ability to work across multiple repositories simultaneously using your native file system, while Claude Code Web executes in ephemeral cloud containers where the entire /workspace directory (5GB limit) is destroyed after each task completion with GitHub serving as the ONLY persistent storage mechanism, no direct IDE access to the cloud environment (all editing is conversational), native support for running multiple parallel tasks across different repos simultaneously in separate containers, and mandatory session timeouts (24 hours continuous or 8 hours inactive) requiring you to commit work to GitHub branches/PRs to preserve anything beyond the session lifetime.


