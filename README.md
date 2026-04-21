# Adding projects to your portfolio

All projects live as folders in this `projects/` directory.
Example structure:

```
projects/
  costa-studio/
    cover.jpg          (shown on the card)
    01.jpg             (shown in lightbox)
    02.jpg
    reel.mp4           (optional video)
    case-study.html    (optional full HTML case study)
```

Then open `Mazen Costa Portfolio.html`, find the `PROJECTS` array at the
top of the `<script>` block, and add one entry:

```js
{
  id: "costa-studio",
  title: "Costa Studio",
  category: "branding",        // branding | design | motion | illustration
  frame: "Brand Identity 2026",
  description: "Complete brand refresh with identity system",
  cover: "projects/costa-studio/cover.jpg",
  featured: true,              // optional — shows large at top of section
  tags: ["Identity", "Print", "Digital"],
  year: "2026",
  client: "Costa Studio",
  role: "Art Direction & Design",
  media: [
    { type: "image", src: "projects/costa-studio/01.jpg" },
    { type: "image", src: "projects/costa-studio/02.jpg" },
    { type: "video", src: "projects/costa-studio/reel.mp4" },
    { type: "youtube", id: "dQw4w9WgXcQ" },
    { type: "vimeo", id: "123456789" },
    { type: "html", src: "projects/costa-studio/case-study.html" }
  ],
  links: [
    { label: "Live site", href: "https://example.com" },
    { label: "Behance", href: "https://behance.net/..." }
  ]
}
```

**Media types supported:**
- `image` — any image format (jpg, png, webp, gif)
- `video` — local .mp4 (or any HTML5 video)
- `youtube` — pass the video `id`
- `vimeo` — pass the video `id`
- `html` — full HTML case study, opens in iframe inside the lightbox

That's it. Refresh the page and your new project shows up in the right
category automatically.
