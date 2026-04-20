# Optima

**Best Practice** — an English tech blog focused on best practices in programming.

Content repository. Posts are published to [dev.to](https://dev.to) via GitHub Actions.

## Structure

- `posts/` — published and publish-ready articles (one `.md` per post)
- `assets/images/` — images referenced from posts
- `.github/workflows/` — publishing automation

## Writing a post

1. Copy `posts/_template.md` to `posts/your-slug.md`.
2. Fill in front matter. Keep `published: false` until ready.
3. Open a PR. Merge to `master` when approved.
4. CI publishes any post with `published: true` and writes back the dev.to article `id` so future edits update the same article.

## Front matter reference

| Field | Notes |
|---|---|
| `title` | Required. |
| `published` | `true` to publish, `false` to keep as draft on dev.to. |
| `description` | Short summary for previews. |
| `tags` | Max 4, lowercase, no spaces. |
| `cover_image` | Absolute URL. |
| `canonical_url` | Set if cross-posted from another source. |
| `series` | Group related posts. |
| `id` | Auto-written by CI. Do not edit. |

## Local setup

Requires a `DEV_TO_API_KEY` secret in the repo settings. Generate one at https://dev.to/settings/extensions.
