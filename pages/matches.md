---
layout: default
permalink: matches
title: Matches
---
<div align="center" class="matchresult">
    {% assign currentMonth = 13 %}
    {% assign newMonth = false %}
    {% assign matches = site.data.matches %}
    {% for match in matches %} 
    {% if match.TeamA.RoundsWon > match.TeamB.RoundsWon %} 
        {% assign scoreAClass = "scoreWinner"%} 
        {% assign scoreBClass = "scoreLoser" %} 
    {% elsif match.TeamA.RoundsWon < match.TeamB.RoundsWon%} 
        {% assign scoreAClass="scoreLoser" %} 
        {% assign scoreBClass="scoreWinner" %} 
    {% else %} 
        {% assign scoreAClass="scoreTie" %} 
        {% assign scoreBClass="scoreTie" %} 
    {% endif %} 

    {% assign monthString = match.Year | append: "-" | append: match.Month | append: "-" | append: match.Day | append: "T" | append: match.Hour | append: ":00:00" %}
    {% if match.Month < currentMonth %}
        {% unless currentMonth == 13 %}
            </table>
        {% endunless %}
        <table class="matchtable">
        <caption>{{monthString | date: "%B, %Y"}}</caption>
        {% assign currentMonth = match.Month %}
        {% assign newMonth = true %}
    {% endif %}
        <tr class='clickablerow' href='/matches/{{match.UID}}.html' id="matchrow">
            <td>
            {% assign d = monthString | date: "%-d" %}
            {% case d %}
            {% when "1" or "21" or "31" %}{{ d }}st
            {% when "2" or "22" %}{{ d }}nd
            {% when "3" or "23" %}{{ d }}rd
            {% else %}{{ d }}th
            {% endcase %} @ {{monthString | date: "%H"}}:00</td>
            <td style="text-align: right">{{match.TeamA.Name}}</td>
            <td style="text-align: center"><span class="{{scoreAClass}}">{{match.TeamA.RoundsWon}}</span> - <span class="{{scoreBClass}}">{{match.TeamB.RoundsWon}}</span></td>
            <td>{{match.TeamB.Name}}</td>
            <td>{{match.MapName}}</td>
        </tr>
        {% if newMatch == true %}
            {% assign newMonth = true %}
        {% else %}
        <tr class="spacer">
            <th></th>
            <th></th>
            <th></th>
            <th></th>
            <th></th>
        </tr>
        {% endif %}
        {% endfor %}
    </table>
</div>