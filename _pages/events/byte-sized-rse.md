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
{% assign mention_previous = "no" %}
{% assign sorted_episodes = site.bytesized_rse | reverse %}
{% for episode in sorted_episodes %}

  <div>
    {% assign post_date = episode.date | date: '%s' %}
    {% if mention_previous == "no" and post_date < current_date %}
        <h2>Past Byte-sized RSE events</h2>
        {% assign mention_previous = "yes" %}
    {% endif %}

    {% if episode.image and episode.image != "" %}
      <img src="{{ site.baseurl }}{{ episode.image }}"
    {% else %}
      <img src="{{ site.baseurl }}/assets/images/team/profile_placeholder.png"
    {% endif %}
          style="border-radius: 50%;
                 float: right;
                 width: 300px;
                 margin-left: 15px;
                 margin-right: 15px;
                 margin-bottom: 10px;">
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
        <a href="{{ episode.slides }}">Slides</a>,
      {% endif %}
      {% if episode.podcast %}
        <a href="{{ episode.podcast }}">Code for Thought podcast</a>
      {% endif %}
    </p>

    <div style="font-size: 0.7em;">
      <p>{{ episode.content | markdownify }}</p>
    </div>
    <div style="clear: both;"></div>
  </div>
  <hr/>

{% endfor %}
