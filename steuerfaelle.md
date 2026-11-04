# Steuerfälle und Steuercodes

Die App legt für jede Position einer Bestellung einen Steuerfall fest und schreibt **eine Buchungszeile je Steuerfall und Bestellung**. Bestimmend sind das Lieferland, die Steuerzeilen, die Shopify berechnet hat, und eine UID des Käufers. Als Lieferland gilt die Lieferadresse, ersatzweise die Rechnungsadresse, ersatzweise Österreich. Das Belegdatum ist das Bestelldatum in der Zeitzone des Shops.

## Übersicht (BMD-Datei)

| Fall | Erlöskonto (Vorbelegung) | Steuercode | Satz im Feld *mwst* |
|---|---|---|---|
| Inland 20 % | 4000 | 3 | 20 |
| Inland 10 % | 4100 | 3 | 10 |
| Inland 13 % | 4200 | 3 | 13 |
| Ausfuhr Drittland | 4600 | 5 | 0 |
| EU-Unternehmer mit UID (igL) | 4500 | 7 | 0 |
| EU-Privatkunde, OSS aktiv | 4700 | 0 | Satz des Bestimmungslandes |
| Inland 0 % | 4600 | 0 | 0 |

## Die Regeln im Einzelnen

**Lieferland Österreich.** Der Satz kommt von der Steuerzeile der Position. Erlaubt sind 20, 10, 13 und 0 %. Ein anderer Satz bricht den Export ab, und die Fehlermeldung nennt die Bestellung, damit Sie sie in Shopify prüfen können.

**Lieferland außerhalb der EU.** Ausfuhr, 0 %, Steuercode 5.

**Lieferland in der EU (nicht Österreich).**
- Hängt an der Bestellung eine UID des Käufers (Shopify-Unternehmenskunde mit Steuer-ID), oder ist Bestellung bzw. Kunde als steuerbefreit markiert, ist es eine **innergemeinschaftliche Lieferung** (igL), 0 %, Steuercode 7. Die UID wird nur in der DATEV-Datei für RZL mitgeschrieben.
- Sonst, bei gesetztem Häkchen **Für das EU-One-Stop-Shop-Verfahren (OSS) registriert**: OSS mit dem Satz, den der Shop berechnet hat, also dem Satz des Bestimmungslandes. Konto *Erlöse OSS (EU B2C)*.
- Sonst, ohne OSS: österreichische Umsatzsteuer, so wie die Steuerzeile lautet (unter der Lieferschwelle von 10.000 €). Berechnet der Shop dabei einen Satz, den Österreich nicht hat, bucht die App ihn als OSS zu diesem Satz.

## Hinweise

- **OSS hat in den öffentlichen BMD-Unterlagen keinen eigenen Steuercode.** Diese Zeilen tragen Code 0, das Konto *Erlöse OSS* trägt den Fall. Der Satz und der Steuerbetrag stehen aber in der Zeile. Hat Ihre Kanzlei dafür einen Code hinterlegt, teilen Sie ihn dem Support mit.
- **Inland 0 %** (etwa bei steuerfreien Inlandsumsätzen) landet auf dem Konto *Erlöse Ausfuhr (Drittland, 0 %)* mit Code 0. Besprechen Sie solche Fälle mit der Kanzlei und ordnen Sie das Konto bei Bedarf um.
- **Netto und Steuer** rechnet die App aus dem Bruttobetrag der Position und dem Satz; die Steuer ist Brutto minus Netto, die beiden Beträge ergeben also immer genau den Bruttobetrag. Steht der Shop auf „Preise inklusive Steuer“ oder auf „zuzüglich Steuer“, wird beides richtig berücksichtigt.
- **Kleinunternehmer** und **Differenzbesteuerung** bildet die App nicht ab, siehe [Grenzen](grenzen.md).
- Die Konten sind in den Einstellungen änderbar, siehe [Kontenzuordnung](kontenzuordnung.md).

Versand, Trinkgeld, Gutscheine und Rabatte: [Buchungsregeln](buchungsregeln.md).
