---
title: "Software Updates"
weight: 2
---

# Software Updates

## Einleitung

Der [Software Hygiene Teil]({{<ref "hygiene.md">}}) hat uns gezeigt, warum es wichtig ist, einen möglichst kleine Angriffsfläche zu bieten. Jedoch ist für die produktive Nutzung eines Laptops, PCs oder Smartphone dennoch zusätzliche Software nötig. Doch wie geht man mit dieser Software um?
Apps, Programme und Betriebssysteme auf dem aktuellen Stand zu halten ist eine der wichtigsten Maßnahemn um die IT-Sicherheit zu verbessern. Denn Updates schließen bekannte Schwachstellen, die sonst Angreifer ausnutzen können. Trotzdem werden Patches oft verzögert installiert - aus Unwissenheit, Misstrauen oder Bequemlichkeit. Deshalb soll es hier darum gehen, warum regelmäßige Aktualisierungen wichtig sind, wie Updates kommiziert werden und welche Update-Strategien von Herstellern genutzt werden um Updates an Anweder zu verteilen.

## Grundproblem

Sehr viele Menschen unterschätzen den Nutzen von Softwareupdates. Sicherheitsexpertinnen und -experten sehen das zeitnahe Einspielen von Sicherheitsupdates als eine der effektivsten Schutzmaßnahmen an - sogar noch vor Passwortmanagern und der Zwei-Faktor-Authentifizierung. So kommt es eben dazu, dass Teilweise innerhalb von einer Woche nach der Veröffentlichung des Updates erst 50 % der Anwender das Update auch durchführen, obwohl nach dem Veröffentlichen des Updates häufig die Angriffsraten auf die in dem Update verbesserte Schwachstelle stark ansteigen.
![Prozentualer Unterschied](Differnce_Experts_Non-IT.png)

> Aus [““...No one Can Hack My Mind”: Comparing Expert and Non-Expert Security Practices, Ion et al.](https://www.usenix.org/system/files/conference/soups2015/soups15-paper-ion.pdf)

> https://www.verbraucherzentrale.nrw/wissen/digitale-welt/apps-und-software/softwareupdates-deshalb-sind-sie-wichtig-81285

## Gründe für Verzögerungen

Aber aus welchen Gründen werden Updates nicht zeitnah eingespielt? Einige Studien haben dies untersucht und folgende Hauptthemen herausgearbeitet[^1][^2]:

- Unklarer Nutzen: Wie oben bereits erklärt ist vielen der Nutzen eines Updates gar nicht bewusst. Häufig wird ein Update nur wegen der neuen Funktionen installiert, nicht aber weil die Sicherheit verbessert wurde.
- Angst vor Problemen: Zudem könnten Updates auch bösartigen Inhalt mithliefern bzw. neue Fehler beinhalten.
- Unverständlicher Prozess: Bei vielen Anwendungen ist es nicht wirklich ersichtlich welche Änderungen ein Update mitbrigt, bzw. wieso man dieses Update jetzt installieren soll.
- Manuelle Abläufe: Eine fehlende Automatisierung des Update-Prozesses ist teilweise herausfordernd für den Anwender und bietet zudem Möglichkeiten für Angreifer (siehe [Quellen]({{<ref "quellen.md">}}))

![xkcd Comic](xkcd_comic.png)

> https://xkcd.com/1328/

## Konkrete Folgen (Beispiele)

Doch was kann passieren wenn Updates nicht eingespielt werden und so Sicherheitslücken weiterhin vorhanden sind:
Hierfür gibt es unzählige Beispiele, wir schauen uns hier konrekt zwei Fälle an die auch private Rchner betroffen hat.

### EternalBlue und WannaCry

EternalBlue ist eine Schwachstelle im SMB‑Protokoll, die 2017 bekannt wurde (CVE‑2017‑0144). Sie wurde von der Schadsoftware WannaCry massenhaft ausgenutzt und infizierte Hunderttausende Rechner weltweit, darunter Krankenhäuser und Unternehmen. Dabei wird eine Lücke in einem alten Dienst (SMBv1) unter Windows benutzt, der eigentlich dazu dient um Dateien und Drucker im Netzwerk zu teilen. Zwar hatte Microsoft schnell einen Patch veröffentlicht der das Problem behebt, hatten viele Organisationen diesen nicht installiert [^3].

Ein Ausführliches Video über die Hintergründe und die Auswirkungen vom Computerphile findet sich hier: https://www.youtube.com/watch?v=88jkB1V6N9w

### WinRAR

WinRAR ist ein Packprogramm, das auf vielen Windowsrechner installiert. Daher ist es immer wieder ein belibtes Ziel von Angriffen. Zuletzt bzw. immernoch wird eine Schwachstelle ausgenutzt, die es ermöglicht, über speziell perparierte Dateien (z. B. PDFs) in den Ordner für die Startprogramme zu schreiben und dort eine Malware zu platzieren, die beim nächsten Log-in automatisch gestartet wird. Diese Sicherheitslücke mit dem Namen CVE-2025-8088 besteht bereits seit Mitte des Jahres 2025. Diese wurde im selben Monat gepacht, also die Sicherheitlücke gestopft, und dennoch wird noch Ende Januar von verschiedenen Akteuren weiter ausgenutzt [^4].

https://www.youtube.com/watch?v=rkMNOC8fhUQ

# Updates besser verstehen

## Was ist ein Update?

Aber gehen wir nochmal ein Schritt zurück und schauen uns an was ein Update ist:
Es ist eine Änderung einer Software mit den Ziel diese zu modernisieren und auf den neuesten Stand zu bringen, indem diese Änerungen Fehler behebt, Funktionen ergänzt und/oder Sicherheitslücken schließt. Entwicklerinnen und Entwickler veröffentlichen zu jedem Patch bzw. Update in der Regel **Changelogs** oder **Release Notes**, die Änderungen in Kategorien wie Neu, Verbesserungen, Fehlerbehebungen und Sicherheit auflisten. Changelogs mit sicherheitsrelevanten Einträge sind besonders zeitkritisch.

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

- **Sicherheitsupdates** diese schließen Schwachstellen und Sicherheitlücke und sollten so schnell wie möglich installiert werden.
- **Funktionsupdates** bringen neue Features; Sie sind grundsätzlich auch wichtig, jedoch meist weniger zeitkritisch.

**Weil Releases jedoch häufig beides kombinieren und keine Wahl lassen, gilt: Alle Updates sollten zeitnah geprüft und installiert werden.**

## Wie Updates verteilt werden

### Vollautomatische Updates

Die Anwendung prüft im Hintergrund auf Updates und installiert sie automatisch. Vorteil: schnelle Verteilung; Nachteil: gelegentliche Neustarts.

### Halbautomatische Updates

Die Software meldet ein verfügbares Update und fragt nach Bestätigung für Installation oder Neustart. Vorteil: Nutzerkontrolle; Nachteil: Verzögerung möglich.

### Manuelle Online‑Updates

Nutzerinnen und Nutzer starten die Update‑Suche in den Einstellungen und bestätigen Downloads manuell.

### Manuelle Offline‑Updates

Updates werden nur auf der Herstellerwebseite bereitgestellt; Nutzer müssen aktiv herunterladen und installieren.

## Worüber Updates herkommen

### Interne Update‑Mechanismen

Einige Hersteller oder Anbieter verteilen Updates direkt über eigene Server oder Management‑Tools. Updates werden je nach Implementierung bzw. Umsetzung automatisch installiert oder müssen manuell angestoßen werden. Im Betriebssystemen ist es gang und gebe, dass Updates über ein eingebauten Updater bzw. über die Einstellungen aktualisert werden können.

### App Stores

Stores wie der Google Play Store, den App Store von Apple, den Microsoft Store oder der Mac App Store verwalten Installation und Aktualisierung vieler Apps zentral. Auch hier werden Updates wahlweise automatisch oder manuell installiert. Informiert wird man jedoch in der Regel immer.

### Herstellerwebseiten

Treiber oder Software von kleinen Entwicklerteams werden häufig auch nur auf der Webseite der Hersteller zur Verfügung gestellt. Zwar bekommt man hier die Software direkt von der Quelle, jedoch können Angreifer bzw. Krimielle versuchen den Benutzer auf eine falsche Seite zu locken, die dann eine modifizierte Software enthält und schaden anrichten kann.

### Paketmanager

Unter Linux sind Paketmanager (apt, yum, dnf, zypper) Standard für das Verwalten von Software. Diese dort häufig den Terminal gesteuert, einige Distribution bieten jedoch auch eine Benutzeroberfläche über die Updates und Installationen komfortabel verwaltet werden können. Vergleichbares gibt es unter Windows seit einigen Jahren mit **winget**[^5]. Diese ist direkt von Microsoft und bietet den Vorteil, dass Anwendungen von Microsoft überprüft werden, jedoch ist das (wie auch unter Linux) nicht perfekt und auch über diese können theoretisch Schadprogramme verteilt werden, nichtdestotrotz bieten diese eine Aktualisierung für Software ohne diese öffnen zu müssen. Vergleichbares, wenn auch nicht so mächtig, findet sich für macOS mit **Homebrew**[^6].

## Übersicht Updateverteilung

| Quelle             | Mechanismus                                    | Beispiele                               | Vorteile                   | **Empfehlung**                                      |
| ------------------ | ---------------------------------------------- | --------------------------------------- | -------------------------- | --------------------------------------------------- |
| Betriebssystem     | Automatisch; Halbautomatisch; Manuell          | Windows Update, macOS Softwareupdate    | Deckt OS‑Sicherheitslücken | **Automatische Updates prüfen/anschalten**          |
| App Store          | Automatisch; Halbautomatisch                   | Google Play, App Store, Microsoft Store | Zentrale Verwaltung        | **Automatische App‑Updates aktivieren**             |
| In‑App Updater     | Automatisch; Halbautomatisch; Benachrichtigung | Browser, PDF‑Reader, Spiele             | Schnelle Verfügbarkeit     | **Regelmäßig nach Udpates suchen und installieren** |
| Herstellerwebseite | Manuell; Halbautomatisch                       | Grafikkartentreiber, Spezialsoftware    | Direkt vom Hersteller      | **Nur offizielle Downloads verwenden**              |
| Paketmanager       | Automatisch; Halbautomatisch                   | apt, winget, Homebrew                   | Batch‑Updates              | **Für technisch Interessierte geeignet** UnigetUI   |

## Empfehlungen

Was sollte man nun konkret umsetzen um Software möglichst schnell zu aktualisieren.

- Überall wo die Option angeboten wird **automatische Updates aktiveren**. Das verhindert, dass man Updates vergisst, jetzt gerade keine Zeit dafür hat oder Angst vor einen Update hat.
  - das gilt inbesondere für das **Betriebsystem**
  - und den **Browser** (lässt sich heutzutage selten _ausschalten_)
- Zudem sollten auch Updates für Software beachtet werden die nicht in der "ersten Reihe" stehen:
  - Browser-Addons aktualisieren,
  - Erweiterungen und Mods in Spielen,
  - Router-Firmware,
  - Bibliotheken die manche Software mitinstalliert, bspw. Java Runtime Environment
  - ...
- **Bei manuellen Downloads** sollte genau geprüft werden ob es sich um die offizielle Herstellerseiten handelt **App‑Store‑Updates erlauben** für alle Apps aus App-Stores.vgl [Sichere Quellen]({{<ref "quellen.md">}}).

[^3]: https://www.heise.de/news/EternalBlue-Hunderttausende-Rechner-ueber-alte-NSA-Schwachstelle-infizierbar-4167918.html

[^4]: https://www.heise.de/news/Angriffe-auf-WinRAR-Luecke-laufen-weiter-11157132.html

[^5]: https://learn.microsoft.com/de-de/training/modules/explore-windows-package-manager-tool/4-update-software

[^6]: https://docs.brew.sh/FAQ#how-do-i-update-my-local-packages
