---
publish: true
title: solarthermie auf kleinem raum
created: 2026-08-18
modified: 2026-08-18T12:07:05.949Z
tags:
  - diy
  - solarthermie
  - balkon
  - energie
---

# solarthermie auf kleinem raum

Die Ausgangsfrage war ziemlich einfach: **Wie viel gekaufte Energie lässt sich mit sehr einfachen Solar-Luft- und Solar-Wasserkollektoren vermeiden?**

Die drei Videos waren dafür weniger Bauanleitung als Ausgangspunkt:

- [Building & Testing 4 DIY Solar Water Heaters](https://youtu.be/NiuYDMNnPCU)
- [DIY Solar Collectors: Upgraded Build & Testing](https://youtu.be/6fCx8LTxLP4)
- [Built & Tested: 5 DIY Solar Air Heaters](https://youtu.be/8cPuVZjnbi4)

## der ort ist das eigentliche problem

Der Balkon zeigt nach Norden und wird teilweise verschattet. Das verändert fast alles.

Ein großer fest montierter Kollektor ist dort vermutlich weniger sinnvoll als ein **kleiner, beweglicher Kollektor**, der kurze Phasen direkter Ost-/Westsonne mitnehmen kann. Diffuses Licht funktioniert weiterhin, aber deutlich schwächer.

Daraus folgt:

> nicht auf konstante Leistung bauen. auf kurze brauchbare Wärmefenster bauen.

Der Gemeinschaftshof könnte deshalb für mobile Kollektoren interessanter sein als der Balkon selbst.

## luftkollektor

Der interessanteste Aufbau aus dem Vergleichsvideo ist der **Screen-Absorber**: mehrere Lagen schwarzes, luftdurchlässiges Netz in einem gedämmten Kasten.

Vorne sitzt keine normale Glasscheibe, sondern eine **Polycarbonat-Doppelstegplatte** — zwei dünne Schichten mit Luftkammern dazwischen. Für den geplanten DIY-Kollektor bietet sich ungefähr **60 × 120 cm** an.

Ein einfacher Aufbau:

```text
sonne
  ↓
doppelstegplatte
  ↓
luftspalt
  ↓
2–4 lagen schwarzes screen/gewebe
  ↓
luftspalt
  ↓
gedämmte rückwand
```

Die Luft wird durch das warme Netz geführt. Ein kleiner 5/12-V-Lüfter reicht für erste Versuche.

Die wichtigste Verbesserung ist keine bessere Farbe oder exotisches Metall, sondern eine **Differenztemperatursteuerung**:

```text
kollektor > zielraum + 3–5 K  →  lüfter an
sonst                         →  lüfter aus / bypass
```

So wird der Kollektor bei Schatten nicht selbst zum Kühler.

## was die forschung dazu sagt

Die besprochene Arbeit zu Solar-Luftkollektoren unter wechselndem Wetter zeigt vor allem, dass Stundenmittelwerte täuschen können.

Bei Wolken schwankt die reale Austrittstemperatur stark. Stationäre und dynamische Modelle konnten kurzfristig um ungefähr **15 °C** auseinanderliegen.

Drei Dinge sind für den Eigenbau besonders nützlich:

1. **wenig thermische Masse reagiert schneller** auf kurze Sonnenfenster,
2. **mehr Luftstrom senkt die Austrittstemperatur**, kann aber mehr Gesamtwärme transportieren,
3. **Steuerung wird bei wechselnder Einstrahlung wichtiger als Spitzenleistung**.

Das spricht ziemlich gut für einen leichten Screen-Absorber plus temperaturgeregelten Lüfter.

## nicht dort sammeln, wo die sonne ohnehin landet

Ein Kollektor **hinter einem sonnigen Wohnungsfenster** bringt als Raumheizung kaum zusätzliche Energie.

Das Licht, das bereits durch das Fenster gekommen ist, wird früher oder später ohnehin von Boden, Möbeln und Wänden absorbiert und zu Wärme.

Interessant ist ein Kollektor erst auf einer Fläche, deren Sonnenenergie sonst **nicht** in der Wohnung landen würde.

## warmwasser

Der Wasserkollektor aus dem ersten Video bleibt technisch reizvoll:

```text
schwarzes rohr
      ↓
verglaster / transparenter kollektor
      ↓
kleine pumpe
      ↓
30–60 l isolierter speicher
```

Wasser ist eine sehr billige Wärmebatterie.

50 l Wasser mit +25 K Temperaturhub speichern ungefähr **1,45 kWh Wärme**.

Für diese Wohnung ist der finanzielle Nutzen aber begrenzt, weil **Warmwasser und Heizung mit Gas** erzeugt werden. Eine thermische kWh ersetzt hier deutlich billigere Gaswärme statt teuren Haushaltsstrom.

Solar-Warmwasser bleibt deshalb eher ein späteres Experiment als der erste Sparhebel.

## der bessere sparhebel: strom vermeiden

Wärme aus Solarthermie ist besonders wertvoll, wenn sie einen elektrischen Verbraucher ersetzt.

Die ursprüngliche Idee war deshalb ein solar unterstützter Wäschetrockenschrank. Der Aufbau entwickelte sich zu einem modularen System aus:

- transparentem Schrank / Hülle
- warmer Zuluft unten
- großer Abluft oben
- Luftverteiler unter der Wäsche
- Solar-Luftkollektor
- 5/12-V-Lüftern

Der gleiche Schrank soll aber nicht nur eine Funktion haben.

## gewächshaus statt einzelgerät

Für den Balkon ist ein **fertiges schmales Foliengewächshaus** wahrscheinlich günstiger als ein kompletter Eigenbau.

Interessante Größen liegen ungefähr bei:

```text
70 cm breit
50 cm tief
160–190 cm hoch
```

Damit entsteht ein kleiner modularer Klimaschrank.

Im Frühjahr und Herbst: Gewächshaus.\
Bei Bedarf: belüfteter Trockenschrank.\
Unten: 20–60 l Wasser als passive thermische Masse.\
Seitlich/unten: NW100-Anschluss für den Luftkollektor.

Auf einem Nordbalkon ist allerdings **Licht eher der Engpass als Wärme**. Der Kollektor sollte deshalb nur ergänzen, nicht versuchen, mangelnde Sonneneinstrahlung durch hohe Temperatur zu kompensieren.

## kleine photovoltaik

Kleine 50-W-PV-Module wurden ebenfalls betrachtet.

Als Mini-Balkonkraftwerk sind sie auf einem verschatteten Nordbalkon wirtschaftlich fraglich. Interessanter ist eine andere Rolle:

```text
kleines pv-panel
     ↓
5/12 V
  ↙      ↘
lüfter   pumpe
```

Sonne vorhanden → Lüfter/Pumpe läuft.\
Sonne weg → System fährt weitgehend von selbst herunter.

Damit spart man Akku, Wechselrichter und einen Teil der Steuerung.

## die sinnvolle architektur

Nicht fünf Kollektoren für fünf Anwendungen bauen.

Eher zwei universelle Quellen:

```text
solar-luftkollektor
  ├─ gewächshaus
  ├─ trocknung
  └─ experimentelle raumluft-erwärmung

solar-wasserkollektor
  ├─ wärmespeicher
  ├─ nutzwasser
  └─ spätere experimente
```

Standardisierte Anschlüsse helfen:

- **Luft:** NW100
- **Wasser:** Gartenschlauch-Schnellkupplungen
- **Elektrik:** 5/12 V

## was zuerst gebaut werden sollte

Die Reihenfolge mit dem besten Verhältnis aus Erkenntnis, Kosten und Nutzen:

1. **kleinen Screen-Luftkollektor** (~60 × 120 cm) bauen,
2. zwei Temperaturfühler + geregelten Lüfter hinzufügen,
3. tatsächliche Leistung auf dem Nordbalkon messen,
4. ein günstiges schmales Foliengewächshaus als Zielraum nutzen,
5. erst danach entscheiden, ob mehr Kollektorfläche sinnvoll ist,
6. Solar-Wasserkollektor nur bauen, wenn ein konkreter Anwendungsfall entsteht.

Der wichtigste Gedanke aus allem bisher:

> **Nicht versuchen, möglichst viel Wärme zu erzeugen. Versuchen, billige Wärme genau dann einzufangen, wenn sie vorhanden ist, und damit gekaufte Energie oder einen anderen Nutzen zu ersetzen.**

---

## material, das bereits sinnvoll erschien

Für den Luftkollektor:

- Polycarbonat-Doppelstegplatte, etwa 4–6 mm
- Holzrahmen + dünne Rückwand
- vorhandene Dämmreste
- schwarzes Fiberglas-Fliegengitter als Screen-Absorber
- NW100-Luftanschlüsse / Schlauch
- 120–140-mm-Lüfter, 5 oder 12 V
- Temperatur-/Feuchtesensoren
- Aluband + wetterfeste Abdichtung

Hornbach war für Platten, Holz, Lüftungsteile und Gewächshaus-Grundkörper bislang die naheliegendste Bezugsquelle; Lüfter und kleine PV-Module können anderswo günstiger sein.

## offene fragen

- Wie viele Minuten/Stunden direkte Sonne erreicht die nutzbare Balkonfläche wirklich?
- Welche Ost-/West-Ausrichtung ist möglich?
- Wie hoch ist die Temperaturdifferenz des 0,7-m²-Kollektors bei diffusem Licht?
- Reicht das für das Gewächshaus im Frühjahr/Herbst?
- Ist ein zweiter kleiner Kollektor wirtschaftlicher als ein größerer erster?

Das lässt sich besser **messen als erraten**.
