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

Man kann sich das in etwa wie bei einer wissenschaftlichen Arbeit vorstellen: Falls man bereits den Fehler gemacht hat und nach der Abgabe diese nochmal erneut durchzugehen fallen sehr häufig grammatikalische Fehler auf die man hätte vor der Abgabe bereits erkennen müssen. Solche Fehler passieren mehr oder weniger auch bei dem entwickeln von Software. Das kann dann dazu führen dass eine bestimtme Funktion nie richtig funktioniert hat, oder dass nach einem Update auf einmal Teile der Software unüblich verhalten. Das kann aber im schlimmsten Fall auch dazu führen, dass über einen solchen Fehler eine Lücke in eurer Verteidigungslinie euerer Angriffsfläche gefunden hat und diese ausnutzen kann.

## Angreifer

Über welche Wege kann der Angreifer nun durch Software auf das System gelangen? Die zuvor genannten Programmfehler können von einem oder mehreren Angreifern ausgenutzt werden um dann Zugriff auf das gesamte System zu erhalten, bzw. Programme auszuführen die verschiedenste Dinge ausführen ...

### Exkurs: Supply-Chain-Attacks

Wie bereits erwähnt, ist Software die wir typischerweise auf dem Rechner ist sehr komplex. Das hat auch damit zu tun, dass auch noch zusätzlich zum selbst geschrieben Programmcode noch weiter von anderen Biblitotheken kommen. Um in der Analaogie der wissenschaftlichen Arbeit zu bleiben, wären das unsere verwendeten Quellen, die dann unter umständen auf weitere Quellen verweisen. Und genau hier
