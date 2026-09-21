---
name: openhandle-tiktok-user-videos
description: Read a public TikTok creator's profile and videos with views, likes, comments, and shares through the Openhandle API, without the Research or Display API.
api: Openhandle API
operations:
- tiktokProfileGet
- tiktokProfilePostsList
- tiktokPostGet
---

# Get TikTok user videos

Read any public TikTok creator with the Openhandle API — no TikTok login, no
Research API application. Authenticate with `Authorization: Bearer <oh_ key>`;
start on a Test key against synthetic data.

## Steps

1. **Fetch the profile** — `tiktokProfileGet`
   `GET /v1/tiktok/profiles/{identifier}`. Followers, following, total likes, and
   video count come back as integers for any public account. Store `data.id`.
2. **List the creator's videos** — `tiktokProfilePostsList`
   `GET /v1/tiktok/profiles/{identifier}/posts`. One page per request; page with
   `meta.cursors.next` → `cursor`. Each post carries `metrics` (views, likes,
   comments, shares, and `metrics.downloads` where TikTok supplies it).
3. **Read one video in full** — `tiktokPostGet`
   `GET /v1/tiktok/posts/{identifier}`. Full metrics, media, and the author
   reference for a single video ID.

## Rules

- Every page is one billable request; failed requests and 30-day cache hits are
  free. Set freshness (`live`/`24h`/`7d`/`30d`) per request.
- Measured zeros stay `0`; a field the platform did not supply is `null`.
- Handle `error.code`: `POST_NOT_FOUND` (404), `RATE_LIMITED` (429, honor
  `Retry-After`), `UPSTREAM_SWITCHED` (409 — restart pagination from page one).
