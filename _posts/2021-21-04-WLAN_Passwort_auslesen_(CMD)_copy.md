---
layout: post
title: WLAN Passwort auslesen (CMD)
date: '2021-04-21T12:31'
author:     eski
summary: Wie man das WLAN Passwort per CMD ausliest
categories: Passwort
thumbnail:  cogs
tags:
  - wlan
  - passwort
  - auslesen
  - CMD
---

## WLAN Passwort per CMD auslesen
<br>

__WIN__ + __R__ -> __cmd__
```
netsh wlan show profile WLAN-NAME key=clear
```
Das "WLAN-NAME" durch den richtigen Namen des Netzes ersetzen.<br>
Ggf. " " hinzufügen wenn der Name ein Leerzeichen enthält.

