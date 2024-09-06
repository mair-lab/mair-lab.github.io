---
layout: page
title: People
permalink: /people/
tags: people
---

# Our Team

## Faculty

<div id="faculty-members" markdown="1">
{% for person in site.people %}
{% if person.position contains "Professor" %}
<div class="faculty-card" markdown="1">

{% if person.image %}
![{{ person.name }}]({{ site.baseurl }}{{ person.image }}){: .profile-image}
{% endif %}

**{{ person.name }}**  
{{ person.position }}  
{{ person.department }}  
{{ person.university }}

{% for affiliation in person.affiliations %}
{{ affiliation }}
{% endfor %}

**Research interests:** {{ person.research_interests | join: ", " }}

[<i class="fas fa-envelope"></i>](mailto:{{ person.email }} "Email") 
[<i class="ai ai-google-scholar"></i>]({{ person.google_scholar }} "Google Scholar")
[<i class="fas fa-globe"></i>]({{ person.personal_website }} "Personal Website")

</div>
{% endif %}
{% endfor %}
</div>

## PhD Students

<div id="phd-students" markdown="1">

{% for person in site.people %}
{% if person.position contains "PhD" %}
<div class="phd-student" markdown="1">

{% if person.image %}
![{{ person.name }}]({{ site.baseurl }}{{ person.image }}){: .profile-image}
{% endif %}

**{{ person.name }}**  
{{ person.position }} ({{ person.start_date }})  
{{ person.research_focus | join: ", " }}  
[<i class="fas fa-envelope"></i>](mailto:{{ person.email }} "Email") {% if person.google_scholar %}[<i class="ai ai-google-scholar"></i>]({{ person.google_scholar }} "Google Scholar"){% endif %}

</div>
{% endif %}
{% endfor %}

</div>

## MSc Students

<div id="msc-students" markdown="1">

{% for person in site.people %}
{% if person.position contains "MSc" %}
<div class="msc-student" markdown="1">

{% if person.image %}
![{{ person.name }}]({{ site.baseurl }}{{ person.image }}){: .profile-image}
{% endif %}

**{{ person.name }}**  
{{ person.position }} ({{ person.start_date }})  
{% if person.research_focus %}
{{ person.research_focus | join: ", " }}  
{% endif %}
[<i class="fas fa-envelope"></i>](mailto:{{ person.email }} "Email") {% if person.google_scholar %}[<i class="ai ai-google-scholar"></i>]({{ person.google_scholar }} "Google Scholar"){% endif %}

</div>
{% endif %}
{% endfor %}

</div>

## Visiting Students / Interns

<div id="visiting-students" markdown="1">

{% for person in site.people %}
{% if person.position contains "Visiting" %}
<div class="visiting-student" markdown="1">

{% if person.image %}
![{{ person.name }}]({{ site.baseurl }}{{ person.image }}){: .profile-image}
{% endif %}

**{{ person.name }}**  
{{ person.position }} ({{ person.start_date }})  
{% if person.research_focus %}
{{ person.research_focus | join: ", " }}  
{% endif %}
[<i class="fas fa-envelope"></i>](mailto:{{ person.email }} "Email") {% if person.google_scholar %}[<i class="ai ai-google-scholar"></i>]({{ person.google_scholar }} "Google Scholar"){% endif %}

</div>
{% endif %}
{% endfor %}

</div>

---

Interested in joining our team? Please submit your application via the [Mila application process](https://mila.quebec/en/prospective-students-postdocs/research-internships). Unfortunately, we are unable to respond to individual emails.