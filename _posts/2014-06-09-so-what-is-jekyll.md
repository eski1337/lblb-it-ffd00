---
layout: post
title: WLAN Passwort auslesen (CMD)
date: '2014-06-02T12:31'
summary: Wie man das WLAN Passwort per CMD ausliest
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
Das "WLAN-NAME" durch den richtigen Namen des Netzes ersetzen.<br>
Ggf. " " hinzufügen wenn der Name ein Leerzeichen enthält.

