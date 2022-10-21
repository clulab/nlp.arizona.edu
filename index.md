---
layout: default
title: "Faculty"
order: 0
---

<div class="row g-2">
{% for person in site.data.people %}
    {% assign department = site.data.departments[person.department] %}
    <div class="col-6 col-sm-4 col-md-3 col-lg-2">
        <div class="col-12 p-1 m-2 h-100 border rounded">
            <p class="text-center">
                <img class="photo" src="{{ person.photo_url }}" /><br/>
                <a href="{{ person.url }}">{{ person.name }}</a><br/>
                <a href="{{ department.url }}">{{ department.name }}</a><br/>
                Apply to: <a href="{{ department.apply_url }}">{{ person.department }} PhD</a>
            </p>
            <p>Research interests: {{ person.interests }}</p>
        </div>
    </div>
{% endfor %}
</div>
