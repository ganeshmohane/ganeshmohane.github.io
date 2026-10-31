---
name: portfolio-project
description: "Add or replace a portfolio project in Ganesh Mohane's Jekyll site. Use when: creating project pages, rebuilding the Projects section, documenting privacy AI, TensorRT, ONNX, CUDA, face detection, license plate detection, MLOps, APIs, infrastructure, dashboards, performance, logging, monitoring, or multi-GPU work."
argument-hint: "Project name, purpose, technologies, implementation, verified outcomes, and links"
user-invocable: true
disable-model-invocation: false
---

# Portfolio Project

Create concise production-oriented project pages in `_portfolio/` without overstating impact.

## Inputs

Before writing, collect:

- Project name
- Verified problem and user need
- Technologies and architecture
- Personal responsibilities
- Rebuilt or redesigned components
- Deployment and operations details
- Measured outcomes and measurement method
- Public URL, demo, repository, or screenshots if available
- Project graphic preferences

Do not invent repository links, uptime, revenue, accuracy, latency, or scale claims.

## Repository conventions

- Project pages belong in `_portfolio/*.md`
- Remove or replace outdated placeholder project files
- Use the template at `./assets/project-template.md`
- Add graphics to `images/<project-slug>-project.svg`
- Frontmatter includes `title`, `excerpt`, `collection: portfolio`, `stack`, and `header`
- Keep project names and technology tags consistent across cards and pages
- Update `_pages/portfolio.html` only if card behavior needs a new field
- Update `_pages/about.md` only if selected-project behavior changes
- Update `_data/cv.json` portfolio entries only when the file is used as source content

## Page structure

Use:

1. Overview: the problem and system purpose
2. What I built: responsibility-focused bullets
3. Architecture or implementation: clear data and model flow
4. Performance or outcome: measured and contextualized
5. Deployment and operations: APIs, logging, monitoring, alerts, scaling
6. Engineering lessons or next improvements if useful

Keep claims measurable:

- Instead of "faster," show a baseline and target only when verified
- Instead of "under 200 ms," specify whether the result is per frame, p95, end-to-end, or a target
- If a result is still being validated, use "designed for" or "targeting"

## Graphic conventions

- Lightweight SVG
- 1200 x 630 viewBox for consistent cards and social previews
- Strong project name and 3-4 central technologies
- Avoid lengthy code, dense tables, or small text
- Give the SVG a meaningful title and description
- Use the same filename for `header.image` and `header.teaser`

## Project checklist

- Outdated template projects removed
- Verified project description
- Technology stack complete
- No unsupported personal or performance claims
- Project graphic added
- Home page card includes the graphic and title
- Project archive card includes the graphic and title
- Internal links to related posts are appropriate
- Content is concise and recruiter-readable
- Jekyll build succeeds

## Validation

```bash
bundle exec jekyll build --trace
git --no-pager diff --check
```

Open the portfolio archive and at least one project page to verify generated cards and graphics.

## Template

Use `./assets/project-template.md`.
