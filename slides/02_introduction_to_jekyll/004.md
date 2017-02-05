
### Directory structure

Jekyll is, at its core, a text transformation engine. The concept behind the system is this: you give it text written in your favorite markup language, be that Markdown, Textile, or just plain HTML, and it churns that through a layout or a series of layout files.

<!-- vertical-slide -->

#### A basic Jekyll site usually looks something like this:

```sh
index.html
_config.yml
_data /
  members.yml
_drafts /
  on-simplicity-in-technology.md
_includes /
  footer.html
  header.html
_layouts /
  default.html
_posts /
  2009-04-26-barcamp-boston-4-roundup.md
_sass /
  _layout.scss
_site /
```

<!-- vertical-slide -->

#FILE | DIRECTORY	DESCRIPTION
------------ | ------------
\_config.yml | Stores configuration data. Many of these options can be specified from the command line executable but it’s easier to specify them here so you don’t have to remember them.
\_data | Well-formatted site data should be placed here. The Jekyll engine will autoload all data files (using either the .yml,  .yaml, .json or .csv formats and extensions) in this directory, and they will be accessible via `site.data`. If there's a file members.yml under the directory, then you can access contents of the file through site.data.members.
\_includes | These are the partials that can be mixed and matched by your layouts and posts to facilitate reuse. The liquid tag {% raw %}`{% include file.ext %}`{% endraw %} can be used to include the partial in \_includes/file.ext.
\_layouts | These are the templates that wrap posts. Layouts are chosen on a post-by-post basis in the YAML Front Matter, which is described in the next section. The liquid tag {% raw %}`{{ content }}`{% endraw %} is used to inject content into the web page.
\_posts | Your dynamic content, so to speak. The naming convention of these files is important, and must follow the format: YEAR-MONTH-DAY-title.MARKUP. The permalinks can be customized for each post, but the date and markup language are determined solely by the file name.

<!-- vertical-slide -->

#FILE | DIRECTORY	DESCRIPTION
------------ | ------------
\_sass | These are sass partials that can be imported into your main.scss which will then be processed into a single stylesheet main.css that defines the styles to be used by your site.
\_site | This is where the generated site will be placed (by default) once Jekyll is done transforming it. It’s probably a good idea to add this to your .gitignore file.
index.html | Provided that the file has a YAML Front Matter section, it will be transformed by Jekyll. The same will happen for any .html, .markdown, .md, or .textile file in your site’s root directory or directories not listed above.
Other Files/Folders | Every other directory and file except for those listed above — such as css and images folders, favicon.ico files, and so forth — will be copied verbatim to the generated site. There are plenty of sites already using Jekyll if you’re curious to see how they’re laid out.

<!-- next-slide -->

### Front Matter

The front matter is where Jekyll starts to get really cool. Any file that contains a YAML front matter block will be processed by Jekyll as a special file. The front matter must be the first thing in the file and must take the form of valid YAML set between triple-dashed lines.

```yaml
---
layout: post
title: Blogging Like a Hacker
---
```

Between these triple-dashed lines, you can set predefined variables or even create custom ones of your own.

These variables will then be available to you to access using Liquid tags both further down in the file and also in any layouts or includes that the page or post in question relies on.

<!-- next-slide -->