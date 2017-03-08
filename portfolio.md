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
      <div data-projects>
        <input id="project-0" name="project-set" type="radio" checked>
        {% include project.html
          title="LogJam"
          link="https://github.com/cbleslie/LogJam"
          content="An API'esq way of managing your flexbox layouts"
          prev="project-4"
          next="project-1"
        %}
        <input id="project-1" name="project-set" type="radio">
        {% include project.html
          title="Viilo"
          link="https://github.com/psalaets/viilo"
          content="The ping pong ladder for your office"
          prev="project-0"
          next="project-2"
        %}
        <input id="project-2" name="project-set" type="radio">
        {% include project.html
          title="Comichron Widget"
          link="https://github.com/comichron-data/widget"
          content="Embedable javascript widget to track a comic's popularity"
          prev="project-1"
          next="project-3"
        %}
        <input id="project-3" name="project-set" type="radio">
        {% include project.html
          title="Github"
          link="https://github.com/cbleslie/"
          content="My profile on Github, with addtional repositories I'm working on"
          prev="project-2"
          next="project-4"
        %}
        <input id="project-4" name="project-set" type="radio">
        {% include project.html
          title="Codpen.io"
          link="http://codepen.io/cbleslie/"
          content="Mostly CSS demos, and experiments"
          prev="project-3"
          next="project-0"
        %}
      </div>
    </div>
  </div>

</main>
