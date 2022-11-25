---
layout: single
title:  "Experiments with Minimal Mistakes"
date:   2022-11-25 19:32:00 +0100
categories: development jekyll
---
Yesterday I dedicated some time to investigate [Minimal Mistakes](https://mmistakes.github.io/). I would say that it well spent time - blog is running now on this theme.

In general theme works fine. The only problem which I had was a local building of the blog ;) I was facing following error:

```
Build Warning: Layout 'single' requested in _posts/2022-07-24-welcome-to-jekyll.markdown does not exist.
```

Not really helpful?

Under [this link](https://github.com/mmistakes/minimal-mistakes/issues/2071#issuecomment-769329832) I have found following recipe:

Add to `_config.yml`:

```yaml
plugins:
  - jekyll-remote-theme
```

Add to `Gemfile`:

```conf
gem 'jekyll-remote-theme'
```

Execute:

```bash
bundle update
```

Now everything should work as expected:

```bash
➜  bluszcz.github.io git:(main) bundle exec jekyll serve 
Configuration file: /home/bluszcz/Dev/bluszcz.github.io/_config.yml
            Source: /home/bluszcz/Dev/bluszcz.github.io
       Destination: /home/bluszcz/Dev/bluszcz.github.io/_site
 Incremental build: disabled. Enable with --incremental
      Generating... 
      Remote Theme: Using theme mmistakes/minimal-mistakes
       Jekyll Feed: Generating feed for posts
                    done in 7.15 seconds.
 Auto-regeneration: enabled for '/home/bluszcz/Dev/bluszcz.github.io'
    Server address: http://127.0.0.1:4000/
  Server running... press ctrl-c to stop.
```

Right now I am investigating *Collections* and *Pages* to incorporate some sort of ***Portfolio*** page.