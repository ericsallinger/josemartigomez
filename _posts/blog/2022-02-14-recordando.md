---
layout: single
title: "Recordando"
date: 2022-02-14 15:35:46 +0100
categories: Blog
classes: wide
comments: 
- name: "eric"
  comment: a
- name: "bbric"
  comment: b
- name: "gric"
  comment: c
- name: "rric"
  comment: d
- name: "mric"
  comment: e
- name: "eric"
  comment: a
- name: "bbric"
  comment: b
- name: "gric"
  comment: c
- name: "rric"
  comment: d
- name: "mric"
  comment: e

---
<script>

function myFunction() {
  document.getElementById("submission").style.display = "none"
}
</script>

{% assign last = page.comments | last %}
{% assign counter = 0 %}
<div class="row">
{% for item in page.comments %}
  
  <div class="col-1-of-3">
  {{ item.name }} // {{item.comment}} // {{counter}}
  </div>
  {% assign counter = counter | plus: 1 %}
  {% if counter == 3 %}
    {% assign counter = 0 %}
    {% if item != last %}
      last
    {% endif %}
    </div><div class="row">
  {% endif %}
{% endfor %}


<form id="comments" action="https://hooks.zapier.com/hooks/catch/5782035/brr6wyu/" method="post">
  <input type="text" name="comment-name" placeholder="su nombre (opcional)">
  <input type="text" name="comment-text" placeholder="su mensaje ">
  <input type="button" onclick="myFunction()" value="Publicar">
  <p id="submission">your note will be read and published shortly</p>
</form>
