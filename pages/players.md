---
layout: default
permalink: players
title: Players
---
{% assign players = site.data.players | sort_natural: 'Name' %}
{% assign len = players | size | minus: 1 %}
{% assign halfLen = players | size | divided_by: 2 | ceil %}
<div class="container">
    <div class="row">
        <table id="playerList" class="highlight col s4 offset-s2 ot1">
            {% for i in (0..halfLen) %}
                <tr>
                    <th style="text-align: center"><a href="/players/{{players[i].UID}}">{{players[i].Name}}</a></th>
                </tr>
            {% endfor %}
        </table>
        {% assign halfLen = halfLen | plus: 1 %}
        <table id="playerList2" class="highlight col s4 ot2">
            {% for i in (halfLen..len) %}
                <tr>
                    <th style="text-align: center"><a href="/players/{{players[i].UID}}">{{players[i].Name}}</a></th>
                </tr>
            {% endfor %}
        </table>
    </div>
</div>