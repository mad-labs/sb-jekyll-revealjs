
### Themes

Jekyll has an extensive theme system, which allows you to leverage community-maintained templates and styles to customize your site’s presentation.

Jekyll themes package layouts, includes, and stylesheets in a way that can be overridden by your site’s content.
<!-- vertical-slide -->

### Installing a theme

To install a theme

* add the theme to your site’s Gemfile:
```sh
 gem 'my-awesome-jekyll-theme'
```
* Save the changes to your Gemfile
* Run the command bundle install to install the theme
* Finally, activate the theme by adding the following to your site’s \_config.yml:

```yaml
 theme: my-awesome-jekyll-theme
```
<!-- vertical-slide -->

### Overriding theme defaults

Jekyll themes set default layouts, includes, and stylesheets, that can be overridden by your site’s content.

For example, if your selected theme has a page layout, you can override the theme’s layout by creating your own page layout in the \_layouts folder (e.g., \_layouts/page.html).

Jekyll will look first to your site’s content, before looking to the theme’s defaults, for any requested file in the following folders:
```sh
/assets
/_layouts
/_includes
/_sass
```

<!-- next-slide -->