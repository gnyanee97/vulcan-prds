# Vulcan PRDs - Central Repository

Central repository for all Vulcan data product PRDs (Product Requirements Documents).

## Structure

```
vulcan-prds/
├── README.md                 # This file
├── registry.json            # Index of all PRDs with metadata
├── prds/                    # PRD files organized by domain
│   ├── analytics/          # Analytics domain PRDs
│   ├── platform/           # Platform/infrastructure PRDs
│   ├── marketing/          # Marketing domain PRDs
│   └── ...                 # Other domains
└── .github/
    └── workflows/          # GitHub Actions for automation
```

## Organization

PRDs are organized by **domain** (business area) to support enterprise-scale:

- **Domain-based**: `prds/{domain}/{product-name}.md`
- **Naming**: Use kebab-case for product names (e.g., `user-activity-dashboard.md`)
- **Registry**: All PRDs are indexed in `registry.json` for discovery

## Adding a PRD

### Option 1: Manual (for now)
1. Create PRD using `generate_data_product_prd` MCP tool
2. Save to appropriate domain directory: `prds/{domain}/{product-name}.md`
3. Update `registry.json` with PRD metadata

### Option 2: CLI Tool (coming soon)
```bash
vulcan-prd publish --domain analytics --file prd.md
```

## Registry Format

Each PRD entry in `registry.json` includes:
- `product_name`: Display name
- `domain`: Business domain (analytics, platform, etc.)
- `owner_team`: Team responsible
- `source_repo`: Original Vulcan project repo
- `prd_path`: Path to PRD file
- `tags`: Searchable tags
- `created_at`: Creation timestamp
- `updated_at`: Last update timestamp

## Search & Discovery

PRDs are indexed in Vectorize for semantic search via MCP tools:
- `search_prds`: Search across all PRDs
- `get_prd`: Retrieve specific PRD by name/path

## Domains

Common domains:
- **analytics**: Analytics, reporting, metrics data products
- **platform**: Infrastructure, core platform data products
- **marketing**: Marketing, growth, customer data products
- **finance**: Financial, revenue, billing data products
- **operations**: Operations, support, internal tooling data products

## Contributing

1. Generate PRD using MCP tools
2. Organize by domain
3. Update registry.json
4. Commit and push

## License

[Add your license here]

