---
# We don't even need 'layout: default' anymore, 
# because _config.yml handles it!
---

# Lab Members

---
## Principal Investigator

{% comment %}
This loops through all files in _people 
and finds anyone with the title "Principal Investigator"
{% endcomment %}

{% assign members = site.people | where: "title", "Principal Investigator" %}
{% for person in members %}
  <a href="{{ person.url | relative_url }}" style="text-decoration: none; color: inherit;">
    <div style="display: inline-block; width: 30%; text-align: center; vertical-align: top; padding: 15px;">
      <img src="{{ person.image_path | relative_url }}" alt="Photo of {{ person.name }}" style="width:200px; height:200px; object-fit: cover; border-radius: 50%;">
      <br>
      <b>{{ person.name }}</b>
      <br>
      {{ person.title }}
    </div>
  </a>
{% endfor %}

---
## Researchers

{% comment %}
This loops through and finds all "PhD Student" members
{% endcomment %}

{% assign members = site.people | where: "title", "Researcher" %}
{% for person in members %}
  <a href="{{ person.url | relative_url }}" style="text-decoration: none; color: inherit;">
    <div style="display: inline-block; width: 30%; text-align: center; vertical-align: top; padding: 15px;">
      <img src="{{ person.image_path | relative_url }}" alt="Photo of {{ person.name }}" style="width:200px; height:200px; object-fit: cover; border-radius: 50%;">
      <br>
      <b>{{ person.name }}</b>
      <br>
      {{ person.title }}
    </div>
  </a>
{% endfor %}
---
## PhD Students

{% comment %}
This loops through and finds all "PhD Student" members
{% endcomment %}

{% assign members = site.people | where: "title", "PhD Student" %}
{% for person in members %}
  <a href="{{ person.url | relative_url }}" style="text-decoration: none; color: inherit;">
    <div style="display: inline-block; width: 30%; text-align: center; vertical-align: top; padding: 15px;">
      <img src="{{ person.image_path | relative_url }}" alt="Photo of {{ person.name }}" style="width:200px; height:200px; object-fit: cover; border-radius: 50%;">
      <br>
      <b>{{ person.name }}</b>
      <br>
      {{ person.title }}
    </div>
  </a>
{% endfor %}

---
## Alumni
* (You can still add alumni manually here, or create a 'Alumni' title for them)
