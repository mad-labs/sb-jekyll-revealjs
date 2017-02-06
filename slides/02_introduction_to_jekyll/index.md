---
title: Introduction to Jekyll
description: Introduction to Jekyll - a static site generator

#databackgroundimage: /assets/images/grunge-danger_custom_2.jpg
#databackgroundsize: "100px" 
#databackgroundposition: "center"
#databackgroundrepeat: "repeat"

#databackgroundcolor: "#ff0000"

#databackgroundiframe: ""

#databackgroundvideo: "https://s3.amazonaws.com/static.slid.es/site/homepage/v1/homepage-video-editor.mp4,https://s3.amazonaws.com/static.slid.es/site/homepage/v1/homepage-video-editor.webm" 
#databackgroundvideoloop: true
#databackgroundvideomuted: true

theme: night
reveal:
  transition: concave
slides: 
intros:
  - presentation/intro_icebreakers.md
  - presentation/intro_madlabs.md
  - presentation/intro_whoami.md
outros:
  - presentation/outro_contacts.md
slides:
  - 000.md
  - 001.md
  - 002.md 
  - 003.md 
  - 004.md 
  - 005.md 
  - 006.md 
  - 007.md 
  - 008.md 
  - 009.md 
  - 010.md 
  - 011.md 
  - 012.md
  - 013.md
---

{% for slide in page.slides %}
  {% include_relative {{ slide }} %}
{% endfor %}

