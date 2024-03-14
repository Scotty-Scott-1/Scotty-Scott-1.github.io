---
layout: page
permalink: /repositories/
title: About
description: What inspired this project?
nav: true
nav_order: 4
---

This is my portfolio project for my foundation year at Holberton. As it's it's such a large project I wanted to chose I subject that was personal to me, and, that also demostrates the technical skills that I have gained on my learning journey.

The first inspiration was that dating services are in high demand. I've noticed a trend that most people who use dating services, are very likes to be on multiple sites. So i wanted to add my own alternative to the market.

The second inspiration was that I have a lot of friends that are single and interested in dating services and I wanted to use my technical skills to help the people I know.

The third reason is that match making is very popular in my commomunity (south asian). Arranged marriages that curtural norm and almost everyone is looking for matches for their friends and family. I believe that this could be a way to serve my local commonunity.


## GitHub users

{% if site.data.repositories.github_users %}

<div class="repositories d-flex flex-wrap flex-md-row flex-column justify-content-between align-items-center">
  {% for user in site.data.repositories.github_users %}
    {% include repository/repo_user.liquid username=user %}
  {% endfor %}
</div>

---

{% if site.repo_trophies.enabled %}
{% for user in site.data.repositories.github_users %}
{% if site.data.repositories.github_users.size > 1 %}

  <h4>{{ user }}</h4>
  {% endif %}
  <div class="repositories d-flex flex-wrap flex-md-row flex-column justify-content-between align-items-center">
  {% include repository/repo_trophies.liquid username=user %}
  </div>

---

{% endfor %}
{% endif %}
{% endif %}

## GitHub Repositories

{% if site.data.repositories.github_repos %}

<div class="repositories d-flex flex-wrap flex-md-row flex-column justify-content-between align-items-center">
  {% for repo in site.data.repositories.github_repos %}
    {% include repository/repo.liquid repository=repo %}
  {% endfor %}
</div>
{% endif %}
