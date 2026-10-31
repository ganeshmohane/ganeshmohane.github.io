---
name: seo-blog-post
description: "Perform an SEO and technical publishing review for a Jekyll blog post. Use when: optimizing a post title, slug, permalink, excerpt, metadata, heading structure, keywords, internal links, Open Graph image, page speed, structured content, sitemap, or search snippet before publication."
argument-hint: "Post path or topic with target search intent"
user-invocable: true
disable-model-invocation: false
---

# SEO Blog Post

Perform a search and technical publishing review without changing the author's voice or inventing claims.

## Inputs

- Post file path
- Primary keyword or topic
- Search intent: informational, tutorial, comparison, or implementation
- Existing related posts
- Any benchmark, deployment, or product details that are verified

## Review procedure

### 1. Search intent

Identify the primary keyword and two or three supporting phrases. Match the title and opening with the likely user intent.

Keep the title:

- Specific and descriptive
- Usually under 60 characters when practical
- Free from emoji, clickbait, and repetitive keywords
- Natural for both users and search engines

### 2. Frontmatter

Check:

- `title`
- `date`
- Stable `permalink`
- `excerpt`
- `tags`
- `categories`
- `header.image`
- `header.teaser`

Use an excerpt of roughly 150-160 characters, written as a summary rather than marketing copy.

Use a stable slug. Avoid changing published permalinks.

### 3. Content structure

Use:

- One clear H1 through frontmatter
- Descriptive H2 sections
- H3 subsections only where needed
- Short paragraphs and scannable lists
- A direct answer near the introduction
- Code and commands with language labels
- Real examples and limitations

Add the primary phrase naturally in:

- Title
- First paragraph
- One or two headings
- Excerpt
- Image text or alt context where appropriate

Do not force keywords or repeat exact phrases unnaturally.

### 4. Internal linking

Link to:

- Related technical posts
- Portfolio projects where relevant
- Resume or About page when contextual

Use descriptive anchor text. Avoid repeated generic links such as "click here".

### 5. Images and social previews

For each post graphic:

- Use a lightweight SVG or optimized image
- Provide meaningful alt text
- Reuse the graphic as `header.image` and `header.teaser`
- Keep text inside the graphic readable and short
- Use `/images/<filename>` or the repository's current frontmatter pattern consistently

Verify the generated Open Graph image through `_includes/seo.html`.

### 6. Technical checks

Confirm:

- Permalink resolves in `_site/<permalink>/`
- No broken local links
- Page source has one article title
- Date and author metadata are rendered
- Graphic loads at the expected size
- `robots.txt`, feed, sitemap, and canonical configuration remain valid
- Mobile header and cards remain readable

### 7. E-E-A-T and credibility

Prefer:

- Specific implementation details
- Honest performance methodology
- Verified personal experience
- Sources and official documentation
- Constraints and caveats

Do not claim rankings, certifications, business results, or benchmark gains without evidence.

## Output format

Before editing, report:

1. Primary keyword and search intent
2. Suggested title
3. Suggested excerpt
4. Required internal links
5. Files to change

After editing, validate the build.

## Validation

```bash
bundle exec jekyll build --trace
git --no-pager diff --check
```

Check generated sitemap and HTML only if the relevant files exist.
