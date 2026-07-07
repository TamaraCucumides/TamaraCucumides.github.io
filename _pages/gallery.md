---
layout: archive
title: "Gallery"
permalink: /gallery/
author_profile: true

# --- Edit the lists below to add/remove items ---
# For posters: `file` is the route to the PDF inside this repo (e.g. under /files/).
# For talks: `youtube_id` is the part after "v=" in a YouTube URL, used both for the
# link and to auto-generate a thumbnail preview (no need to upload one yourself).

posters:
  - title: "Poster title placeholder"
    venue: "DBDBD 2025"
    date: "2025"
    file: "/files/Poster-DBDBD2025.pdf"
  - title: "Poster title placeholder"
    venue: "DBDBD 2025"
    date: "2025"
    file: "/files/Poster-DBDBD2025.pdf"

talks:
  - title: "Talk title placeholder"
    venue: "Event name placeholder"
    date: "2026"
    youtube_id: "kMBvSbxKVNU"
  - title: "Talk title placeholder"
    venue: "Event name placeholder"
    date: "2026"
    youtube_id: "kMBvSbxKVNU"
---

<style>
.gallery-section { margin-bottom: 2.5em; }
.gallery-grid {
  display: grid;
  grid-template-columns: repeat(auto-fill, minmax(220px, 1fr));
  gap: 1.5em;
  margin-top: 1em;
}
.gallery-item {
  text-align: center;
}
.gallery-item a { text-decoration: none; }
.gallery-thumb {
  display: block;
  width: 100%;
  aspect-ratio: 16 / 9;
  object-fit: cover;
  border-radius: 6px;
  border: 1px solid rgba(0,0,0,0.1);
  margin-bottom: 0.5em;
}
.gallery-poster-icon {
  display: flex;
  align-items: center;
  justify-content: center;
  width: 100%;
  aspect-ratio: 16 / 9;
  border-radius: 6px;
  border: 1px solid rgba(0,0,0,0.1);
  background: rgba(0,0,0,0.03);
  font-size: 2.5em;
  margin-bottom: 0.5em;
}
.gallery-item .gallery-title { font-weight: 600; }
.gallery-item .gallery-meta { font-size: 0.9em; opacity: 0.75; margin: 0.2em 0 0; }
</style>

{% include base_path %}

Posters and talk recordings — click through for the full PDF or video.

## 🖼️ Posters

<div class="gallery-section">
<div class="gallery-grid">
{% for poster in page.posters %}
  <div class="gallery-item">
    <a href="{{ base_path }}{{ poster.file }}" target="_blank" rel="noopener">
      <div class="gallery-poster-icon">📄</div>
      <div class="gallery-title">{{ poster.title }}</div>
    </a>
    <p class="gallery-meta">{{ poster.venue }}{% if poster.date %}, {{ poster.date }}{% endif %}</p>
  </div>
{% endfor %}
</div>
</div>

## 🎥 Talks

<div class="gallery-section">
<div class="gallery-grid">
{% for talk in page.talks %}
  <div class="gallery-item">
    <a href="https://www.youtube.com/watch?v={{ talk.youtube_id }}" target="_blank" rel="noopener">
      <img class="gallery-thumb" src="https://img.youtube.com/vi/{{ talk.youtube_id }}/hqdefault.jpg" alt="{{ talk.title }} thumbnail">
      <div class="gallery-title">{{ talk.title }}</div>
    </a>
    <p class="gallery-meta">{{ talk.venue }}{% if talk.date %}, {{ talk.date }}{% endif %}</p>
  </div>
{% endfor %}
</div>
</div>
