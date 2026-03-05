# Platform Reference Guide

Quick-reference for platform constraints, best practices, and author-specific details.

## Twitter/X

### Character Limits
- **Single tweet:** 280 characters (including spaces and links)
- **Links:** URLs count as 23 characters regardless of actual length (t.co wrapping)
- **Media:** images, GIFs, and polls don't count toward character limit
- **Thread:** no limit on number of tweets, but 3-5 is the sweet spot for engagement

### Thread Best Practices
- **Hook tweet:** the most important tweet. If it doesn't stop the scroll, the thread dies.
- **Number tweets:** use `1/` `2/` format (not `1/5` — it locks you in and looks less casual)
- **Each tweet should standalone:** if someone sees only one tweet from the thread, it should still make sense
- **End with a CTA:** link to the post, ask a question, or invite replies
- **Self-reply structure:** post tweet 1, then reply to it with tweet 2, etc.
- **Optimal length:** 3-5 tweets. Beyond 5, engagement drops unless each tweet is genuinely valuable.

### Articles (Premium)
- **Available with Twitter Premium.** Articles are long-form posts published natively on the platform.
- **Rich formatting:** headings, bold, italic, code blocks, images, and embedded tweets are all supported
- **Length:** no hard character limit, but 500-1000 words is the sweet spot for blog promotion. Distill the blog post, don't replicate it.
- **Discovery:** articles appear in followers' timelines like regular tweets. They also have their own permalink you can share.
- **Pair with a hook tweet:** publish the article, then tweet a one-liner that links to it. The hook tweet drives initial engagement; the article provides depth.
- **Use articles when:** the post is too nuanced for a thread, or when code formatting matters (threads mangle code blocks, articles render them properly)
- **Don't use articles when:** a single tweet or short thread is sufficient. Not every post needs an article.

### Hashtag Conventions
- **2-3 hashtags max** per tweet (more looks spammy)
- Place at the **end** of the tweet, not inline
- Use established community hashtags relevant to your content area (see `blog-config.md` for your hashtags)
- Avoid generic hashtags: `#coding`, `#tech`, `#programming` (too broad, no community)
- For threads: hashtags only on the **last tweet**

### Tone
- Conversational, opinionated, first-person
- Short sentences. Line breaks between ideas.
- Bold claims and questions perform well
- Avoid corporate-speak and PR language
- Tag relevant accounts when genuinely relevant (not for attention)

## LinkedIn

### Character Limits
- **Post body:** 3,000 characters max
- **Sweet spot:** 800-1,300 characters (enough for substance, short enough to not lose readers)
- **"See more" cutoff:** approximately 210 characters — the first ~2 lines are all most people see
- **Comments:** 1,250 characters max

### Formatting Tips
- **Line breaks are your friend:** LinkedIn's algorithm and readers both reward whitespace
- **One idea per paragraph** — keep paragraphs to 1-3 sentences
- **No bold/italic support** in regular posts (only in articles)
- **Lists:** use line breaks + dashes or bullet characters, not numbered lists (they look dense)
- **Links:** place the link near the end — LinkedIn deprioritizes posts with links (the algorithm prefers native content), but the link is the whole point for blog promotion

### Algorithm Insights
- **First line is everything:** it's the only thing visible before "see more". Make it a hook.
- **Engagement in the first hour** determines reach — post when your audience is active
- **Comments > reactions:** posts that generate conversation get pushed to more feeds
- **Personal stories outperform announcements:** "I learned X" beats "X is now available"
- **Native content > links:** LinkedIn deprioritizes link posts. Consider putting the link in a comment instead of the post body (mention "link in comments"). However, for blog promotion, a link in the post is acceptable — just make the surrounding content strong enough to earn engagement despite the penalty.
- **Tagging people:** tag colleagues, projects, or companies when relevant. It increases visibility and shows community connection.

### Hashtag Conventions
- **3-5 hashtags** at the bottom of the post, on a separate line
- Never inline (e.g., "I love #Golang" — no)
- Use a mix of broad and specific hashtags from `blog-config.md`
- Capitalize each word for readability: `#SoftwareTesting` not `#softwaretesting`

### Tone
- Professional but personal — not stiff, not casual
- Share the *why* behind the post — what motivated you to write it
- "I" statements drive engagement: "I was wrong about X", "I learned X the hard way"
- Avoid: jargon without context, humble-bragging, engagement bait ("Agree?")

## Author Social Handles and Tags

Social handles, accounts to tag, and hashtags are configured in `blog-config.md` in the blog repo root. Read that file for the author's specific handles and tagging preferences. If the config file does not exist, use `AskUserQuestion` to ask the author for their handles before generating drafts.

## Tone Reference: Examples from Similar Technical Blogs

These examples illustrate the target tone — opinionated, practical, first-person:

**Twitter thread hook (technical):**
> I mass-migrated 60 Go modules to a new CI pipeline in one afternoon.
>
> An AI agent did the repetitive work. I reviewed and merged. Here's the workflow.

**Twitter single tweet (opinion):**
> The best test isn't the one with 100% coverage. It's the one that caught the bug your mock never would have.

**LinkedIn hook (storytelling):**
> Last month I mass-migrated 60 Go modules from an internal CI to GitHub Actions. It took an afternoon — and I didn't write a single workflow file by hand.

**LinkedIn hook (lesson learned):**
> I spent 3 hours debugging a query that an AI agent wrote in 30 seconds. That's when I changed my testing strategy.

These are illustrative — adapt the voice to the specific post content.
