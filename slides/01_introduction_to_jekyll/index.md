---
title: Introduction to Jekyll
description: Introduction to Jekyll - a static site generator
layout: presentation_multipage
databackgroundimage: /assets/images/grunge-danger_custom_2.jpg

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
  - a_simple_static_site_generator.md
  - so_what_is_Jekyll_exactly.md
  - installation.md
  - basic_usage.md
  - directory_structure.md
  - templates.md
  - writing_posts.md
  - creating_pages.md
  - collections.md
  - assets.md
  - themes.md
  - jekyll_and_github_pages.md
  - jekyll_official_website.md
  - jekyll_resources.md
---

{% for slide in page.slides %}
  {% include_relative {{ slide }} %}
{% endfor %}

