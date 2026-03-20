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

### Content structure
- `index.mdx` - Home page
- `get-started/` - Onboarding, environment setup, quick start, go-live checklist
  - `onboarding/` - KYB requirements, dashboard, FAQ
  - `environment-setup/` - Credentials, sandbox, webhooks
- `how-grain-works/` - Overview, payment lifecycle, settlement, supported crypto, pricing
- `payment-sdk/` - SDK overview, installation, integration, testing, API reference
  - `integration-guide/` - Initialize, create session, handle completion, handle errors
  - `testing/` - Sandbox testing, simulate outcomes, test wallets
  - `api-reference/` - Authentication, endpoints, error codes, rate limits
- `partner-dashboard/` - Dashboard overview, transactions, settlements, analytics, settings
  - `transactions/` - View/search, details/statuses, export
  - `settings/` - API keys, webhooks, team members, notifications
- `support/` - Getting help, system status, FAQ, release notes

### Brand colors
- Grain Sandstone: `#cdc2af` — used for dark mode logo, light-mode accent
- Grain Charcoal: `#4b4847` — used for light mode logo, primary color, dark-mode accent

### Adding pages
1. Create an MDX file in the appropriate directory
2. Add the page path to `docs.json` under the correct navigation group

## Writing Guidelines

### General rules (all pages)
- **Second person** — address the reader as "you" / "your"
- **Concise** — short paragraphs (2-3 sentences max), no filler
- **Frontmatter** — every page needs `title` (1-4 words), `description` (one sentence, no period), and optional `icon`
- **Headings** — H2 (`##`) for major sections, H3 (`###`) for subsections. No H1 (title serves as H1)
- **Code references** — use backticks for file names, commands, config keys, and paths
- **Section intros** — open each section with a 1-sentence summary before details

### Technical documentation
Pages covering developer setup, API references, integrations, and code workflows.
- **Imperative tone** — "Install the CLI", "Run the command", not "You should install..."
- **Code-first** — lead with code blocks and examples, explain after
- **Components**: `<Steps>`, `<CodeGroup>`, `<ResponseField>`, `<Accordion>` for troubleshooting
- **Callouts**: `<Tip>`, `<Note>`, `<Warning>`, `<Info>` for supplementary context

### Business & merchant experience documentation
Pages covering getting started guides, merchant onboarding, product overviews, and non-developer workflows.
- **Informative tone** — explain the "what" and "why" clearly before the "how"
- **Approachable** — friendly but professional, avoid jargon or define it on first use
- **Guide the reader** — use `<Steps>`, `<Card>`, `<CardGroup>` to create clear paths through content
- **Visual hierarchy** — use callouts (`<Tip>`, `<Note>`) and cards to break up text and highlight key takeaways
- **Outcome-oriented** — frame content around what the reader will achieve, not just what to click
