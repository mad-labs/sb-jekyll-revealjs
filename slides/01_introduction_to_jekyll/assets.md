
### Assets

Jekyll provides built-in support for Sass and can work with CoffeeScript via a Ruby gem. In order to use them, you must first create a file with the proper extension name (one of .sass, .scss, or .coffee) and start the file with two lines of triple dashes, like this:

```sh
---
---

// start content
.my-definition
  font-size: 1.2em
```

Jekyll treats these files the same as a regular page, in that the output file will be placed in the same directory that it came from. For instance, if you have a file named css/styles.scss in your site’s source folder, Jekyll will process it and put it in your site’s destination folder under css/styles.css
<!-- next-slide -->
