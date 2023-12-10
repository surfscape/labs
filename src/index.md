---
layout: page.njk
---

Labs is a project created to share and test inside experiments from the SurfScape project. This includes new services, features, and run code on a production enviroment.

This is directed to developers but we also encourage all users to look around.

It is recommended to use a desktop computer to test/run the studies.

## Current studies

<div style="overflow-x:auto;">
<table class="study-table">
<thead>
<tr>
<th>Study Name</th>
<th>Track Code</th>
<th>Summary</th>
<th>Status</th>
<th>Overview</th>
</tr>
</thead>
<tbody>
{%- for study in collections.studies | reverse -%}
<tr>
<td>{{study.data.title}}</td>
<td class="track_code" title="Study Public Track Code">{{study.data.track_code}}</td>
<td class="summary">{{study.data.summary}}</td>
<td class="status status-{{study.data.status | slugify}}">{{study.data.status}}</td>
<td><a class="button" href="{{study.url}}">Access</a></td>
</tr>
{%- endfor -%}
</tbody>
</table>
</div>
