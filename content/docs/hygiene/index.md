---
title: "Software Hygiene"
weight: 1
---

# Software-Hygiene

# Einleitung

Software-Hygiene bedeutet, die auf Geräten installierte Software bewusst zu verwalten, zu pflegen und unnötige Programme zu entfernen. Ziel ist es, die **Angriffsfläche** zu verkleinern, Sicherheitsrisiken zu reduzieren und die Stabilität sowie Performance der Geräte zu verbessern. Warum das immer wichtiger wird, welche Risiken besonders relevant sind und welche konkreten, leicht umsetzbaren Maßnahmen ergriffen werden können, wird im Folgenden erläutert.

# Was ist die Angriffsfläche?

Die Angriffsfläche (engl. attack surface) umfasst alle Komponenten eines Systems, über die ein Angreifer potenziell eindringen kann: Installierte Programme, Dienste, Treiber, Browser-Plug-ins, Hintergrundprozesse und Netzwerkdienste. Jede zusätzliche Anwendung oder Bibliothek vergrößert diese Fläche.

## Warum viele Programme problematisch sind

**Mehr Code = mehr Fehler**: Programme werden immer komplexer und bestehen aus vielen Zeilen Code. Da dieser meist von Menschen geschrieben wird, schleichen sich mit der Zeit immer wieder Fehler ein. Zwar muss ein Fehler nicht gleich zu einer Schwachstelle werden. Wenn dies jedoch an einer kritischen Stelle in der Software passiert, sind Geräte, die diese Software benutzen, anfällig.

![xkcd-Comic über Sicherheitslücken](xkcd_comic_security_holes.png)

> https://xkcd.com/424/

Was auf den ersten Blick wie eine leichte, einfache Software aussieht - beispielsweise der VLC-Player - ist in Wahrheit ein riesiges Softwareprojekt. Es besteht aus ca. 800.000 Zeilen Code von über 1.000 verschiedenen Entwicklern [^1]. Hier den Überblick zu behalten, ist nahezu unmöglich. Zudem ist alles über viele Dateien verteilt, was es zwar übersichtlicher macht, eine Kontrolle jedoch nicht wirklich erleichtert. Wenn nun bei jeder 1000. bis 2000. Zeile ein Fehler passiert, sind das bei 800.000 Zeilen Code dennoch 400 bis 800 Fehler in einem Softwareprojekt wie dem VLC-Player. Viele Anwendungen bauen auf sogenannten Bibliotheken bzw. Programmen von anderen auf, die ebenfalls Komplexität einbringen.

![VLC-Logo](VLC_icon.png)

[Richard C. G. Øiestad](https://commons.wikimedia.org/wiki/File:VLC_Icon.svg) · [GPL](http://www.gnu.org/licenses/gpl.html)

# Supply-Chain-Risiken

Wie gerade [weiter oben](#warum-viele-programme-problematisch-sind) erläutert, ist eine Anwendung meist komplex. Sie basiert auf verschiedenen anderen Bibliotheken und Entwicklungen Dritter. Das reduziert zwar den Arbeitsaufwand erheblich, führt aber auch dazu, dass man auf die Arbeit Dritter angewiesen ist. Daher ist es nicht verwunderlich, wenn Angreifer dies ebenfalls als Ziel entdecken: Es handelt sich hierbei um sogenannte **Supply-Chain-Angriffe**. Diese zielen nicht direkt auf das Endgerät, sondern auf Software, Komponenten, Bibliotheken oder Build-Prozesse ab, die von (vielen) Anwendungen verwendet werden. Wird eine zentrale Komponente kompromittiert, kann Schadcode in zahlreiche Programme gelangen. Deshalb ist es wichtig, nicht nur die eigenen Programme, sondern auch deren Herkunft und Vertrauenswürdigkeit zu beachten.

## Beispiele

### XZ Utils [^2]

![XZ-Logo von potenzieller Täterin](XZ_Logo.png)

[Jia Tan, CC BY-SA 4.0](https://creativecommons.org/licenses/by-sa/4.0>), via Wikimedia Commons

XZ Utils ist eine Bibliothek für Dekomprimierung und Komprimierung, die auf vielen Linux-Distributionen vorinstalliert ist und dort häufig von unterschiedlichen Programmen und Anwendungen benutzt wird. Wichtig zu wissen ist zudem, dass dieses Projekt „Open Source” ist. Die Quelle, in diesem Fall der Code, ist für potenziell alle frei zugänglich und wurde hauptsächlich von einer Person betreut.

Über mehrere Jahre hinweg hat ein Angreifer Social Engineering eingesetzt, um das Vertrauen dieser Person zu gewinnen, bis sie Zugriff auf die Quelle erhielt und diese selbst ändern durfte. Hierdurch war es möglich, eine Backdoor, also einen Teil der Software, einzubauen, der es ermöglicht, die Anwendung so zu verändern, dass sie potenziell Zugriff auf den gesamten PC erhält.

Diese Backdoor fiel nur auf, da es einem anderen Entwickler beim Testen einer Anwendung, die diese Bibliothek nutzt, zu sehr geringen, jedoch unerklärlichen Verzögerungen kam. Dadurch konnte Schlimmeres verhindert werden. Die New York Times bezeichnete diesen Entwickler mit folgender Metapher: „In der Welt der Cybersicherheit ist ein Datenbankingenieur, der versehentlich eine Hintertür in einer Kernfunktion von Linux entdeckt, ein wenig wie ein Bäcker, der den Duft von frisch gebackenem Brot wahrnimmt, merkt, dass etwas nicht stimmt, und daraus richtig schließt, dass jemand die gesamten weltweiten Hefevorräte manipuliert hat.” – Kevin Roose, New York Times [^3]

Hätte diese Backdoor tatsächlich in viele Linux-Distributionen Einzug gehalten, wäre auf all diesen ein Root-Zugriff möglich gewesen, also mehr oder weniger ein Vollzugriff auf alle Linux-Server, die dieses Tool benutzten. Deshalb wird diese Backdoor als „die gefährlichste und raffinierteste Backdoor überhaupt” bezeichnet.[^3]

Dieses Beispiel zeigt, dass selbst bzw. gerade bei Software die gefühlt von jedem genutzt wird, anfällig für diese Art der Angriffe ist. Zudem wird hierdurch deutlich, dass unsere gesamte IT-Welt stark verbunden ist, dass ein einziges Tool eine gesamte Lieferkette in große Schwierigkeiten bringen kann.

Ein Video zu den Hintergründen und zum Ablauf dieses Angriffs ist hier verlinkt:
[Youtube - Simplicissimus | Wie ein Deutscher die xz-Backdoor entdeckt hat](https://www.youtube.com/watch?v=8p8PHeGg--U)

### British Airways

![British Airways](British_Airways_Plane.jpg) von johanwiden69 [(Pixabay)](https://pixabay.com/de/photos/flugzeug-flug-fl%c3%bcgel-abfahrt-jet-5654534/)

Im Fall British Airways geht es nicht primär um Schadcode auf Privatgeräten. Vielmehr zeigt er, wie Supply-Chain-Angriffe auf Dienstleister indirekt die Kunden betreffen können.
Zwischen dem 14. August und dem 5. September 2018 wurden bei British Airways mehrere hunderttausend Zahlungs- und Kontaktdaten von Kunden an Angreifer weitergeleitet. Diese hatten zuvor nicht British Airways direkt kompromittiert, sondern ein Konto eines Mitarbeiters der Firma Swissport übernommen. Swissport ist der weltgrößte Serviceanbieter für Fluggesellschaften.

Über diesen Account wurde das Netzwerk durchsucht und ein Admin-Account kompromittiert. Der Admin-Account hatte wiederum die Rechte, den Code der British-Airways-Seite zu verändern. Über eine veränderte JavaScript-Bibliothek wurden alle Zahlungsdaten an die Seite „baways.com” weitergeleitet, die wiederum von den Angreifern kontrolliert wurde [^4] [^5].

### CCleaner

Im März 2018 wurden die Systeme des Herstellers Piriform, der das Tool „CCleaner” entwickelt hat und von Avast aufgekauft wurde, von Angreifern übernommen. Dabei hatten sich die Angreifer über ein Remote-Desktop-Konto Zugriff zu einem Entwickler-PC verschafft.

Von dort aus kundschafteten sie die Netzwerke der Firma aus, infiltrierten die Updateserver und veränderten bei einer bestimmten Version des CCleaners das Update so, dass es den Angreifern ermöglichte, Code bzw. Malware aus der Ferne auszuführen. Insgesamt waren 2,27 Millionen Nutzer betroffen, die innerhalb eines Zeitraums von neun Tagen dieses Update installiert hatten.

Zwar hat sich herausgestellt, dass die Angreifer speziell Firmen wie Samsung, Sony und Epson angreifen wollten und der Rest als „Beifang” gewertet werden kann, jedoch war diese Sicherheitslücke auf über zwei Millionen Geräten installiert. Ein weiteres Update, das kurz nach Bekanntwerden der Sicherheitslücke bereitgestellt wurde, hat das Problem behoben[^6].

## Unnötige Hintergrund-Dienste:

Als Hintergrunddienste werden Programme bezeichnet, die aufgrund bestimmter Bedingungen gestartet werden. Beispielsweise: „Starte jeden Tag zum Zeitpunkt X Programm Y” oder „Starte bei Anmeldung bzw. beim ersten Starten Programm Z”.
Das birgt jedoch die Möglichkeit für schädliche Programme, sich dauerhaft, auch nach einem Neustart und dem Löschen einzelner, auf dem PC zu halten.
Zu diesen gehören zwar teilweise notwendige Dienste, wie z. B. Treiber oder die Antiviren-Software, jedoch werden sie häufig durch Installationen oder andere Schadsoftware bzw. Adware hinterlegt, die bei einer Anmeldung mitgestartet wird und so den PC-Start unnötig verzögert.

## Browser-Erweiterungen

Browser-Erweiterungen sind Dateien, die häufig in Form einer ZIP-Datei vorliegen und entsprechenden Code enthalten. Sie sorgen dafür, dass ein Browser um Funktionen erweitert wird, die er standardmäßig nur teilweise oder gar nicht kann.

Aber auch Browser-Erweiterungen können zur Gefahr werden. Da die meisten Erweiterungen für ihre berechtigte bzw. gewünschte Funktion teilweise weitreichende Berechtigungen benötigen, ist es umso schwerer, Erweiterungen, die diese Berechtigungen ausnutzen, um dem Nutzer zu schaden, von den anderen zu unterscheiden. Zudem kann eine Erweiterung auch aus fehlerhaftem Code bestehen. So kann das Ändern der Suchmaschine oder der Startseite durch ein Add-on dazu führen, dass teilweise dubiose Firmen Informationen über den Suchverlauf und somit auch über die Interessen der Nutzer erhalten. Auch können Cookies entwendet oder neue verteilt werden. Über letztere kann dann Schadcode den Computer erreichen [^7] [^8].

## Beispiele

Im Juli 2025 wurde bekannt, dass insgesamt 18 Chrome-Erweiterungen, von denen einige von Google verifiziert waren und über zwei Millionen Nutzer hatten, alle besuchten Webseiten inklusive Tracking-IDs an einen Webserver gesendet und ggf. auf eine Webseite weitergeleitet haben. Darunter waren unter anderem ein Farb-Picker, verschiedene Unlocker/VPNs für Discord und Tiktok sowie eine Sucherweiterung mit ChatGPT. Die Anwendungen erfüllten auf den ersten Blick ihre Funktionen und waren lange Zeit auch unproblematisch.

Erst mit einem automatischen Update, das die Funktion unbemerkt einführte, wurden besuchte Webseiten auf einen Server der Angreifer weitergeleitet (Warum man dennoch Updates trotz potenzieller Gefahren automatisch installieren sollte, wird in [Software Hygiene]({{<ref "updates.md">}}) erläutert). Die Angreifer hatten damit vollständigen Zugriff auf den Datenverkehr zwischen dem Nutzer und dem Browser[^9].

# Berechtigungen von Anwendungen

Was im Hinblick auf Browser-Plug-ins gilt, gilt insbesondere auch für Anwendungen und Apps. In erster Linie sind (unbegründete) Berechtigungen, wie sie typischerweise in mobilen Betriebssystemen vorkommen, ein Datenschutzrisiko. Sie können beispielsweise dazu führen, dass Fotos oder Geolokalisationsdaten bei Firmen und Personen landen, die diese für die Bereitstellung des Services, der App oder Anwendung gar nicht benötigen. Berechtigungen sind jedoch auch für Angreifer wichtig, da sie diese teilweise benötigen, um Schaden am System anzurichten. Auch bei Desktop-Betriebssystemen können Berechtigungen die Privatsphäre verletzen. So können unter Umständen unbemerkt Kamera- und Tonaufnahmen erstellt werden. Mithilfe des freigegebenen Standorts können Bewegungsprofile erstellt bzw. Rückschlüsse auf den Wohnort, den Arbeitsort oder auf Routinen gezogen werden. Daher ist es immer ratsam, einer App nur die Berechtigungen zu gewähren, die sie mutmaßlich für die beworbene Funktion benötigt.

## Beispiele

Ein Beispiel für die weitreichenden Folgen erteilter Berechtigungen ist der sogenannte Anatsa-Banking-Trojaner unter Android. Er gelangt über getarnte Apps aus dem Google Play Store wie einen QR-Code-Scanner oder einen Smartphone-Reiniger auf das Smartphone. Diese Apps fragen verschiedene Berechtigungen ab, darunter den Zugriff auf SMS und die sogenannten Accessibility Options bzw. Bedienhilfen. Letztere ist sehr weitreichend und gewährt einer App Zugriff auf den gesamten Bildschirm, auch von anderen Apps. Zudem darf diese App mit anderen Apps interagieren und Sensoren verfolgen. Mit diesen Berechtigungen können Zugangsdaten aus der Banking-App gelesen und Transaktionen ausgeführt werden. Zudem können Kryptowallets leergeräumt werden [^10].

Doch auch unter iOS gibt es Malware, die versucht, Passwörter zu stehlen. Die sogenannte SparkCat-Malware wird sowohl über den Play Store als auch über den App Store verteilt. Diese Apps fordern Zugriff auf die Fotogalerie in iOS. Mit dieser Berechtigung scannt die Anwendung Fotos nach vorgegebenen Schlüsselbegriffen und übermittelt mögliche Treffer an den Server der Angreifer. Im Visier sind hier hauptsächlich Kryptowallets, aber auch Passwörter und Benutzernamen werden weitergeleitet[^11].

# Empfehlungen

Doch was kann man tun, um diese Probleme zu beheben bzw. die Angriffsfläche zu reduzieren? Es geht darum, die Anzahl der Software auf Endgeräten zu reduzieren. Man kann sich also folgende Fragen stellen: - Braucht es wirklich diese neue App, die etwas vermeintlich besser kann?

- Muss die Erweiterung, die ich seit Jahren nicht mehr benötige, noch im Browser installiert sein? Braucht mein Taschenrechner auf dem Handy oder der PDF-Viewer auf dem PC wirklich Zugriff auf die Kamera?

Konkret heißt das, dass Folgendes angeschaut werden sollte:

- [ ] **Inventur**: Unnötige Programme/Apps deinstallieren. – Alles, was nicht aktiv genutzt wird.
- [ ] **Browser-Check**: Das Gleiche gilt für Browser-Erweiterungen, ggf. auch in verschiedenen Browsern. Hier sollten nur vertrauenswürdige und benötigte Add-ons behalten werden.
- [ ] **Autostart-Kontrolle**: Zudem sollte hin und wieder geprüft werden, welche Programme beim Systemstart gestartet werden.

[^1]: https://openhub.net/p/vlc

[^2]: https://www.akamai.com/de/blog/security-research/critical-linux-backdoor-xz-utils-discovered-what-to-know

[^3]: https://www.nytimes.com/2024/04/03/technology/prevent-cyberattack-linux.html

[^4]: https://www.wired.com/story/british-airways-data-breach-gdpr-fine/

[^5]: https://baways.com (früher die bösartige Webseite für die Bezahlvorgänge, heute von cside aufgekauft um den Fall darzustellen, ggf. von Filterlisten markiert)

[^6]: https://www.wired.com/story/inside-the-unnerving-supply-chain-attack-that-corrupted-ccleaner/

[^7]: https://www.crowdstrike.com/en-us/cybersecurity-101/exposure-management/browser-extensions/

[^8]: https://arxiv.org/pdf/2503.04292v1

[^9]: https://www.koi.ai/blog/google-and-microsoft-trusted-them-2-3-million-users-installed-them-they-were-malware

[^10]: https://www.heise.de/news/Klaut-Passwoerter-aus-Screenshots-Stealer-Apps-erstmals-im-App-Store-gesichtet-10273411.html

[^11]: https://thehackernews.com/2025/02/sparkcat-malware-uses-ocr-to-extract.html
