---
title: "Strapi-Jekyll-4"
excerpt: "Static Site Generator with help of Jekyll and Strapi 4."
header:
  image: /assets/images/headless.jpg
  teaser: /assets/images/strapi+jekyll.png
sidebar:
  - title: "Role"
    image: /assets/images/deer-logo.png
    image_alt: "logo"
    text: "Project Maintainer, Lead Developer"
  - title: "Responsibilities"
    text: "Roadmap of the plugin, implementing new features, reviewing the community requests and work."
gallery:
  - url: /assets/images/strapi1.webp
    image_path: assets/images/strapi1.webp
    alt: "Creating field in Strapi"
  - url: /assets/images/strapi2.webp
    image_path: assets/images/strapi2.webp
    alt: "Adding the content in Strapi"
  - url: /assets/images/strapi3.jpg
    image_path: assets/images/strapi3.jpg
    alt: "Generated website with basic theme"
---

Static site generator using with the help of Jekyll and Headless CMS Strapi 4, following the Jamstack principles and the architecture. You can read more about Jamstack here: [https://jamstack.org/](https://jamstack.org/).

{% include gallery caption="Strapi 4 gallery and generated simply website." %}

Since my professional experience with Plone, I have become a fan of CMS solutions. A few years ago, when the new headless trend have been born - I chose Strapi as my main solution in this domain. In 2022 I was checking available static site generators to work with Strapi, and I found one using Jekyll. I liked the idea, but the plugin was in poor condition - not updated to the latest version of Strapi, not supporting authentication, not allowing to pull the media files, etc.

I did a few weeks of Ruby work, I provided solid Pull Request and some time after I received ownership of the main [Github repo](https://github.com/strapi-community/jekyll-strapi) of the project.

List of the main features which I provided for the plugin:
* Update for version 4 of the plugin
* Authentication
* Support for the media files
* Unit tests for the development

I wrote a starter article which you can find on [Dev.To](https://dev.to/bluszcz/static-site-generator-with-strapi-4-and-jekyll-5afp) but also on [Medium](https://medium.com/@bluszcz/static-site-generator-with-strapi-4-and-jekyll-4c5404cc9715).