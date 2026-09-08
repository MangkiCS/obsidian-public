---
publish: true
title: Fire TV Stick als besseres YouTube-Gerät mit SmartTube
created: 2026-09-05
modified: 2026-09-08T10:43:10.456Z
tags:
  - fire-tv
  - smarttube
  - youtube
  - android
  - self-hosting
  - privacy
---

Fire TV Stick als besseres YouTube-Gerät mit SmartTube

Ein älterer Amazon Fire TV Stick kann überraschend gut als dediziertes YouTube-Gerät funktionieren — ohne Browser, Maus oder Tastatur.

Mein Setup basiert auf einem Fire TV Stick 4K der ersten Generation mit Fire OS 6.7.1.1. Das Ziel war ursprünglich, YouTube ähnlich wie im Desktop-Browser zu verwenden: weniger Werbung, SponsorBlock, Kontrolle über Sprache und Wiedergabe und trotzdem vollständige Bedienung mit der Fire-TV-Fernbedienung.

Die sinnvollste Lösung dafür ist nicht Firefox oder Chrome, sondern SmartTube.

Warum kein Browser?

Fire OS basiert bei älteren Fire-TV-Geräten auf Android. Man kann deshalb Android-APKs sideloaden.

Theoretisch könnte man Firefox oder Chrome installieren. Praktisch ist das am Fernseher aber unkomfortabel:

- Android-Browser sind auf Touchbedienung ausgelegt
- Navigation mit dem Steuerkreuz ist mühsam
- Chrome für Android unterstützt keine normalen Desktop-Chrome-Extensions
- Firefox Android unterstützt Extensions, ist aber nicht als TV-Oberfläche gedacht
- Eingabefelder und Webseiten-Navigation sind mit einer Fernbedienung unangenehm

Wenn das Hauptziel YouTube ist, löst SmartTube genau dieses Problem.

SmartTube

"SmartTube" (https://github.com/yuliskov/SmartTube) ist ein Open-Source-YouTube-Client für Android-TV-Geräte.

Im Gegensatz zu NewPipe oder PipePipe ist SmartTube explizit für einen Fernseher und eine normale TV-Fernbedienung gebaut.

Zu den interessanten Funktionen gehören:

- keine klassischen YouTube-Werbeunterbrechungen
- SponsorBlock
- YouTube-Konto und eigene Abonnements
- Verlauf
- Playlists
- Empfehlungen
- Geschwindigkeitssteuerung
- Videoqualitätsauswahl
- HDR und 4K
- Untertitel
- Livechat
- konfigurierbare Fernbedienung
- Filter für Shorts
- verschiedene Audio-Spuren

SmartTube fühlt sich damit ein wenig an wie:

«YouTube im Desktop-Browser mit einigen Extensions — nur als native TV-App.»

SmartTube vs. NewPipe und PipePipe

Die drei Apps verfolgen etwas unterschiedliche Ziele.

Funktion| SmartTube| NewPipe| PipePipe
TV-Fernbedienung| sehr gut| schlecht| schlecht
YouTube-/Google-Konto| ja| nein| teilweise
YouTube-Abos synchronisieren| ja| lokal| überwiegend lokal
Werbung entfernen| ja| ja| ja
SponsorBlock| ja| nicht standardmäßig| ja
Downloads| nebensächlich| sehr gut| sehr gut
Shorts-Filter| ja| begrenzt| sehr umfangreich
TV-Oberfläche| ja| nein| nein

Für ein Smartphone würde ich weiterhin NewPipe oder PipePipe interessant finden.

Für den Fernseher ist SmartTube deutlich geeigneter.

Installation per Sideloading

Ein klassischer Jailbreak oder Root ist nicht nötig.

Fire OS erlaubt die Installation externer Android-APKs.

Entwickleroptionen aktivieren

Auf dem Fire TV:

Einstellungen
→ Mein Fire TV
→ Entwickleroptionen

Dort:

Apps aus unbekannten Quellen → EIN

Falls die Entwickleroptionen nicht sichtbar sind:

Einstellungen
→ Mein Fire TV
→ Info

Den Eintrag des Fire TV Sticks markieren und mehrfach die mittlere OK-Taste drücken.

Downloader installieren

Im Amazon Appstore nach folgender App suchen:

Downloader

Danach Downloader öffnen.

SmartTube installieren

SmartTube stellt einen kurzen offiziellen Download-Link bereit.

Für die Beta-Version:

https://kutt.to/stn\_beta

Für Stable:

https://kutt.to/stn\_stable

Den Link direkt in Downloader eingeben.

Danach:

Download
→ APK öffnen
→ Installieren

Die APK-Datei kann anschließend wieder gelöscht werden.

SmartTube selbst bleibt installiert.

Amazon-Konto

SmartTube benötigt kein Amazon-Konto.

Der Fire TV Stick selbst möchte allerdings für den normalen Betrieb bei einem Amazon-Konto registriert sein.

Das Amazon-Konto und das YouTube-Konto sind voneinander unabhängig:

Amazon-Konto
↓
Fire-TV-System

Google-/YouTube-Konto
↓
SmartTube

Ein altes oder fremdes Amazon-Konto kann vom Fire TV deregistriert werden.

Danach kann man ein eigenes oder auch ein separates minimalistisches Amazon-Konto verwenden.

SmartTube automatisch starten

Fire OS besitzt keine normale Einstellung wie:

Beim Einschalten → SmartTube starten

Dafür gibt es die kleine Open-Source-App Launch on Boot.

Bei meinem Fire OS 6.7.1.1 ist sie interessanter als einige neuere Launcher-Hacks.

Warum nicht FTVLaunchX oder Home on Fire?

FTVLaunchX war früher eine interessante Möglichkeit, sogar die Home-Taste umzuleiten.

Neuere Fire-OS-6-Versionen blockieren diese Methode allerdings.

Auch Home on Fire funktioniert laut Projekt nicht auf Fire OS 6.7.1.1.

Für einen einfachen Autostart ist Launch on Boot deshalb die weniger invasive Lösung.

Launch on Boot installieren

Die APK kann direkt aus dem F-Droid-Repository geladen werden:

https://f-droid.org/repo/news.androidtv.launchonboot\_12.apk

In Downloader:

URL eingeben
→ Go
→ APK installieren

Danach Launch on Boot öffnen.

Einstellungen

Für SmartTube:

Enabled → ON

Launch TV app on boot → OFF

Launch when device wakes up → ON

Select App → SmartTube

Wichtig ist besonders:

Launch when device wakes up

Ein Fire TV Stick wird beim Ausschalten des Fernsehers normalerweise nicht komplett heruntergefahren. Er geht nur in Standby.

Im Alltag ist deshalb das Aufwachen wichtiger als ein echter Boot.

Das gewünschte Verhalten ist dann:

TV einschalten
↓
Fire TV wacht auf
↓
SmartTube öffnet sich

Die Home-Taste führt weiterhin zurück zur Amazon-Oberfläche.

Das finde ich sogar sinnvoll: Man erhält einen einfachen Rettungsweg, falls SmartTube einmal nicht funktioniert.

Empfohlene SmartTube-Einstellungen

SmartTube besitzt sehr viele Einstellungen. Für einen älteren Fire TV Stick würde ich zunächst nur einige davon ändern.

SponsorBlock

Einstellungen
→ SponsorBlock

Sponsoren:

automatisch überspringen

Auch Dinge wie:

Like & Subscribe
Eigenwerbung

kann man automatisch überspringen lassen.

Intro und Outro würde ich zunächst nur mit einer Überspringen-Schaltfläche versehen und nicht komplett automatisch überspringen.

Shorts ausblenden

Falls Shorts nicht gewünscht sind:

Einstellungen
→ Inhalte / Interface
→ Shorts ausblenden

Die genaue Bezeichnung kann je nach SmartTube-Version etwas variieren.

Videoqualität

Der Fire TV Stick 4K der ersten Generation unterstützt problemlos VP9 und 4K.

Sinnvoll:

Maximum: 2160p
Codec: VP9

AV1 sollte man auf diesem älteren Modell vermeiden.

Buffer

Buffer → High

Nicht unbedingt maximale oder extreme Buffer-Größen verwenden, weil der alte Stick nur relativ wenig RAM besitzt.

Auto Frame Rate

Zunächst:

Auto Frame Rate / AFR → AUS

Wenn später alles stabil läuft, kann man damit experimentieren.

Keine automatisch übersetzten Audiospuren

YouTube verwendet mittlerweile automatisch generierte bzw. übersetzte Tonspuren.

Das kann dazu führen, dass beispielsweise ein englisches Video plötzlich deutsch synchronisiert abgespielt wird.

In SmartTube sollte man dafür die bevorzugte Audio-Sprache deaktivieren.

Sinngemäß:

Einstellungen
→ Player
→ Audio Language
→ None / Keine

Dann sollte SmartTube möglichst die Originaltonspur verwenden.

Bei einem einzelnen Video kann man die Sprache trotzdem manuell ändern:

Video starten
→ OK
→ HQ / Player-Menü
→ Audio Language

Damit bleibt normalerweise:

Standard → Originalsprache

und nur bei Bedarf:

manuell → deutsche oder andere Tonspur

Originaltitel statt Übersetzungen

Falls SmartTube bzw. YouTube auch Videotitel automatisch übersetzt:

Unlocalized video titles → EIN

Damit wird versucht, den Originaltitel des Videos anzuzeigen.

Alexa-Sprachsuche mit SmartTube

Die Mikrofontaste der Fire-TV-Fernbedienung funktioniert anders als die Sprachsuche auf Android TV.

Sie gehört zu Alexa und nicht direkt zum aktuell fokussierten Eingabefeld.

SmartTube stellt dafür eine kleine Amazon Bridge bereit.

Bridge installieren

Zuerst sollte die offizielle YouTube-App vom Fire TV entfernt werden.

Danach in Downloader:

https://kutt.to/stn\_bridge\_amazon

APK installieren.

Die Bridge läuft im Hintergrund und muss normalerweise nicht separat geöffnet werden.

Danach können Sprachsuchen wie:

YouTube Veritasium Black Holes

über Alexa an SmartTube weitergeleitet werden.

Es handelt sich allerdings nicht um klassisches Diktieren in das gerade sichtbare SmartTube-Suchfeld.

Das Modell ist eher:

Alexa-Suche
↓
YouTube-Suchanfrage
↓
SmartTube

Bluetooth-Soundbar und Lautstärke 0

Ein weiteres interessantes Problem trat mit einer per Bluetooth verbundenen Soundbar auf.

Symptom:

Video startet
↓
ca. 0,5 Sekunden später
↓
Lautstärkeanzeige: 0
↓
Ton weg

Wenn die Bluetooth-Soundbar ausgeschaltet wurde, trat das Problem nicht mehr auf.

Damit liegt die Ursache wahrscheinlich in der Bluetooth-Lautstärkesynchronisation zwischen Fire TV und Soundbar.

Android verwendet dafür Bluetooth Absolute Volume.

Dabei werden:

Fire-TV-Lautstärke

und:

Bluetooth-Gerät-Lautstärke

miteinander gekoppelt.

Ein falscher Lautstärkewert beim Start des Players kann dadurch direkt auf die Soundbar übertragen werden.

Eine mögliche Lösung ist, Absolute Volume per ADB zu deaktivieren:

adb shell setprop persist.bluetooth.disableabsvol true
adb reboot

Alternativ existiert bei manchen Android-Systemen:

adb shell settings put global bluetooth\_disable\_abs\_volume 1
adb reboot

Danach werden Fire-TV- und Soundbar-Lautstärke stärker voneinander getrennt.

Falls möglich, ist für eine Soundbar allerdings eine kabelgebundene Verbindung wie:

HDMI ARC / eARC

meist robuster als Bluetooth.

Wenn SmartTube nur noch lädt

Ein weiteres Problem:

Beim Öffnen eines Videos erscheint nur noch ein Ladekreis.

Der Kreis verschwindet kurz und erscheint erneut.

Wenn das bei mehreren Videos passiert, sollte man zunächst nicht sämtliche Einstellungen zurücksetzen.

Die erste Fehlerbehebung:

Einstellungen
→ Anwendungen
→ Installierte Apps verwalten
→ SmartTube
→ Stopp erzwingen
→ Cache löschen

Nicht:

Daten löschen

weil dabei Anmeldung und Einstellungen verloren gehen können.

Danach:

Mein Fire TV
→ Neustart

Weitere mögliche Ursachen:

- problematische SmartTube-Version
- VPN
- AdGuard
- NextDNS
- Pi-hole
- andere DNS-/Tunnel-Konfigurationen
- problematischer Codec

Bei einem alten Fire TV Stick sollte man testweise:

VP9

oder:

AVC / H.264

verwenden und AV1 vermeiden.

Ergebnis

Ein älterer Fire TV Stick ist für dieses Projekt fast interessanter als ein neues Modell.

Mit:

Fire TV Stick 4K Gen. 1

- Fire OS 6
- SmartTube
- Launch on Boot
- Amazon Bridge

entsteht ein ziemlich gutes dediziertes YouTube-Gerät.

Der ideale Ablauf sieht dann so aus:

Fernseher einschalten
↓
Fire TV wacht auf
↓
SmartTube startet
↓
YouTube-Abos und Empfehlungen
↓
SponsorBlock
↓
keine normalen Werbeunterbrechungen
↓
Originalton
↓
Fernbedienungssteuerung

Und falls etwas schiefgeht:

Home

führt weiterhin zurück zur normalen Fire-TV-Oberfläche.

Das ist für mich der attraktivste Kompromiss: SmartTube fühlt sich im Alltag beinahe wie das eigentliche Betriebssystem des Sticks an, ohne Fire OS selbst tiefgreifend modifizieren zu müssen.
