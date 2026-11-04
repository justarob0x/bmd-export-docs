# Einrichtung

Die App ist in wenigen Minuten bereit. Die Einrichtung läuft in dieser Reihenfolge.

## 1. App installieren

BMD-Export gibt es im Shopify App Store: https://apps.shopify.com/bmd-export-2. Bei der Installation fragt Shopify nach Lesezugriff auf Bestellungen, Kunden (nur Land und Steuerbefreiung, keine Namen) und Shopify-Payments-Auszahlungen. Beim ersten Öffnen der Auszahlungen fragt Shopify unter Umständen noch einmal nach der Berechtigung dafür. Das gilt für Shopify-Payments-Shops.

Zur Anmeldung beim Abo siehe [Abo, Daten und Support](abo-daten-support.md). Der Onboarding-Check ist schon vor dem Abo nutzbar.

## 2. Onboarding-Check

Auf der Startseite erscheint vor dem ersten Export der Hinweis **Vor dem ersten Export: Onboarding-Check** mit dem Link **Onboarding-Check starten**. Details in [Onboarding-Check](onboarding-check.md).

## 3. Einstellungen prüfen

Unter **Einstellungen** sind für BMD-Export voreingestellt:

- **Kontenrahmen**: *EKR (Österreich)*
- **Exportformat**: *BMD NTCS — Buchungsimport (CSV)*
- alle Konten laut [Kontenzuordnung](kontenzuordnung.md)

Weiter oben und unten auf der Seite:

- **Sachkontenlänge**: Stellen Ihrer Sachkonten in BMD, meist 4. Die App prüft jede Kontonummer gegen diese Länge.
- **Für das EU-One-Stop-Shop-Verfahren (OSS) registriert**: nur ankreuzen, wenn Sie bei OSS registriert sind. Dann werden EU-Verkäufe an Privatkunden mit dem Steuersatz des Bestimmungslandes auf das OSS-Konto gebucht, sonst gilt österreichische Umsatzsteuer. Siehe [Steuerfälle](steuerfaelle.md).
- **Warnung zur EU-Lieferschwelle per E-Mail**: erscheint nur ohne OSS, siehe [OSS und Lieferschwelle](oss-und-lieferschwelle.md).
- **Gebühren je Transaktion buchen**: betrifft die Auszahlungsdatei, siehe [Auszahlungen](auszahlungen.md).

Mit **Speichern** übernehmen. Steht danach ein gelbes Banner **Kontoprüfung** oder ein rotes, lesen Sie [Kontenzuordnung](kontenzuordnung.md).

## 4. Wenn Ihre Kanzlei mit RZL arbeitet

Unter **Exportformat** *DATEV-Format — für RZL (liest DATEV-CSV)* wählen. Dann erscheint die Karte **DATEV-Mandant**. Ihre Kanzlei nennt Ihnen die Werte:

- **Beraternummer** (1–7 Ziffern)
- **Mandantennummer** (1–5 Ziffern)
- **Beginn des Wirtschaftsjahres**
- **Sachkontenlänge** (meist 4)
- **Diktatkürzel (optional)**, genau 2 Buchstaben

Für das BMD-Format sind Berater- und Mandantennummer nicht nötig; die Felder bleiben ausgeblendet, gespeicherte Werte bleiben erhalten, falls Sie zurückwechseln.

## 5. Ersten Monat exportieren

Startseite, Monat wählen, **Herunterladen**. Solange etwas fehlt, steht dort das Banner **Noch nicht bereit** mit dem Grund, und die Schaltfläche ist gesperrt. Mehr zum Ablauf: [README](README.md).

## 6. Kanzlei einbinden

Datei per Mail senden oder den [Steuerberater-Zugang](steuerberater-zugang.md) einrichten.
