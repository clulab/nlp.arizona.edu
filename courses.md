---
layout: default
title: "Courses"
order: 2
---

<div class="row g-2">
{% for department_obj in site.data.departments %}
    {% assign department = department_obj[1] %}
    <div class="col-12 col-md-6">
        <div class="col-12 p-1 m-2 h-100 border rounded">
            <h4>{{ department.name }}</h4>
            {% for course in department.courses %}
                {%- for item in course.codes -%}
                    {%- if forloop.index > 1 -%}
                        /
                    {%- endif -%}
                    {%- if item.url -%}
                        <a href="{{ item.url }}">{{ item.code }}</a>
                    {%- else -%}
                        {{ item.code }}
                    {%- endif -%}
                {% endfor %}
                {{ course.title }}<br/>
            {% endfor %}
        </div>
    </div>
{% endfor %}
</div>
