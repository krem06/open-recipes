# Contributing to Open Recipes

Thanks for wanting to contribute. Open Recipes grows through real-world experience — the best recipes come from people who have actually built something with a given stack.

---

## Ways to contribute

### Submit a new recipe
If you've built something and want to share the stack, write a recipe for it.

1. Fork this repository
2. Create a folder under `recipes/` with a short kebab-case name (e.g. `recipes/self-hosted-analytics/`)
3. Add a `recipe.yaml` following the [spec](SPEC.md)
4. Optionally add a `diagram.md` with a Mermaid graph and a `README.md` with narrative context
5. Open a pull request — describe what the recipe is for and why you think it's useful

### Improve an existing recipe
If you've used a recipe and found a better ingredient, a missing step, or something that no longer works:

1. Fork and create a branch — name it descriptively (e.g. `swap-auth0-for-clerk`, `fix-lambda-setup-steps`)
2. Make your changes
3. In your PR description, explain **why** — what problem did you hit, what made the alternative better? This is where the collective experience lives.

### Open an issue
If something in a recipe caused you problems, open an issue on the repo. Your experience helps future users even if you don't have a fix.

---

## Recipe structure

```
recipes/
  your-recipe-name/
    recipe.yaml      ← required
    diagram.md       ← optional, Mermaid graph
    README.md        ← optional, narrative context
```

Minimum viable recipe is just a `recipe.yaml`. Everything else is optional but appreciated.

---

## What makes a good recipe

- **A clear point of view.** A recipe that says "use Supabase because X" is more useful than one that says "you could use Supabase or Auth0 or Clerk, it depends." Opinions are good. Alternatives can be listed but the recipe should represent a real, tested choice.
- **Real `why` fields.** "Industry standard" is weak. "We tried Auth0 and hit the free tier limit at 200 users, Supabase gave us more headroom" is useful.
- **Working setup steps.** Steps should be actionable. If a step involves getting an API key, link to exactly where you get it.
- **Honest alternatives.** If you know a component has a strong alternative, list it. Let forks argue the case for the other option.

---

## What doesn't belong in a recipe

- **Pricing numbers** — prices change, recipes shouldn't. Pricing is a live layer fetched at consumption time.
- **Code** — recipes describe what and why, not how. Code lives in your project repo.
- **Opinions disguised as facts** — if something is contested, say so in your PR and let the community discuss it.

---

## Spec changes

If you think the recipe schema itself should change, open an issue first before writing a PR. Schema changes affect all existing recipes so they deserve discussion.

---

## License

By contributing, you agree that your recipes are published under [CC-BY-4.0](LICENSE) unless you explicitly specify otherwise in your recipe's `license` field.
