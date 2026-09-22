# CSC 394 - Week 2: Project Management, Roles, and MCP

The lecture introduces team roles, Agile planning, project scope, risk management,
and development workflows, then uses the same **TaskBoard** project to introduce
**Model Context Protocol (MCP)** from first principles.

## Lecture files

| File | Purpose |
|------|---------|
| [week-02-deck.md](week-02-deck.md) | Authoritative Marp source, including worked examples, explanations in speaker notes, and official references |
| [week-02-deck.html](week-02-deck.html) | Browser slide deck; download and open locally |
| [week-02-deck.pptx](week-02-deck.pptx) | PowerPoint slide deck with speaker notes |

The MCP module explains hosts, clients, servers, tools, resources, prompts,
discovery, transports, permissions, and the model/tool execution loop. It compares
MCP with direct API calls and model-provider tool calling, shows how Copilot,
Claude Code, and Codex use it, and covers security, privacy, cost, reliability,
and when **not** to use MCP. Examples use fictional classroom data, not a live
GitHub repository or student records.

Core teaching slides are followed by an optional technical appendix. Speaker
notes expand the examples and provide discussion answers. In the HTML deck,
press **P** for presenter view, **O** for the overview, and the arrow keys to
navigate. In PowerPoint, use the Notes pane or Presenter View.

The 104-slide deck preserves the original course material. The **main MCP
module is slides 42-76**; the **optional appendix is slides 84-104**, including
a complete read-only Python server and a client that demonstrates MCP without
an LLM. The lab uses the official Python SDK `mcp==2.2.0`.

Protocol details and product instructions are dated **September 22, 2026**.
Version labels matter: current protocol examples and compatibility examples are
identified separately. Follow the versioned references in the lecture rather
than assuming that every installed host or SDK implements the newest revision.

## Regenerate both decks

Install Node.js 22 or later and a supported browser (Chrome, Edge, or Firefox).
Then run these commands from this repository:

```powershell
npm ci
npm run build
```

Marp CLI and its compatible browser driver are pinned in `package.json` and
`package-lock.json`. To regenerate one format, run `npm run build:html` or
`npm run build:pptx`.

Edit **only the Markdown source**, then regenerate and commit all three lecture
files together. The inline HTML in the source is trusted lecture layout markup;
the build enables it with `--html`. No external slide images or API credentials
are required.

The PPTX uses Marp's standard rendered-slide export to preserve its appearance
and speaker notes. Slide bodies are images, not individually editable PowerPoint
text boxes; make content changes in Markdown and rebuild. Use the Markdown or
HTML for clickable reference links; full source URLs are also included in the
PowerPoint reference slides' notes.