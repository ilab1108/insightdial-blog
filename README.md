# Insight Dial blog posts

Articles for https://insightdial.com/blog. Each file in `posts/` is one article as JSON (data only, never code).
An hourly cron job on the website (`cron_blog_sync.php`) downloads new or changed files, cleans the HTML and publishes them.

## Format (`posts/<slug>.json`)

```json
{
  "slug": "lowercase-words-with-hyphens",
  "title": "SEO title, max 55 characters (site appends | Insight Dial)",
  "h1": "On-page heading in sentence case",
  "description": "Meta description, 120-155 characters",
  "date": "YYYY-MM-DD",
  "minutes": 5,
  "faq": [["Question 1", "Answer 1"], ["Question 2", "Answer 2"], ["Question 3", "Answer 3"]],
  "body": "<p>HTML using only p, h2, h3, ul, ol, li, strong, em, a. Links: relative (/features) or https.</p>"
}
```

The file name must be `<slug>.json` and match the `slug` field. To unpublish, change the file; deleting a file here does not remove it from the site.
