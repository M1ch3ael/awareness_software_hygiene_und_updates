---
title: "Software Hygiene"
weight: 1
---

# Software Hygiene

# Einleitung

Software‑Hygiene bedeutet, die auf Geräten installierte Software bewusst zu verwalten, zu pflegen und unnötige Programme zu entfernen. Ziel ist es, die Angriffsfläche zu verkleinern, Sicherheitsrisiken zu reduzieren und die Stabilität sowie Performance der Geräte zu verbessern. Hier wird nun erklärt, warum das wichtig ist, wie Angriffe typischerweise ablaufen, welche Risiken besonders relevant sind und welche konkreten, leicht umsetzbaren Maßnahmen Privatanwenderinnen und ‑anwender ergreifen können.

# Die Angriffsfläche verstehen

Was ist die Angriffsfläche
Die Angriffsfläche (engl. attack surface) umfasst alle Komponenten eines Systems, über die ein Angreifer potenziell eindringen kann: installierte Programme, Dienste, Treiber, Browser‑Plugins, Hintergrundprozesse und Netzwerkdienste. Jede zusätzliche Anwendung oder Bibliothek vergrößert diese Fläche.

## Warum viele Programme problematisch sind

Mehr Code = mehr Fehler: Große Programme bestehen aus vielen Zeilen Code; Fehler und Schwachstellen können sich einschleichen.

![xkcd Comic about Security Holes](xkcd_comic_security_holes.png)

> https://xkcd.com/424/

Was ggf. wie eine leichte, einfache Software aussieht, wie bspw. den VLC-Player hat in Wahrheit über einer Millionen Zeilen Code von vielen verschiedenen Entwicklern. Hier den Überblick für einzlene zu behalten ist nahezu unmöglich. Alles ist über viele Dateien verteilt was es zwar übersichtlicher macht, jedoch eine Kontrolle nicht wirklich erleichtert. Zudem bauen viele Anwendungen auf sogenannten Bibliotheken bzw. Programmen von anderen auf die ebenfalls komplexit Komplexität einbringen.

![VLC Logo](VLC_Icon.svg?width=90)  
[Richard C. G. Øiestad](https://commons.wikimedia.org/wiki/File:VLC_Icon.svg) · [GPL](http://www.gnu.org/licenses/gpl.html)

## Drittanbieter‑Bibliotheken:

Bei der Entwicklung von Software wird typischerweise auf bereits erstellten bzw. vorhanden Code zurückgegriffen, dadurch reduziert sich der Arbeitsaufwand jedoch ist man dann auf die Arbeit dritter angewiesen. Ist eine solche Software bzw. häufig Bibliothek kompromittiert bzw. infiltiert, betrifft es alle Programme die diese nutzen.

## Unnötige Dienste:

Auch Programme bzw. Dienste die typischerweise auf dem Desktop im Hintergrund laufen bieten eine weitere Einfallstore.
Hintergrunddienste, die nicht benötigt werden, bieten zusätzliche Einfallstore. Gerade unter Windows schleichen sich in Installtionen verschiedenste Programme ein die einen Eintrag in den Autostart legen und entsprechend jedes mal starten wenn der Rechner startet.
Auch werden bestimmte Anwendungen erst gestartet wenn ein bestimmtes Ereignis eintritt. Gerade hier schleichen sich verschiendste Schadsoftware in den Rechner ein, bzw. sorgen dafür nicht mehr gelöscht werden zu können.

## Browser Plugins

Auch Browser Plugins können zur Gefahr werden. Da die meisten Extensions bzw. Erweiterungen für ihre berechtigte bzw. gewünschte Funktion teilweise weitreichende Berechtigungen benötigt, ist es umso schwerer Erweiterungen diese von Erweiterungen zu unterscheiden die diese Berchtigungen ausnutzen um den Nutzer zu schaden.

https://www.crowdstrike.com/en-us/cybersecurity-101/exposure-management/browser-extensions/

# Typische Angriffsabläufe

Aufklärung (Reconnaissance): Angreifer oder automatisierte Scanner suchen nach erreichbaren Geräten, offenen Ports oder bekannten Diensten.

Schwachstellensuche: Es wird geprüft, ob installierte Software bekannte Sicherheitslücken hat.

Ausnutzung (Exploit): Gefundene Schwachstellen werden genutzt, um Schadcode auszuführen, Daten zu stehlen oder Kontrolle zu erlangen.

Persistenz und Ausbreitung: Nach erfolgreichem Zugriff versucht der Angreifer, Zugang zu halten und sich ggf. im Netzwerk auszubreiten.

# Supply‑Chain‑Risiken

**Supply‑Chain‑Angriffe** zielen nicht direkt auf das Endgerät, sondern auf Komponenten, Bibliotheken oder Build‑Prozesse, die viele Anwendungen verwenden. Wird eine zentrale Komponente kompromittiert, kann Schadcode in zahlreiche Programme gelangen. Deshalb ist es wichtig, nicht nur die eigenen Programme, sondern auch deren Herkunft und Vertrauenswürdigkeit zu beachten.

# Konkrete Beispiele

Ungepatchte Programme: Wenn ein Programm ein bekanntes Sicherheitsproblem hat und kein Update installiert wird, kann ein Angreifer diese Lücke nutzen.

Manipulierte Archive: Schadarchive können beim Entpacken Code ausführen, wenn die Software fehlerhaft mit Dateinamen oder Pfaden umgeht.

Komplexe Bibliotheken: Eine kompromittierte Bibliothek kann viele Anwendungen gleichzeitig gefährden.

# Empfehlungen

- Unnötige Programme deinstallieren. Alles was nicht mehr aktiv genutzt wird.
- Browser-Erweiterungen kontrollieren und nur vertrauenwürdige Add-Ons behalten
- Die Berchtigungen von Anwendungen prüfen
- Autostarts regelmäßig prüfen
- Vorher ggf. Backup bzw. Systemwiederherstellungspunkt erstellen
