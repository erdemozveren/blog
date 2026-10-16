# Erdem Özveren — Developer Blog

Source code for my personal developer blog, built with [Astro](https://astro.build/) and based on the [AstroPaper](https://github.com/satnaing/astro-paper) theme.

I write about software development, personal projects, technical decisions, and things I've learned along the way.

## Tech Stack

- [Astro](https://astro.build/)
- [TypeScript](https://www.typescriptlang.org/)
- [Tailwind CSS](https://tailwindcss.com/)
- [Pagefind](https://pagefind.app/) — Static search

## Getting Started

```bash
pnpm install
pnpm dev
```

The development server runs at `http://localhost:4321`.

## Commands

| Command        | Description                                  |
| -------------- | -------------------------------------------- |
| `pnpm dev`     | Start the development server                 |
| `pnpm build`   | Build the site and generate the search index |
| `pnpm preview` | Preview the production build                 |
| `pnpm sync`    | Generate Astro types                         |

## Project Structure

| Path                    | Purpose                                     |
| ----------------------- | ------------------------------------------- |
| `src/content/posts/`    | Blog posts (Markdown / MDX)                 |
| `src/content/pages/`    | Static pages, including About               |
| `src/components/`       | UI components                               |
| `src/layouts/`          | Page layouts                                |
| `src/styles/`           | Global styles                               |
| `astro-paper.config.ts` | Site metadata, theme settings, social links |
| `public/`               | Static assets, favicon, OG image            |

## Configuration

Most site settings are managed through `astro-paper.config.ts`.

This includes site metadata, author information, timezone, pagination, social links, and feature toggles.

For all configuration options, see the [AstroPaper configuration guide](https://astro-paper.pages.dev/posts/how-to-configure-astropaper-theme/).

### Adding Posts

Create a Markdown or MDX file inside `src/content/posts/`.

Example frontmatter:

```yaml
---
author: Erdem Özveren
pubDatetime: 2026-10-16T00:00:00Z
title: "My Post Title"
slug: my-post-title
featured: false
draft: false
tags:
  - software-development
description: "A short description of the post."
---
```

Posts can also be organized into subdirectories. The subdirectory name becomes part of the URL.

See the [AstroPaper post guide](https://astro-paper.pages.dev/posts/adding-new-posts-in-astropaper-theme/) for more details.

### Customizing Colors

Theme colors and color schemes can be customized.

- [Customizing color schemes](https://astro-paper.pages.dev/posts/customizing-astropaper-theme-color-schemes/)
- [Predefined color schemes](https://astro-paper.pages.dev/posts/predefined-color-schemes/)

### SEO & Social Images

Site title, description, language, and default OG image are configured in `astro-paper.config.ts`.

The theme supports automatic OG image generation for individual posts, along with sitemap and RSS feed generation.

See [Dynamic OG Image Generation](https://astro-paper.pages.dev/posts/dynamic-og-image-generation-in-astropaper-blog-posts/).

### Google Search Console

To verify site ownership, add the Google verification value to `astro-paper.config.ts`:

```ts
export default defineAstroPaperConfig({
  site: {
    // ...
    googleVerification: "your-google-site-verification-value",
  },
  // ...
});
```

See the [AstroPaper discussion](https://github.com/satnaing/astro-paper/discussions/334#discussioncomment-10139247) for more details.

## Credits & License

This blog is based on [AstroPaper](https://github.com/satnaing/astro-paper), created by [Sat Naing](https://satnaing.dev) and its [contributors](https://github.com/satnaing/astro-paper/graphs/contributors).

AstroPaper is licensed under the MIT License. The original license and copyright notices are preserved in this repository.
