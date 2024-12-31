---
layout: page #profiles
permalink: /group/
title: group
description: 
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
{% include members.liquid %}
{% endfor %}


## former members

{% for alum in site.data.alumni %}
{% include alumni.liquid %}
{% endfor %}


## opportunities

DAWN hires postdoc Fellows and PhD students yearly and we also can host visitors. My group has openings for postdocs, PhD and MSc students at the Niels Bohr Institute. Inquiries from people interested in working at DAWN and/or applying for independent research funding in Denmark are very welcome. I am always interested in collaborating with new people.

---

## funding

I am grateful for the support of my research from a number of sources. My group is currently supported by an ERC Starting Grant ([RISES, 101163035](https://cordis.europa.eu/project/id/101163035)), the Carlsberg Foundation (Sempers Ardens Accelerate, CF22-1322), and VILLUM FONDEN via a Villum Young Investigator grant (37459). My research has previously been supported by NASA Headquarters through the NASA Earth and Space Science Fellowship Program Grant NNX16AO85H, and through the NASA Hubble Fellowship grant HST-HF2-51413.001-A awarded by the Space Telescope Science Institute, which is operated by the Association of Universities for Research in Astronomy, Inc., for NASA, under contract NAS5-26555.
