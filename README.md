# Igly Canvas plugin

Pick from 2,400+ free design templates or draw on an editable [Igly](https://igly.ai) canvas from Claude, ChatGPT and Codex: menus, posters and social posts from templates, plus flowcharts, mind maps, roadmaps, kanban and retro boards, wireframes, storyboards and moodboards.

The board shows up right in the chat. Move, retype and draw on it by hand, export a PNG, or open it in the full Igly editor. Free, no account needed to draw.

## What's inside

- **MCP server** `https://igly.ai/api/mcp` (Streamable HTTP, no sign-in) with tools to browse templates (with a picker in the chat), create a canvas, apply a template beside an existing board, add / update / remove elements, arrange and export PNG. Configured in `.mcp.json` (Claude) and `mcp.json` (portable / OpenAI).
- **Skills** in `skills/`:

| Skill | Use it for |
|---|---|
| `flowchart` | processes, user flows, decision trees, system diagrams |
| `mind-map` | brainstorms and topic maps |
| `roadmap-timeline` | roadmaps, release plans, timelines |
| `kanban-retro` | kanban, retros, SWOT, affinity maps |
| `wireframe` | page and app screen wireframes |
| `storyboard` | video, ad and slide storyboards |
| `moodboard` | style directions, palettes, type pairings |
| `template-design` | posters, social posts, menus, invitations from templates |

## Install

**Claude Code**

```bash
claude plugin marketplace add Whatscheap/igly-canvas-plugin
claude plugin install igly-canvas@igly
```

**Claude (web / desktop)**: Settings → Connectors → Add custom connector → `https://igly.ai/api/mcp`.

**ChatGPT**: Settings → Plugins → Add → custom MCP server → `https://igly.ai/api/mcp`.

**Codex**: `codex plugin marketplace add Whatscheap/igly-canvas-plugin`.

## Try

- "Draw a flowchart of our customer onboarding"
- "Make a mind map for a podcast launch"
- "Turn these notes into a Q1 to Q4 roadmap"
- "Sketch a wireframe for a pricing page"
- "Make an Instagram post for our bakery's summer menu from a template"

## Privacy

Boards are stored without an account for 30 days and are reachable only through their unguessable link. See [igly.ai/legal/privacy](https://igly.ai/legal/privacy).

## License

MIT
