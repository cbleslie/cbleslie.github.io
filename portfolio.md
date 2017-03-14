---
layout: portfolio
title: Work Samples
permalink: /samples/
navigation_weight: 1
---
<main role="main" data-layout="portfolio">
  <div data-area="thumbnail">
    <div class="wrapper">

      <div data-layout="thumbnails">
        <div data-area="title">
          <div class="wrapper">
            <h2 class="trafalgar">{{ page.title }}</h2>
          </div>
        </div>
        {% assign sorted_portfolio = site.portfolio | sort: "weight" %}
        {% for artwork in sorted_portfolio %}

          <div data-area="thumb">
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
      </div>
    </div>
  </div>
  <div data-area="projects">
    <div class="wrapper">
      <h3 class="double-pica">Projects</h3>
      <br/>
      {% include project.html
        title="LogJam"
        link="https://github.com/cbleslie/LogJam"
        content="An API for managing your flexbox layouts"
      %}
      {% include project.html
        title="Viilo"
        link="https://github.com/psalaets/viilo"
        content="The ping pong ladder for your office, using the Elo ranking algorithm"
      %}
      {% include project.html
        title="Comichron Widget"
        link="https://github.com/comichron-data/widget"
        content="Embeddable Javascript widget to track a comicbook's popularity using the Comichron-Data API"
      %}
      <br/>
      <h3 class="double-pica">Other</h3>
      <br/>
      {% include project.html
        title="Github"
        link="https://github.com/cbleslie/"
        content="My profile on Github"
      %}
      {% include project.html
        title="Codpen.io"
        link="http://codepen.io/cbleslie/"
        content="Mostly CSS demos, and experiments"
      %}
    </div>
  </div>

</main>
