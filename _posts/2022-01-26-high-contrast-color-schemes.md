---
layout: post
title: "High Contrast Color Schemes"
date: 2022-01-26 12:00
categories: [Announcements]
tags: [design, quattle, accessibility]
---

I am now including an accessibility minded high contrast color scheme version of my website for both light and dark mode. I have been including features such as captions and alt text for screen readers for some time but this addition was long overdue[^1].

Handling this with Jekyll is as simple as maintaining a [separate branch](https://github.com/victorwynne/victorwynne/tree/a11y) and merging commits unrelated to styling differences from `main` to ensure consistency when publishing new posts/pages or making site-wide design/config changes.

The ability to use {% raw %} `{{ site.baseurl }}` {% endraw %} Liquid tags rather than hard coding links is very important here. As one example; a reader who prefers the high contrast design can subscribe to an RSS feed that links back to the sub-domain for the specified branch. Mine resides at [a11y.victorwynne.com](https://a11y.victorwynne.com) and has the same assets available but a hard coded link in this example would lead the reader to the root domain styling or require multiple versions of the same file. Start creating many branches and this becomes quite messy and totally unnecessary. Liquid and Ruby handle this beautifully, so let them.

This branch method will also be used in the future as a way to include more default color schemes in [Quattle](https://github.com/victorwynne/). Current plans are to roll this high contrast branch out in the v1.5.0 release sometime next month.

***

[^1]: Code blocks and syntax highlighting have not yet been given the high contrast treatment but will be updated soon.
