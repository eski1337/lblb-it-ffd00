---
layout: post
title: Microsoft Lizenzen auslesen
date: '2021-04-21T12:31'
author:     eski
summary: 'Microsoft - Windows, Office Linzenzen auslesen'
categories: Lizenzen Windows
thumbnail:  cogs
tags:
  - Microsoft
  - Lizenz auslesen
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