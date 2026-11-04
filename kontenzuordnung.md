# Kontenzuordnung

Unter **Einstellungen** › **Kontenzuordnung** legen Sie fest, auf welche Konten die App bucht. Beim Kontenrahmen *EKR (Österreich)* ist die Vorbelegung der BMD-Standard. Jede Zelle ist änderbar. RZL und viele Kanzleien nummerieren anders, deshalb bestätigt Ihre Kanzlei die Konten einmal. Die Geldtransit-, Gutschein- und OSS-Konten sind Konventionen der App, keine Vorgabe von BMD.

## Vorbelegte Konten (EKR)

| Feld in den Einstellungen | Konto |
|---|---|
| Erlöse 20 % | 4000 |
| Erlöse 10 % | 4100 |
| Erlöse 13 % | 4200 |
| Erlöse Ausfuhr (Drittland, 0 %) | 4600 |
| Erlöse EU B2B (igL, mit UID) | 4500 |
| Erlöse OSS (EU B2C) | 4700 |
| Gutschein-Verbindlichkeit | 3600 |
| Geldtransit Shopify Payments | 2850 |
| Geldtransit PayPal | 2851 |
| Geldtransit sonstige Zahlungsarten | 2852 |
| Kassa (Barzahlung, Shopify POS) | 2700 |
| Zahlungsgebühren | 7790 |
| Bank (Auszahlungen Shopify Payments) | 2800 |
| Anpassungen Shopify Payments | 7790 |

Das **Geldtransit**-Konto ist das Gegenkonto jeder Verkaufsbuchung: Shopify zahlt erst später aus. Die Auszahlungsdatei bucht dann Bank gegen Geldtransit, damit das Konto aufgeht. Jede Zahlungsart hat ihr eigenes Konto. Barzahlungen am Shopify-POS gehen auf die Kassa, Karte am POS läuft über Shopify Payments.

## Kontoprüfung

Die App prüft jede Kontonummer, während Sie tippen, und beim Export:

- **Rot (Fehler)**: Nummer nicht nur aus Ziffern, leer, oder die Stellenzahl passt nicht zur **Sachkontenlänge**. Rote Konten blockieren den Export, bis sie korrigiert sind, damit keine Datei entsteht, die der Import ablehnt.
- **Gelb (Hinweis)**: eine Stelle länger als die Sachkontenlänge gilt als Personenkonto (Debitor/Kreditor). Oder das Konto liegt nicht in der üblichen Kontenklasse. Für EKR sind das: Erlöse Klasse 4, Gutschein-Verbindlichkeit 3, Geldtransit, Kassa und Bank 2, Gebühren und Anpassungen 7. Gelb blockiert nichts. Kanzleien haben oft eigene Pläne, dann ist das Konto richtig.

Die Hinweise erscheinen auch als Banner **Kontoprüfung: bitte kurz ansehen** auf Startseite und Auszahlungen.

## Kontenrahmen wechseln

Die Auswahl *EKR (Österreich)* ist für BMD-Export Standard. Es gibt auch SKR03 und SKR04 (deutsche Kontenrahmen); für Österreich werden sie nicht gebraucht. Ein Wechsel setzt alle Konten auf die Standardwerte des gewählten Rahmens zurück.

## Auf die Kanzlei abstimmen

Der [Onboarding-Bericht](onboarding-check.md) listet alle Einstellungen und Konten auf einer Seite. Schicken Sie ihn Ihrer Kanzlei zur Bestätigung, bevor Sie den ersten Monat einspielen.
