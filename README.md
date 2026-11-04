# BMD-Export

BMD-Export is a Shopify app for Austrian shops. It reads one month of orders and refunds and writes the booking file your tax advisor imports: the BMD booking import (CSV) for BMD NTCS, or a file in DATEV format that RZL reads. VAT at 20/10/13 %, OSS, exports and EU B2B sales are booked on the Austrian standard chart of accounts (EKR). This documentation is in German, for Austrian merchants and their advisors.

---

BMD-Export ist eine Shopify-App für österreichische Shops. Sie macht aus den Bestellungen und Erstattungen eines Monats die Buchungsdatei, die Ihre Kanzlei einliest: den BMD-Buchungsimport (CSV) für BMD NTCS oder, für RZL, eine Datei im DATEV-Format. Umsatzsteuer 20/10/13 %, OSS, Ausfuhr und innergemeinschaftliche Lieferung werden auf dem Einheitskontenrahmen (EKR) gebucht. Preis: 19 € alle 30 Tage oder 190 € im Jahr, 14 Tage kostenlos testen.

## Das Problem

Ein Shop verkauft jeden Tag zu mehreren Steuersätzen, an Kunden im Inland, in der EU und in Drittländern, mit Versand, Gutscheinen, Rabatten und Erstattungen. Die Kanzlei braucht daraus am Monatsende saubere Buchungen, und zwar auf den richtigen Erlöskonten und mit dem richtigen Steuercode. Von Hand oder aus Excel ist das fehleranfällig. BMD-Export liest die Daten aus Shopify und schreibt die Datei, die Ihre Kanzlei ohne Nacharbeit importieren kann. Die Buchhaltung selbst bleibt bei der Kanzlei.

## Ein Monat in sieben Schritten

1. **Einrichten.** Unter **Einstellungen** stehen Kontenrahmen *EKR (Österreich)* und Exportformat *BMD NTCS — Buchungsimport (CSV)* schon voreingestellt. Die Konten sind mit dem BMD-Standard belegt. Ihre Kanzlei bestätigt sie einmal. Siehe [Einrichtung](einrichtung.md) und [Kontenzuordnung](kontenzuordnung.md).
2. **Onboarding-Check (einmalig).** Fünf Fragen, dazu ein Blick in Ihre Einstellungen und Bestellungen. Heraus kommt ein Bericht für die Kanzlei. Siehe [Onboarding-Check](onboarding-check.md).
3. **Monat wählen.** Auf der Startseite im Feld **Monat** den Kalendermonat wählen.
4. **Herunterladen.** Ein Klick auf **Herunterladen** erzeugt `BMD_Buchungen_JJJJ-MM.csv`. Die App zeigt, wie viele Bestellungen, Erstattungen und Buchungszeilen darin stehen.
5. **Auszahlungen (mit Shopify Payments).** Unter **Auszahlungen** der zweite Stapel des Monats: Bankbuchung, Gebühren, Anpassungen. Siehe [Auszahlungen](auszahlungen.md).
6. **An die Kanzlei.** Datei senden oder der Kanzlei einen privaten Link geben, über den sie selbst herunterlädt. Siehe [Steuerberater-Zugang](steuerberater-zugang.md). Die Kanzlei liest die Datei in BMD NTCS bzw. RZL ein, siehe [Dateiformate und Import](dateiformate.md).
7. **OSS je Quartal.** Wer im One-Stop-Shop registriert ist, lädt unter **OSS-Meldung** die Datei für FinanzOnline. Siehe [OSS und Lieferschwelle](oss-und-lieferschwelle.md).

## Wo was zu finden ist

- **Startseite** (Name der App): Monat wählen, Buchungsdatei herunterladen, **Letzte Exporte**.
- **Onboarding-Check**: Einrichtungsbericht für die Kanzlei.
- **OSS-Meldung**: OSS-Übersicht je Quartal und die Dateien dazu.
- **Auszahlungen**: Abgleich der Shopify-Payments-Auszahlungen.
- **Einstellungen**: Kontenrahmen, Exportformat, Konten, OSS, Steuerberater-Zugang.
- **Abo**: Monats- oder Jahresabo, Wechsel. Siehe [Abo, Daten und Support](abo-daten-support.md).

## Weitere Seiten

- [Steuerfälle und Steuercodes](steuerfaelle.md): welcher Fall auf welches Konto und welchen Code kommt
- [Erstattungen, Gutscheine, Versand und Rabatte](buchungsregeln.md)
- [Grenzen](grenzen.md): was die App nicht abbildet
- [FAQ](faq.md)

## Status: Beta

Die Dateien sind nach den Schnittstellenbeschreibungen von BMD und RZL gebaut. Ein von einer Kanzlei bestätigter Import steht laut App noch aus. Prüfen Sie den ersten Import mit Ihrer Kanzlei und geben Sie dem Support Rückmeldung (`support+bmd@justarobot.online`); als Dank gibt es einen Gratismonat.

## Über diese Dokumentation

Diese Dokumentation ist öffentlich. Sie ist für Menschen geschrieben oder zum Einfügen in einen KI-Assistenten, damit Sie Fragen wie „Warum steht diese Bestellung auf dem OSS-Konto?“ beantwortet bekommen, die sich auf das tatsächliche Verhalten der App stützen. Sie beschreibt nur das Verhalten der App: keine Kundendaten, kein Quellcode. Sie ist keine Steuerberatung; die Zuordnung zu Konten und Steuercodes bestätigt Ihre Kanzlei.
