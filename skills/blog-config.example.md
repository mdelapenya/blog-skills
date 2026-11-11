# Blog Configuration

> Copy this file to `blog-config.md` in the same directory and fill in your values.
> `blog-config.md` is gitignored so your personal settings stay local.

## Blog

- **Domain:** example.com
- **Name:** My Blog
- **Hugo theme:** PaperMod
- **Blog repo path:** ~/path/to/your-blog-repo
- **Subscribe URL:** <domain>/<subscribe-url>

## Author

- **Name:** Your Name
- **GitHub username:** your-username

## Content Structure

- **Posts directory:** content/posts/
- **Talks directory:** content/talks/
- **Images directory:** static/images/posts/

## Publication Settings

- **Publication time:** 09:00:00
- **Timezone offset:** +0000
- **Deployment notes:** Posts go live after deploy. Adjust the time and timezone to match your deployment pipeline.

## Languages

Used by the blog-translator skill. Omit this whole section if your blog is
single-language.

- **Default language:** en
- **Additional languages:** es
- **Pairing mechanism:** translationKey
  (`translationKey` | `filename-suffix` | `content-dir`)
- **Translate slugs:** yes
- **Filename pattern:** `YYYY-MM-DD-<slug-in-that-language>.<lang>.md`
- **Write both languages on approval:** yes
  (when a draft is approved, blog-translator runs before the post is committed,
  so a post never lands in only one language)
- **Record source commit:** yes
  (each translation carries `translatedFrom: <short-sha>` so stale translations
  can be detected)
- **Language conventions file:** language-conventions.md in the blog repo root
  (copy from `skills/blog-translator/references/language-conventions.example.md`)

## Voice

Used by blog-writer, blog-editor and blog-translator to learn the blog's voice from the blog itself.

- **Voice reference posts:**
  (slugs, one list per language; leave blank to use the most recent posts
  originally written in the post's language. Posts with `translatedFrom` or
  `ai: true` are never used.)

## Front Matter Defaults

- **type:** post
- **weight:** (leave blank if your theme doesn't use it)

## Social Handles

Used by the blog-marketer skill when generating social media content.

- **Twitter/X handle:** @yourhandle
- **LinkedIn:** Your Name (linkedin.com/in/your-profile)
- **Accounts to tag:**
  - @relevant-project (Twitter/X), Project Name on LinkedIn
  - @another-account (Twitter/X)

## Topic Areas

Used by the blog-planner skill to suggest relevant new topics.

- Primary topics: (e.g., Go, containers, CI/CD)
- Communities: (e.g., CNCF, Go community, Docker community)
- Conferences: (e.g., GopherCon, KubeCon)

## Hashtags

Common hashtags for your content area. Used by the blog-marketer skill.

- Twitter/X: #topic1 #topic2 #topic3
- LinkedIn: #Topic1 #Topic2 #Topic3
