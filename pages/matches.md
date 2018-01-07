---
layout: default
permalink: matches
title: Matches
---
<div align="center" class="matchresult">
    {% assign currentMonth = 13 %}
    {% assign currentYear = 0 %}
    {% assign newMonth = false %}
    {% assign matches = site.data.matches %}
    {% for match in matches %}
        {% if match.TeamA.RoundWins > match.TeamB.RoundWins %} 
            {% assign scoreAClass = "scoreWinner"%} 
            {% assign scoreBClass = "scoreLoser" %} 
        {% elsif match.TeamA.RoundWins < match.TeamB.RoundWins %} 
            {% assign scoreAClass="scoreLoser" %} 
            {% assign scoreBClass="scoreWinner" %} 
        {% else %} 
            {% assign scoreAClass="scoreTie" %} 
            {% assign scoreBClass="scoreTie" %} 
        {% endif %} 

        {% assign monthString = match.Year | append: "-" | append: match.Month | append: "-" | append: match.Day | append: "T" | append: match.Hour | append: ":00:00" %}
        {% if match.Year < currentYear %}
            {% assign currentMonth = match.Month | plus: 1 %}
            {% assign currentYear = match.Year %}
        {% endif %}

        {% if match.Month < currentMonth %}
            {% if currentMonth == 13 %}
                {% assign currentMonth = match.Month %}
                {% assign currentYear = match.Year %}
            {% else %}
                </table>
            {% endif %}
            <table class="matchtable">
            <caption>{{monthString | date: "%B, %Y"}}</caption>
            {% assign currentMonth = match.Month %}
            {% assign newMonth = true %}
        {% endif %}
        <tr class='clickablerow' href='/matches/{{match.UID}}' id="matchrow">
            <td style="width: 10%;">
                {% assign d = monthString | date: "%-d" %}
                {% case d %}
                {% when "1" or "21" or "31" %}{{ d }}st
                {% when "2" or "22" %}{{ d }}nd
                {% when "3" or "23" %}{{ d }}rd
                {% else %}{{ d }}th
                {% endcase %} @ {{monthString | date: "%H"}}:00
            </td>
            <td style="text-align: right;width: 25%">{{match.TeamA.Name}}</td>
            <td style="text-align: center;width: 8%"><span class="{{scoreAClass}}">{{match.TeamA.RoundWins}}</span> - <span class="{{scoreBClass}}">{{match.TeamB.RoundWins}}</span></td>
            <td style="width: 25%">{{match.TeamB.Name}}</td>
            <td style="width: 15%">{{match.Map}}</td>
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