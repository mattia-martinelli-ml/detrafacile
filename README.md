# DetraFacile

**App mobile privacy-first per gestire scontrini e spese detraibili IRPEF (modello 730).**

Scansiona scontrini, categorizza automaticamente le spese detraibili (mediche, istruzione, ecc.), stima il risparmio fiscale e prepara i dati per la dichiarazione dei redditi.

## Caratteristiche MVP

- 📸 Scansione scontrini con fotocamera + OCR base
- 🏷️ Categorizzazione spese (Sanitarie, Istruzione, Ristrutturazioni, Altro)
- 💰 Stima detrazione IRPEF 19% (con franchigia 129,11 €)
- 📁 Archivio locale (offline-first)
- 📤 Export CSV / PDF per commercialista o precompilata
- 🔔 Promemoria scadenze semplici
- 🔒 Dati sul dispositivo (nessun account obbligatorio)

## Disclaimer importante

Questa app è **solo uno strumento di supporto**. Non fornisce consulenza fiscale. Le stime sono indicative. Consulta sempre un professionista o l'Agenzia delle Entrate per la dichiarazione dei redditi.

## Stack tecnico (MVP)

- **Framework**: Flutter (cross-platform iOS + Android)
- **OCR**: Google ML Kit / Apple Vision
- **Storage**: Hive / SQLite locale
- **State management**: Riverpod o Provider

## Roadmap

- [x] Repo e struttura base
- [ ] Setup Flutter project
- [ ] Schermata home + lista spese
- [ ] Scanner fotocamera
- [ ] OCR + categorizzazione
- [ ] Calcolo detrazione
- [ ] Export
- [ ] Monetizzazione freemium

## Come contribuire / sviluppare

1. Clona il repo
2. `flutter create .` (se non già presente)
3. `flutter pub get`
4. `flutter run`

## Licenza

MIT (per ora)

---

Made in Italy 🇮🇹 | Privacy first | Per i contribuenti italiani
