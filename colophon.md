---
layout: page
permalink: /colophon/
title: Colophon
---

{% assign totalWords = 0 %}
{% assign dateOb = '' %}

{% for post in site.posts %}
	{% assign postWords = post.content | number_of_words %}
	{% assign totalWords = totalWords | plus:  postWords %}
	{% assign pd = post.date | date: "%Y-%m-%d" %}
	{% unless forloop.first %}
		{% assign dateOb = dateOb | append: "," %}
	{% endunless %}
	{% assign dateOb = dateOb | append: pd %}
{% endfor %}

This website is authored, produced, designed and developed by Victor Wynne.

## <small>Publishing</small>

All of the blog posts are written in [Markdown](https://daringfireball.net/projects/markdown/) and converted to static markup by the [Jekyll](https://jekyllrb.com) engine. Functionality for the site is constructed with Shopify's [Liquid](https://shopify.github.io/liquid/) template language and written in Ruby. The design is crafted using valid [HTML5](https://validator.w3.org/nu/?doc=https%3A%2F%2Fvictorwynne.com%2F) and [CSS3](https://jigsaw.w3.org/css-validator/validator?uri=https%3A%2F%2Fvictorwynne.com&profile=css3svg&usermedium=all&warning=0&vextwarning=) and the feed is valid [RSS](https://validator.w3.org/feed/check.cgi?url=https%3A%2F%2Fvictorwynne.com%2Ffeed.xml). Domain registration and DNS is handled with [Hover](https://hover.com/) and hosting is provided by [Netlify](https://www.netlify.com) deploying from the [GitHub](https://www.github.com/victorwynne/victorwynne/) repo.

## <small>Accessibility</small>

A high contrast version of this website is available at [a11y.victorwynne.com](https://a11y.victorwynne.com)

## <small>Syndicated Feeds</small>

Full feed: [victorwynne.com/feed.xml](https://victorwynne.com/feed.xml)

Articles: [victorwynne.com/articles.xml](https://victorwynne.com/articles.xml)

Links: [victorwynne.com/links.xml](https://victorwynne.com/links.xml)

## <small>Software</small>

[AirBuddy](https://v2.airbuddy.app)<br>
[AlDente](https://apphousekitchen.com)<br>
[Apollo](https://apolloapp.io)<br>
[BBEdit](https://www.barebones.com/products/bbedit/)<br>
[CARROT Weather](https://www.meetcarrot.com/weather/)<br>
[DaisyDisk](https://daisydiskapp.com)<br>
[Displaperture](https://manytricks.com/displaperture/)<br>
[Fantastical](https://flexibits.com/fantastical)<br>
[Homebrew](https://brew.sh)<br>
[IINA](https://iina.io)<br>
[iStat Menus](https://bjango.com/mac/istatmenus/)<br>
[Nova](https://nova.app)<br>
[Oh My Zsh](https://ohmyz.sh)<br>
[Parcel](https://parcelapp.net)<br>
[PCalc](https://www.pcalc.com/mac/)<br>
[Pixelmator Pro](https://www.pixelmator.com/pro/)<br>
[Raindrop](https://raindrop.io)<br>
[Reeder](https://reederapp.com)<br>
[SF Symbols](https://developer.apple.com/sf-symbols/)<br>
[Sketch](https://www.sketch.com)<br>
[TextMate](https://macromates.com)<br>
[Transmit](https://panic.com/transmit/)<br>
[Tweetbot](https://tapbots.com/tweetbot/mac/)<br>
[Typora](https://typora.io)<br>
[Xcode](https://developer.apple.com/xcode/)

## <small>Stats</small>

Total Published Posts: {{ site.posts.size }}<br>
Total Words Written: {{ totalWords | number_with_delimiter: delimiter: ',' }}<br>
Build: {{ site.time | date: '%R %Z' }} on {{ site.time | date_to_long_string: "ordinal", "US" }}

## <small>Privacy</small>

Everything about this website is static. There is zero PHP, JavaScript, Python or Perl. No server databases, no analytics. Not even a single cookie. None of your personal data is collected, tracked or stored because it physically cannot be.
