---
layout:     post
title:      Teilsynchronisierte Profile
date:       2021-04-21
author:     watchme
summary:    Roamingprofil wurde nicht vollständig synchronisiert.
categories: Windows Server
thumbnail:  cogs
tags:
 - windows
 - server
 - roaming
 - synchronisiert
 - profil
 - teil
---

## Roamingprofil wurde nicht vollständig synchronisiert

<h4>Mit Windows Server 2016 und 2019 hat MS die Art geändert, mit der die Windows Suche arbeitet.
So kann es geschehen, dass bei einem der neuen Server die Roamingprofile nicht mehr korrekt synchronsiert werden können sobald Windows Search aktiviert ist.  
  
Um dies zu beheben muss folgender Ordner aus den Roamingprofilen ausgeschlossen werden:</h4>
<b>AppData\Roaming\Microsoft\Search\Data\Applications</b>


<h4>Dazu am besten folgende Gruppenrichtlinie erstellen:</h4>
  - <b>WIN + R -> gpedit.msc</b>

```
- Benutzerkonfiguration
- Administrative Vorlagen
- System
- Benutzerprofile
- Verzeichnisse aus servergespeichertem Profil ausschließen
- Status - aktiviert
- Folgende Verzeichnisse vom servergespeicherten Profil ausschließen - <br>AppData\Roaming\Microsoft\Search\Data\Applications</br> 
```

Alternativ kann die Option auch in der Registry eingestellt werden:
  - <b>WIN + R -> regedit</b>
1. Dazu den folgenden Pfad in der Registry aufrufen:
```
Computer\HKEY_CURRENT_USER\SOFTWARE\Microsoft\Windows NT\CurrentVersion\Winlogon
```
2. Den Folgenden Eintrag zur Zeichenfolge **ExcludeProfileDirs** hinzufügen:
```
AppData\Roaming\Microsoft\Search\Data\Applications
```

## Inhalt einer Registry-Datei um die Einstellung automatisch vorzunehmen:

```
Windows Registry Editor Version 5.00

[HKEY_CURRENT_USER\SOFTWARE\Microsoft\Windows NT\CurrentVersion\Winlogon]
"ExcludeProfileDirs"="AppData\\Local;AppData\\LocalLow;$Recycle.Bin;OneDrive;Work Folders"
```