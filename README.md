# MimDB Documentation

Documentation source for [docs.mimdb.cloud](https://docs.mimdb.cloud) - the official documentation for MimDB, a self-hosted Backend-as-a-Service platform.

## Structure

```
docs.json              # Site configuration (navigation, branding, theme)
openapi-spec.json      # OpenAPI 3.1 spec (source of truth for API reference)
introduction.mdx       # Landing page
quickstart.mdx         # Docker Compose quickstart guide
auth/                  # Authentication (6 pages)
database/              # Database management (4 pages)
rest-api/              # REST API via PostgREST (5 pages)
realtime/              # WebSocket subscriptions (3 pages)
storage/               # File storage and uploads (4 pages)
vectors/               # pgvector similarity search (2 pages)
cron/                  # Scheduled jobs via pg_cron (2 pages)
sql/                   # Raw SQL execution (1 page)
stats/                 # Query performance stats (1 page)
platform/              # Organizations, projects, API keys (5 pages)
self-hosting/          # Deployment and configuration (6 pages)
client-integration/    # supabase-js, HTTP, WebSocket examples (3 pages)
```

## Contributing

Documentation is written in [MDX](https://mdxjs.com/) (Markdown with JSX components). To contribute:

1. Fork this repository
2. Edit or create `.mdx` files following the existing structure
3. Submit a pull request

### Frontmatter

Every page requires YAML frontmatter:

```yaml
---
title: "Page Title"
description: "A complete sentence describing this page."
---
```

### Custom Components

These components are available in all MDX files without importing:

| Component | Usage |
|-----------|-------|
| `<Note>` | Blue informational callout |
| `<Warning>` | Amber warning callout |
| `<Tip>` | Green tip/suggestion callout |
| `<Steps>` | Numbered step-by-step guide |
| `<CodeGroup>` | Multi-language tabbed code blocks |
| `<CardGroup cols={2}>` | Grid of navigation cards |
| `<Card title="..." href="...">` | Linked card |
| `<Accordion title="...">` | Collapsible section |
| `<ParamField name="..." type="..." required>` | API parameter |

### Accuracy

All documentation claims must be verified against the [Mimisbrunnr source code](https://github.com/MimDB/Mimisbrunnr). When referencing defaults, limits, or API paths, check the actual implementation.

## License

Content is licensed under [CC BY 4.0](https://creativecommons.org/licenses/by/4.0/).
