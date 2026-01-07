---
title: "Software Hygiene"
weight: 1
---

# Software Hygiene

## Die Angriffsfläche

Was passiert wenn man ein neuen Laptop oder Desktop-PC erhählt: Man installiert erstmal, wenns nicht der erste gewesen ist, sein bekannten Software-Stack. Sei es ein neuer Browser, die Office Anwendung, der Passwortmanager, ein PDF-Viewer und gerade in den letzten Jahren Software für die Kommunikation.

Später kommen dann noch Anwendungen hinzu die man einmal installiert und etwas zu testen bzw. dieses einmal zu benutzen, löscht es später dann aber nicht mehr. Zudem benötigten einige Anwendungen sogenannte Frameworks, Tools oder Kits damit diese überhaupt funktionieren. Zudem kommen noch Treiber oder andere Software die mit bestimmter Peripherie mitgeliefert wird.

Eine Auswertung von Microsoft für Windows 7 von ... hat ergeben das auf einem Rechner im Median ca. 80 Anwendungen installiert sind. Avast hatte 2017 eine Auswertung unter ihren Kunden erstellt und dargelegt, dass ca. 50 Anwendungen durchschnittlich auf einem Rechner installiert sind.

Jetzt mag man ggf. beim Blick auf die Anzahl der installierten Apps auf dem eigenen Smartphone schmunzeln, doch genau davon ist die Rede wenn man in einer digitalen Umgebung von einer Angriffsfläche (engl. Attack Surface) spricht, womit wir zu der Überschrift kommen:

Die Attack Surface beschreibt im Grunde alle Vektoren an denen Angreifer in ein System eindringen können und Schaden, typischerweise Daten entwenden, oder das System übernehmen können. Diese Angriffsfläche wird aus folgendem Grund druch Software vergrößert: Selbst eine Software bei der man sich ggf. denk, Sie sei relativ einfach gestrickt, wie z. B. der VLC-Player besteht heute aus über einer Millionen Zeilen Code. Und hier als einzele Person den Überblick über alles zu behalten ist kaum möglich. Und so führt das eben auch dazu, dass sich bei der Entwicklung Fehler einschleichen.

Man kann sich das in etwa wie bei einer wissenschaftlichen Arbeit vorstellen: Falls man bereits den Fehler gemacht hat und nach der Abgabe diese nochmal erneut durchzugehen fallen häufig grammatikalische Fehler auf die man hätte vor der Abgabe bereits erkennen müssen. Solche Fehler passieren mehr oder weniger auch bei dem entwickeln von Software. Das kann dann dazu führen dass eine bestimtme Funktion nie richtig funktioniert hat, oder dass nach einem Update auf einmal Teile der Software unüblich verhalten. Das kann aber im schlimmsten Fall auch dazu führen, dass über einen solchen Fehler eine Lücke in eurer Verteidigungslinie euerer Angriffsfläche gefunden hat und diese ausnutzen kann.

## Der Angriff

Über welche Wege kann der Angreifer nun durch Software auf das System gelangen? Typischerweise erfolgt dies in mindestes drei Phasen: 
1. Zuerst wird in der Reconnaissance bzw. der Aufklärung nach möglichen Schwachstellen auf entweder über das Internet auf vielen verschiedenen Rechnern oder auf ein spezielles Netzwerk geschaut. Das passiert in der Regel automatisiert. 
2. Im nächsten Schritt wird nach automatisiert nach speziellen Schachstellen, in diesem Fall eine Schwachstelle in einer (vor-)installierten Software gesucht. 
3. Ist diese vorhanden wird über ein oder mehrere  passenden Exploit(s) die Lücke ausgenutzt.

### Exkurs: Supply-Chain-Attacks

Wie bereits erwähnt, ist Software die wir typischerweise auf dem Rechner ist sehr komplex. Das hat auch damit zu tun, dass auch noch zusätzlich zum selbst geschrieben Programmcode  von anderen Biblitotheken Funktionen dazukommen. Um in der Analogie der wissenschaftlichen Arbeit zu bleiben, wäre das vergleichbar mit den Quellen die wir in dieser Verwenden. Und auch wie in bei unser schritlichen Ausarbeitung, die innerhalb dieser Quellen die wir in unser Arbeit benutzen werden Bibliotheken häufig zusätzliche Codeteile von anderen Entwicklern.

Das Problem hierbei ist, dass wie auch in einer Arbeit wir in der Regel wenig einfluss auf die Quelle bzw. die Bibliothek selbst haben. Jetzt ist es aber so, dass es gerade in den letzten Jahren häufiger zu sogenannten Supply-Chain-Attacks gekommen ist. Es gab also ein Angriff auf eine Bibliothek, die dann ggf. Schadcode in eine andere Anwedung mitgebracht hat. Das wäre so als wenn eine Person die nicht zu den Authoren der Quelle gehört, Informationen so verändert, dass diese für viele arbeiten die darauf aufbauen auf einmal nicht mehr gültigt.
Bei einer Supply-Chain-Attack ist dies auch so. ist hier eine Bibliothek angegriffen, betrifft dies häufig viele verschiedene Programme, bzw. Betriebssysteme. Über diese enthält dann das Endprodukt eine Schwachstelle die Angreifer wie oben erklärt ausnutzen kann.

## Was kann man tun
Es gibt also selbt bei einer noch so gut programmierten Software keine Garantie, dass diese ohne Fehler ist, und selbst dann ist es möglich, dass diese durch neuartige Angriffe genutzt werden kann. Es gibt daher auch keinen 100 % Schutz vor Angreifern die einem etwas böses tun wollen. Jedoch kann man zumindest die o. g. Angriffsfläche reduzieren, also konkret möglichst viel Software deinstallieren. Das Bundesamt für Sicherheit in der Informationstechnik schreibt hierzu im Bezug auf Apps: 
"Jede Software enthält Sicherheitslücken, gerade bei kostenlosen Apps handeln Sie sich auch schnell potenziell unerwünschte Programme (PUP) wie falschen AV oder Adware ein"
Postive Nebeneffekte davon: Man bekommt beim durchgehen ein Überblick über die installierte Software. Man reduziert den genutzten Speicherplatz, verkürzt unter Umständen die Startzeit und entfern ggf. Popups oder ähnliche Dinge die auf die nerven gehen könnten. 


