
### Writing posts

One of Jekyll’s best aspects is that it is “blog aware”.

If you write articles and publish them online, you can publish and maintain a blog simply by managing a folder of text-files on your computer.
<!-- vertical-slide -->

### The Posts Folder

As explained on the directory structure page, the \_posts folder is where your blog posts will live. These files are generally Markdown or HTML, but can be other formats with the proper converter installed. All posts must have YAML Front Matter, and they will be converted from their source format into an HTML page that is part of your static site.
<!-- vertical-slide -->

### Creating Post Files

To create a new post, all you need to do is create a file in the \_posts directory. How you name files in this folder is important. Jekyll requires blog post files to be named according to the following format:

```sh
.
..
YEAR-MONTH-DAY-title.MARKUP
```

Where YEAR is a four-digit number, MONTH and DAY are both two-digit numbers, and MARKUP is the file extension representing the format used in the file. For example, the following are examples of valid post filenames:

```sh
.
..
2011-12-31-new-years-eve-is-awesome.md
2012-09-12-how-to-write-a-blog.md
```
<!-- next-slide -->