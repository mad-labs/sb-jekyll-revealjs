
#### Basic Usage

The Jekyll gem makes a jekyll executable available to you in your Terminal window. You can use this command in a number of ways:

```sh
#Install Jekyll and Bundler gems through RubyGems
~ $ gem install jekyll bundler

#Create a new Jekyll site at ./myblog
~ $ jekyll new myblog

#Change into your new directory
~ $ cd myblog

#Build the site on the preview server
~/myblog $ bundle exec jekyll serve

#Now browse to http://localhost:4000
```
<!-- vertical-slide -->

### Basic concepts and commands

Jekyll will use these files and folders as a basis to create a fully static website. 

This static website is generated in the **_site** folder by default.

Jekyll will process all files with a **YAML Front Matter** (including empty YAML Front Matters), 
make them available in memory and make them usable by the Liquid templating engine and Jekyll tags.

Files and folders with a name starting with underscore will not be transferred to the _site folder, 
while the others will be after having been processed by the Jekyll pipeline.

When in your project folder, the jekyll **build** or **bundle exec jekyll build** commands are used to 
generate your website. 

If you want the regeneration to happen every time a file is changed, just 
use the --watch flag: jekyll build --watch.


<!-- vertical-slide -->

#Jekyll also comes with a built-in development server that will allow you to preview what the generated site will look like in your browser locally.

```sh
$ jekyll serve
#=> A development server will run at http://localhost:4000/
#Auto-regeneration: enabled. Use `--no-watch` to disable.

$ jekyll serve --detach
#=> Same as `jekyll serve` but will detach from the current terminal.
#If you need to kill the server, you can `kill -9 1234` where "1234" is the PID.
#If you cannot find the PID, then do, `ps aux | grep jekyll` and kill the instance.
```

<!-- next-slide -->