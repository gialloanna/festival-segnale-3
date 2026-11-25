## Sessione 1 — Struttura dei dati e programma

- Ho chiesto all’AI come organizzare i dati di eventi e sedi per il sito del festival.
- Ho definito le entità `Evento` e `Sede`, la relazione tra `Evento.sede_id` e `Sede.id` e la quantità prevista: sei eventi e tre sedi.
- Ho predisposto i file JSON e `dati/SCHEMA.md` con le definizioni, le relazioni e il diagramma ER.
- Ho aggiornato `programma.html` per caricare i dati con `fetch` e generare le schede degli eventi.
- Ho considerato la gestione del caricamento, della lista vuota, degli errori e degli eventi senza una sede valida, da indicare come “Sede da definire”.

## Sessione 2 — Meteo in `info.html`

- Ho chiesto di completare il widget meteo, che inizialmente non mostrava velocità del vento e orario del dato.
- Ho usato Open-Meteo per recuperare le condizioni attuali di Torino.
- Ho aggiornato il widget per mostrare temperatura, velocità del vento e timestamp, con messaggi di caricamento ed errore.
- Ho aggiunto l’attribuzione a Open-Meteo con licenza CC BY 4.0 e la precisazione che si tratta di meteo attuale, non di previsioni per le date del festival.

## Sessione 3 — Revisione della pagina informativa

- Ho fornito il contenuto esistente di `info.html` e ho chiesto di modificarlo senza cambiare il collegamento a `style.css`.
- Ho usato una versione aggiornata del file che mantiene galleria, mappa, sedi e navigazione, modificando il widget meteo e il relativo script.
- Ho mantenuto nel testo i nomi e gli indirizzi delle tre sedi.

## Sessione 4 — File delle sedi e verifiche

- Ho chiesto come organizzare il file con i dati delle sedi.
- Ho usato l’esempio per `dati/sedi.json` con gli identificativi 1, 2 e 3, i nomi e gli indirizzi delle sedi.
- Ho annotato che gli ID devono corrispondere ai valori `sede_id` in `dati/eventi.json`.
- È stato individuato un possibile problema con `fetch`: aprire le pagine direttamente con `file://` può impedirne il funzionamento. La verifica va fatta con un server locale.
- Restano da controllare il funzionamento effettivo dei file JSON e del widget, e la versione pubblicata su GitHub Pages.