# Front Matter Template

Complete template with all fields:

```yaml
---
title: "Post Title"
date: 2026-02-24 09:00:00 +0000
description: "Short summary of the post (shows in previews and SEO)"
categories: [Technology, AI, Software Development]
tags: ["coding-agents", "developer-experience", "automation"]
type: post
weight: 30
showTableOfContents: true
image: "/images/posts/optional-cover.png"
---
```

## Field notes

- **title:** Use double quotes. Title case.
- **date:** Always include timezone offset (see `blog-config.md` for your timezone). Use the publication time from your config.
- **description:** One sentence. Shows in link previews and search results.
- **categories:** Title case, no quotes. Common values: `Technology`, `AI`, `Software Development`, `Open Source`.
- **tags:** Lowercase, hyphenated, in double quotes. Keep to 3-6 tags.
- **type:** Always `post` for blog posts.
- **weight:** Use the value from `blog-config.md` if your theme uses it for ordering.
- **showTableOfContents:** Set to `true` for posts with 3+ sections.
- **image:** Optional. Path relative to `static/`. Used as cover image.
