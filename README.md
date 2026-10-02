# Divine

**AI development for Roblox Studio that works inside the project, not beside it.**

Divine is a desktop development environment that connects an AI coding agent directly to Roblox Studio. Instead of stopping at generated snippets, Divine gives the agent tools to inspect a live experience, create and edit instances, work with scripts and properties, and carry out multi-step development tasks inside Studio.

Divine is being built around a simple idea: describe what you want to make, give the agent the right context, and let it work through the actual development process.

> **Status:** Divine is in active development. This repository is the public home for releases, documentation, bug reports, and project updates. The application source is not published here.

## What makes Divine different

### Direct Studio control
Divine connects the agent to Roblox Studio through the Divine Studio plugin and local bridge. The agent can inspect the current project and make changes in Studio rather than handing you code to move over manually.

### More than scripting
The Studio connection is designed around the project itself. Current tooling can create and modify instances, edit properties, inspect hierarchy and nearby objects, work with scripts, clone and resize objects, and perform grouped edits.

### Image references
Attach reference images to a task and keep them with the active workflow. Divine can use those references while planning and building instead of treating an image as a one-off prompt attachment.

### Task workflows you can follow
Reference-driven builds use a visible workflow that moves through inspection, planning, primary construction, detail, verification, and completion. You can see what phase the agent is in, what it is doing, and whether a failed strategy was recovered.

### Developer observability
Divine exposes the execution path between **Agent ↔ Divine ↔ Studio**. Raw Studio events, tool calls, timings, recoveries, and root failures can be inspected when something goes wrong without filling the normal workspace with debugging noise.

### Runtime capability awareness
Studio features are reported by the plugin at runtime. Divine distinguishes between capabilities that are available, unavailable, or unsupported by the current Studio environment instead of assuming every API works everywhere.

### Managed Studio plugin
Divine includes a generated Roblox Studio plugin and tracks the bundled, installed, and currently running versions separately. The installer is being designed so plugin updates are handled by Divine without relying on a developer source checkout.

## How it works

```text
You
 │
 ▼
Divine desktop app
 │
 ▼
AI coding agent
 │
 ▼
Divine local bridge
 │
 ▼
Roblox Studio plugin
 │
 ▼
Your Roblox experience
```

The bridge runs locally and gives the agent a controlled set of Studio operations. Divine tracks the work around those operations so longer tasks remain understandable and debuggable.

## Current development areas

Divine is still moving quickly. Current work is focused on making Studio editing more reliable, improving larger environment builds, strengthening plugin installation and versioning, and expanding the agent's ability to inspect and verify its own work.

Visual verification is currently environment-dependent. Roblox Studio's screenshot capability is not available in every environment, so Divine reports visual capture as unavailable when Studio does not support it rather than pretending verification succeeded.

## Getting started

Public installation instructions will be added with the first supported public build. Until then, please avoid downloading or redistributing unofficial Divine binaries.

When public builds are available, releases and setup instructions will be published here.

## Bugs and feature requests

Found something broken or have an idea that would make Divine better? Use the repository's issue templates so we have the information needed to reproduce the problem or understand the request.

Please do not post security vulnerabilities as public issues. See [SECURITY.md](SECURITY.md) for reporting guidance.

## Project direction

The long-term goal is not simply better code generation. Divine is being built toward an agent that can take a larger Roblox development task, understand the existing experience, build within it, inspect the result, recover from problems, and keep iterating through a visible workflow.

We will only list features here once they are implemented or actively available for testing. Experimental and internal systems may change before a public release.

## Roblox and third-party services

Divine is an independent project and is not affiliated with or endorsed by Roblox Corporation. Roblox and Roblox Studio are trademarks of Roblox Corporation.

AI model availability and capabilities may depend on the providers and accounts configured by the user.

---

**Divine** — built for creating inside Roblox Studio.