---
name: blog-post-authoring
description: "Write and add a Jekyll blog post for Ganesh Mohane's portfolio. Use when: creating a new ML, MLOps, TensorRT, ONNX, CUDA, privacy AI, software engineering, or technical blog post; updating an existing post; adding frontmatter, a summary, tags, categories, code examples, graphics, or internal links."
argument-hint: "Topic, key experience, target audience, and desired post length"
user-invocable: true
disable-model-invocation: false
---

# Blog Post Authoring

Use this workflow for technical posts on Ganesh Mohane's Jekyll portfolio.

## Inputs

Before writing, collect:

- Topic and working title
- Primary audience and practical goal
- Real experience or project context
- Technologies and commands to cover
- Relevant code or benchmark evidence
- Preferred level: beginner, practitioner, or advanced

Do not invent employers, products, benchmark results, dates, credentials, or experience.

## Repository conventions

- Create posts in `_posts/`
- Name files `YYYY-MM-DD-post-slug.md`
- Place custom post graphics in `images/`
- Use the site title, author, permalink, date, tags, categories, excerpt, and `header` conventions in the template at `./assets/post-template.md`
- Keep author metadata in the post layout; do not repeat it inside the Markdown body
- Add the graphic through `header.image` and `header.teaser`
- Use SVG graphics for lightweight diagrams unless a real screenshot is specifically useful
- Link existing posts with relative permalink paths where relevant

## Writing structure

1. Start with a short problem or production context.
2. Add a clear overview explaining what the reader will learn.
3. Explain concepts and decisions in a practical order.
4. Use headings that describe outcomes or questions.
5. Include working code examples where they add value.
6. Include validation, measurement, limitations, and failure modes.
7. End with a concise implementation takeaway.
8. Add only relevant internal and official documentation links.

## Style

- Write in first person only when describing verified personal experience.
- Prefer direct, technical prose over promotional claims.
- Explain commands and tradeoffs.
- Do not present sample numbers as measured results unless supplied by the user or source data.
- Keep snippets complete enough to understand and run.
- Use one H1 title in frontmatter; begin the body with H2 sections.
- Use code fences with a language identifier.

## Article checklist

- Correct date and filename
- Valid YAML frontmatter
- Unique descriptive permalink
- Useful 150-160 character excerpt
- 3-8 focused tags
- Relevant categories
- Realistic graphic and meaningful alt text
- No duplicate information or unnecessary closing CTA
- Internal links to related posts and portfolio work
- SEO pass completed with the `seo-blog-post` skill for public articles
- Jekyll build succeeds

## Validation

Run:

```bash
bundle exec jekyll build --trace
git --no-pager diff --check
```

Review `_site/` only as generated output; edit source files, not `_site/`.

## Template

Use `./assets/post-template.md`.
