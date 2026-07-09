# Adding Publications

Edit `publications-data.js` to add, remove, or reorder publications.

Put newest items first. The first visible item becomes the large featured item on the Publications page. The category buttons filter by the `type` field.

Use one of these type values:

- `analysis`
- `policy-paper`
- `institutional-note`

Example:

```js
{
  type: "analysis",
  label: "Analysis",
  title: "Article title",
  description: "One short sentence describing the piece.",
  source: "Publication Name",
  date: "June 1, 2026",
  topics: ["Finance", "Reconstruction"],
  image: "assets/my-image.jpg",
  imageAlt: "Short image description",
  url: "https://example.com/article",
  external: true
}
```

For images you upload yourself, place the image in the `assets` folder and use a relative path like `assets/my-image.jpg`.
