---
layout: single
classes: wide
title: UNIVERSE-HPC Events
permalink: /events/
author_profile: false
sidebar:
  nav: "uhpc_menu"

---

{% assign current_date = site.time | date: '%s' %}
{% assign mention_future = "no" %}
{% assign mention_previous = "no" %}
{% assign sorted_events = site.events | reverse %}

Here we provide details of upcoming and past UNIVERSE-HPC project events.

You can find details of our monthly Byte-sized RSE sessions on the separate
[Byte-sized RSE page]({{ site.baseurl}}/events/byte-sized-rse/).

These are the [External Events]({{ site.baseurl}}/events/external-events) we have been participating in.

{% comment %}
Put a placeholder for future events if there are none in the system.
Get a date of the first event and if it's before the current date, we
show that there are no future events.
{% endcomment %}

{% if sorted_events.size > 0 %}
  {% assign first_event_date = sorted_events[0].date | date: '%s' %}
{% else %}
  {% assign first_event_date = "2000-01-01 00:00" | date: '%s' %}
{% endif %}

{% if first_event_date < current_date %}
  <div>
    <h2>Upcoming UNIVERSE-HPC events</h2>
<div class="notice notice--info">
<strong>No upcoming events:</strong> We currently have no planned events. We'll be running more events in the coming months so check back again soon to see what's coming up.
</div>
  </div>
{% endif %}

{% for event in sorted_events %}

  {% assign event_date = event.date | date: '%s' %}
  {% if mention_future == "no" and event_date >= current_date %}
  <div>
    <h2>Upcoming UNIVERSE-HPC events</h2>
  </div>
  {% assign mention_future = "yes" %}
  {% elsif mention_previous == "no" and event_date < current_date %}
  <div>
    <h2>Past UNIVERSE-HPC events</h2>
  </div>
  {% assign mention_previous = "yes" %}
  {% endif %}

  <div>
    {% comment %}
    IMAGES: Aim for images with a 640 pixel width (or a multiple)
    {% endcomment %}

    <div class="archive__item-teaser" style="margin-right: 15px; float: right;">
      {% if event.event_page and event.event_page != "" %}
            <a href="{{ site.baseurl }}/events/{{ event.event_page }}" rel="noopener noreferrer">
      {% endif %}
      
      {% if event.image and event.image != "" %}
        <img src="{{ site.baseurl }}{{ event.image }}"
      {% else %}
        <img src="{{ site.baseurl }}/assets/images/events/event_placeholder.png"
      {% endif %}
            style="width: 400px; max-height: 300px; margin-left: 15px;">
            {% if event.event_page and event.event_page != "" %}
              </a>
            {% endif %}
      {% if event.image_caption %}
        <span class="archive__item-caption">{{ event.image_caption | markdownify | remove: "<p>" | remove: "</p>" }}</span>
      {% endif %}
    </div>

    <p style="font-size: 0.9em; margin-bottom: 10px;">
      <strong>
        {% if event.title %}
          {% if event.event_page and event.event_page != "" %}
            <a href="{{ site.baseurl }}/events/{{ event.event_page }}" rel="noopener noreferrer" style="color: #aaa; text-decoration: none;">{{ event.title }}</a>
          {% else %}
            {{ event.title }}
          {% endif %}
        {% endif %}
      </strong>
    </p>
    <p style="font-size: 0.7em; margin-bottom: 0;"><strong>Speaker: </strong>
        {{ event.speaker }}{% if event.affiliation and event.affiliation != "" %}, {{ event.affiliation }}{% endif %}
    </p>
    <p style="font-size: 0.7em; margin-bottom: 0;"><strong>Date: </strong>{{ event.date | date: "%A %e %B %Y" }},
        {% if event.time-range-link and event.time-range-link != "" %}
          <a href="{{ event.time-range-link }}" target="_blank" rel="noopener noreferrer">{{ event.time-range }}</a>
        {% else %}
          {{ event.time-range }}
        {% endif %}
    </p>
    
    <p style="font-size: 0.7em; margin-bottom: 0;"><strong>Links: </strong>
      <ul style="font-size: 0.7em; margin: 0 auto;">
      {% if event.event_page and event.event_page != "" %}
            <li style="font-size: 0.9em; margin-bottom: 0;"><a href="{{ site.baseurl }}/events/{{ event.event_page }}" rel="noopener noreferrer">Further event information</a></li>
      {% endif %}
      {% if event.slides and event.slides != "" %}
        <li style="font-size: 0.9em; margin-bottom: 0;">Slides: <a href="{{ event.slides }}" target="_blank" rel="noopener noreferrer">Slides </a></li>
      {% endif %}
      {% if event.video and event.video != "" %}
        <li style="font-size: 0.9em; margin-bottom: 0;">Video: <a href="{{ event.video }}" target="_blank" rel="noopener noreferrer">Video</a></li>
      {% endif %}
      </ul>
    </p>

    <div style="font-size: 0.7em; color: #ccc;">
      <p>{{ event.overview | markdownify }}</p>
    </div>
    <div style="clear: both;"></div>
    <hr>

  </div>

{% endfor %}









