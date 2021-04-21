---
layout:     post
title:      Microsoft Lizenzen auslesen
date:       2014-06-08 12:32:18
summary:    Microsoft - Windows, Office Linzenzen auslesen
categories: jekyll
thumbnail: jekyll
tags:
 - thumbnails
 - carte noire
---

Lizenzen / Keys mit `ProduKey` auslesen.
<br>Download:[ProduKey][1].


## Images

DIGIMOMTo use your own custom images as a thumbnail you must upload them to a web available
location (I use [Imgur][3]) and then you need to add the url to `_data/thumbnail.yml`
with an associated keyword.
Digimon

```
jekyll: "http://i.imgur.com/aRQcGSi.png"
```

You then add a `thumbnail` option to the article's frontmatter and provide the keyword
for that thumbnail.

```
thumbnail: jekyll
```

This allows you to re-use thumbnails across multiple articles without having to
specify the url each time.

## Font Awesome

If jekyll can't find a corresponding image in your `thumbnail.yml` file then it
will assume you want to use a Font Awesome icon instead. You can find the full
list of Font Awesome icons [here][4].

So for example if your article is about android and you want to use the [android icon][5]
from font awesome you can just specify the following in your frontmatter.

```
thumbnail: android
```

Then in the future if you decide you want to use your own android icon you can just
add it to `_data/thumbnails.yml` which will override it for all articles using
the android thumbnail.

[1]: http://www.nirsoft.net/utils/product_cd_key_viewer.html
[2]: http://fortawesome.github.io/Font-Awesome/
[3]: http://imgur.com/
[4]: http://fortawesome.github.io/Font-Awesome/icons/
[5]: http://fortawesome.github.io/Font-Awesome/icon/android/
