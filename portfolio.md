---
layout: portfolio
title: Work Samples
permalink: /samples/
navigation_weight: 1
---
<main role="main" data-layout="portfolio">
  <div data-area="heading">
    <div class="wrapper">
      <h2 class="trafalgar">{{ page.title }}</h2>
      <h3 class="double-pica">Code Samples</h3>
      <ul>
        <li><a href="https://github.com/cbleslie/" title="Github Profile">Github Profile</a></li>
        <li><a href="http://codepen.io/cbleslie/" title="Code Pens">Code Pens</a></li>
      </ul>
      <h3 class="double-pica">Art Samples</h3>
    </div>
  </div>
  {% assign sorted_portfolio = site.portfolio | sort: "weight" %}
  {% for artwork in sorted_portfolio %}
    <div data-area="thumbnail">
      <div class="wrapper">
        {% include portfolio-thumbnail.html
           thumbnail=artwork.thumbnail
           title=artwork.title
           client=artwork.client
           type=artwork.type
           content=artwork.content
        %}
      </div>
    </div>
  {% endfor %}

</main>
