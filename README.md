# Piano Learning – Catalogo

Brani e spartiti per l'app **Piano Learning** (RC Digital). Questo spazio è **pubblico in sola lettura**:
l'app legge i file da qui, solo RC Digital può aggiungerli o toglierli.

## Contenuto
- `brani/` – file MIDI (uno per brano).
- `catalogo.json` – scheda di ogni brano: titolo, compositore, opera, durata, licenza, autore del MIDI, fonte e crediti.
- `spartiti/<nome-brano>/1.png, 2.png, …` – pagine dello spartito, ricavate dal PDF Mutopia del brano (stessa licenza).
- `spartiti.json` – quante pagine ha lo spartito di ogni brano (chiave = nome del file in `brani/`).
- `privacy.html`, `collega.html` – informativa privacy e pagina aperta dal codice QR (pubblicate con GitHub Pages).

## Regole
- SOLO brani di **pubblico dominio** o con **licenza libera che permette l'uso commerciale** (CC0, CC BY, CC BY-SA). Mai NC (non commerciale) o ND.
- Conta la licenza del **file**, non solo della musica: un brano di Beethoven trascritto da un sito commerciale NON è libero.
- Ogni file in `brani/` deve avere la sua scheda in `catalogo.json`, con i crediti: le licenze CC BY / CC BY-SA obbligano a citare l'autore del file.

## Scheda di un brano (`catalogo.json` → elenco `brani`)
```json
{
  "id": "chopin-nocturne",
  "titolo": "Nocturne",
  "compositore": "Fryderyk Chopin",
  "opera": "Op. 9, No. 2",
  "file": "brani/chopin-nocturne.mid",
  "durata_sec": 202,
  "licenza": "CC BY-SA 3.0",
  "licenza_url": "https://creativecommons.org/licenses/by-sa/3.0/",
  "autore_midi": "Renato Biolcati Rinaldi",
  "fonte": "Mutopia Project",
  "fonte_url": "https://www.mutopiaproject.org/ftp/ChopinFF/O9/chopin_nocturne_op9_n2/",
  "crediti": "MIDI: Renato Biolcati Rinaldi / Mutopia Project (…) — Licenza: CC BY-SA 3.0 (…)"
}
```

## Come aggiungere un brano
1. Carica il MIDI nella cartella `brani` (Add file → Upload files → Commit changes).
2. Aggiungi la sua scheda in `catalogo.json`.
3. Facoltativo: aggiungi le pagine dello spartito in `spartiti/<nome-brano>/` e il numero di pagine in `spartiti.json`.
Entro qualche minuto il brano compare nell'app (tasto «Catalogo Piano Learning»).
