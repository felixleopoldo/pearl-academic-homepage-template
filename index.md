---
layout: default
title: Home
---

<section class="intro">
  <p>Welcome to my homepage. Here you can find out what I am up to — new submissions, working papers, talks, and projects.</p>
</section>

<section class="current-position">
  <h2>Current Position</h2>
  <p>
    <strong>{{ site.author.position }}</strong> at
    {% if site.author.affiliation_url %}
      <a href="{{ site.author.affiliation_url }}" target="_blank" rel="noopener">{{ site.author.affiliation }}</a>.
    {% else %}
      {{ site.author.affiliation }}.
    {% endif %}
  </p>
</section>

<section class="research-interests">
  <h2>Research Interests</h2>
  <p>
    [Replace this with a short paragraph describing your research interests — the questions, methods,
    and topics you work on. Link to a project or collaborator's page where relevant.]
  </p>
</section>

{% if site.news %}
<section class="news">
  <h2>News</h2>
  <ul>
    {% for item in site.news %}
      <li><span class="news-date">{{ item.date | date: "%b %Y" }}</span>{{ item.text }}</li>
    {% endfor %}
  </ul>
</section>
{% endif %}

{% if site.reviewer_for %}
<section class="reviewer-for">
  <h2>Reviewer For</h2>
  <ul>
    {% for item in site.reviewer_for %}
      <li><a href="{{ item.url }}" target="_blank" rel="noopener">{{ item.name }}</a></li>
    {% endfor %}
  </ul>
</section>
{% endif %}
