---
layout: default
title: Teaching
permalink: /teaching/
---

# Teaching

<div class="tabs">

{% for year in site.data.teaching.years %}
<button class="tab-button {% if forloop.first %}active{% endif %}"
        onclick="openTab(event, '{{ year[0] }}')">
    {{ year[1].label }}
</button>
{% endfor %}

</div>


{% for year in site.data.teaching.years %}

<div id="{{ year[0] }}" 
     class="tab-content"
     {% if forloop.first %}
     style="display:block;"
     {% endif %}>

    {% if year[1].courses.size > 0 %}

    <div class="cards">

        {% for course in year[1].courses %}

        <div class="card">
            <div class="title">{{ course.title }}</div>
            <div class="desc">{{ course.desc }}</div>
            <div class="meta">{{ course.hours }} hours</div>
        </div>

        {% endfor %}

    </div>

    {% endif %}


    {% if year[1].topics.size > 0 %}

    <ul>
        {% for topic in year[1].topics %}
        <li>{{ topic }}</li>
        {% endfor %}
    </ul>

    {% endif %}

</div>

{% endfor %}


<script>
function openTab(evt, tabName) {

  const contents = document.getElementsByClassName("tab-content");
  for (let c of contents)
      c.style.display = "none";

  const buttons = document.getElementsByClassName("tab-button");
  for (let b of buttons)
      b.classList.remove("active");

  document.getElementById(tabName).style.display = "block";
  evt.currentTarget.classList.add("active");
}
</script>