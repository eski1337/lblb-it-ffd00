---
layout:     post
title:      WLAN Passwort auslesen (CMD)
date:       21-04-2021 16:32:18
summary:    Wie man das WLAN Passwort per CMD ausliest
categories: jekyll
thumbnail: jekyll
tags:
 - about
 - jekyll
---

## WLAN Passwort per CMD auslesen

WIN+R -> cmd
```
netsh wlan show profile WLAN-NAME key=clear
```
Das "WLAN-NAME" durch den richtigen Namen des Netzes ersetzen.
ggf. "" hinzufügen wenn der Name ein Leerzeichen enthält.

