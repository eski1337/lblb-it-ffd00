---
layout: post
title: Nur ein kleiner Test!
date: '2022-04-21T12:31'
summary: Wie man das WLAN Passwort per CMD ausliest
categories: Passwort
tags:
  - wlan
  - passwort
  - auslesen
  - CMD
---

## WLAN Passwort per CMD auslesen

WIN+R -> cmd
```
netsh wlan show profile WLAN-NAME key=clear
```
Das "WLAN-NAME" durch den richtigen Namen des Netzes ersetzen.<br>
Ggf. " " hinzufügen wenn der Name ein Leerzeichen enthält.

