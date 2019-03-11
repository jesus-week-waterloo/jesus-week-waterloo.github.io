---
title: Fellowships
date: 2019-03-09 00:00 -0500
layout: page
---

<div class="tabber">
    <div class="tabber-tabbar">
        <a class="tabber-tab" data-active aria-controls="uwaterloo" href="#uwaterloo">UWaterloo</a>
        <a class="tabber-tab" aria-controls="wlu" href="#wlu">Wilfred Laurier</a>
    </div>
    <div class="tabber-tabs">
        <div class="tabber-section" id="uwaterloo">
            {% for felly in site.data.fellowships.UWaterloo %}
            <h2>{{ felly[0] }}</h2>
            <p>{{ felly[1].Meetings.Time }} <span class="slash-sep">//</span> {{ felly[1].Meetings.Location }}</p>
            {% for link in felly[1].Links %}
            <p>
            {% if link.Type == "Facebook" %}
                {% include icons/facebook-square.svg %}
            {% else %}
                {% include icons/link.svg %}
            {% endif %}
                <a class="raw" href="{{ link.URL }}" rel="noreferrer">{{ link.URL }}</a></p>
            {% endfor %}
            <hr>
            {% endfor %}
        </div>
        <div class="tabber-section" id="wlu">
            {% for felly in site.data.fellowships.WLU %}
            <h2>{{ felly[0] }}</h2>
            <p>{{ felly[1].Meetings.Time }} <span class="slash-sep">//</span> {{ felly[1].Meetings.Location }}</p>
            {% for link in felly[1].Links %}
            {% if link.Type == "Facebook" %}
                {% include icons/facebook-square.svg %}
            {% else %}
                {% include icons/link.svg %}
            {% endif %}
                <a class="raw" href="{{ link.URL }}" rel="noreferrer">{{ link.URL }}</a>
            {% endfor %}
            <hr>
            {% endfor %}
        </div>
    </div>
</div>
