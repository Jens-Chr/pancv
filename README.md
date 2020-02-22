# pancv

A pandoc LaTeX template for creating a curriculum vitae.

- [English](#english)
  - [Installation](#installation)
  - [Usege](#usege)
  - [Variables](#variables)
- [Italiano](#italiano)
  - [Installazione](#installazione)
  - [Uso](#uso)
  - [Variabili](#variabili)

## English

### Installation

*To-Do*

### Usage

*To-Do*

### Variables

*To-Do*

## Italiano

**Pancv** è un template per [pandoc](https://pandoc.org/) per la realizzazione di *curriculum vitae*.

*Pancv* utilizza il pacchetto [moderncv](https://launchpad.net/moderncv) e il pacchetto [europasscv](https://github.com/gmazzamuto/europasscv).

### Installazione

- Installare pandoc e una distribuzione LaTeX.
- Scaricare l'ultima versione di questo tema dalla pagina delle release.
- Copiare il file `pancv.tex` nella cartella dei template e rinominarlo in `pancv.latex`. La cartella dei template varia a seconda del sistema operativo.
  - Unix, Linux, macOS: `~/.pandoc/templates/`
  - Windows XP: `C:\Documents And Settings\USERNAME\Application Data\pandoc\templates`
  - Windows Vista o superiore: `C:\Users\USERNAME\AppData\Roaming\pandoc\templates`

### Uso

Una volta installato e configurato tutto il materiale necessario sarà possibile utilizzare `pancv` attraverso il flag `--template`.

Nel seguente esempio tutte le variabili sono state settate all'interno del file `cv.yaml` e come file di output è stato scelto `cv.pdf`.

```bash
pandoc cv.yaml --template pancv -o cv.pdf
```

### Variabili

- `europass` (*boolean*) pari a `true` se si desidera un curriculum in formato *europass*
- `name`
  - `first` (*string*) nome.
  - `family` (*string*) cognome.
- `address`
  - `first` (*string*) indirizzo.
  - `second` (*string*) [opzionale] indirizzo.
- `email` (*string*) indirizzo email.
- `mobile` (*string*) numero di cellulare.
- `phone` (*string*) numero fisso.
- `cron-sections` (*list*) sezioni cronologiche.
  - `section` (*string*) nome della sezione.
  - `entries` (*list*) elementi della sezione.
    - `year` (*string*) durata.
    - `degree` (*string*) 
    - `institution` (*string*)
    - `city` (*string*) [opzionale]
    - `grade` (*string*) [opzionale]
    - `description` (*string*) [opzionale]
- `sections` (*list*) sezioni.
  - `section` (*string*) nome della sezione.
  - `items` (*list*) elementi della sezione.
    - `left` (*string*) parte di sinistra della sezione.
    - `right` (*string*) parte di destra della sezione.
