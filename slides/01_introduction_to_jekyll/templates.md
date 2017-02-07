
### Templates

Jekyll uses the Liquid templating language to process templates. All of the standard [Liquid](https://shopify.github.io/liquid/) tags and filters are supported.

![Liquid website]({{ "assets/images/liquid_template_language.png" }})

Jekyll even adds a few handy filters and tags of its own to make common tasks easier.
<!-- vertical-slide -->

### Liquid tags

There are two main types of tags in Liquid:

* Output tags {% raw %}**{{ output }}**{% endraw %} allowing you to output variables in your templates.
{% raw %}
```liquid
<li>{{ item.title }}</li>
```
{% endraw %}
* Logical or execution tags {% raw %}**{% logic %}**{% endraw %}. For example {% raw %}**{% if %}**{% endraw %},
  {% raw %}**{% endif %}**{% endraw %} or {% raw %}**{% assign myariable = site.mycollection %}**{% endraw %}
  all allow you execute actions or add logic to your templates.

{% raw %}
```liquid
{% assign blogpostsPerTitle = site.posts | sort: 'title' | reverse %}
```
```liquid
{% if user.age > 18 %}
  <p>Would you like a beer ?</p>
{% endif %}
```
```liquid
{% for item in site.posts %}
  {{ item.title }}
{% endfor %}
```
{% endraw %}
<!-- vertical-slide -->

### Access your data

When it runs, Jekyll makes a bunch of variables available to you via the Liquid templating system.

* **site**: Sitewide information + configuration settings from  _config.yml.

* **page**: Page specific information + the YAML front matter. Custom variables set via the YAML 
  Front Matter will be available here. See below for details.

* **paginator**: When the paginate configuration option is set, this variable becomes available for use.
  See Pagination for details.

* **layout**: Layout specific information + the YAML front matter. Custom variables set via the YAML
  Front Matter in layouts will be available here.

* **content**: In layout files, the rendered content of the Post or Page being wrapped. Not defined in Post
  or Page files.

Ex.
{% raw %}
```liquid
{{ site.pages }} <!--A list of all Pages.-->
{{ page.url }} <!--The URL of the Post without the domain.-->
{{ paginator.total_posts }} <!--Total number of Posts.-->
```
{% endraw %}

<!-- vertical-slide -->


### Ex. Displaying an index of posts

With templates you can create an index of posts on another page, thanks to the Liquid template language and its tags:

{% raw %}
```liquid
<ul>
  {% for post in site.posts %}
    <li>
      <a href="{{ post.url }}">{{ post.title }}</a>
    </li>
  {% endfor %}
</ul>
```
{% endraw %}

<!-- vertical-slide -->

### Includes

If you have small page fragments that you wish to include in multiple places on your site, you can use the include tag.

{% raw %}
```liquid
{% include footer.html %}
```
{% endraw %}

Jekyll expects all include files to be placed in an \_includes directory at the root of your source directory.
This will embed the contents of <source>/\_includes/footer.html into the calling file.

You can also pass parameters to an include. Omit the quotation marks to send a variable’s value. Liquid curly brackets should not be used here:

{% raw %}
```liquid
{% include footer.html param="value" variable-param=page.variable %}
```
{% endraw %}

These parameters are available via Liquid in the include:

{% raw %}
```liquid
{{ include.param }}
```
{% endraw %}

<!-- vertical-slide -->

### Including files relative to another file

You can also choose to include file fragments relative to the current file:

{% raw %}
```liquid
{% include_relative somedir/footer.html %}
```
{% endraw %}

You won’t need to place your included content within the \_includes directory.
Instead, the inclusion is specifically relative to the file where the tag is being used.
For example, if \_posts/2014-09-03-my-file.markdown uses the include_relative tag, the included file must be within the \_posts directory, or one of its subdirectories.
You cannot include files in other locations.

All the other capabilities of the include tag are available to the include_relative tag, such as using variables.

<!-- vertical-slide -->

### Link

If you want to include a link to a collection’s document, a post, a page or a file the link tag will generate the correct permalink URL for the path you specify.

You must include the file extension when using the link tag.

{% raw %}
```liquid
{{ site.baseurl }}{% link _collection/name-of-document.md %}
{{ site.baseurl }}{% link _posts/2016-07-26-name-of-post.md %}
{{ site.baseurl }}{% link news/index.html %}
{{ site.baseurl }}{% link /assets/files/doc.pdf %}
```
{% endraw %}

<!-- vertical-slide -->

### Post URL

If you would like to include a link to a post on your site, the post_url tag will generate the correct permalink URL for the post you specify.

{% raw %}
```liquid
{{ site.baseurl }}{% post_url 2010-07-21-name-of-post %}
```
{% endraw %}

If you organize your posts in subdirectories, you need to include subdirectory path to the post:

{% raw %}
```liquid
{{ site.baseurl }}{% post_url /subdir/2010-07-21-name-of-post %}
```
{% endraw %}

There is no need to include the file extension when using the post_url tag.
<!-- vertical-slide -->

### Including images and resources

Chances are, at some point, you’ll want to include images, downloads, or other digital assets along with your text content.

One common solution is to create a folder in the root of the project directory called something like assets or downloads, into which any images, downloads or other resources are placed.

Including an image asset in a post:

```markdown
... which is shown in the screenshot below:
![My helpful screenshot]({{ site.url }}/assets/screenshot.jpg)
```
<!-- next-slide -->