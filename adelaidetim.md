---
layout: page
title: List of Current Adelaide Public Transport Timetables
---

This is a list of current timetables for
[Adelaide Metro](https://www.adelaidemetro.com.au). Each row
in the table represents either an individual paper or PDF timetable.

Adelaide  Buses  are  operated   by:

* LIGHT  STREET  BUSES  Contract  areas     NORTH-SOUTH    and    OUTER  NORTH  EAST
* SOUTHLINK       BUSES  Contract  areas    OUTER   NORTH   and     OUTER  SOUTH
* TORRENS   TRANSIT     Contract  area       EAST  -  WEST

Note that a timetable may appear several times as the list includes:

* The generally available printed timetable, even if out of date
* Available online and current
* Available online and proposed even if the start date has passed

Last Updated August 2018

<table>
<tbody>
<tr>
<th style="text-align:left">Description</td>
<th style="text-align:left">Routes</td>
<th>Effective</td>
<th>Revision Number</td>
<th>Distribution List</td>
</tr>
{% for timetable in site.data.adelaide %}
{% if timetable.SupercededDate == nil %}
<tr>
<td style="text-align:left">{{timetable.RouteDescription}}</td>
<td style="text-align:left">{{timetable.RouteNumbers}}</td>
<td>{{timetable.EffectiveDates}}</td>
<td style="text-align:center">{{timetable.VersionNumber}}</td>
<td style="text-align:center">{{timetable.DistributionList}}</td>
</tr>
{% endif %}
{% endfor %}
</tbody>
</table>
This table is derived from [this YAML file](https://github.com/austta/austta.org.au/blob/master/_data/adelaide.yaml) which is in the same format as the National TimeTable Collection. Feel free to download, modify and submit changes!
