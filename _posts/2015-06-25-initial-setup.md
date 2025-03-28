---
layout: post
section-type: post
has-comments: true
title: Initial setup
category: tech
tags: ["tutorial"]
---

All features of { Personal } are controlled by setting values to variables that
are defined in the `_config.yml` file. Let's start with the initial variables
that you have to set before serving your { Personal } website for the first
time.

### Setting up the url

```yaml
# NB! Set your site's url, otherwise nothing will work
url: "https://le4ker.github.io/personal-jekyll-theme"
```

The `url` variable is essential, because it's used \_everywhere\* where an
anchor is defined. It's needed only for repositories that are published on
Github Pages, since the root url becomes `github.com/username/repo-name`. If you
are not hosting your {Personal Jekyll Theme }, you can remove the variable and
all its references (`{{site.url}}`).

````yaml

### Theme Customization

You can define the colors that you want in your { Personal } website by setting
the following variable sin the `_sass/variables.scss` file:

```scss
$primary-color: #232a2e;
$secondary-color: #3a94c5;
$font-color: #efebd4;
$background-color: $font-color;
````

### HTML Head

```yaml
lang: "en"
author: "John Smith"
title: "{ John Smith }"
description:
  "Blog and website of John Smith, blogging mainly for tech. Opinions expressed
  are mine."
keywords: "smith, jones, personal, jekyll, theme"
favicon: "/img/favicon.ico"
```

The values that you set, will be placed in the head section of every generated
HTML page.

### Google Analytics

The Google tracking code will be placed in every generated page. If you don't
want Google analytics tracking your website's traffic, set the
google-tracking-id to false.

```yaml
google-tracking-id: "UA-XXXXXXXX-X"
```

### Serving { Personal } locally

You can use Docker to run the website to avoid installing any dependencies to
your local environment. To do so, run:

```shell
docker-compose up --build
```

Alternatively, you can run the website locally by installing the dependencies:

```shell
bundle install
```

And then start serving the website:

```shell
bundle exec jekyll serve --watch --livereload
```

That's it!

Visit [http://0.0.0.0:4000](http://0.0.0.0:4000) and you are ready to start
hacking around your { Personal } website.
