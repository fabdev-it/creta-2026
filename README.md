# Case a Creta — 3-17 settembre 2026

Sito statico con la selezione verificata di case vacanze a Creta per 4 persone,
dal 3 al 17 settembre 2026.

**👉 [Apri il sito](https://fabdev-it.github.io/creta-2026/)**

## Cosa c'è dentro

- `index.html` — il sito, pagina singola, senza dipendenze esterne
- `case-creta-3-17-settembre-2026.md` — la stessa ricerca in formato documento

## I criteri

| Requisito | Filtro Booking usato |
|---|---|
| Casa tutta per noi | `privacy_type=3` (casa/appartamento intero) |
| Letto vero per tutti e 4 | min. 2 camere (`entire_place_bedroom_count=2`) + controllo manuale dei letti |
| Giardino **o** terrazza | `roomfacility=123` (terrazza) + verifica del giardino scheda per scheda |
| Parcheggio | `hotelfacility=2` |
| Budget ≤ €2.000 | `price=EUR-50-145-1` (max ~€145/notte) |

Su tutta Creta rientrano **209 case**. Le 8 pubblicate qui sono quelle sopravvissute
al controllo manuale: letti camera per camera, distanze reali da spiagge e aeroporti,
parcheggio, condizioni di cancellazione, licenza e tipo di host.

## Come funziona il sito

- Tabella ordinabile: clicca su qualunque intestazione di colonna
- Filtri rapidi: solo 2 matrimoniali, solo cancellazione gratuita, spiaggia entro 1,5 km
- Ogni scheda ha descrizione, pro, contro e link diretto alla pagina Booking
  con date e ospiti già impostati
- Si adatta a telefono e desktop, tema chiaro e scuro

## Aggiornare i dati

I dati stanno nell'array `DATA` dentro `index.html`, uno per casa.
Per aggiungere o correggere una casa basta modificare quell'array — non serve altro.

Il campo `id` è lo slug Booking: il link viene costruito come
`https://www.booking.com/hotel/gr/{id}.it.html` con date e ospiti in query string.

## Attenzione

Prezzi e disponibilità **rilevati l'8 agosto 2026**. Cambiano di continuo:
verifica sempre sulla pagina Booking prima di prenotare. Due case della selezione
(Villa Katerina e Villa MALENA) sono **non rimborsabili** con pagamento online immediato.

## Pubblicare su GitHub Pages

Settings → Pages → Source: `Deploy from a branch` → branch `main`, cartella `/ (root)`.
Dopo un paio di minuti il sito è online su https://fabdev-it.github.io/creta-2026/
