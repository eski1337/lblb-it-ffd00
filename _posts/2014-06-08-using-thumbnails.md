---
layout:     post
title:      Microsoft Lizenzen auslesen
date:       21-04-2021 16:32:18
summary:    Microsoft - Windows, Office Linzenzen auslesen
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