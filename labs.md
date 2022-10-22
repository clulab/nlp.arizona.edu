---
layout: default
title: "Labs"
order: 1
---

<div class="row g-2">
{% for lab in site.data.labs %}
    <div class="col-6 col-sm-4 col-md-3 col-lg-2">
        <div class="col-12 p-1 m-2 h-100 border rounded">
            <p class="text-center">
                <img class="icon" src="{{ lab.icon_url }}" /><br/>
                <a href="{{ lab.url }}">{{ lab.name }}</a><br/>
            </p>
        </div>
    </div>
{% endfor %}
</div>
