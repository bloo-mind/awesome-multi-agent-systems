# Contributing to Awesome Multi-Agent Systems

Thanks for helping keep this list useful! The goal is a **curated, annotated** list — quality over quantity. One strong primary source beats five blog posts.

## How to add an entry

1. Open a pull request adding **one item per PR** (or a small, closely related set) to the appropriate section.
2. Use the entry format:

   ```
   - [**Title**](Link) (Year) by Authors/Maintainers
     Annotation (1–3 sentences; what it is, why it matters, when to use it). `tag1`, `tag2`
   ```

3. For tools/frameworks, use:

   ```
   - [**Name**](https://github.com/org/repo) — Language · License · Maturity
     One-line description. ![Stars](https://img.shields.io/github/stars/org/repo.svg?style=social&label=Star)
   ```

4. Mark anything you can't verify from a primary source as `unspecified` — don't guess.

## Checklist before submitting

- [ ] Link points to a **primary/official source** (paper DOI/arXiv, official repo or organisation page).
- [ ] Entry includes title, authors/maintainers, year, a neutral 1–3 sentence annotation, and tags.
- [ ] For tools: language, license, and maturity signal (active / maintenance mode / archived) are stated.
- [ ] The item is not already listed elsewhere in the README.
- [ ] Alphabetical or chronological ordering of the surrounding section is preserved (papers are reverse-chronological; check the section).
- [ ] Links pass the CI link check (dead or paywall-redirect links will be flagged).

## What gets accepted

An entry is likely to be accepted if it satisfies most of:

- **Research relevance**: directly informs MAS theory, algorithms, evaluation protocols, or reproducible tooling.
- **Demonstrated impact**: strong citations, adoption, or clear milestone status.
- **Reproducibility**: code, data, benchmarks, or explicit evaluation methodology where applicable.
- **Clarity and neutrality**: the annotation states what it's good for and its limitations — no marketing copy.

## What gets declined

- Self-promotional entries without demonstrated adoption or peer review.
- Listicles, secondary blog posts, or paywalled content with no open alternative.
- Products/tools with no clear multi-agent research or engineering relevance.

## Removing or updating entries

PRs that fix dead links, update archival/maintenance status, or correct metadata are always welcome — they're as valuable as additions.
