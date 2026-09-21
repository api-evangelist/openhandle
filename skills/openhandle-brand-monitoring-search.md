---
name: openhandle-brand-monitoring-search
description: Track brand or keyword mentions across X (Twitter) and TikTok, and find matching Instagram profiles, through the Openhandle API's search endpoints in one normalized schema.
api: Openhandle API
operations:
- twitterSearchPosts
- tiktokSearchPosts
- instagramSearchProfiles
---

# Monitor brand mentions across platforms

Search public posts and profiles across platforms with the Openhandle API to
watch a brand, campaign, or keyword. Authenticate with
`Authorization: Bearer <oh_ key>`; rehearse on a Test key first.

## Steps

1. **Search X (Twitter) posts** — `twitterSearchPosts`
   `GET /v1/twitter/search/posts?query=<term>`. Latest or top posts, one page per
   request, with author, text, and metrics (including `metrics.quotes`,
   `metrics.bookmarks`). Page with `meta.cursors.next` → `cursor`.
2. **Search TikTok posts** — `tiktokSearchPosts`
   `GET /v1/tiktok/search/posts?query=<term>`. Public videos with author, caption,
   and metrics, one page at a time.
3. **Find Instagram profiles** — `instagramSearchProfiles`
   `GET /v1/instagram/search/profiles?query=<term>` to resolve accounts behind a
   brand name before reading their profiles and posts.

## Rules

- Run searches on a schedule, store the returned IDs, and diff to detect new
  mentions — there is no webhook for public accounts you do not own.
- Every page is one billable request; 30-day cache hits and failed requests are
  free. Cursors are opaque and bound to their request (`CURSOR_MISMATCH`
  otherwise).
- Branch on `error.code`; honor `Retry-After` on `RATE_LIMITED` (429) and add
  jitter when several workers share a key.
