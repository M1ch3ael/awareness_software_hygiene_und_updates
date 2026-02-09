---
title: "Software Updates"
weight: 2
---

# Software Updates

## Einleitung

Der [Software Hygiene Teil]({{<ref "hygiene.md">}}) hat uns gezeigt, warum es wichtig ist, einen möglichst kleine Angriffsfläche zu bieten. Jedoch ist für die produktive Nutzung eines Laptops, PCs oder Smartphone dennoch zusätzliche Software nötig. Doch wie geht man mit dieser Software um?
Diese Software auf dem aktuellen Stand zu halten ist eine der wichtigsten Maßnahemn um die IT-Sicherheit zu verbessern. Denn Updates schließen bekannte Schwachstellen, die sonst Angreifer ausnutzen können. Trotzdem werden Patches oft verzögert installiert - aus Unwissenheit, Misstrauen oder Bequemlichkeit. Deshalb soll es hier darum gehen, warum regelmäßige Aktualisierungen wichtig sind, wie Updates kommiziert werden und welche Update-Strategien von Herstellern genutzt werden um Updates an Anweder zu verteilen.

## Grundproblem

Sehr viele Menschen unterschätzen den Nutzen von Softwareupdates. Sicherheitsexpertinnen und -experten sehen das zeitnahe Einspielen von Sicherheitsupdates als eine der effektivsten Schutzmaßnahmen an - sogar noch vor Passwortmanagern und der Zwei-Faktor-Authentifizierung. So kommt es eben dazu, dass Teilweise innerhalb von einer Woche nach der Veröffentlichung des Updates erst 50 % der Anwender das Update auch durchführen, obwohl nach dem Veröffentlichen des Updates häufig die Angriffsraten auf die in dem Update verbesserte Schwachstelle stark ansteigen.
![Prozentualer Unterschied](Differnce_Experts_Non-IT.png)

> Aus [““...No one Can Hack My Mind”: Comparing Expert and Non-Expert Security Practices, Ion et al.](https://www.usenix.org/system/files/conference/soups2015/soups15-paper-ion.pdf)

> https://www.verbraucherzentrale.nrw/wissen/digitale-welt/apps-und-software/softwareupdates-deshalb-sind-sie-wichtig-81285

## Gründe für Verzögerungen

Aber aus welchen Gründen werden Updates nicht zeitnah eingespielt? Einige Studien haben dies untersucht und folgende Hauptthemen herausgearbeitet:

- Unklarer Nutzen: Wie oben bereits erklärt ist vielen der Nutzen eines Updates gar nicht bewusst. Häufig wird ein Update nur wegen der neuen Funktionen installiert, nicht aber weil die Sicherheit verbessert wurde.
- Angst vor Problemen: Zudem könnten Updates auch bösartigen Inhalt mithliefern bzw. neue Fehler beinhalten.
- Unverständlicher Prozess: Bei vielen Anwendungen ist es nicht wirklich ersichtlich welche Änderungen ein Update mitbrigt, bzw. wieso man dieses Update jetzt installieren soll.
- Manuelle Abläufe: Eine fehlende Automatisierung des Update-Prozesses ist teilweise herausfordernd für den Anwender und bietet Möglichkeiten für Angriffe (siehe [Quellen]({{<ref "quellen.md">}}))

![xkcd Comic](xkcd_comic.png)

> https://xkcd.com/1328/

## Konkrete Folgen (Beispiele)

Doch was kann passieren wenn Updates nicht eingespielt werden und so Sicherheitslücken weiterhin vorhanden sind:
Hierfür gibt es unzählige Beispiele wir schauen uns hier zwei besonders schwerwiegende bzw. weitreichende Fälle an, die hätten durch ein Update verhindert werden können.

### EternalBlue und WannaCry

EternalBlue ist eine Schwachstelle im SMB‑Protokoll, die 2017 bekannt wurde (CVE‑2017‑0144). Sie wurde von der Schadsoftware WannaCry massenhaft ausgenutzt und infizierte Hunderttausende Rechner weltweit, darunter Krankenhäuser und Unternehmen. Dabei wird eine Lücke in einem alten Dienst (SMBv1) unter Windows benutzt, der eigentlich dazu dient um Dateien und Drucker im Netzwerk zu teilen. Zwar hatte Microsoft schnell einen Patch veröffentlicht der das Problem behebt, hatten viele Organisationen diesen nicht installiert.

https://www.youtube.com/watch?v=88jkB1V6N9w

### WinRAR

WinRAR ist ein Packprogramm, das auf vielen Windowsrechner installiert. Daher ist es immer wieder ein belibtes Ziel von Angriffen. Zuletzt bzw. immernoch wird eine Schwachstelle ausgenutzt, die es ermöglicht, über speziell perparierte Dateien (z. B. PDFs) in den Ordner für die Startprogramme zu schreiben und dort eine Malware zu platzieren, die beim nächsten Log-in automatisch gestartet wird. Diese Sicherheitslücke mit dem Namen CVE-2025-8088 besteht bereits seit Mitte des Jahres 2025. Diese wurde im selben Monat gepacht, also die Sicherheitlücke gestopft, und dennoch wird noch Ende Januar von verschiedenen Akteuren weiter ausgenutzt.

https://www.heise.de/news/Angriffe-auf-WinRAR-Luecke-laufen-weiter-11157132.html
https://www.youtube.com/watch?v=rkMNOC8fhUQ

# Updates besser verstehen

## Was ist ein Update?

Aber gehen wir nochmal ein Schritt zurück und schauen uns an was ein Update ist:
Eine Aktualisierung bringt Software auf den neuesten Stand, indem sie Fehler behebt, Funktionen ergänzt oder Sicherheitslücken schließt. Entwicklerinnen und Entwickler veröffentlichen in der Regel **Changelogs** oder **Release Notes**, die Änderungen in Kategorien wie Neu, Verbesserungen, Fehlerbehebungen und Sicherheit auflisten. Sicherheitsrelevante Einträge sind besonders zeitkritisch.

## Changelog Beispiel

**[3.2.0] – 2026‑01‑01**

**Neu**

- Dark Mode für bessere Nutzung am Abend.
- Überarbeitete Startseite mit schnellerem Zugriff auf Favoriten.

**Verbesserungen**

- Schnellere Synchronisierung zwischen Geräten.
- Optimierte Push‑Benachrichtigungen.

**Fehlerbehebungen**

- Doppelanzeige von Benachrichtigungen behoben.
- Absturz beim Öffnen der Einstellungen korrigiert.

**Sicherheit**

- Aktualisierung einer internen Netzwerkbibliothek zur Behebung der Schwachstelle CVE‑2025‑12345.
- Verbesserte Prüfungen bei der Anmeldung.

(Dieses Beispiel ist fiktiv.)

## Sicherheitsupdates versus Funktionsupdates

- **Sicherheitsupdates** schließen Schwachstellen und sollten so schnell wie möglich installiert werden.
- **Funktionsupdates** bringen neue Features; sie sind wichtig, aber meist weniger zeitkritisch.

**Weil Releases häufig beides kombinieren und keine Wahl lassen, gilt: Alle Updates sollten zeitnah geprüft und installiert werden.**

## Wie Updates verteilt werden

### Vollautomatische Updates

Die Anwendung prüft im Hintergrund auf Updates und installiert sie automatisch. Vorteil: schnelle Verteilung; Nachteil: gelegentliche Neustarts.

### Halbautomatische Updates

Die Software meldet ein verfügbares Update und fragt nach Bestätigung für Installation oder Neustart. Vorteil: Nutzerkontrolle; Nachteil: Verzögerung möglich.

### Manuelle Online‑Updates

Nutzerinnen und Nutzer starten die Update‑Suche in den Einstellungen und bestätigen Downloads manuell.

### Manuelle Offline‑Updates

Updates werden nur auf der Herstellerwebseite bereitgestellt; Nutzer müssen aktiv herunterladen und installieren.

## Wo Updates herkommen

### Interne Update‑Mechanismen

Einige Hersteller oder Anbieter verteilen Updates direkt über eigene Server oder Management‑Tools.

### App Stores

Stores wie Google Play, App Store, Microsoft Store oder Mac App Store verwalten Installation und Aktualisierung vieler Apps zentral.

### Herstellerwebseiten

Treiber und Spezialsoftware werden oft direkt auf den Herstellerseiten angeboten.

### Paketmanager

Unter Linux sind Paketmanager (apt, yum, dnf, zypper) Standard. Unter Windows gibt es seit einigen Jahren **winget**; für macOS nutzen viele **Homebrew**.

## Übersicht Updateverteilung

| Quelle             | Mechanismus                                    | Beispiele                               | Vorteile                   | **Empfehlung**                                      |
| ------------------ | ---------------------------------------------- | --------------------------------------- | -------------------------- | --------------------------------------------------- |
| Betriebssystem     | Automatisch; Halbautomatisch; Manuell          | Windows Update, macOS Softwareupdate    | Deckt OS‑Sicherheitslücken | **Automatische Updates prüfen/anschalten**          |
| App Store          | Automatisch; Halbautomatisch                   | Google Play, App Store, Microsoft Store | Zentrale Verwaltung        | **Automatische App‑Updates aktivieren**             |
| In‑App Updater     | Automatisch; Halbautomatisch; Benachrichtigung | Browser, PDF‑Reader, Spiele             | Schnelle Verfügbarkeit     | **Regelmäßig nach Udpates suchen und installieren** |
| Herstellerwebseite | Manuell; Halbautomatisch                       | Grafikkartentreiber, Spezialsoftware    | Direkt vom Hersteller      | **Nur offizielle Downloads verwenden**              |
| Paketmanager       | Automatisch; Halbautomatisch                   | apt, winget, Homebrew                   | Batch‑Updates              | **Für technisch Interessierte geeignet** UnigetUI   |

## Empfehlungen

- **Automatische Updates aktivieren** für Betriebssystem und Browser.
- **App‑Store‑Updates erlauben** für alle Apps aus App-Stores.
- **Bei manuellen Downloads** nur offizielle Herstellerseiten nutzen vgl [Sichere Quellen]({{<ref "quellen.md">}}).
