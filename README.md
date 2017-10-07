

Running website locally
=======================

To run the website locally you will need to do some initial setup:

https://help.github.com/articles/setting-up-your-github-pages-site-locally-with-jekyll

Then to actually run the local webserver with the website, type:

```bash
	./.sever
```

which is a script with this contents:

```bash
	bundle exec jekyll serve --port 2222 --host 127.0.0.1
```



Files/directories in this repository
====================================

Gemfile		-- Contains setup files needed for first getting the website
			running locally.
README.md	-- This file.
_config.yml	-- Site-level configuration variables for the website.
_data/		-- Data variables for website shared across pages.  This currently
			holds a list of the pages in the tutorial and the order
			in which they should be displayed.
_includes/	-- HTML snippets used to construct webpage for markdown pages.
_layouts/	-- Starting templates for markdown pages.
_site/		-- Not stored in repository, but will be visible if you run the
			website locally.  It contains the output of the
			template expansions for the website.
mei-basic/	-- This directory contains all of the Markdown files for the documentation.
resources/	-- This directory contains the javascript (particularly external code)
			and css files for the website.
samples/	-- This directory contains the MEI data for the examples on the pages
			in /mei-basic/ markdown files.
