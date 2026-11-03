# Cataloghi offline di Sir Collector

File di dati che l'app Sir Collector scarica per cercare gli oggetti anche senza internet.
Per ogni catalogo ci sono due file:
- `<nome>.db.gz`: database SQLite compresso, con l'indice di ricerca;
- `<nome>.json`: versione, numero di righe e dimensioni. L'app lo legge per sapere se c'è un aggiornamento.

| Catalogo | Contenuto | Fonte |
|---|---|---|
| `vinili` | Tutti i vinili (LP, 45 giri, 10") | [MusicBrainz](https://musicbrainz.org), CC0 |
| `pokemon` | Carte Pokémon, in italiano dove disponibili | [TCGdex](https://tcgdex.dev) |
| `yugioh` | Stampe Yu-Gi-Oh! (carta, set, codice, rarità) | [YGOPRODeck](https://ygoprodeck.com) |
| `magic` | Stampe inglesi di Magic: The Gathering, con il nome italiano | [Scryfall](https://scryfall.com) |
| `lorcana` | Carte Disney Lorcana | [Lorcast](https://lorcast.com) |
| `onepiece` | Carte One Piece Card Game | [OPTCG API](https://optcgapi.com) |
| `digimon` | Carte Digimon Card Game | [digimoncard.io](https://digimoncard.io) |
| `fab` | Stampe Flesh and Blood | [The Fab Cube](https://github.com/the-fab-cube/flesh-and-blood-cards) |
| `giochi` | Videogiochi per console classiche (No-Intro, Redump) | [libretro-database](https://github.com/libretro/libretro-database) |

`euro-monete.json` è l'elenco delle monete euro (2 € commemorativi dalle pagine della
[BCE](https://www.ecb.europa.eu/euro/coins/comm/html/index.it.html) e monete di circolazione
per paese). È incluso nell'app; l'app scarica questa copia una volta al mese per aggiornarlo.

## Immagini

Nessun catalogo contiene immagini. L'app le mostra dai siti delle fonti (Cover Art Archive,
TCGdex, Scryfall, Lorcast, thumbnails.libretro.com…) e le salva sul telefono solo se l'utente lo chiede.

## Marchi

Pokémon, Yu-Gi-Oh!, Magic: The Gathering, Disney Lorcana, One Piece, Digimon, Flesh and Blood
e i nomi dei videogiochi sono marchi dei rispettivi proprietari.

## Aggiornamento

I file si rigenerano con gli script in `collezioni/scripts/` del progetto Sir Collector
(la procedura è in `collezioni/NOTE_SVILUPPO.md`), poi si copiano qui e si fa il push.
