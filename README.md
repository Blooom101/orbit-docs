# Orbit Documentation

Complete Mintlify documentation for Orbit, the operating system for Claude-powered businesses.

## Structure

```
orbitagents-docs/
├── mint.json                          # Mintlify configuration
├── README.md                          # This file
│
├── docs/                              # Core documentation
│   ├── introduction.mdx               # What Orbit is
│   ├── quickstart.mdx                 # Get started in 5 min
│   ├── core-concepts.mdx              # Agents, decisions, vault
│   ├── architecture.mdx               # System design
│   ├── data-model.mdx                 # TypeScript schemas
│   └── trust-levels.mdx               # Confidence and source trust
│
├── api/                               # API reference
│   ├── overview.mdx                   # API summary, auth, patterns
│   ├── heartbeat.mdx                  # orbit_heartbeat tool
│   ├── events.mdx                     # orbit_event tool
│   ├── results.mdx                    # orbit_result tool
│   ├── decisions.mdx                  # orbit_decide tool
│   ├── files.mdx                      # File upload tools
│   ├── tables.mdx                     # orbit_table_write tool
│   └── search.mdx                     # Search, discovery, instructions
│
└── guides/                            # How-to guides
    ├── agents-101.mdx                 # Building your first agent (stub)
    ├── integrations.mdx               # Integrate Orbit into existing code
    ├── best-practices.mdx             # Patterns that work at scale
    └── troubleshooting.mdx            # Common issues and fixes
```

## Key Features Documented

### Getting Started
- **Introduction** - High-level overview of what Orbit is and why
- **Quickstart** - Wire Orbit into your first agent in 5 minutes
- **Core Concepts** - Deep dive into agents, decisions, knowledge, results

### API Reference
- Complete reference for all `orbit_*` MCP tools
- Request/response formats with TypeScript signatures
- Real-world code patterns for each tool
- Error handling and troubleshooting per tool

### Integration
- How to add Orbit to existing Claude agents
- Integration for scheduled tasks (cron)
- Phased adoption (heartbeat → events → results → decisions)
- Multi-provider support (Claude, ChatGPT, n8n)

### Best Practices
- 17 core patterns for working with Orbit
- Anti-patterns to avoid
- Scaling strategies
- Team collaboration patterns

### Architecture
- High-level system design
- Request flow diagrams
- Data model and schemas
- Trust and source authority
- Performance limits and reliability

## How to Use

### Local Development

```bash
cd orbitagents-docs
npm install -g @mintlify/cli
mintlify dev
```

Opens local preview at http://localhost:3000

### Deployment

Push to GitHub and connect to Mintlify:
1. Push this folder to your Orbit GitHub repo
2. Go to https://dashboard.mintlify.com
3. Connect your GitHub repo
4. Docs automatically publish on push

### Content Organization

Each `.mdx` file:
- Has frontmatter with `title` and `description`
- Includes code examples (JavaScript for MCP tools)
- Links to related pages
- Organized with semantic headings

## Content Highlights

### Comprehensive Examples

Every tool has:
- Basic usage example
- Real-world patterns
- Common mistakes
- Best practices

Example: `api/heartbeat.mdx` includes:
- Simple start/end pattern
- Handling pending messages
- Reading decisions before acting
- Migration from manual agents

### Decision Framework

Detailed guidance on:
- When to use each trust level (exploratory/conclusion/authoritative)
- How confidence scores work
- How operator promotion works
- How to handle conflicts

### Patterns

17 core best practices for:
- Stable agent identity
- Always heartbeat
- Full content in results
- Reading directives
- Citing sources
- Reusing trackers
- Handling errors
- And more

### Troubleshooting

16 common issues with:
- Root causes
- Detection strategies
- Solutions and code samples
- How to prevent

## Maintenance

### Adding New Pages

1. Create `.mdx` file in appropriate folder
2. Add to `mint.json` navigation
3. Link from related pages
4. Deploy (auto if in GitHub)

### Updating Content

- Frontmatter controls title/description
- Markdown with code blocks (use syntax highlighting)
- Embed TypeScript interfaces for clarity
- Linking between pages with relative paths

### Versioning

Consider adding version selector if Orbit API changes:

```json
{
  "versions": ["v1.0", "v0.9"]
}
```

## Mintlify Configuration

Key settings in `mint.json`:
- **colors** - Brand colors for UI
- **navigation** - Left sidebar organization
- **topbarLinks** - Dashboard, GitHub links
- **anchors** - Floating sidebar links

Customize colors, logos, and footer social links as needed.

## Next Steps

1. **Deploy** - Push to GitHub and connect to Mintlify
2. **Add API keys** - Wire up example environment setup
3. **Gather feedback** - Share docs with first agents/teams
4. **Iterate** - Add missing scenarios, clarify confusing sections
5. **Monitor usage** - See which pages get traffic via analytics

## Contributing

Structure for contributions:
- Bug fixes → update relevant `.mdx` file
- New tools → add `api/[tool-name].mdx`
- New patterns → add to `guides/best-practices.mdx`
- Operator workflows → add to `docs/`

Keep all examples working and tested.

## License

Documentation is part of Orbit project.

---

**Created:** June 28, 2026  
**Status:** Complete and ready for deployment  
**Last Updated:** June 28, 2026
