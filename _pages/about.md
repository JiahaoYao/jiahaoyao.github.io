---
layout: about
title: About
permalink: /
description:


news: true
social: true
years: [2021, 2020]
---

Ph.D. Candidate, Applied Mathematics<br/>

---- 

I am a fourth year Ph.D. candidate in Applied Mathematics in UC Berkeley, advised by [Lin Lin](https://math.berkeley.edu/~linlin/). I did my undergrad in the Department of Mathematics, Peking University.

My research is centered on scientific mathine learning, with various applications on quantum control, reinforcement learning and deep unsupervised learning. 


**Email**: jiahao [at] math [dot] berkeley [dot] edu

----

##### Publications

<div class="publications-front">

{% for y in page.years %}
  <h3 class="year">{{y}}</h3>
  {% bibliography -f papers -q @*[year={{y}}]* %}
{% endfor %}

</div>

----

**Acknowledgements**: based on the [al-folio](https://github.com/alshedivat/al-folio) template modified by [Tony Song](https://tsong.me/).