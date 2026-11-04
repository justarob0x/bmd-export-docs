# Erstattungen, Gutscheine, Versand und Rabatte

Was die App für Nebenfälle bucht. Alle Beträge in der Shopwährung; der Euro wird vorausgesetzt (siehe [Grenzen](grenzen.md)).

## Rabatte

Gebucht wird, was der Kunde für die Position bezahlt hat: Positionspreis abzüglich der zugeteilten Rabatte, egal ob der Rabatt auf die Position oder auf die ganze Bestellung gilt. Es gibt keine eigene Rabattbuchung.

## Versand

Der Versand folgt der Ware. Er wird im Verhältnis der Warenwerte auf die Steuersätze der Waren aufgeteilt, eine Bestellung mit 20-%- und 10-%-Ware bekommt also zwei Versandzeilen. Rundungsreste gehen auf die größte Gruppe, die Summe stimmt immer genau. Besteht die Bestellung nur aus Gutschein oder Trinkgeld, gilt für den Versand der Normalsatz 20 %. Der Versand wird auf dasselbe Erlöskonto gebucht wie die Ware.

## Trinkgeld

Als Erlös zum Normalsatz 20 %.

## Gutscheine

- **Verkauf eines Geschenkgutscheins**: auf das Konto *Gutschein-Verbindlichkeit*, ohne Umsatzsteuer.
- **Einlösung**: Der Warenwert steht voll im Erlös. Der mit Gutschein bezahlte Teil kommt nie über Shopify Payments oder PayPal, deshalb bucht die App ihn von der *Gutschein-Verbindlichkeit* auf das Geldtransitkonto der Bestellung. Im Buchungstext steht „Gutscheineinlösung“, dazu die letzten Zeichen der Gutscheinnummer, damit Sie Verkauf und Einlösung zuordnen können.

## Erstattungen

- Gebucht wird nur Geld, das tatsächlich zurückgezahlt wurde (erfolgreiche Rückzahlung in Shopify). Eine Erstattung nur mit Rückbuchung ins Lager, noch offene oder fehlgeschlagene Rückzahlungen erzeugen keine Buchung.
- Die Erstattung spiegelt den Verkauf: dieselben Steuerfälle und Erlöskonten, auf der Gegenseite (Soll). Erstatteter Versand wird wie beim Verkauf auf die Steuersätze der Warenwerte der Bestellung verteilt.
- Weicht der zurückgezahlte Betrag vom Wert der Positionen plus Versand ab (etwa weil Sie den Betrag in Shopify gesenkt oder eine Bearbeitungsgebühr einbehalten haben), werden Positionen und Versand anteilig auf den zurückgezahlten Betrag skaliert.
- Eine Erstattung nur über einen Betrag, ohne ausgewählte Positionen, wird im Verhältnis auf die Steuersätze der Bestellung verteilt.
- Erstattete Gutscheine gehen auf die *Gutschein-Verbindlichkeit*.
- Das **Belegdatum** der Erstattung ist das Datum der Erstattung. Eine Erstattung im Mai zu einer Bestellung vom April steht im Mai-Export.
- Die **Belegnummer** der Erstattung ist die Nummer der Erstattung in Shopify. Die Bestellnummer steht in der externen Belegnummer und im Buchungstext („Erstattung #1042“).

## Gebühren

- **PayPal**: Die Gebühr pro Bestellung steht im Monatsexport auf dem Konto *Zahlungsgebühren*, 0 % Steuer, gegen das PayPal-Geldtransitkonto.
- **Shopify Payments**: Die Gebühren stehen in der [Auszahlungsdatei](auszahlungen.md), nicht im Monatsexport.

## Zahlungsarten

Die Zahlungsart der Bestellung bestimmt das Geldtransitkonto: Shopify Payments, PayPal (jede Schreibweise, die mit „paypal“ beginnt), Barzahlung am POS (Kassa) oder alles andere (*Geldtransit sonstige Zahlungsarten*, z. B. Klarna oder Vorkasse).

## Buchungstext

„Shopify #1042“ bei Verkäufen, dazu „Versand“, „Trinkgeld“, „Erstattung“, „Gutscheinverkauf“, „Gutscheineinlösung“ oder „Gebühr PayPal“ mit der Bestellnummer. Kundennamen liest die App nicht; sie stehen nie in der Datei. Maximal 40 Zeichen in der BMD-Datei.
