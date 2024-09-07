---
layout: page
title: People
permalink: /people/
tags: people
---

## Faculty

<div id="faculty-members">
{% for person in site.people %}
{% if person.position contains "Professor" %}
<div class="faculty-member">
  <div class="faculty-image">
    {% if person.image %}
    <img src="{{ site.baseurl }}{{ person.image }}" alt="{{ person.name }}" class="profile-image">
    {% endif %}
  </div>
  <div class="faculty-info">
    <h3>{{ person.name }}</h3>
    <p class="position">{{ person.position }}</p>
    <p class="department">{{ person.department }}</p>
    <p class="university">{{ person.university }}</p>
    {% for affiliation in person.affiliations %}
    <p class="affiliations">{{ affiliation }}</p>
    {% endfor %}
    {% if person.research_interests %}
    <p class="research-interests"><strong>Research interests:</strong> {{ person.research_interests | join: ", " }}</p>
    {% endif %}
    <div class="faculty-links">
      <a href="mailto:{{ person.email }}" title="Email"><i class="fas fa-envelope"></i></a>
      <a href="{{ person.google_scholar }}" title="Google Scholar"><i class="ai ai-google-scholar"></i></a>
      <a href="{{ person.personal_website }}" title="Personal Website"><i class="fas fa-globe"></i></a>
    </div>
  </div>
</div>
{% endif %}
{% endfor %}
</div>

## PhD Students

<div id="phd-students">
{% for person in site.people %}
{% if person.position contains "PhD" %}
<div class="phd-student">
    {% if person.image %}
    <img src="{{ site.baseurl }}{{ person.image }}" alt="{{ person.name }}" class="profile-image">
    {% endif %}
    <div class="student-name">
        {{ person.name }}
        <span class="student-links">
            <a href="mailto:{{ person.email }}" title="Email"><i class="fas fa-envelope"></i></a>
            {% if person.google_scholar %}<a href="{{ person.google_scholar }}" title="Google Scholar"><i class="ai ai-google-scholar"></i></a>{% endif %}
        </span>
    </div>
    <p>{{ person.position }} ({{ person.start_date }})</p>
    <p>{{ person.research_focus | join: ", " }}</p>
</div>
{% endif %}
{% endfor %}
</div>

## MSc Students

<div id="msc-students">
{% for person in site.people %}
{% if person.position contains "MSc" %}
<div class="msc-student">
    {% if person.image %}
    <img src="{{ site.baseurl }}{{ person.image }}" alt="{{ person.name }}" class="profile-image">
    {% endif %}
    <div class="student-name">
        {{ person.name }}
        <span class="student-links">
            <a href="mailto:{{ person.email }}" title="Email"><i class="fas fa-envelope"></i></a>
            {% if person.google_scholar %}<a href="{{ person.google_scholar }}" title="Google Scholar"><i class="ai ai-google-scholar"></i></a>{% endif %}
        </span>
    </div>
    <p>{{ person.position }} ({{ person.start_date }})</p>
    {% if person.research_focus %}<p>{{ person.research_focus | join: ", " }}</p>{% endif %}
</div>
{% endif %}
{% endfor %}
</div>

## Visiting Students / Interns

<div id="visiting-students">
{% for person in site.people %}
{% if person.position contains "Visiting" %}
<div class="visiting-student">
    {% if person.image %}
    <img src="{{ site.baseurl }}{{ person.image }}" alt="{{ person.name }}" class="profile-image">
    {% endif %}
    <div class="student-name">
        {{ person.name }}
        <span class="student-links">
            <a href="mailto:{{ person.email }}" title="Email"><i class="fas fa-envelope"></i></a>
            {% if person.google_scholar %}<a href="{{ person.google_scholar }}" title="Google Scholar"><i class="ai ai-google-scholar"></i></a>{% endif %}
        </span>
    </div>
    <p>{{ person.position }} ({{ person.start_date }})</p>
    {% if person.research_focus %}<p>{{ person.research_focus | join: ", " }}</p>{% endif %}
</div>
{% endif %}
{% endfor %}
</div>

---

Interested in joining our team? Please submit your application via the [Mila application process](https://mila.quebec/en/prospective-students-postdocs/research-internships). Unfortunately, we are unable to respond to individual emails.