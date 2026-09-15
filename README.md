# Grünwerk Kassa

Ein lokales, responsives Kassaführungssystem für eine Gärtnerei. Die Anwendung läuft ohne Backend direkt im Browser und speichert Verkäufe, Kassenstand und Produktbestand im `localStorage`.

## Start

```bash
python3 -m http.server 4173
```

Danach `http://localhost:4173` öffnen.

## Enthaltene Funktionen

- Tagesübersicht mit Umsatz, Barbestand und Transaktionszahl
- Produktsuche und Filter nach Warengruppe
- Warenkorb mit Mengensteuerung und automatischer Steuerberechnung
- Zahlung per Bar, Karte oder Gutschein
- Wechselgeldberechnung und digitaler Beleg
- Kassenjournal mit Storno-Funktion
- Bestandswarnungen und automatisch aktualisierter Lagerbestand
- Kassenabschluss als CSV-Export
- Lokale Demo-Daten, die jederzeit zurückgesetzt werden können

## Benötigte Eckdaten für den Echtbetrieb

Vor dem produktiven Einsatz müssen mindestens folgende Punkte festgelegt werden:

1. **Betrieb:** Firmenwortlaut, Anschrift, UID/Steuernummer, Währung und Beleg-Fußzeile.
2. **Steuern:** Gültige Umsatzsteuersätze je Warengruppe und Regeln für Gutscheine/Rabatte.
3. **Sortiment:** Artikelnummer, Bezeichnung, Warengruppe, Verkaufspreis, Steuersatz, Einheit, Bestand und Mindestbestand.
4. **Kassenprozess:** Anfangsbestand, erlaubte Zahlungsarten, Einlagen/Entnahmen, Storno- und Rabattberechtigungen.
5. **Belege:** Fortlaufender Nummernkreis, Pflichtangaben, Druckerformat und Aufbewahrungsfrist.
6. **Benutzer:** Mitarbeitende, Rollen, PIN/Anmeldung und Schichtzuordnung.
7. **Recht & Technik:** Landesspezifische Fiskalisierung, Datenschutz, Datensicherung, Offline-Betrieb und Hardware.

> Die Demo ist ein fachlicher Prototyp und ersetzt keine Prüfung der jeweils geltenden steuer- und kassenrechtlichen Anforderungen.
