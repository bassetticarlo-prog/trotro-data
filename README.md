# trotro-data

Dati aperti per l'app **TROTRO OBD-II**: catalogo degli adattatori OBD-II e pacchetti di definizioni per veicoli e costruttori. L'app li scarica da qui e ne tiene una copia locale, così funziona anche senza rete.

## Contenuto

| Percorso | Cosa contiene |
|---|---|
| `adapters/adapters.json` | Adattatori provati: nomi Bluetooth, canali, capacità misurate, particolarità note |
| `packs/vw_ea288.json` | Valori costruttore (UDS servizio 22) del 2.0 TDI VW EA288 |

## Stati dei dati

- **verified** — scala e significato verificati su un'auto reale (indicata nel campo `evidence` o `tested`).
- **plausible** — risponde e si comporta in modo coerente, ma la scala non è ancora certa.
- **candidate** — risponde, significato o scala da capire.

## Sola lettura

Tutti i dati qui descritti si leggono con richieste di sola lettura (modi OBD 01, 02, 03, 07, 09, 0A e UDS 22). Nessun pacchetto contiene comandi di scrittura, cancellazione o sessioni diagnostiche.

## Formule

Le formule usano `A`, `B`, `C`, `D` per i byte di dati della risposta (dopo `62` e l'identificativo, o dopo `41` e il PID). `A_s` indica il byte con segno.
