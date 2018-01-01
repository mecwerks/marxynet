---
layout: default
permalink: leaderboards
title: Leaderboards
---
<div align="center">
<table class="halfTable">
<tr>
    <th style="text-align: center">Kills</th>
    <td style="text-align: center">{% include award.html Field="Kills" %}</td>
</tr>
<tr>
    <th style="text-align: center">Assists</th>
    <td style="text-align: center">{% include award.html Field="Assists" %}</td>
</tr>
<tr>
    <th style="text-align: center">Deaths</th>
    <td style="text-align: center">{% include award.html Field="Deaths" %}</td>
</tr>
<tr>
    <th style="text-align: center">KAST %</th>
    <td style="text-align: center">{% include award.html Field="KASTRounds" DivideByField="TotalRounds" ValueAppend="%"%}</td>
</tr>
<tr>
    <th style="text-align: center">ADR</th>
    <td style="text-align: center">{% include award.html Field="DamageDealt" DivideByField="TotalRounds" NonPercent=true%}</td>
</tr>
<tr>
    <th style="text-align: center">Damage Dealt</th>
    <td style="text-align: center">{% include award.html Field="DamageDealt" %}</td>
</tr>
<tr>
    <th style="text-align: center">Headshot %</th>
    <td style="text-align: center">{% include award.html Field="Headshots" DivideByField="Kills" ValueAppend="%"%}</td>
</tr>
<tr>
    <th style="text-align: center">Plants</th>
    <td style="text-align: center">{% include award.html Field="Plants"%}</td>
</tr>
<tr>
    <th style="text-align: center">Defuses</th>
    <td style="text-align: center">{% include award.html Field="Defuses"%}</td>
</tr>
<tr>
    <th style="text-align: center">MVPs</th>
    <td style="text-align: center">{% include award.html Field="MVPs"%}</td>
</tr>
<tr>
    <th style="text-align: center">Team Kills</th>
    <td style="text-align: center">{% include award.html Field="TeamKills"%}</td>
</tr>
<tr>
    <th style="text-align: center">AWP Kills</th>
    <td style="text-align: center">{% include award.html Field="AWPKills"%}</td>
</tr>
<tr>
    <th style="text-align: center">Trade Kills</th>
    <td style="text-align: center">{% include award.html Field="TradeKills"%}</td>
</tr>
<tr>
    <th style="text-align: center">Times Traded</th>
    <td style="text-align: center">{% include award.html Field="TimesTraded"%}</td>
</tr>
<tr>
    <th style="text-align: center">First Kills</th>
    <td style="text-align: center">{% include award.html Field="FirstKills"%}</td>
</tr>
<tr>
    <th style="text-align: center">First Deaths</th>
    <td style="text-align: center">{% include award.html Field="FirstDeaths"%}</td>
</tr>
<tr>
    <th style="text-align: center">Total Rounds</th>
    <td style="text-align: center">{% include award.html Field="TotalRounds"%}</td>
</tr>
<tr>
    <th style="text-align: center">Rounds Won</th>
    <td style="text-align: center">{% include award.html Field="RoundsWon"%}</td>
</tr>
</table>
