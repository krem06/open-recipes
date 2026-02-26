# Open Recipes 🧪

> **Note:** The example recipe below is AI-generated to illustrate the format. Real-world recipes based on actual experience are coming soon. The whole point of Open Recipes is to capture human experience — patterns that help others, AI or not, build effective setups grounded in what actually works.
>
> To protect that authenticity, this project plans to use [Vouch](https://github.com/mitchellh/vouch) to ensure only verified humans can contribute recipes. In a world where AI can generate plausible-looking content, trust matters — especially for a project whose value depends entirely on real experience.

**A standard for describing how products are assembled.**

Open Recipes is an open format for documenting the tools, services, and components that make up a product — and the reasoning behind each choice. Not code, not infrastructure. Just a clear, structured description of what goes into something and how it fits together.

A recipe can describe a SaaS application, a hardware device, a self-hosted server setup, a mobile app, or anything else made of assembled parts.

---

## Why?

When you build something, you make dozens of decisions: which database, which auth provider, which hosting platform, why this and not that. That knowledge usually lives in someone's head, in a scattered Notion doc, or nowhere at all.

Open Recipes gives that knowledge a home — structured enough to be useful, simple enough that people will actually write it.

A recipe can be:
- A **starting point** for a new project — skip the "which tools should I use?" phase
- **Context for an AI assistant** — paste a recipe and it immediately understands your stack
- **Input for an agent** — walk through setup steps, fetch live pricing, compare alternatives
- A **reference for your team** — understand why decisions were made, not just what they were

---

## What a recipe looks like

```yaml
name: "Bootstrapped SaaS on AWS"
description: "Minimal viable SaaS stack for solo founders"
version: "1.0"
author: "your-github-username"
license: "CC-BY-4.0"
tags: [saas, aws, bootstrapped]

ingredients:
  - id: auth
    name: Supabase Auth
    url: https://supabase.com
    docs: https://supabase.com/docs
    role: "User authentication and session management"
    why: "Avoids building auth from scratch, generous free tier"
    alternatives: [Clerk, Auth0]

relations:
  - from: frontend
    to: auth
    how: "Supabase JS client manages sessions client-side"

setup:
  - "Go to supabase.com, create a new project, copy the ANON_KEY and project URL"
```

→ See the full [spec](SPEC.md) for the complete schema.

---

## Browse recipes

| Recipe | Tags | Author |
|---|---|---|
| [Bootstrapped SaaS on AWS](recipes/bootstrapped-saas-aws/) | saas, aws, solo-founder | Claude code ;) |

*More recipes welcome — see [Contributing](CONTRIBUTING.md).*

---

## Using a recipe

**As a human** — read `recipe.yaml` and `README.md` to understand the stack and the decisions behind it. Fork it as your starting point.

**With an AI assistant** — paste the recipe into your context. The AI immediately understands your stack and can generate code without you re-explaining your choices.

**With an agent** — an agent can walk through the `setup` steps, fetch live pricing for each ingredient, and produce a personalised cost breakdown or interactive setup guide.

---

## Contributing

See [CONTRIBUTING.md](CONTRIBUTING.md).

---

## License

The spec and all recipes in this repository are released under [CC-BY-4.0](LICENSE) unless otherwise noted.
