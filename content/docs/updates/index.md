---
title: "Software Updates"
weight: 2
---

# Software Updates

# Grundproblem

In der [Software Hygiene]({{<ref "hygiene.md">}}) wurde bereits dargelegt, warum es schlecht ist möglichst viel Software auf verschiedenen Geräten zu haben. Jedoch können wir natürlich nicht nur mit einem blanken Betriebssystem ohne Anwendungen produktiv arbeiten. Doch wie arbeitet man mit der Software weiter die dann tatsächlich auf dem Endgerät bleiben soll.

Es ist hier wichtig diese, sobald eine Aktualisierung veröffentlicht wurde diese zu installieren.

Nach Experten ist das die wichtigste Maßnahme um Sicherheit zu gewärhleisten, noch vor der Nutzung eines Passwortmanagers und der Aktivierung vom 2-Faktor. Diese Aussage stammt aus einer Studie bei der Sicherheitsexperten und Laien über die effektivität von möglichen Umsetzungen befragt wurden. Das spannende aus dieser Studie ist, dass die meisten Laien diese Methode als nicht effektive.
![Prozentualer Unterschied](image.png)

Und das führt leider dazu, dass die Software die auf den Rechnern installiert ist zudem viel zu spät aktualisiert werden.
Hierzu gibt es auch einige Wissenschaftliche Ausarbeitungen: Beispielsweise hat die University of Houston untersucht, wann bestimmte Updates heruntergeladen werden. Dabei wurde festgestellt, das nach über 100 Tagen nach der Veröffentlichung des Updates noch 25 % der Anwender erst installieren. Nach 300 Tagen waren es immernoch ca. 10 %. Das Problem hierbei ist, dass es wiederum von der veröffentlichung eines Updates zur ersten Ausnutzung der darin behobenen Sicherheitslücken nur wenige Stunden bis Tage dauert. Es gibt hier den intial von Mircosoft eingeführten Patch Tuesday. Das ist immer der zweite Dienstag innerhalb eines Monats. An diesem Datum werden immer Sicherheitsupdates für verschiedene Microsoft Produkte veröffentlicht. Dazu gibt es unter Hackern folgendes Sprichtwort: Patch Tuesday, Exploit Wednesday. Der hintergrund dieses Sprichtworts liegt daran, dass anhand dieser Änderungen die an diesem Dienstag veröffentlich werden, verhältnismäßig leicht herauszufinden was nun gefixt wurde mit dem Wissen, dass sehr viele dieses Update erst sehr viel später installieren werden.

-QUELLE die konrekte Verstärkte Ausnutzung zeigt.

# Die Gründe

Aber wenn das so wichtig ist, warum haben wir dann noch teilweise Software auf den Endgeräten die seit Jahren verfügbare Sicherheitsupdates nicht erhalten haben?
Hierfür gibt es mehrere Gründe: Viele kennen genau diese Hintergründe nicht und kennen den "Wert" solcher Updates nicht. **_Das wurde hiermit deutlich, dass gerade Sicherheitsupdates wichtig sind_**.
In der bereits zitierten Studie "no one can hack my mind" gab es auch einige Meldungen dazu, wieso Peronen ohne IT-Sicherheitshintergrund Updates für nicht wichtig für die Sicherheit halten:
So wurde Beispielsweise gesagt, dass es unsicher sei, Updates zu installieren, Updates bösartigen Inhalt mitliefern, oder selbst Fehler mitliefern könnten.
Bei einer weiteren Studie, der "[A risk assessment study](https://arxiv.org/pdf/2411.06262)" wurde untersucht warum Nutzer Software-Updates verzögern. Dabei wurde festgestellt, dass 50 % der Teilnehmer den Updateprozess nicht verstehen bzw. unabhängig davon 30 % nicht wissen welche Änderungen ein Update mit sich bringt. Es hat sich aber auch gezeigt, dass eine bessere (Risiko)-Information der User zu einem besseren Updateversorgung führt.
Daher wollen wir nun etwas hinter die Kulissen von einem Update-Prozess schauen und uns anschauen wo wir Informationen zu Updates herausfinden und was dort alles drinstehen kann.

# Die Folgen

Was passiert aber nun wenn wir Updates einfach nicht installieren? Hierzu gibt und gab es über die letzten Jahre unzählige Angriffe auf ungepachte (nicht aktualsierte) Anwendungen. Eine wollen wir uns etwas genauer anschauen:

## WinRAR

Ist ein Programm das für das Entpacken und Öffnen von Dateien wie .7z, .tar, .rar, .zip Archiven nutzen lässt hierbei gab es in Versionen vor 6.23 folgende Sicheheitslücke, die 2023 Publik wurde:
Eine Sicherheitslücke hatte dafür gesorgt, dass wenn man ein ZIP-Archiv geöffnet hatte das zwei Dinge enthielt: eine Datei, z. B. Awareness.png sowie einen Ordner! mit dem Namen Awareness.png, dann wurde beim öffnen der PNG in WinRAR beim autmatischen entpacken der Ordner und der darin enthaltene Schadcode ausgeführt.
Es hätte jeden betreffen können der die Software nicht aktulaisierte und sich eine solche .zip-Datei aus den Internet herunterlädt und öffnet.

## EternalBlue / WannaCry

EternalBlue ist eine alte Sicherheitslücke aus dem Jahr 2017, und betraf bzw. betrifft alte Windows 7 PCs.
Es gab dort eine Sicherheitslücke die die NSA damals verschwiegen hatte mit dem Codenamen EternalBlue. Die Sicherheitslücke hat es erlaubt über eine alte Version eines Protokolls für den Datei- und Druckerzugriff im Netzwerk ohne Passwort den Computer zu Übernehmen. Der oder die Angreifer können dann alles auf den Rechner tun.
Gerade 2017 waren hier sehr viele Firmen betroffen

https://www.bbc.com/news/technology-39913630
Jetzt denkt man sich vielleicht Windows 7 hat heute sowie keiner niemand mehr, aber das stimmt nicht. Laut statcounter haben Stand Ende 2025 immernoch knapp 4 % aller Windows Dekstops Windows 7 installiert, der Support von diesem Betriebssystem lief vor 6 Jahren im Jahr 2020 aus.
Es wurde bzw. wird weiterhin nach diese Protokol (genauer nach dem Port) gesucht und versucht diese Schwachstelle auszunutzen.

# Das Update

# Die Aktualisierung

Das [Digitale Wörterbuch der deutschen Sprache](https://www.dwds.de/wb/Aktualisierung#d-1-1-1) Beschreibt eine Aktualsierung mit einer "Anpassung an den zeitgemäßen, neuesten Stand, Einbeziehung und Ergänzungen der neusten Ereignisse und Entwicklungen.

Diese "Ergänzungen, Ereignisse und Entwicklungen werden, abgesehen sicherheitskritschen Aktualsierungen typischerweise in Zyklen bzw. bestimmten Abständen veröffentlicht. Das sorgt dafür, dass bei einer Veröffentlichung von einem Update häufig viele unterschiedliche Funktionen und ggf. Sicherheitsupdates kombiniert. Um es Nutzern und Entwicklern leichter zu machen die Überblick über die gemachten Änderungen zu behalten werden in der Regel immer Informationen zu den Veröffentlichungen bereitgestellt:

# Changelog und Realese Notes (Änderungsprotokoll und Versionshinweise)

Wenn nun eine neue Version von einer Software bereitsteht, geben die Entwickler in fast allen Fällen übersichtlich Informationen über die Änderungen dieser Verion.
Je nachdem an wen eine Liste dieser Änderungen gerichtet ist, wird unterschiedlich darüber kommuniziert. Ist diese Beispielsweise für Entwickler gedacht wird diese sehr schnell komplex und technisch. Sollen die Änderungen für Endkunden veröffentlicht werden sind diese sehr viel leichter Verständlich und es ist leichter erkennbar was sich ändert. Änderungen werden häufig in unterschiedliche Kategorieren wie Neu (New), Verbesserungen (Fixed), Änderungen (Changed) und Sicherheit (Security) unterteilt um einen bessern Überblick zu gewährleisten.

# Beispiel

---

# Changelog

## [3.2.0] – 2026-01-01

### Neu

- Darkmode für eine angenehmere Nutzung am Abend.
- Verbesserte Startseite mit schnellerem Zugriff auf Favoriten.

### Verbesserungen

- Schnellere Synchronisierung deiner Daten zwischen Geräten.
- Optimierte Push-Benachrichtigungen, damit du nur relevante Infos erhältst.

### Fehlerbehebungen

- Problem behoben, bei dem Benachrichtigungen gelegentlich doppelt angezeigt wurden.
- Seltener Absturz beim Öffnen der Einstellungen korrigiert.

### Sicherheit

- Aktualisierung einer internen Netzwerkbibliothek zur Behebung der Schwachstelle CVE-2025-12345 (konnte in seltenen Fällen unverschlüsselte Verbindungen zulassen).
- Stärkere Überprüfung bei der Anmeldung, um unberechtigte Zugriffe besser zu verhindern.

[Hier sind exemplarisch weitere Update-Hinweise von echter Software gesammelt]({{<ref "beispiele.md">}})

(Anmerkung: Dies ist weder eine Empfehlung an Software noch stehen wir in irgendeiner Verbindung zu den Entwicklern.)

# Sicherheitsupdates vs. Funktionsupdates

In den Changelogs wird häufig zwischen Funktionsänderungen (Fixes, Fixed; Changes) und Sicherheitsänderungen (Security) Unterschieden. Häufig gibt
Bei Sicherheitsupdates handelt es sich in der Regel um ein Lösung bzw. ein Fix für eine sicherheitsrelevante Schwachtstelle. Diese sollten immer, möglichst schnell installiert werden. Handlet es sich um ein Funktionsupdate werden typischerweise, wie es der Name vermuten lässt um ein Update das in der Regel neue Funktionen hinzufügt bzw. bestehende Verändert.
Das Problem hierbei ist, dass bei einer Veröffentliung eines Updates bzw. einer neuen Version diese meinst Kombiniert sind, und man beide installieren muss. **Es sollten daher immer alle Updates möglichst schnell installiert werden.**

# Wo und Wie

Nachdem nun gezeigt wurde wie neue Versionen erklärt werden, und wir im Ansatz verstanden haben was darin beschrieben wird, wollen wir uns nun anschauen wie Updates ausgeliefert werden bzw. zur Verfügung gestellt werden.

# Wie

# Vollautomatische Updates

Das ist sozusagen der Goldstandard wenn es darum geht eine Anwendung schnell zu Updaten. Hier wird beim Starten der Anwendung oder der App nach Updates gesucht und, sofern vorhanden, werden diese direkt bzw. nach dem nächsten Neustart installiert.

# Halbautomatische Updates

Hier wird der User über einen Pop-Up bzw. ein Benachrichtigung über ein ausstehendes Update informiert. Er kann dann entscheiden zu welchem Zeitpunkt oder unter welchen Bedingungen er die Anwendungen installiert werden soll. Der Updateprozess selbst läuft wie beim Vollautomatischen Update über die Software selbst.

# Manuelle Online-Updates

Typischerweise ist hier ein Eintrag in den Einstellungen, der dem Nutzer die möglichkeit gibt die Updatesuche selbst anzustoßen. Ist eine neue Version verfügbar, wird der Benutzer gerfragt, ob er diese installieren möchte. Der Update-Prozess selbst wird entweder über die Anwendung selbst oder über ein Downloadlink gelöst.

# Manuelle Offline-Updates

Es gibt leider auch die Version, bei dem neue Versionen ausschließlich über die Herstellerwebseite bekannt gegeben. Hier muss der Nutzer aktiv nach Updates suchen um diese zu erhalten.

# Wo

# Intern

Viele gerade große Firmen bieten aktualisieren Ihre Apps auf Desktop Geräten über einen eigenen Updateprozess in der App selbst. Das kann automatisch passieren oder manuell angestoßen werden. Der Nutzer muss hierbei jedoch nicht auf eine Webseite gehen oder einen Store besuchen

# Stores

Die verschiedenen Stores in Betriebssystemen verwalten die daraus installierten Apps und sind auch für die Aktualisierung davon zuständig. Für alle gängigen Betriebssysteme gibt diese. Für Windows den Microsoft Store, für MacOS die MacOS App Store, für Android den Google Play Store, sowie für iOS den App Store. Über diese werden entweder automatisch oder manuell mehrere Aktualisierungen durchgeführt.

# Herstellerwebseite

Eine Aktualisierung kann auch über die Webseite des Herstellers bereit gestellt werden. Hier wird entweder um einem Eintrag in den Einstellungen direkt auf die Webseite verwiesen, bei einer Update-suche darauf hingewiesen, dass eine neue Version unter einer bestimmten URL installiert werden kann, oder man muss selbst auf die Webseite gehen, um herauszufinden ob eine neue Version verfügbar ist.

# Zusatz: Paketmanager

Diese sind gerade unter Linux der Standard wenn es darum geht Anwendungen zu verwalten.
Über diese können neue Software installiert aber auch aktualisiert werden. Hier besitzt der Paketmanager eine Liste von Quellen. Wenn nun ein Nutzer eine Software installieren möchte sucht der Paketmanager innerhalb dieser Quellen ob diese Verfügbar ist, falls ja, lädt er die benötigten Dateien von dieser herunter und installiert diese. Der Vorteil bei diesen Paketmanager ist, dass hier ähnlich wie bei einem Store mehrere Anwendungen in einem Rutsch aktualisiert werden. Hierbei würd protokolliert welche Anwendungen ,mit welchen Versionen auf dem Betriebssystem installiert und prüft die Versionen nun mit denen in den Quellen die hinterlegt sind. Ist eine oder mehrere Versionsnummern verschiedener Anwendungen in der Quelle höher als die der aktuell installierten App kann ein Update durchgeführt werden.
Unter Linux heißen diese Paketmanger apt, yum, dnf , zypper ...
Windows besitzt seit 2020 auch einen Paketmanager der vergleichbar ist mit den Paketmanager von Linux. Unter Windows heißt dieser winget (Windows Package Manager).


