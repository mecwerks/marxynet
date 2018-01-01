---
layout: default
permalink: killmatrix
title: Killmatrix
---
<div align="left">
{% assign length = site.data.players | size | minus: 1 %}
{% assign halfLen = length | divided_by: 2 | ceil %}
{% assign leftLen = length | minus: halfLen %}
<table id="matrix" class="row-border hover order-column">
  <thead>
    <tr class="header" id="ignoreglobal">
      <th></th>
      {% for i in (0..length) %}
        <th class="col" style="text-align: center">{{site.data.players[i].Name}}</th>
      {% endfor %}
    </tr>
  </thead>
  <tbody>
    {% for i in (0..length) %}
      <tr id="ignoreglobal">
        <th class="row" style="text-align: right">{{site.data.players[i].Name}}</th>
          {% for j in (0..length) %}
          {% assign steamid = site.data.players[j].SteamID | downcase %}
          {% assign myid = site.data.players[i].SteamID | downcase %}
          <td style="text-align: center">{{site.data.players[i].KilledPlayers[steamid] | default: 0}} : {{site.data.players[j].KilledPlayers[myid] | default: 0}}</td>
        {% endfor %}
      </tr>
    {% endfor %}
  </tbody>
</table>
</div>
<script>
  $(document).ready(function() {
    var table = $('#matrix').DataTable(
      {
        "paging":   false,
        "ordering": false,
        "info":     false,
        "searching": false
      }
    );

    $('#matrix tbody').on( 'mouseenter', 'td', function () {
          var colIdx = table.cell(this).index().column;
          var rowIdx = table.cell(this).index().row;

          $( table.column( colIdx ).nodes() ).addClass( 'highlight' );
          $( table.row( rowIdx ).nodes() ).addClass( 'highlight' );
    } ).on('mouseleave', 'td', function () {
          $( table.cells().nodes() ).removeClass( 'highlight' );
          $( table.rows().nodes() ).removeClass( 'highlight' );
    });
  });
</script>
