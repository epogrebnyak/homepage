+++
title = "Setting Up Academic Theme"
date = 2019-03-15T10:57:57+03:00
draft = false

# Tags and categories
# For example, use `tags = []` for no tags, or the form `tags = ["A Tag", "Another Tag"]` for one or more tags.
tags = ["hugo", "setup"]
categories = []

+++

[Academic theme](https://sourcethemes.com/academic/) is great, well-thought in design and popular with users. Below is a track record of my site setup using Hugo and Academic. 

Precursor
---------

I'm migrating from a [Jekyll-based CV theme](https://github.com/sharu725/online-cv) to Academic. CV 
had a clean look and helped me to sort out my personal information, but it was not easily extensible. I did set it up once on Github Pages and rarely updated. 

As for site generators in general, Jekyll still looks a bit more popular than Hugo based on Github 
stars, but I like Hugo better, because of the following:
 
- definitive separation of content and presentation
- a bit less blog-oriented (more themes to build non-blog sites)
- supplied as a binary, not a library (you do not need Golang installation for Hugo, but you are
using Ruby environment for Jekyll)
- finally, because it has Academic theme.

My setup
--------

Some steps in my site setup I have spent a bit extra time with:

- contacts section configuration explained in [Leslie Myint blog post](https://lmyint.github.io/post/hugo-academic-tips/#modifying-contact-section)
- added StackOverflow fas icon (had to look up a font library, can be provided by default)
- contact form by https://formspree.io will need activation (both on `localhost` and your server)
- added personal photo as `avatar.png` (from the layout code it appears that file extension  does not matter)
- replaced favicon as [suggested in docs](https://sourcethemes.com/academic/docs/customization/#website-icon)


I disabled the following sections:

- people and groups - probably good for another, more collaborative site
- `publications`, `featured` (duplicated, not filled yet)
- `skills` (great look, had it in Jekyll CV, but how do you access + must move off the front page)
- `accomplishments` (must put a list of econometrics courses in)
- `talks` (would be nice to recollect!)
- `experience` (to fill later, was not filled in a CV)
- `hero` widget

Also moved several files (including `.sh`) to `ignore` folder - cleans root of the repository. 


Is blog a relic?
----------------

I first disabled the blog too. I thought of blogging as such an archaic activity, but now I see it as a form of notetaking and knowledge management. And the best way of managing some internal knowledge is:

<blockquote class="twitter-tweet"><p lang="en" dir="ltr">The most effective way to share knowledge within your organization is to share it with the whole world</p>&mdash; Chris Whong (@chris_whong) <a href="https://twitter.com/chris_whong/status/1106170436411445249?ref_src=twsrc%5Etfw">March 14, 2019</a></blockquote> <script async src="https://platform.twitter.com/widgets.js" charset="utf-8"></script> 

Why filtering?
--------------

Also is [Academic documentation web site](https://sourcethemes.com/academic) blocking traffic from Russia? A provider thing or site configuration? Had to use a proxy to access it, but the proxy also interferes with `localhost` - rather messy.

UPDATE: blocking no more as of 16-03-2019. Maybe a coffee helped.

Gratitude
---------

I [paid up for a coffee](https://sourcethemes.com/academic/#support) to Academic on paypal.  A small gratitude to an open source project.