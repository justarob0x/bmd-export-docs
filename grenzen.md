# Grenzen

Was BMD-Export nicht tut, damit Sie und Ihre Kanzlei es vorher wissen.

## Beta-Status des Imports

Die BMD- und die RZL-Datei sind nach den Schnittstellenbeschreibungen gebaut und mit den Tests der App geprüft, aber nach Angabe der App noch nicht von einer Kanzlei produktiv importiert worden. Jede Kanzlei hat eigene Kontenpläne und Steuercodes. Prüfen Sie den ersten Import mit einem Monat und melden Sie das Ergebnis dem Support. Als Dank für die Rückmeldung zum ersten Import gibt es einen Gratismonat.

## Steuer

- **Kleinunternehmer** (§ 6 Abs. 1 Z 27 UStG): kein eigener Schalter. Der Onboarding-Check fragt danach und gibt den Fall an den Support weiter.
- **Differenzbesteuerung** (§ 24 UStG): wird nicht abgebildet.
- **OSS-Umsätze haben keinen eigenen BMD-Steuercode**, sie tragen Code 0 und das OSS-Konto. Siehe [Steuerfälle](steuerfaelle.md).
- Steuersätze außer 20/10/13/0 % für Inlandsumsätze brechen den Export ab (mit Bestellnummer in der Meldung).
- Die App entscheidet nach den Daten, die Shopify liefert. Ob die Zuordnung für Ihr Unternehmen richtig ist, bestätigt Ihre Kanzlei; die App ist keine Steuerberatung.

## Daten und Umfang

- **Nur Shopify-Bestellungen.** Umsätze aus anderen Kanälen (Amazon, eBay, andere Kassen) bucht die Kanzlei getrennt. Kartenzahlungen am Shopify-POS laufen wie online. Die Kassenführung selbst (Kassabuch, Registrierkasse) bleibt bei Ihrem Kassensystem.
- **Nur Euro.** Shops mit anderer Basiswährung werden nicht umgerechnet; der Onboarding-Check meldet es.
- **Keine Belege** (Rechnungs-PDFs), **keine Debitoren je Kunde**, keine Fremdwährungsumrechnung.
- **Zeitfenster der Bestelldaten:** BMD-Export hat keine Shopify-Berechtigung für ältere Bestellungen; Shopify liefert der App nur die Bestellungen der letzten 60 Tage. Exportieren Sie jeden Monat bald nach Monatsende: Ein Monat, der weiter zurückliegt, wäre unvollständig. Bei der OSS-Meldung und der Lieferschwelle weist die App darauf hin.
- **Eine Datei je Kalendermonat.** Der laufende Monat ist eine Vorschau und wird nach Monatsende neu exportiert.

## Zahlungen

- **PayPal-Auszahlungen** werden nicht abgeglichen; die Gebühr je Bestellung steht im Export, den Rest gleicht die Kanzlei am Kontoauszug ab.
- Auszahlungsabgleich nur mit **Shopify Payments**.

## Sprache

Die App ist deutsch. Es gibt keine englische Oberfläche.
