---
layout: single
classes: wide
title: Byte-sized RSE
permalink: /events/byte-sized-rse/
author_profile: false
sidebar:
  nav: "uhpc_menu"
---

Byte-sized RSE is a series of events providing key research software skills in 
just 1 hour!

Run by the UNIVERSE-HPC project, the byte-sized RSE series began in October 2022.

Each session has a companion podcast episode in the [Code for Thought](https://codeforthought.buzzsprout.com/) 
podcast series.

See below for details of upcoming sessions and links to podcasts and other 
outputs from previous byte-sized RSE sessions.

For any questions related to the series, or if you'd like to run a session on a 
topic that we've not yet covered, you can get in touch with 
[Jeremy Cohen](https://www.imperial.ac.uk/people/jeremy.cohen) or 
[Steve Crouch](https://www.software.ac.uk/our-people/steve-crouch).

{% assign current_date = site.time | date: '%s' %}
{% assign mention_future = "no" %}
{% assign mention_previous = "no" %}
{% assign sorted_episodes = site.bytesized_rse | reverse %}
{% for episode in sorted_episodes %}

  {% assign post_date = episode.date | date: '%s' %}
  {% if mention_future == "no" and post_date >= current_date %}
  <div>
    <h2>Future Byte-sized RSE events</h2>
  </div>
  {% assign mention_future = "yes" %}
  {% elsif mention_previous == "no" and post_date < current_date %}
  <div>
    <h2>Past Byte-sized RSE events</h2>
  </div>
  {% assign mention_previous = "yes" %}
  {% endif %}

  <div>

    <div class="archive__item-teaser" style="margin-right: 15px; float: right;">
      {% if episode.image and episode.image != "" %}
        <img src="{{ site.baseurl }}{{ episode.image }}"
      {% else %}
        <img src="{{ site.baseurl }}/assets/images/team/profile_placeholder.png"
      {% endif %}
            style="width: 400px; max-height: 300px; margin-left: 15px;">
      {% if episode.image_caption %}
        <span class="archive__item-caption">{{ episode.image_caption | markdownify | remove: "<p>" | remove: "</p>" }}</span>
      {% endif %}
    </div>

    <p style="font-size: 0.9em; margin-bottom: 10px;">
      <strong>
        {% if episode.series %}
          Series {{ episode.series }},
        {% endif %}
        {% if episode.episode %}
          Episode {{ episode.episode }}:
        {% endif %}
        {% if episode.title %}
          {{ episode.title }}
        {% endif %}
      </strong>
    </p>
    <p style="font-size: 0.7em; margin-bottom: 0;"><strong>Date: </strong>{{ episode.date | date: "%A %e %B, %Y &nbsp;" }}{{ episode.time-range }}</p>
    <p style="font-size: 0.7em; margin-bottom: 0;"><strong>Instructors: </strong>{{ episode.instructors }}</p>
    <p style="font-size: 0.7em; margin-bottom: 0;"><strong>Links: </strong>
      {% if episode.slides %}
        <a href="{{ episode.slides }}">Slides</a>{% if episode.podcast %},{% endif%}
      {% endif %}
      {% if episode.podcast %}
        <a href="{{ episode.podcast }}">Code for Thought podcast</a>
      {% endif %}
    </p>

    <div style="font-size: 0.7em;">
      <p>{{ episode.content | markdownify }}</p>
    </div>
    <div style="clear: both;"></div>
    <hr>

  </div>

{% endfor %}
