# Archify

Archify is an Agent Skill for generating architecture, workflow, sequence, data-flow, and lifecycle diagrams. Start with a system description, Mermaid input, or repository evidence. The result is a self-contained interactive HTML file with light and dark themes, node details, path tracing, and browser-based export.

This review candidate contains the unchanged Archify 3.0.1 Skill and its executable resources. It is not an official platform listing. Node.js 18 or newer is required. Real-browser delivery checks require a supported local Chrome/Chromium executable. Browser availability and filesystem access depend on the host. Cursor IDE host loading and platform-managed upgrades have not yet been verified.

## First use

Ask: “Use Archify to show a web request: Browser calls an API, the API checks Redis, and a cache miss queries PostgreSQL and fills the cache.” The Agent should follow skills/archify/SKILL.md and resolve its CLI from that installed Skill folder, rather than from the user's project.

## Runtime and data

Rendering and validation run locally. Repository analysis is performed by the user's chosen Agent under that host's permissions; Archify is not a hosted inference service and does not control the model provider's data policy. The optional update check requests the public stable-version manifest; it does not send diagram contents and never installs updates. Browser checks launch a local browser. Export uses the browser. There is no MCP server, hook, dependency installation, or automatic installer in this plugin.

## Updates

Update this plugin through its host after approved versions are published. A newer Skill version reminder is informational: it must not replace plugin-managed files or invoke a Skills CLI installation automatically. Host update behavior and reminder wording remain pending host acceptance.

Source: https://github.com/tt-a1i/archify
Examples: https://tt-a1i.github.io/archify/gallery.html
License: MIT; third-party notices accompany the Skill.

## Provenance and verification

This standalone Cursor distribution packages stable Archify 3.0.1 from upstream commit `bb6f126f1748a4079df1d263302466eb4333e3b0`. It is a publisher review candidate, not a claim of marketplace acceptance. The tracked-only staging payload excludes local files and symlinks.

Outside the upstream repository, all five recommended diagram examples passed validate, deliver, check, and real-browser check with the packaged CLI. Doctor passed. An isolated, controlled future-version manifest test triggered the informational update notice without modifying source files. These checks do not substitute for Cursor IDE acceptance.
