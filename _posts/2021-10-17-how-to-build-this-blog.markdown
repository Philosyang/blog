---
layout: post
title:  "How to Build this Blog"
date:   2021-10-17 15:33:00 -0500
categories: jekyll
---
Took me a while and some hiccups to get this jekyll thing running.

**The main issue:** I wanted my blog to be at `https://philosyang.com/blog` instead of `https://philosyang.com` (I still want my homepage right there). I was trying to achieve this by buliding a new jekyll blog inside a new folder of my `github.io` repo, but it failed to work (No, just changing `baseurl` and `url` did not work).

[This post](https://shahrajat.com/2016-06-22-install-jekyll-subdirectory-blog-github-pages/) helped me a lot, but it brought me a hiccup as well, so I will list out my steps below:

1. Need "Ruby **with devkit**", I am using Windows, so I used RubyInstaller from [here](https://rubyinstaller.org/downloads/).
1. `gem install jekyll`; I can't recall clearly but it asked me to input 1-3 to choose something at the cmd and I chose 1.
1. Create a new repo named `blog` on GitHub.
1. `git clone` to local.
1. **do `jekyll new blog` but drag everything `.\blog` out to the parent dir `.\`, `.\blog` should be empty now, can delete `.\blog` safely.** (I don't know if you can do `jekyll new` to prevent the cut and paste, you can try.)
1. `git checkout -b gh-pages` so that GitHub knows this branch is used as a GitHub Pages Project. ([ref](https://stackoverflow.com/questions/23417062/getting-jekyll-running-just-for-a-subdirectory-on-github))
1. We can now go to the jekyll `_config.yml` and change `baseurl: "/blog"` and `url: "https://yourdomainhere.com"`. This means we will visit our blog at `https://yourdomainhere.com/blog`.
1. `jekyll serve` at `.\` should be successful. If having `Load error: cannot load such file – webrick`, try `bundle add webrick` then `jekyll serve` again. ([ref](https://talk.jekyllrb.com/t/load-error-cannot-load-such-file-webrick/5417/3))
1. That's basically all. Do the usual commit and push, and the blog should be live.

At least everything worked out eventually.