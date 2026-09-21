---
name: openhandle-instagram-profile-and-posts
description: Read a public Instagram account's profile, its recent posts, and the comments on a post through the Openhandle API, in one normalized schema with a capture time and source on every answer.
api: Openhandle API
operations:
- instagramProfileGet
- instagramProfilePostsList
- instagramPostCommentsList
---

# Get Instagram profile data and posts

Read any public Instagram account with the Openhandle API. Start on a Test key
(`oh_test_`) against synthetic data at $0.000, then switch to a Live key
(`oh_live_`) for real data. Send the key as `Authorization: Bearer <key>` on every
request; keep it on the server.

## Steps

1. **Fetch the profile** — `instagramProfileGet`
   `GET /v1/instagram/profiles/{identifier}` where `{identifier}` is a handle
   (`@northstar_forge_test`), a numeric ID, or a profile URL. The envelope returns
   `data` with followers, bio, verification, and metrics; store `data.id` — IDs are
   stable, handles change.
2. **List recent posts** — `instagramProfilePostsList`
   `GET /v1/instagram/profiles/{identifier}/posts`. One page per request; follow
   `meta.cursors.next` as the `cursor` parameter. Pass `since` (RFC 3339) to stop
   paging at a point in time and avoid paying for pages you would discard.
3. **Read comments on a post** — `instagramPostCommentsList`
   `GET /v1/instagram/posts/{identifier}/comments`. One page of author, text, and
   likes, with its own cursor. A cursor is bound to its request — reusing it
   elsewhere returns `CURSOR_MISMATCH`.

## Rules

- Every page is one billable request; 30-day cache hits are free, failed requests
  are free. Choose freshness per request: `live`, `24h`, `7d`, or `30d`.
- Nulls mean the platform did not supply the field (hidden likes stay `null`, never
  0). A private account returns `PROFILE_PRIVATE` (403, billable, no data).
- Branch on `error.code`, not the message; retry only when `retryable` is true,
  honoring `Retry-After` on `RATE_LIMITED` (429).
