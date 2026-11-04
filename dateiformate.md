# Dateiformate und Import

Unter **Einstellungen** › **Exportformat** wählen Sie, in welchem Format die App schreibt. Beide Formate enthalten dieselben Buchungen.

## BMD NTCS: Buchungsimport (CSV)

Standard. Die Datei heißt `BMD_Buchungen_JJJJ-MM.csv` (Auszahlungen: `BMD_Auszahlungen_JJJJ-MM.csv`).

**Aufbau**
- Textdatei, Spalten durch `;` getrennt, Zeilenende CRLF, Dezimalkomma, Datum als JJJJMMTT, Zeichensatz ANSI (Windows-1252).
- Die erste Zeile benennt die Spalten (variabler Satzaufbau). Die Datei hat keinen Kopfsatz mit Berater- und Mandantennummer.
- Eine Zeile je Buchung.

**Spalten, in dieser Reihenfolge:** `belegnr`, `belegdat`, `buchdat`, `konto`, `gkto`, `bucod`, `betrag`, `mwst`, `steuer`, `steucod`, `symbol`, `extbelegnr`, `text`, `gegenbuchkz`, `verbuchkz`.

**Was drinsteht**
- `konto`: das Erlös- bzw. Aufwandskonto. Nur dort rechnet BMD die Steuer. `gkto`: das Gegenkonto, bei Verkäufen das Geldtransitkonto der Zahlungsart.
- `betrag` ist der Nettobetrag, `steuer` der Steuerbetrag, beide getrennt. Erlöse stehen im Haben (negativ, `bucod` 2), Erstattungen im Soll (positiv, `bucod` 1).
- `mwst`: der Satz, z. B. `20`. `steucod`: der Steuercode, siehe [Steuerfälle](steuerfaelle.md) (3, 5, 7 oder 0).
- `symbol`: immer `AR`. `belegnr`: die Ziffern der Bestellnummer (höchstens 9), bei Erstattungen die Nummer der Erstattung. `extbelegnr`: die Bestellnummer, `text` der Buchungstext.
- `gegenbuchkz` `E` und `verbuchkz` `A`: BMD erzeugt Gegen- und Sammelbuchungen selbst, die Datei enthält keine.

**Import in BMD NTCS:** FIBU › Buchen › Import, mit variablem Satzaufbau. Die Angaben zum Pfad stammen aus der App-Hilfe; die genauen Menüs hängen von Ihrer BMD-Version und Ihrer Kanzlei ab.

## DATEV-Format für RZL

Wählen Sie *DATEV-Format — für RZL (liest DATEV-CSV)*. Die Datei heißt `EXTF_Buchungsstapel_JJJJ-MM.csv` (Auszahlungen: `EXTF_Auszahlungen_JJJJ-MM.csv`).

- Es ist das DATEV-Buchungsstapelformat (EXTF) mit Kopfsatz. In den Kopf kommen **Beraternummer**, **Mandantennummer**, Wirtschaftsjahr, Sachkontenlänge und optional das **Diktatkürzel**, siehe [Einrichtung](einrichtung.md).
- Die Konten sind die EKR-Konten aus Ihren Einstellungen. Ein DATEV-Steuerschlüssel (BU-Schlüssel) wird für EKR nicht geschrieben.
- Die Datei geht unverändert an die Kanzlei. RZL FIBU bzw. EA-Rechnung lesen sie über die Datenimport-Schnittstelle für das DATEV-Format ein; nach der App-Hilfe als „DATEV-Format“.

## Beta

Beide Dateien sind nach den Schnittstellenbeschreibungen von BMD und RZL gebaut, aber nach Angabe der App noch von keiner Kanzlei produktiv importiert worden. Importiert die Kanzlei zum ersten Mal, sollte sie zuerst einen Monat prüfen. Meldet der Import einen Fehler, schicken Sie dem Support die Meldung des Programms, den Monat, die BMD-Version und die Bestellnummer: Zeichensatz, Steuercodes und Spalten lassen sich anpassen.

## Erneut exportieren

Die Datei wird bei jedem Klick frisch erzeugt. Importieren Sie einen Monat, den die Kanzlei schon verbucht hat, nicht ein zweites Mal.
