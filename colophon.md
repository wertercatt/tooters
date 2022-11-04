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

## <small>Publishing</small>

All of the blog posts are written in [Markdown](https://daringfireball.net/projects/markdown/) and converted to static markup by the [Jekyll](https://jekyllrb.com) engine. Functionality for the site is constructed with Shopify's [Liquid](https://shopify.github.io/liquid/) template language and written in Ruby. The design is crafted using valid [HTML5](https://validator.w3.org/nu/?doc=https%3A%2F%2Fvictorwynne.com%2F) and [CSS3](https://jigsaw.w3.org/css-validator/validator?uri=https%3A%2F%2Fvictorwynne.com&profile=css3svg&usermedium=all&warning=0&vextwarning=) and the feed is valid [RSS](https://validator.w3.org/feed/check.cgi?url=https%3A%2F%2Fvictorwynne.com%2Ffeed.xml). Domain registration and DNS is handled with [Hover](https://hover.com/) and hosting is from [Netlify](https://www.netlify.com) deploying a [GitHub](https://www.github.com/victorwynne/victorwynne/) repo.

ISSN: [2831-2880](https://portal.issn.org/resource/ISSN/2831-2880)<br>

## <small>Syndicated Feeds</small>

Full Feed: [victorwynne.com/feed.xml](https://victorwynne.com/feed.xml)<br>
Articles: [victorwynne.com/articles.xml](https://victorwynne.com/articles.xml)<br>
Links: [victorwynne.com/links.xml](https://victorwynne.com/links.xml)

## <small>Software</small>

[AirBuddy](https://v2.airbuddy.app)<br>
[AlDente](https://apphousekitchen.com)<br>
[Apollo](https://apolloapp.io)<br>
[Audio Hijack](https://rogueamoeba.com/audiohijack)<br>
[BBEdit](https://www.barebones.com/products/bbedit)<br>
[Bear](https://bear.app)<br>
[Cakebrew](https://www.cakebrew.com)<br>
[CARROT Weather](https://www.meetcarrot.com/weather)<br>
[DaisyDisk](https://daisydiskapp.com)<br>
[Deliveries](https://deliveries.app/en.html)<br>
[Displaperture](https://manytricks.com/displaperture)<br>
[Downie](https://software.charliemonroe.net/downie)<br>
[Drafts](https://getdrafts.com/)<br>
[Fantastical](https://flexibits.com/fantastical)<br>
[Final Cut Pro](https://www.apple.com/final-cut-pro/)<br>
[Flighty](https://www.flightyapp.com)<br>
[Homebrew](https://brew.sh)<br>
[IINA](https://iina.io)<br>
[iStat Menus](https://bjango.com/mac/istatmenus)<br>
[Kaleidoscope](https://kaleidoscope.app)<br>
[Keyboard Maestro](https://www.keyboardmaestro.com/main/)<br>
[Nova](https://nova.app)<br>
[Oh My Zsh](https://ohmyz.sh)<br>
[OpenEmu](https://openemu.org)<br>
[Overcast](https://overcast.fm)<br>
[Parcel](https://parcelapp.net)<br>
[Pastel](https://www.highcaffeinecontent.com/blog/20200610-Pastel)<br>
[Path Finder](https://www.cocoatech.io)<br>
[PCalc](https://www.pcalc.com/mac)<br>
[Pixelmator Pro](https://www.pixelmator.com/pro)<br>
[Raindrop](https://raindrop.io)<br>
[Rectangle](https://rectangleapp.com)<br>
[Reeder](https://reederapp.com)<br>
[ScreenFlow](https://www.telestream.net/screenflow/overview.htm)<br>
[SF Symbols](https://developer.apple.com/sf-symbols)<br>
[Sketch](https://www.sketch.com)<br>
[TextMate](https://macromates.com)<br>
[Things](https://culturedcode.com/things/)<br>
[Tower](https://www.git-tower.com/mac)<br>
[Transmit](https://panic.com/transmit)<br>
[Tweetbot](https://tapbots.com/tweetbot/mac)<br>
[Typora](https://typora.io)<br>
[WaterMinder](https://waterminder.com)<br>
[Working Copy](https://workingcopyapp.com)<br>
[Xcode](https://developer.apple.com/xcode)

## <small>Stats</small>

Posts: {{ site.posts.size }}<br>
Words: {{ totalWords | number_with_delimiter: delimiter: ',' }}<br>
Build: {{ site.time | date: '%R %Z' }} on {{ site.time | date_to_long_string: "ordinal", "US" }}

## <small>Contact</small>

Twitter: [@victorwynne](https://twitter.com/victorwynne/)<br>
Email: <a href="mailto:hello@victorwynne.com">hello@victorwynne.com</a><br>
PGP: [public key](https://victorwynne.com/key.txt)

## <small>Privacy</small>

Everything about this website is static. There is zero PHP, JavaScript, Python or Perl. No server databases, no analytics. Not even a single cookie. None of your personal data is collected, tracked or stored because it physically cannot be. §
<br><br>
