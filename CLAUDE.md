# Project: Grain Documentation Site

This is a Mintlify-powered documentation site for Grain.

## Stack

- **Framework**: Mintlify (https://mintlify.com/docs)
- **Config**: `docs.json` (Mintlify settings, navigation, theming)
- **Content**: MDX files

## Mintlify Conventions

### docs.json structure
- `theme`: One of mint, maple, palm, willow, linden, almond, aspen, sequoia, luma
- `logo`: Object with `light` and `dark` SVG paths (or a single string for both)
- `favicon`: Object with `light` and `dark` paths (or a single string for both)
- `colors`: Object with `primary` (required), `light`, and `dark` hex values
- `appearance`: Controls dark/light mode (`default`: system/light/dark, `strict`: boolean)
- `navigation`: Uses `tabs` with nested `groups` and `pages`

### File layout
- `logo/light.svg` - Logo for light mode (Grain Logo Charcoal)
- `logo/dark.svg` - Logo for dark mode (Grain Logo Sandstone)
- `favicon-light.svg` - Favicon for light mode (Grain Logomark Charcoal)
- `favicon-dark.svg` - Favicon for dark mode (Grain Logomark Sandstone)
- `images/` - Documentation images
- `snippets/` - Reusable MDX snippets
- `essentials/` - Core documentation pages
- `api-reference/` - API documentation

### Brand colors
- Grain Sandstone: `#cdc2af`
- Grain Charcoal: dark variant for light backgrounds

### Adding pages
1. Create an MDX file in the appropriate directory
2. Add the page path to `docs.json` under the correct navigation group
