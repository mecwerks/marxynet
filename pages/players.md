---
layout: default
permalink: players
title: Players
---
{% assign players = site.data.players | sort_natural: 'Name' %}
{% assign len = players | size | minus: 1 %}
{% assign halfLen = players | size | divided_by: 2 | ceil | minus: 1 %}
<div>
<table id="playerList" class="halfTable" style="float: left">
    {% for i in (0..halfLen) %}
        <tr>
            <th style="text-align: center"><a href="/players/{{players[i].UID}}">{{players[i].Name}}</a></th>
        </tr>
    {% endfor %}
</table>
</div>
{% assign halfLen = halfLen | plus: 1 %}
<div>
<table id="playerList2" class="halfTable">
    {% for i in (halfLen..len) %}
        <tr>
            <th style="text-align: center"><a href="/players/{{players[i].UID}}">{{players[i].Name}}</a></th>
        </tr>
    {% endfor %}
</table>
</div>

<script>

</script>