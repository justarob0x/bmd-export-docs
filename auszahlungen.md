# Auszahlungen (Shopify Payments)

Der Monatsexport bucht jede Zahlung gegen ein **Geldtransitkonto**: Das Geld ist verdient, aber noch nicht auf dem Bankkonto. Die Auszahlungsdatei schließt diesen Kreis. Sie ist der **zweite Stapel des Monats** und gilt nur für Shopify Payments. Hat Ihr Shop kein Shopify Payments, meldet die Seite, dass es nichts abzugleichen gibt.

## So geht es

1. **Auszahlungen** im Menü öffnen. Beim ersten Mal fragt Shopify einmalig nach der Berechtigung für Auszahlungen (Banner **Neue Berechtigung nötig**).
2. **Monat (Auszahlungsdatum)** wählen. Maßgeblich ist das Datum, an dem Shopify die Auszahlung ausgelöst hat, nicht das Datum der Verkäufe.
3. **Abgleich anzeigen** zeigt die Summen und die Tabelle (Datum, Auszahlung, Umsätze, Erstattungen, Gebühren, Anpassungen, Netto, Hinweise). Die Vorschau ist für jeden Zeitraum frei.
4. **Herunterladen** erzeugt `BMD_Auszahlungen_JJJJ-MM.csv` (bzw. `EXTF_Auszahlungen_JJJJ-MM.csv` im DATEV-Format).

## Was gebucht wird

Nur Auszahlungen mit Status „ausgezahlt“. Je Auszahlung:

- **Bankbuchung**: *Bank* gegen *Geldtransit Shopify Payments* über den **Nettobetrag**, den Shopify überwiesen hat. Eine Rückbelastung (Shopify zieht Geld zurück) dreht die Seiten um.
- **Gebühren**: eine Zeile je Auszahlung auf *Zahlungsgebühren*, 0 % Steuer, gegen das Geldtransitkonto. Mit dem Häkchen **Gebühren je Transaktion buchen** in den Einstellungen stattdessen eine Zeile je Zahlung mit der Bestellnummer im Buchungstext, ungefähr zehnmal so viele Zeilen für dieselbe Summe.
- **Anpassungen**: Änderungen, die Shopify von sich aus am Guthaben vornimmt, auf *Anpassungen Shopify Payments*. Sie sind in der Tabelle als **prüfen** markiert.

Nicht gebucht werden Verkäufe und Erstattungen (die stehen schon im Monatsexport), reservierte Beträge (das Geld liegt noch bei Shopify, das Geldtransitkonto behält den Saldo bis zur Freigabe) und Auszahlungen, die geplant, unterwegs oder fehlgeschlagen sind. Diese zeigt die Seite an, die Datei enthält sie nicht.

## Hinweise in der Tabelle

- **geht auf**: Auszahlung und Einzeltransaktionen stimmen überein.
- **prüfen**: eine Anpassung oder ein Chargeback (Zahlungsstreit). Bei einem verlorenen Chargeback prüfen Sie, ob der Erlös storniert werden muss.
- **Differenz**: Auszahlung und Transaktionen gehen nicht auf. Die Datei wird trotzdem erzeugt, die Auszahlung ist markiert.
- **davon Umsätze aus dem Vormonat**: Verkäufe, die in einem früheren Monat gebucht und erst jetzt ausgezahlt wurden. Das ist normal.

## Nicht abgedeckt

PayPal: Shopify weiß nicht, wann PayPal überweist. Die PayPal-Gebühr je Bestellung steht im Monatsexport. Das PayPal-Konto gleicht die Kanzlei am Kontoauszug ab.

Siehe auch [Kontenzuordnung](kontenzuordnung.md) für die Konten *Bank*, *Zahlungsgebühren* und *Anpassungen*.
