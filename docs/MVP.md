# Specifiche MVP - DetraFacile

## Obiettivo
Permettere a un utente italiano di scansionare scontrini/fatture, categorizzarli per detrazioni IRPEF del modello 730 e ottenere una stima del risparmio fiscale.

## User Stories prioritarie

1. Come contribuente, voglio scattare una foto a uno scontrino e salvarlo con data, importo e categoria.
2. Come contribuente, voglio vedere l'elenco delle mie spese detraibili dell'anno.
3. Come contribuente, voglio una stima della detrazione IRPEF 19% sulle spese sanitarie (al netto della franchigia di 129,11 €).
4. Come contribuente, voglio esportare i dati in CSV o PDF per il commercialista o per verificare la precompilata.
5. Come utente privacy-conscious, voglio che i miei dati restino sul dispositivo.

## Schermate MVP

1. **Home / Lista spese**
   - Totale spese detraibili anno corrente
   - Stima risparmio
   - Lista cronologica con filtri per categoria
   - FAB "Nuova spesa" / Scanner

2. **Scanner / Aggiungi spesa**
   - Fotocamera o galleria
   - Anteprima + OCR (data, importo, negozio se possibile)
   - Selezione categoria (Sanitarie, Istruzione, Ristrutturazioni, Altro detraibile, Non detraibile)
   - Note libere
   - Salva

3. **Dettaglio spesa**
   - Foto + dati estratti + categoria
   - Modifica / Elimina

4. **Report / Export**
   - Riepilogo per categoria
   - Calcolo detrazione stimata
   - Pulsanti Export CSV e PDF

5. **Impostazioni**
   - Anno fiscale
   - Privacy policy / Disclaimer
   - (Futuro) Backup locale

## Categorie iniziali

- Sanitarie (farmaci, visite, ticket, dispositivi medici)
- Istruzione
- Ristrutturazioni / Ecobonus (semplificato)
- Altro detraibile
- Non detraibile

## Calcolo detrazione (semplificato)

Per spese sanitarie:
```
detrazione = max(0, (totale_spese_sanitarie - 129.11) * 0.19)
```

Altre categorie: solo archiviazione + export (calcolo completo in versioni successive).

## Tecnologie consigliate

- Flutter 3.x
- `camera` + `google_mlkit_text_recognition` (o `apple_vision`)
- `hive` o `sqflite` per storage
- `pdf` + `csv` packages per export
- `share_plus` per condividere file

## Note legali

- Disclaimer ben visibile in app e store
- Privacy policy (dati solo locali)
- Nessuna trasmissione di dati a terzi senza consenso esplicito
