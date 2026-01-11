---
title: "Software Updates"
weight: 2
---

# Software Updates

## Einleitung

Software auf dem aktuellen Stand zu halten ist eine der wichtigsten Maßnahmen zur Verbesserung der IT‑Sicherheit. Updates schließen bekannte Schwachstellen, bevor Angreifer sie ausnutzen können. Trotzdem werden Patches oft verzögert installiert — aus Unwissenheit, Misstrauen oder Bequemlichkeit. Hier wird deshalb erklärt, warum regelmäßige Aktualisierungen wichtig sind, wie Updates kommuniziert werden und welche Update‑Strategien Hersteller anbieten.

## Grundproblem

Nach [Software Hygiene]({{<ref "hygiene.md">}}) sollten nur Programme auf Geräten bleiben, die tatsächlich genutzt werden. Diese verbleibende Software muss jedoch regelmäßig gepflegt werden. Sicherheitsexpertinnen und -experten sehen das zeitnahe Einspielen von Sicherheitsupdates als eine der effektivsten Schutzmaßnahmen an — noch vor Passwortmanagern oder Zwei‑Faktor‑Authentifizierung. Viele Anwenderinnen und Anwender unterschätzen jedoch den Nutzen, weshalb Patches oft spät installiert werden.

![Prozentualer Unterschied](Differnce_Experts_Non-IT.png)

> Aus [““...No one Can Hack My Mind”: Comparing Expert and Non-Expert Security Practices, Ion et al.](https://www.usenix.org/system/files/conference/soups2015/soups15-paper-ion.pdf)

## Gründe für Verzögerungen

Nutzerinnen und Nutzer nennen verschiedene Gründe, warum sie Updates aufschieben:

- Unklarer Nutzen: Der Wert eines Updates ist vielen nicht bewusst.
- Angst vor Problemen: Sorge, dass Updates Fehler einführen oder bösartigen Code enthalten könnten.
- Unverständlicher Prozess: Es ist oft nicht ersichtlich, welche Änderungen ein Update bringt.
- Manuelle Abläufe: Fehlende Automatisierung macht die Installation aufwändig.

## Konkrete Folgen (Beispiele)

### EternalBlue und WannaCry

EternalBlue ist eine Schwachstelle im SMB‑Protokoll, die 2017 bekannt wurde (CVE‑2017‑0144). Sie wurde von der Schadsoftware WannaCry massenhaft ausgenutzt und infizierte Hunderttausende Rechner weltweit, darunter Krankenhäuser und Unternehmen. Systeme ohne aktuelle Patches blieben anfällig. **(Quelle ergänzen)**

### WinRAR

In älteren WinRAR‑Versionen (vor 6.23) wurde 2023 eine Schwachstelle öffentlich, die manipulierte ZIP‑Archive ausnutzte. Unter bestimmten Bedingungen konnte beim Entpacken Schadcode ausgeführt werden. Nutzerinnen und Nutzer ohne aktuelles Update waren gefährdet. **(Quelle: CVE‑Eintrag / Hersteller‑Advisory ergänzen)**

## Was ist ein Update

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
  Weil Releases häufig beides kombinieren, gilt: **Alle Updates sollten zeitnah geprüft und installiert werden.**

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

Unter Linux sind Paketmanager (apt, yum, dnf, zypper) Standard. Unter Windows gibt es seit einigen Jahren **winget**; für macOS nutzen viele Homebrew.

## Übersicht Updateverteilung

| Quelle             | Mechanismus                                    | Beispiele                               | Vorteile                   | Empfehlung                                 |
| ------------------ | ---------------------------------------------- | --------------------------------------- | -------------------------- | ------------------------------------------ |
| Betriebssystem     | Automatisch; Halbautomatisch; Manuell          | Windows Update, macOS Softwareupdate    | Deckt OS‑Sicherheitslücken | Automatische Updates prüfen/anschalten     |
| App Store          | Automatisch; Halbautomatisch                   | Google Play, App Store, Microsoft Store | Zentrale Verwaltung        | Automatische App‑Updates aktivieren        |
| In‑App Updater     | Automatisch; Halbautomatisch; Benachrichtigung | Browser, PDF‑Reader, Spiele             | Schnelle Verfügbarkeit     | Bei Sicherheitshinweis sofort installieren |
| Herstellerwebseite | Manuell; Halbautomatisch                       | Grafikkartentreiber, Spezialsoftware    | Direkt vom Hersteller      | Nur offizielle Downloads verwenden         |
| Paketmanager       | Automatisch; Halbautomatisch                   | apt, winget, Homebrew                   | Batch‑Updates              | Für technisch Interessierte geeignet       |

## Empfehlungen für Privatanwender

- **Automatische Updates aktivieren** für Betriebssystem und Browser.
- **App‑Store‑Updates erlauben** für alle Apps aus App-Stores.
- **Bei manuellen Downloads** nur offizielle Herstellerseiten nutzen vgl [Sichere Quellen]({{<ref "quellen.md">}}).
