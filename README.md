
# SparkzLab!

As with any jekyll theme, layouts and includes are all in their default directories and the main stylesheets are in ```css``` with the variables and mixins in ```_sass```. In case you are unfamiliar with Jekyll's basic structure, here is what it looks like:

```bash

basic Jekyll
├── _config.yml                          # stores configuration data
├── _drafts                              # unpublished posts
|   ├── crazy-ideas.md
|   └── technology.md
├── _includes                            # partials that can be mixed and matched by your layouts and posts to facilitate reuse
|   ├── footer.html                      # {% include footer.html %} to add footer to html
|   └── header.html                      # {% include header.html %} to add header to html
├── _layouts                             # templates that wrap up posts {{ content }} to inject content
|   ├── default.html
|   └── post.html
├── _posts                               # naming convention of these files is important, and must follow the format: YEAR-MONTH-DAY-title.MARKUP
|   ├── 2015-10-29-wubalubadubdub.md
|   └── 2016-04-26-sudaodecojones.md
├── _data                                # well-formatted site data should be placed here
|   └── members.yml
├── _site                                # this is where the generated site will be placed (by default) once Jekyll is done transforming it
├── .jekyll-metadata                     # keeps track of which files have not been modified since the site was last built
└── index.html                           # provided that the file has a YAML Front Matter section, it will be transformed by Jekyll

```

YAML front matter is everything at the top of a file enclosed in ```--- ---```. Liquid handles are anything enclosed in ```{{ }}``` or ```{% %}```. This can be used to call on the elements in the ```_config.yml``` file by stating ```{{ site.whatever }}```.
If you get the gist :grin: , then here is petti-jekyll's theme structure.

```bash

petti-jekyll
├── _blog                      # contains the blog's index page
|  └── index.html              # the blog's index page, NOT to be confused with the main index.html
├── _includes                  # partials that can be used and reused in layouts and pages
|  ├── aboutme                 # this is a section of the main index.html, a short description
|  ├── color-browser           # snippets for site color depending on browser or device
|  ├── comments                # add to layout or html itself for "disqus" commments
|  ├── contact                 # this is a section of the main index.html, the contact section
|  ├── footer                  # site footer, plain and simple
|  ├── force-https             # forces https, not really needed, false on _config by default
|  ├── head                    # site head, with links to stylesheets, javascript and other includes
|  ├── header                  # landing header of index file, contains the background image and icon
|  ├── js                      # contains all the JavaScript custom functions, don't touch unless you know what you are doing
|  ├── latest-post             # section on the main index.html showing latest blog post
|  ├── navigation              # the index navigation bar, contains the elements and their links
|  ├── navigation_pages        # navigation bar for pages other than index (could be removed)
|  ├── pagination              # pagination for blog posts
|  ├── post-list               # post list by category
|  ├── share                   # share buttons for posts
|  ├── social-buttons          # social media buttons, duh
|  ├── swipe-instructions      # neat swipe instructions by javascript
|  ├── syntax-highlighting     # syntax highlighting in posts
|  ├── timeline                # section of main index.html, the timeline duh
|  └── web-app                 # for web-app mode, ignore if you don't know what that is
├── _layouts                   # the layouts or templates for different pages
|  ├── blog                    # layout for blog page
|  ├── category                # layout for category page for posts
|  ├── error                   # every site needs a 404 error page
|  ├── index                   # you guessed it, the layout for the main index.html
|  ├── post                    # blog post layout
|  └── tag                     # tag page for blog posts
├── css                        # the stylesheets of the theme
|  ├── font-awesome.min        # contains the info for all the icons
|  ├── grayscale               # main stylesheet, contains most custom styles
|  ├── rrssb                   # Ridiculously Responsive Social Sharing Buttons
|  ├── slick                   # stylesheet for slick slider JavaScript plugin (slideshow)
|  ├── slick-theme             # unsure if needed or not yet... ignore!
|  └── timeline                # yup, the stylesheet for the timeline section in the main index.html
├── js                         # JavaScript plugins
|  ├── hammer.min              # support for touch gestures (touchscreens)
|  ├── rrssb.min               # Ridiculously Responsive Social Sharing Buttons
|  ├── slick                   # JavaScript for slick slider plugin
|  └── typed.min               # enter a string and watch it type e.g. https://slack.com/
├── _sass
|  ├── libs                    # stylesheets for experimenting, ignore!
|  ├── mixins                  # ignore
|  └── variables               # colour variables for the whole website
├── _posts                     # where the posts go
├── categories                 # categories pages for blog posts
├── extras                     # for experimenting, ignore!
├── img                        # all images used in theme
├── _config.yml                # site configuration, contains all the site variables
├── 404.html                   # custom 404 error page
├── aboutme.html               # about section in the main index.html
├── index.html                 # main index.html, look at _layouts/index.html
├── contact.html               # contact section in main index.html
├── latest-post.html           # latest-post section in main index.html
├── timeline.html              # timeline section in main index.html
├── _site                      # ignore
├── feed.xml                   # ignore
├── sitemap.xml                # ignore
└── manifest.json              # ignore

```

This Jekyll theme is based on the [{ Personal } theme](https://github.com/PanosSakkos/personal-jekyll-theme), which is in turn a fork of [Timeline](https://github.com/kirbyt/timeline-jekyll-theme) (mashup of [Grayscale by Start Bootstrap](https://github.com/IronSummitMedia/startbootstrap-grayscale) and [Agency Jekyll Theme](https://github.com/y7kim/agency-jekyll-theme)). You've got to love opensource! :grin:

You can watch it in action [here](https://www.nicolaspettican.com/)!

Screenshot will be available soon :smile:, once the theme is fully finished!

## How to run locally

First, you need to install jekyll and the dependencies of { Personal } by running:

````
./scripts/install
````

Then, you can build and serve your website by simply running:

````
./scripts/serve-production
````

Easy peasy :grin:!

## OSS used in my theme

  1. [Personal](https://github.com/PanosSakkos/personal-jekyll-theme)
  2. [Grayscale](http://startbootstrap.com/template-overviews/grayscale/)
  3. [hammer.js](https://hammerjs.github.io/)
  4. [highlightjs](https://highlightjs.org/)
  5. [RRSSB](https://github.com/kni-labs/rrssb)
  6. [Timeline](https://github.com/kirbyt/timeline-jekyll-theme)
  7. [typed.js](https://github.com/mattboldt/typed.js/)

## Supporting the repo

Proposals, pull requests and issues are more than welcome, let's make the web a bit more beautiful and secure :wink:
