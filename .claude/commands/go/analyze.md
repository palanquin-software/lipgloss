---
description: Analyze tapeheads2 architecture
model: opus
---

Analyze Go project architecture:

1. `go list -json ./...` - package structure
2. `go mod graph` - module dependencies
3. `go list -f '{{.ImportPath}}: {{join .Imports ", "}}' ./...` - internal imports
4. Directory structure (cmd/game, cmd/editor, core/, game/, assets/)
5. `go doc` on key packages

Output:

- Package purposes (cmd/game, cmd/editor, cmd/lambda/*)
- Dependencies & relationships
- Entry points
- Internal patterns (core/, game/)
- Key types/interfaces

Create mind map via mcp__mindpilot__render_mermaid:

- Root: tapeheads2
- Branches: cmd/, core/, game/, assets/
- Sub-branches: packages
- Leaves: key types/interfaces