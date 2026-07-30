---
# You don't need to edit this file, it's empty on purpose.
# Edit theme's home layout instead if you wanna make some changes
# See: https://jekyllrb.com/docs/themes/#overriding-theme-defaults
layout: home

hero:
  image: /assets/img/site/hero_entrance.jpg

title: Home 
description: "THInK Team at UC Irvine researches chiplet design, heterogeneous integration, and fine-pitch interconnect platforms for AI and high-performance computing systems."

tagline: "<span class='tagline-accent'>T</span>he<br><span class='tagline-accent'>H</span>eterogeneous<br><span class='tagline-accent'>I</span>ntegration<br><span class='tagline-accent'>Kn</span>owledge<br><span class='tagline-accent'>Team</span>."
intro: |
  At THInK Team, we focus on enabling heterogeneous integration of systems. We deep dive into advanced packaging fine-pitch integration platforms and generate architectures, design methodologies, circuits, and EDA tools to increase system performance, reduce energy footprint, and enable novel applications. 

  Follow us for updates from [THInK Team LinkedIn Page](https://www.linkedin.com/company/thinkteam-uci){:target="_blank"}.
---
<h2>Latest News</h2>

<div class="news-box">
{% assign latest_news = site.news | reverse %}
{% for news in latest_news %}
  <div class="news-box-item">
  <h3>{{ news.title }}</h3>
    <p>
      <b>{{ news.date | date: "%-d %B %Y" }}</b> |
      {{ news.blurb }} <a href="{{ news.url | relative_url }}">Click for details.</a>
    </p>
  </div>
{% endfor %}
</div>