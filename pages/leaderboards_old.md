---
layout: default
permalink: leaderboards_old
title: Leaderboards
---
<div align="center">
<table class="fullTableAllBorders">
<tr>
    <th></th>
    <th style="text-align: center">Total</th>
    <th style="text-align: center">Average (round/total)</th>
    <th style="text-align: center">Average per Match</th>
</tr>
<tr>
    <th style="text-align: center">Kills</th>
    <td style="text-align: center">{% include award.html Field="Kills" %}</td>
    <td style="text-align: center" class="CellWithComment">{% include award.html Field="Kills" DivideByField="Rounds" NonPercent=true %}<span class="CellComment">per Round</span></td>
    <td style="text-align: center">{% include award.html Field="Kills" DivideByField="matches" %}</td>
</tr>
<tr>
    <th style="text-align: center">Assists</th>
    <td style="text-align: center">{% include award.html Field="Assists" %}</td>
    <td style="text-align: center" class="CellWithComment">{% include award.html Field="Assists" DivideByField="Rounds" NonPercent=true %}<span class="CellComment">per Round</span></td>
    <td style="text-align: center">{% include award.html Field="Assists" DivideByField="matches" %}</td>
</tr>
<tr>
    <th style="text-align: center">Deaths</th>
    <td style="text-align: center">{% include award.html Field="Deaths" %}</td>
    <td style="text-align: center" class="CellWithComment">{% include award.html Field="Deaths" DivideByField="Rounds" NonPercent=true %}<span class="CellComment">per Round</span></td>
    <td style="text-align: center">{% include award.html Field="Deaths" DivideByField="matches" %}</td>
</tr>
<tr>
    <th style="text-align: center">KAST Rounds</th>
    <td style="text-align: center">{% include award.html Field="KASTRounds" %}</td>
    <td style="text-align: center" class="CellWithComment">{% include award.html Field="KASTRounds" DivideByField="Rounds" ValueAppend="%" %}<span class="CellComment">Round %</span></td>
    <td style="text-align: center">{% include award.html Field="KASTRounds" DivideByField="matches" %}</td>
</tr>
<tr>
    <th style="text-align: center">Damage Dealt</th>
    <td style="text-align: center">{% include award.html Field="DamageDealt" %}</td>
    <td style="text-align: center" class="CellWithComment">{% include award.html Field="DamageDealt" DivideByField="Rounds" NonPercent=true %}<span class="CellComment">per Round</span></td>
    <td style="text-align: center">{% include award.html Field="DamageDealt" DivideByField="matches" %}</td>
</tr>
<tr>
    <th style="text-align: center">Headshots</th>
    <td style="text-align: center">{% include award.html Field="Headshots" %}</td>
    <td style="text-align: center" class="CellWithComment">{% include award.html Field="Headshots" DivideByField="Kills" ValueAppend="%" %}<span class="CellComment">Headshot %</span></td>
    <td style="text-align: center">{% include award.html Field="Headshots" DivideByField="matches" %}</td>
</tr>
<tr>
    <th style="text-align: center">Plants</th>
    <td style="text-align: center">{% include award.html Field="Plants"%}</td>
    <td style="text-align: center" class="CellWithComment">{% include award.html Field="Plants" DivideByField="Rounds" ValueAppend="%"%}<span class="CellComment">Round %</span></td>
    <td style="text-align: center">{% include award.html Field="Plants" DivideByField="matches" %}</td>
</tr>
<tr>
    <th style="text-align: center">Defuses</th>
    <td style="text-align: center">{% include award.html Field="Defuses"%}</td>
    <td style="text-align: center" class="CellWithComment">{% include award.html Field="Defuses" DivideByField="Rounds" ValueAppend="%"%}<span class="CellComment">Round %</span></td>
    <td style="text-align: center">{% include award.html Field="Defuses" DivideByField="matches" %}</td>
</tr>
<tr>
    <th style="text-align: center">MVPs</th>
    <td style="text-align: center">{% include award.html Field="MVPRounds"%}</td>
    <td style="text-align: center" class="CellWithComment">{% include award.html Field="MVPRounds" DivideByField="Rounds" ValueAppend="%"%}<span class="CellComment">Round %</span></td>
    <td style="text-align: center">{% include award.html Field="MVPRounds" DivideByField="matches" %}</td>
</tr>
<tr>
    <th style="text-align: center">Team Kills</th>
    <td style="text-align: center">{% include award.html Field="TeamKills"%}</td>
    <td style="text-align: center" class="CellWithComment">{% include award.html Field="TeamKills" DivideByField="Rounds" NonPercent=true %}<span class="CellComment">per Round</span></td>
    <td style="text-align: center">{% include award.html Field="TeamKills" DivideByField="matches"%}</td>
</tr>
<tr>
    <th style="text-align: center">Trade Kills</th>
    <td style="text-align: center">{% include award.html Field="TradeKills"%}</td>
    <td style="text-align: center" class="CellWithComment">{% include award.html Field="TradeKills" DivideByField="Rounds" NonPercent=true%}<span class="CellComment">per Round</span></td>
    <td style="text-align: center">{% include award.html Field="TradeKills" DivideByField="matches"%}</td>
</tr>
<tr>
    <th style="text-align: center">Times Traded</th>
    <td style="text-align: center">{% include award.html Field="TimesTraded"%}</td>
    <td style="text-align: center" class="CellWithComment">{% include award.html Field="TimesTraded" DivideByField="Rounds" ValueAppend="%"%}<span class="CellComment">Round %</span></td>
    <td style="text-align: center">{% include award.html Field="TimesTraded" DivideByField="matches"%}</td>
</tr>
<tr>
    <th style="text-align: center">First Kills</th>
    <td style="text-align: center">{% include award.html Field="FirstKills"%}</td>
    <td style="text-align: center" class="CellWithComment">{% include award.html Field="FirstKills" DivideByField="Rounds" ValueAppend="%"%}<span class="CellComment">Round %</span></td>
    <td style="text-align: center">{% include award.html Field="FirstKills" DivideByField="matches"%}</td>
</tr>
<tr>
    <th style="text-align: center">First Deaths</th>
    <td style="text-align: center">{% include award.html Field="FirstDeaths"%}</td>
    <td style="text-align: center" class="CellWithComment">{% include award.html Field="FirstDeaths" DivideByField="Rounds" ValueAppend="%"%}<span class="CellComment">Round %</span></td>
    <td style="text-align: center">{% include award.html Field="FirstDeaths" DivideByField="matches"%}</td>
</tr>
<tr>
    <th style="text-align: center">Total Rounds/Matches</th>
    <td style="text-align: center">N/A</td>
    <td style="text-align: center" class="CellWithComment">{% include award.html Field="Rounds"%}<span class="CellComment">Total Rounds</span></td>
    <td style="text-align: center" class="CellWithComment">{% include award.html Field="matches"%}<span class="CellComment">Total Matches</span></td>
</tr>
<tr>
    <th style="text-align: center">Rounds/Matches Won</th>
    <td style="text-align: center">N/A</td>
    <td style="text-align: center" class="CellWithComment">{% include award.html Field="RoundsWon"%}<span class="CellComment">Total Rounds Won</span></td>
    <td style="text-align: center" class="CellWithComment">{% include award.html Field="matchesWon"%}<span class="CellComment">Total Matches Won</span></td>
</tr>
</table>
</div>
