---
layout: page
title: People
permalink: /people/
tags: people
---

# Our Team

## Faculty

{% for person in site.people %}
{% if person.position contains "Professor" %}

{% if person.image %}
![{{ person.name }}]({{ site.url }}{{ person.image }}){: .profile-image}
{% endif %}

### {{ person.name }}
{{ person.position }}  
{{ person.department }}  
{{ person.university }}

{% for affiliation in person.affiliations %}
{{ affiliation }}
{% endfor %}

- **Research interests:** {{ person.research_interests | join: ", " }}
- **Email:** {{ person.email }}
- [Google Scholar]({{ person.google_scholar }})
- [Personal Website]({{ person.personal_website }})

{% endif %}
{% endfor %}

## PhD Students

{% for person in site.people %}
{% if person.position contains "PhD" %}

{% if person.image %}
![{{ person.name }}]({{ site.url }}{{ person.image }}){: .profile-image}
{% endif %}

### {{ person.name }}
{{ person.position }} ({{ person.start_date }})
- **Research focus:** {{ person.research_focus | join: ", " }}
- **Email:** {{ person.email }}

{% endif %}
{% endfor %}

## MSc Students

{% for person in site.people %}
{% if person.position contains "MSc" %}
### {{ person.name }}
{{ person.position }} ({{ person.start_date }})
{% if person.research_focus %}
- **Research focus:** {{ person.research_focus | join: ", " }}
{% endif %}
- **Email:** {{ person.email }}

{% endif %}
{% endfor %}

## Visiting Students / Interns

{% for person in site.people %}
{% if person.position contains "Visiting" or person.position contains "Intern" %}
### {{ person.name }}
({{ person.start_date }} — {{ person.end_date }})

{% endif %}
{% endfor %}

---

Interested in joining our team? Please submit your application via the [Mila application process](https://mila.quebec/en/cours/admission-2/). Unfortunately, we are unable to respond to individual emails.