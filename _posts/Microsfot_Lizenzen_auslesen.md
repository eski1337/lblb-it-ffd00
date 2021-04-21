---
layout: post
title: Microsoft Lizenzen auslesen Teil 2
date: '2020-04-21T12:31'
summary: 'Microsoft - Windows, Office Linzenzen auslesen'
categories: jekyll
thumbnail: jekyll
tags:
  - thumbnails
  - carte noire
---


## ProduKey


Lizenzen / Keys mit `ProduKey` auslesen.
<br>Download: [ProduKey][1]


## Powershell

Win+R -> powershell
```
(Get-WmiObject -query 'select * from SoftwareLicensingService').OA3xOriginalProductKey

```



[1]: http://www.nirsoft.net/utils/produkey.zip