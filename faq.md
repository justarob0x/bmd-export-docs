# FAQ und Fehlersuche

## Einrichtung und Format

**Meine Kanzlei arbeitet mit RZL. Was lade ich hoch?** Wählen Sie unter Einstellungen das Exportformat *DATEV-Format — für RZL (liest DATEV-CSV)* und tragen Sie Berater- und Mandantennummer ein, die Ihre Kanzlei nennt. Siehe [Dateiformate](dateiformate.md).

**Meine Kanzlei bucht mit einem anderen Programm.** Viele Programme lesen das DATEV-Format ein. Fragen Sie, ob das Ihrer Kanzlei reicht. Der Onboarding-Check hält die Antwort im Bericht fest.

**Mein Steuerberater hat andere Kontonummern.** Jede Zelle der Kontenzuordnung ist änderbar. Die Vorbelegung ist der BMD-Standard, RZL und viele Kanzleien nummerieren anders. Siehe [Kontenzuordnung](kontenzuordnung.md).

**Die Schaltfläche „Herunterladen“ ist gesperrt.** Auf der Startseite steht das Banner **Noch nicht bereit** mit dem Grund, meist ein rotes Konto (falsche Stellenzahl) oder bei RZL fehlende Berater- oder Mandantennummer. Beheben Sie es unter Einstellungen.

**Die App meldet „Kontoprüfung“, obwohl meine Konten stimmen.** Gelbe Hinweise sind nur Vorschläge (Konto in ungewöhnlicher Klasse oder ein Personenkonto). Sie blockieren nichts. Rote Konten blockieren den Export.

## Buchungen

**Warum steht eine EU-Bestellung auf dem Inlandskonto?** Ohne gesetztes OSS-Häkchen gilt österreichische Umsatzsteuer, solange der Shop einen österreichischen Satz berechnet hat. Siehe [Steuerfälle](steuerfaelle.md).

**Warum hat eine Zeile Steuercode 0 und ein OSS-Konto?** Für OSS gibt es in den öffentlichen BMD-Unterlagen keinen Code. Das Konto trägt den Fall. Hat Ihre Kanzlei einen Code, nennen Sie ihn dem Support.

**Der Export bricht mit einer Fehlermeldung zu einer Bestellung ab.** Meist hat die Bestellung einen Steuersatz, den Österreich nicht kennt, oder fehlerhafte Daten. Die Meldung nennt die Bestellnummer; prüfen Sie sie in Shopify. Mit **Problem melden** schicken Sie die Meldung samt Vorgangsnummer an den Support.

**Eine Erstattung fehlt in der Datei.** Gebucht wird nur Geld, das tatsächlich zurückgezahlt wurde, und im Monat der Erstattung, nicht der Bestellung. Siehe [Buchungsregeln](buchungsregeln.md).

**Wie werden Rabatte gebucht?** Der Erlös ist der bezahlte Betrag nach Rabatt. Es gibt keine eigene Rabattzeile.

**Wohin kommen Barzahlungen im Geschäft?** Auf das Konto *Kassa (Barzahlung, Shopify POS)*, vorbelegt 2700.

**Kann ich einen Monat mehrmals exportieren?** Ja, die Datei wird jedes Mal neu erzeugt. Bereits verbuchte Monate nicht erneut importieren.

**Warum ist der laufende Monat „Vorschau“?** Er ist noch nicht abgeschlossen. Exportieren Sie ihn nach Monatsende erneut.

## Auszahlungen und OSS

**Warum brauche ich zwei Dateien?** Die erste bucht Verkäufe gegen das Geldtransitkonto, die zweite bucht Bank, Gebühren und Anpassungen gegen dasselbe Konto. So geht es auf. Siehe [Auszahlungen](auszahlungen.md).

**Der Auszahlungsabgleich meldet „Differenz“.** Auszahlung und Einzeltransaktionen gehen nicht auf; die Datei entsteht trotzdem. Schicken Sie dem Support die Auszahlungsnummer.

**Wie reiche ich die OSS-Meldung ein?** Siehe [OSS und Lieferschwelle](oss-und-lieferschwelle.md): FinanzOnline-Datei herunterladen, im EU-OSS-Portal hochladen, prüfen, absenden, in der App als abgegeben speichern.

**Ich bin nicht bei OSS registriert und bekomme eine Mail zur Lieferschwelle.** Die App meldet bei 80 % und 100 % der 10.000 € netto. Abschalten unter Einstellungen mit **Warnung zur EU-Lieferschwelle per E-Mail**.

## Abo und Daten

**Was kostet die App?** 19 € alle 30 Tage oder 190 € im Jahr, 14 Tage kostenlos. Siehe [Abo, Daten und Support](abo-daten-support.md).

**Welche Daten speichert die App?** Keine Bestell- oder Kundendaten. Nur Einstellungen, Exportprotokoll und was in [Abo, Daten und Support](abo-daten-support.md#daten) steht.

**Was passiert bei der Deinstallation?** Die Sitzung endet sofort, ein Steuerberater-Link funktioniert nicht mehr, 48 Stunden später werden Einstellungen und Protokoll gelöscht. Ihre Shopify-Daten bleiben unberührt. Das Abo endet mit der Deinstallation.

**Kann ich Shopifys Sidekick nutzen?** Ja. Sidekick beantwortet fünf Auskünfte aus der App, nur lesend: Stand der Einrichtung, Lieferschwelle, Exportverlauf, gespeicherte OSS-Meldungen und Kontenzuordnung, z. B. „Habe ich den September schon exportiert?“. Er liest keine Bestellungen und ändert keine Einstellungen.

**Wer hilft bei Problemen?** `support+bmd@justarobot.online`, Antwort in der Regel innerhalb eines Werktags. Siehe [Support](abo-daten-support.md#support).
