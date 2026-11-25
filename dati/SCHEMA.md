# Scheda dati — Festival Segnale

## Entità: Sede

| Campo | Tipo | Esempio |
|---|---|---|
| `id` | numero intero | `1` |
| `nome` | stringa | `"Officina Nord"` |
| `indirizzo` | stringa | `"Corso Duca degli Abruzzi 24, Torino"` |

**Chiave primaria:** `id`, numerico, univoco nell’entità e stabile.

## Entità: Evento

| Campo | Tipo | Esempio |
|---|---|---|
| `id` | numero intero | `1` |
| `titolo` | stringa | `"Lettere in movimento"` |
| `data` | stringa, formato `YYYY-MM-DD` | `"2026-06-12"` |
| `orario` | stringa, formato `HH:MM` | `"10:00"` |
| `categoria` | stringa | `"Incontro"` |
| `descrizione` | stringa | `"Come cambia un messaggio quando cambiano le lettere? Un incontro su tipografia, ritmo e comunicazione visiva."` |
| `immagine` | stringa, percorso del file | `"assets/lettere-in-movimento.svg"` |
| `immagine_alt` | stringa | `"Lettere geometriche disposte su una griglia"` |
| `sede_id` | numero intero, chiave esterna | `1` |

**Chiave primaria:** `id`, numerico, univoco nell’entità e stabile.

## Relazione

Una sede può ospitare più eventi; ogni evento si svolge in una sede.
`Evento.sede_id` fa riferimento a `Sede.id`.

## Quantità

- **Eventi:** 6
- **Sedi:** 3

## Aggiornamento dei dati

Chi mantiene il progetto modifica i file JSON nella repository e pubblica le modifiche insieme al sito.

## Che cosa mostra la pagina

La pagina Programma mostra gli appuntamenti con data, orario, categoria, titolo, descrizione, immagine e nome della sede. La pagina Info e luoghi mostra le sedi, i rispettivi indirizzi e il meteo corrente di Torino.

## Schema Evento–Sede

```mermaid
erDiagram
SEDE ||--o{ EVENTO : ospita
SEDE {
int id PK
string nome
string indirizzo
}
EVENTO {
int id PK
string titolo
string data
string orario
string categoria
string descrizione
string immagine
string immagine\_alt
int sede\_id FK
}