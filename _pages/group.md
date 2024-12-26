---
layout: page #profiles
permalink: /group/
title: group
description: members of the lab or group
nav: true
nav_order: 2

# profiles:
#   # if you want to include more than one profile, just replicate the following block
#   # and create one content file for each profile inside _pages/
#   - align: right
#     image: prof_pic.jpg
#     content: about_einstein.md
#     image_circular: false # crops the image to make it circular
#     more_info: >
#       <p>555 your office number</p>
#       <p>123 your address street</p>
#       <p>Your City, State 12345</p>
#   - align: left
#     image: prof_pic.jpg
#     content: about_einstein.md
#     image_circular: false # crops the image to make it circular
#     more_info: >
#       <p>555 your office number</p>
#       <p>123 your address street</p>
#       <p>Your City, State 12345</p>
---

{% for person in site.data.members %}

<!-- The paddingtop and margin-top edits allow anchors to link properly. -->

<div class="container">
    <div id = "{{person.name | replace: ' ', '-'}}" class="row" style="padding-top: 60px; margin-top: -60px;">
      <img style="float: left; height:30%; width: 30%; border-radius: 50%;" src="{{ person.image | prepend: '/assets/img/' | prepend: site.baseurl | prepend: site.url }}" alt="photo of {{person.name}}">
    <div class="col-sm-8" >
        <h4>{{person.name}}{% if person.degrees %}, {{person.degrees}} {% endif %}</h4>
        {{person.position}} <br>
            {% if person.email %}
            <i class="fa fa-envelope"></i> <em>{{person.email}}</em> <br>
            {% endif %}
            {% if person.twitter %}
              <i class="fab fa-twitter"></i> <a href= "http://twitter.com/{{person.twitter}}" target="_blank"> @{{person.twitter}} </a> <br>
            {% endif %}
            {% if person.website %}
              <i class="fa fa-globe"></i> <a href= "{{person.website}}" target="_blank">{{person.website}}</a> <br>
            {% endif %}
            {% if person.github %}
              <i class="fab fa-github"></i> <a href= "https://github.com/{{person.github}}" target="_blank"> {{person.github}} </a> <br>
            {% endif %}
            {% if person.scholar %}
              <i class="ai ai-google-scholar"></i> <a href= "http://scholar.google.com/citations?user={{person.scholar}}" target="_blank"> Scholar Citations </a> <br>
            {% endif %}
            {% if person.orcid %}
              <i class="ai ai-orcid"></i> <a href="http://{{person.orcid}}" target="_blank"> {{person.orcid}}</a> <br>
            {% endif %}
        <p class="text-justify">{{person.description | markdownify}}</p>

</div>
</div>
</div>
<hr>
{% endfor %}

---

## former members

<!-- {% for alum in site.data.alumni %} -->

<!-- <div class="col-sm-12" >
    <b>{{alum.name}}{% if alum.degrees %}, {{alum.degrees}} {% endif %}</b>    
    {% if alum.website %}
      <i class="fa fa-globe"></i> <a href= "{{alum.website}}" target="_blank">{{alum.website}}</a>
    {% endif %}<br>
    <i>previously:</i> {{alum.previously}} <br>
    <i>now:</i> {{alum.now}}<br><br>
</div>
{% endfor %} -->

{% for alum in site.data.alumni %}

<div class="container">
    <div id = "{{alum.name | replace: ' ', '-'}}" class="row" style="padding-top: 60px; margin-top: -60px;">
      <img style="float: left; height: 15%; width: 15%; border-radius: 50%;" src="{{ alum.image | prepend: '/assets/img/' | prepend: site.baseurl | prepend: site.url }}" alt="photo of {{alum.name}}">
    <div class="col-sm-10" >
        <b>{{alum.name}}{% if alum.degrees %}, {{alum.degrees}} {% endif %}</b>
        {{alum.position}}<br>
        {% if alum.website %}
          <i class="fa fa-globe"></i> <a href= "{{alum.website}}" target="_blank">{{alum.website}}<br></a>
        {% endif %}
        <i>previously:</i> {{alum.previously}} <br>
        <i>now:</i> {{alum.now}}
        <p class="text-justify">{{alum.description | markdownify}}</p>

</div>
</div>
</div>
<hr>
{% endfor %}
---

## opportunities

DAWN hires postdoc Fellows and PhD students yearly and we also can host visitors. My group has openings for postdocs, PhD and MSc students at the Niels Bohr Institute. Inquiries from people interested in working at DAWN and/or applying for independent research funding in Denmark are very welcome. I am always interested in collaborating with new people.

---

## funding

I am grateful for the support of my research from a number of sources. My group is currently supported by VILLUM FONDEN via a Villum Young Investigator grant (37459). My research has previously been supported by NASA Headquarters through the NASA Earth and Space Science Fellowship Program Grant NNX16AO85H, and through the NASA Hubble Fellowship grant HST-HF2-51413.001-A awarded by the Space Telescope Science Institute, which is operated by the Association of Universities for Research in Astronomy, Inc., for NASA, under contract NAS5-26555.
