# Cataloghi offline di Sir Collector

File di dati che l'app Sir Collector scarica per cercare gli oggetti anche senza internet.

| File | Contenuto |
|---|---|
| `vinili.db.gz` | Database SQLite compresso. Contiene tutti i vinili (LP, 45 giri, 10") di MusicBrainz, con l'indice di ricerca full-text. |
| `vinili.json` | Versione (data dell'archivio MusicBrainz), numero di dischi e dimensioni. L'app lo legge per sapere se c'è un aggiornamento. |

## Fonte e licenza dei dati

I dati dei vinili vengono da [MusicBrainz](https://musicbrainz.org). Sono rilasciati come
[CC0 (pubblico dominio)](https://creativecommons.org/publicdomain/zero/1.0/) e sono
estratti dall'archivio pubblico <https://data.metabrainz.org/pub/musicbrainz/data/fullexport/>.

Le copertine non sono incluse. L'app le mostra dal [Cover Art Archive](https://coverartarchive.org).

## Aggiornamento

Il file si rigenera con lo script `scripts/build_vinyl_catalog.py` del progetto Sir Collector:
1. Scaricare l'archivio più recente.
2. Lanciare lo script.
3. Copiare qui `vinili.db.gz` e `vinili.json` e fare il push.
