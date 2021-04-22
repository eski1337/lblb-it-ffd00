---
layout: post
title: Nur ein kleiner Test!
date: '2021-04-22T12:31'
summary: lol Test 
categories: Passwort
tags:
  - test
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

