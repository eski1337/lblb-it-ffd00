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

<h5>Mit Windows Server 2016 und 2019 hat MS die Art geändert, mit der die Windows Suche arbeitet.
So kann es geschehen, dass bei einem der neuen Server die Roamingprofile nicht mehr korrekt synchronsiert werden können sobald Windows Search aktiviert ist.  
  
Um dies zu beheben muss folgender Ordner aus den Roamingprofilen ausgeschlossen werden:  </h5>
**AppData\Roaming\Microsoft\Search\Data\Applications**  


Dazu am besten folgende Gruppenrichtlinie erstellen:
  - WIN + R -> gpedit.msc

```
- Benutzerkonfiguration
- Administrative Vorlagen
- System
- Benutzerprofile
- Verzeichnisse aus servergespeichertem Profil ausschließen
- Status - aktiviert
- Folgende Verzeichnisse vom servergespeicherten Profil ausschließen - AppData\Roaming\Microsoft\Search\Data\Applications  
```

Alternativ kann die Option auch in der Registry eingestellt werden:
  - WIN + R -> regedit
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