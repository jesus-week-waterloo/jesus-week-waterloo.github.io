---
title: connect-fellys
date: 2019-03-09 00:00 -0500
layout: page
excerpt: none
lang: zh-hk
---

{% assign lang = page.lang | default: site.lang %}

{{ page.type }}
<div class="tabber">
    <div class="tabber-tabbar">
        <a class="tabber-tab" data-active aria-controls="uwaterloo" href="#uwaterloo">UWaterloo</a>
        <a class="tabber-tab" aria-controls="wlu" href="#wlu">Wilfrid Laurier</a>
    </div>
    <div class="tabber-tabs">
        <div class="tabber-section" id="uwaterloo">
            {% for felly in site.data.fellowships.UWaterloo %}
            <h2>{{ felly.name[lang] }}</h2>
            <p>{{ felly.meetings.time[lang] }} <span class="slash-sep">//</span> {{ felly.meetings.location }}</p>
            {% for link in felly.links %}
            {% if link.type == "Facebook" %}
                {% include icons/facebook-square.svg %}
            {% else %}
                {% include icons/link.svg %}
            {% endif %}
                <a class="raw" href="{{ link.URL }}" rel="noreferrer">{{ link.url }}</a>
            {% endfor %}
            <hr>
            {% endfor %}
        </div>
        <div class="tabber-section" id="wlu">
            {% for felly in site.data.fellowships.WLU %}
            <h2>{{ felly.name[lang] }}</h2>
            <p>{{ felly.meetings.time[lang] }} <span class="slash-sep">//</span> {{ felly.meetings.location }}</p>
            {% for link in felly.links %}
            {% if link.type == "Facebook" %}
                {% include icons/facebook-square.svg %}
            {% else %}
                {% include icons/link.svg %}
            {% endif %}
                <a class="raw" href="{{ link.URL }}" rel="noreferrer">{{ link.url }}</a>
            {% endfor %}
            <hr>
            {% endfor %}
        </div>
    </div>
</div>
