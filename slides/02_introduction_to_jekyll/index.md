---
title: Introduction to Jekyll
description: Introduction to Jekyll - a static site generator
layout: presentation_multipage
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

intros:
  - presentation/intro_icebreakers.md
  - presentation/intro_madlabs.md
  - presentation/intro_whoami.md

outros:
  - presentation/outro_contacts.md

whoami:
  name: Gabriele Manfredi
  image:
    title: Gabriele
    url: /assets/images/fb_profile.jpg
  contacts:
    - "Skype: [gabriele_manfredi](skype:gabriele_manfredi?add)"
    - "Twitter: [GabOnlain](https://twitter.com/GabOnlain)"
    - "Facebook:  [Gabriele Manfredi](https://www.facebook.com/Gabriele.Manfredi.999/)"
    - "Mail: [gabriele.manfredi.999@gmail.com](mailto:gabriele.manfredi.999@gmail.com)"
  resume:
    - "Senior Java Developer in Object Method: [http://www.objectmethod.it/](http://www.objectmethod.it/)"
    - "Strong Web development skills: Java (SE -EE), SQL, Html, JavaScript, CSS and more..."
    - "Worked with Reply, NTT, Enel, Eni and more..."
    - "Love develop, boardgame, books, series, movie, photography & learn new things"

slides:
  - 001.md
  - 000.md
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

