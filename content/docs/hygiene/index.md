---
title: "Software Hygiene"
weight: 1
---

# Software Hygiene

Software Hygiene
Einleitung
Software‑Hygiene bedeutet, die auf Geräten installierte Software bewusst zu verwalten, zu pflegen und unnötige Programme zu entfernen. Ziel ist es, die Angriffsfläche zu verkleinern, Sicherheitsrisiken zu reduzieren und die Stabilität sowie Performance der Geräte zu verbessern. Hier wird nun erklärt, warum das wichtig ist, wie Angriffe typischerweise ablaufen, welche Risiken besonders relevant sind und welche konkreten, leicht umsetzbaren Maßnahmen Privatanwenderinnen und ‑anwender ergreifen können.

# Die Angriffsfläche verstehen

Was ist die Angriffsfläche
Die Angriffsfläche (engl. attack surface) umfasst alle Komponenten eines Systems, über die ein Angreifer potenziell eindringen kann: installierte Programme, Dienste, Treiber, Browser‑Plugins, Hintergrundprozesse und Netzwerkdienste. Jede zusätzliche Anwendung oder Bibliothek vergrößert diese Fläche.

## Warum viele Programme problematisch sind

Mehr Code = mehr Fehler: Große Programme bestehen aus vielen Zeilen Code; Fehler und Schwachstellen können sich einschleichen.

![xkcd Comic about Security Holes](xkcd_comic_security_holes.png)

## Drittanbieter‑Bibliotheken:

Viele Anwendungen nutzen externe Bibliotheken. Ist eine Bibliothek kompromittiert, betrifft das alle Programme, die sie verwenden.

## Unnötige Dienste:

Hintergrunddienste, die nicht benötigt werden, bieten zusätzliche Einfallstore.

# Typische Angriffsabläufe (einfach erklärt)

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
