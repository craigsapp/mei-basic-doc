
Liquid header for Markdown pages
================================

Liquid header parameters for page (accessed in liquid by prefixing the
variable name with "page.", such as "{{ page.verovio }}":


The liquid header is enclose between two lines with the content "---" at the
start of a file (This header will be removed when createing the webpage).  Here
is an example header:

```liquid
---
verovio:       "true"
author:        Johannes Kepper
creation_date: 9 May 2017
last_updated:  6 Oct 2017
github:        mei-basic/artic.md
permalink:     /artic.html
---
```

The meaning of the above variables:

verovio
: Set this variable to "true" in order to include the javascript verovio toolkit on the page.  Delete or set the variable to something else to not load verovio.  The value "true" should be in quotes.  Verovio should not be included on pages (currently the introduction) which do not use verovio so that they do not need to load it.

author:
: The author of the text content of the page.  This variable currently is not used, but this could be used to cite the author, such as in the page footer.  Also, editors coulbe be listed in an *editor* variable.  Multiple authors could be done like this `["Johannes Kepper", "Freddie Krueger"]`.

creation_date
: The date the page was created.  This is not used for anything, but could be displayed on the page header, or kept for bookkeeping (but that would duplicate the function of the repository).

last_updated
: The date the page was last (significantly) changed.  This is not used for anything, but could be displayed on the page header, or kept for bookkeeping (but that would duplicate the function of the repository).

github
: This is the location of the (Markdown) page that a general user can go to in order to edit the contents of the markdown pages.  There are settings for the Github URL and prefixes stored in the `/_config.yml` file.  The file `/_includes/github-edi-button.html` uses this variable.

permalink
: This is the location of the compiled index page on the website.  In other words, the compiled HTML file does not need to go in the parallel directory structure that the markdown files are stored.  This is a special Jekyll variable.  See more info on the page: https://jekyllrb.com/docs/permalinks/


Page titles
===========

The titles of pages are not stored in the markdown pages themselves.
They are rather stored in `_data/pages.yml`.  To add the page title to the page, use
this liquid template:

```
{% include page-title.html %}
```




