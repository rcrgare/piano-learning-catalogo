# Catalogo Piano Learning

Questo spazio contiene i brani MIDI per pianoforte usati dall'app **Piano Learning**. L'app li legge da qui in sola lettura.

## Cosa contiene

- `catalogo.json`: l'elenco dei brani. Ogni scheda riporta titolo, compositore, file, durata, licenza, autore del file MIDI e crediti.
- `brani/`: i file `.mid`.

## Regole: cosa si può caricare

Ogni brano deve rispettare **due condizioni**:

1. **La composizione è di pubblico dominio.** Il compositore è morto da più di 70 anni, oppure si tratta di musica tradizionale. Canzoni pop, rock e colonne sonore moderne **non** vanno caricate, anche se il MIDI si trova gratis in rete.
2. **Il file MIDI ha una licenza che consente l'uso commerciale.** Sono ammesse:
   - Pubblico dominio / CC0
   - CC BY (obbligo di citare l'autore)
   - CC BY-SA (obbligo di citare l'autore; il file va ridistribuito con la stessa licenza)

   **Non** sono ammesse: CC BY-NC (non commerciale), CC BY-ND, licenze sconosciute.

## Fonte attuale

Tutti i brani iniziali provengono dal **Mutopia Project** (https://www.mutopiaproject.org). I MIDI sono stati generati dai sorgenti LilyPond originali, senza modifiche alle note. La licenza di ogni brano è quella indicata dal trascrittore nel sorgente ed è riportata in `catalogo.json`.

## Come aggiungere un brano

1. Verifica che il brano rispetti le due regole qui sopra.
2. Apri la cartella `brani`, poi **Add file → Upload files**, carica il `.mid` (nome in minuscolo, con trattini) e conferma con **Commit changes**.
3. Apri `catalogo.json`, clicca la matita (Edit) e aggiungi una scheda in fondo all'elenco `brani`, copiando lo schema di quelle esistenti:

```json
{
  "id": "compositore-titolo",
  "titolo": "Titolo",
  "compositore": "Nome Cognome",
  "opera": "Op. 1",
  "file": "brani/compositore-titolo.mid",
  "durata_sec": 120,
  "licenza": "Pubblico dominio",
  "licenza_url": null,
  "autore_midi": "Nome del trascrittore",
  "fonte": "Mutopia Project",
  "fonte_url": "https://...",
  "crediti": "MIDI: Nome / Fonte (link) — Licenza: ..."
}
```

4. Conferma con **Commit changes**. L'app vedrà il nuovo brano entro pochi minuti.

## Crediti

I crediti di ogni brano sono nel campo `crediti` di `catalogo.json`. L'app li mostra nella schermata «Informazioni».
