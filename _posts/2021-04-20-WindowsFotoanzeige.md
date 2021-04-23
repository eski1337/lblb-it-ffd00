---
layout: post
title: Windows Fotoanzeige
date: '2021-04-20'
author: watchme
summary: Windows Fotoanzeige kann nicht verwendet werden.
categories: Windows Server
thumbnail: cogs
tags:
  - windows
  - server
  - fotoanzeige
  - vorschau
  - foto
---
## Windows Fotoanzeige auf Windwows Server 2016++

Per Default werden Bilder in Paint geöffnet – die Windows Fotoanzeige ist aber weiterhin enthalten und kann manuell wieder aktiviert werden.\
Folgende Schritte müssen unternommen werden um die Fotoanzeige wieder verfügbar zu machen.

1.  Zuerst müssen die passenden DLLs regisitriert werden.
    *   CMD als Administrator ausführen und die folgenden Befehle eingeben
    
```PHP
regsvr32 “C:\Program Files (x86)\Windows Photo Viewer\PhotoViewer.dll”

regsvr32 “C:\Program Files\Windows Photo Viewer\PhotoViewer.dll”
```

2.  In der Registry einen Eintrag als Zeichenfolge für den jeweiligen Dateityp anlegen unter:
    *   WIN + R -> regedit

```c++
    Computer\\HKEY_LOCAL_MACHINE\SOFTWARE\Microsoft\Windows Photo Viewer\Capabilities\\FileAssociations
```
Beispielhafter Inhalt einer .reg-Datei um typische Bild-Dateien mit der Windows Fotoanzeige zu verknüpfen.

    Windows Registry Editor Version 5.00

    [HKEY_LOCAL_MACHINE\SOFTWARE\Microsoft\Windows Photo Viewer\Capabilities\FileAssociations]
    ".tif"="PhotoViewer.FileAssoc.Tiff"
    ".tiff"="PhotoViewer.FileAssoc.Tiff"
    ".jpg"="PhotoViewer.FileAssoc.Tiff"
    ".png"="PhotoViewer.FileAssoc.Tiff"
