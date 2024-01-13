---
title: Instruksi yang Tersedia Online
permalink: index.html
layout: home
---

# Daftar Isi Direktori

Hyperlink ke masing-masing latihan lab tercantum di bawah ini.

## Lab

{% assign labs = site.pages | where_exp:"page", "page.url contains '/Instructions/Labs'" %}
| Modul | Laboratorium |
| --- | --- | 
{% untuk aktivitas di lab %}| {{ activity.lab.module }} | [{{ activity.lab.title }}{% if activity.lab.type %} - {{ activity.lab.type }}{% endif %}]({{ site.github.url }}{{ activity.url }}) |
{% endfor %}

## Demo

{% assign demos = site.pages | where_exp:"page", "page.url berisi '/Instructions/Demos'" %}
| Modul | Demo |
| --- | --- | 
{% untuk aktivitas di Demo %}| {{ activity.demo.module }} | [{{ activity.demo.title }}]({{ site.github.url }}{{ activity.url }}) |
{% endfor %}
