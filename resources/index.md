---
title: Learning Resources
---

<table id="mainTable" data-page-length="50" data-pagefind-ignore>
  <thead>
    <tr>
      <th>Resource</th>
      <th>Type</th>
      <th>Skills</th>
      <th>Roles</th>
    </tr>
  </thead>
  <tbody>
{% for item in site.resources %}
    <tr>
      <td data-sortable="true">
    <a href="{{ item.url | relative_url }}">
      {{ item.title }}
    </a>
      </td>
      <td>
        {{ item['resource-type'] }}
      </td>
      <td>
      {% include skill_levels.html skills=item.skill-levels %}
      </td>
      <td>
      {% include roles.html roles=item.roles %}
      </td>
    </tr>
{% endfor %}
  </tbody>
</table>

<hr>

{% if site.editable %}
<p style="text-align: right">
  <a target="_blank" class="btn btn-primary" href="{{ site.editor_url }}/admin/#/collections/resources/new" role="button">Add A Resource</a>
</p>
{% endif %}

