---
title: Skills
---

<style>
tr.area-governance-resourcing-and-management td {
 background-color: lightpink;
}
tr.area-communications-and-advocacy td {
 background-color: lightyellow;
}
tr.area-information-technology td {
 background-color: lightgreen;
}
tr.area-legal-and-social-responsibilities td {
 background-color: lightblue;
}
tr.area-digital-preservation-domain-specific td {
 background-color: #CBC3E3;
}
</style>

{% assign skills_by_area = site.skills | group_by:"competency-area" %}

<table class="table table-bordered border-dark">
  <thead class="table-light border-dark">
    <tr>
      <th>Competency Area</th>
      <th>Skill Element</th>
    </tr>
  </thead>
  <tbody class="table-group-divider">
  {% for area in skills_by_area %}
  {% for skill in area.items %}
    <tr class="area-{{ area.name | slugify }}">
     {% if forloop.first %}
     <td rowspan="{{ forloop.length }}">
      {{ area.name }}
      </td>
      {% endif %}
      <td>
        <a href="{{ skill.url  | relative_url }}">
        {{ skill.title }}
        </a>
      </td>
    </tr>
    {% endfor %}
    {% endfor %}
  </tbody>
</table>

{% if site.editable %}
<!--
<p style="text-align: right">
  <a target="_blank" class="btn btn-secondary" href="{{ site.editor_url }}/admin/#/collections/skills/new" role="button">Add A Skill</a>
</p>
-->
{% endif %}



<br>

<h2 id="skill-levels">Skill Levels</h2>

<table class="table table-bordered border-dark">
<colgroup>
<col style="width: 9%">
<col style="width: 18%">
<col style="width: 39%">
<col style="width: 32%">
</colgroup>
<thead class="table-light border-dark">
<tr>
<th>Level No.</th>
<th>Skill Level</th>
<th>Description</th>
<th>Example Activity Descriptor Words</th>
</tr>
</thead>
<tbody class="table-group-divider">
<tr class="odd">
<td><strong>0</strong></td>
<td><strong>Awareness</strong></td>
<td>A basic awareness of the skill element.</td>
<td>Has heard of, recognizes, is aware of</td>
</tr>
<tr class="even">
<td><strong>1</strong></td>
<td><strong>Understanding</strong></td>
<td>An understanding of the skill element (e.g. has received some training) but little or no practical experience.</td>
<td>Understands, has studied, is familiar with, uses, collaborates, communicates, supports</td>
</tr>
<tr class="odd">
<td><strong>2</strong></td>
<td><strong>Basic Application</strong></td>
<td>A sound understanding of the skill element and some experience of its practical application.</td>
<td>Has delivered, has used, applies, implements, inputs to, plans, selects, documents</td>
</tr>
<tr class="even">
<td><strong>3</strong></td>
<td><strong>Advanced Application</strong></td>
<td>A thorough understanding of the skill element and significant experience of its practical application on a regular or sustained basis.</td>
<td>Develops, leads on, manages, analyzes, monitors</td>
</tr>
<tr class="odd">
<td><strong>4</strong></td>
<td><strong>Expert</strong></td>
<td>An in-depth understanding of the skill element and a leader in the development of approaches to its practical application.</td>
<td>Innovates, authors, designs, researches</td>
</tr>
</tbody>
</table>
