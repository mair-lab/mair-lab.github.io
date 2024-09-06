---
layout: page
title: Research
permalink: /research/
tags: research
---

<style>
.talks-section {
  display: grid;
  grid-template-columns: repeat(auto-fit, minmax(300px, 1fr));
  gap: 20px;
  margin-top: 30px;
  margin-bottom: 30px;
}
.talk {
  border: 1px solid #e0e0e0;
  border-radius: 8px;
  overflow: hidden;
}
.talk-video {
  position: relative;
  padding-bottom: 56.25%; /* 16:9 aspect ratio */
  height: 0;
}
.talk-video iframe {
  position: absolute;
  top: 0;
  left: 0;
  width: 100%;
  height: 100%;
}
.talk-info {
  padding: 10px;
}
.talk-title {
  font-size: 1em;
  font-weight: bold;
  margin-bottom: 5px;
}
.talk-venue {
  font-size: 0.8em;
  color: #666;
}
.talk-links {
  margin-top: 5px;
  font-size: 0.8em;
}
.talk-links a {
  color: #0066cc;
  text-decoration: none;
  margin-right: 10px;
}
</style>

Our research interests lie at the intersection of Computer Vision, Deep Learning, and Natural Language Processing, with a focus on developing Artificial Intelligence (AI) systems that can 'see' (i.e., understand the contents of an image: who, what, where, doing what?) and 'talk' (i.e., communicate the understanding to humans in free-form natural language).

## Research Topics

Below are some example research topics that are of interest to me in the space of vision-language:

- Culturally aware and geo-diverse vision-language models
- Data-efficient adaptation to new tasks
- Robust automatic evaluation
- Visio-linguistic reasoning (fine-grained, compositional, knowledge-based, etc.)
- Generalization to out-of-distribution datasets

For more details, please check out my [latest talks](#recent-talks).

## Recent Talks

<div class="talks-section">
{% for talk in site.data.talks %}
  <div class="talk">
    <div class="talk-video">
      {% assign video_id = talk.video_url | split: "v=" | last | split: "&" | first %}
      <iframe src="https://www.youtube.com/embed/{{ video_id }}" frameborder="0" allow="autoplay; encrypted-media" allowfullscreen></iframe>
    </div>
    <div class="talk-info">
      <div class="talk-title">{{ talk.title }}</div>
      <div class="talk-venue">{{ talk.venue }} ({{ talk.date | date: "%b %Y" }})</div>
      <div class="talk-links">
        {% if talk.slides_url and talk.slides_url != "#" %}
          <a href="{{ talk.slides_url }}">Slides</a>
        {% endif %}
      </div>
    </div>
  </div>
{% endfor %}
</div>
