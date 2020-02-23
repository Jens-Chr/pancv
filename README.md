# pancv

A pandoc LaTeX template for creating a curriculum vitae.

- [English](#english)
  - [Installation](#installation)
  - [Usage](#usage)
  - [Variables](#variables)
- [Italiano](#italiano)
  - [Installazione](#installazione)
  - [Uso](#uso)
  - [Variabili](#variabili)

## English

**Pancv** is a template for [pandoc](https://pandoc.org/) for the realization of curriculum vitae.

*Pancv* uses packages [moderncv](https://launchpad.net/moderncv) and [europasscv](https://github.com/gmazzamuto/europasscv).

***Warning***: Europass support is still experimental.

### Installation

- Install pandoc and a LaTeX distribution.
- Download the latest version of this template from the [release page](https://git.norangeb.it/norangebit/pancv/releases).
- Move the template `pancv.tex` to your pandoc templates folder and rename the file to `pancv.latex`. The location of the templates folder depends on your operating system.
  - Unix, Linux, macOS: `~/.pandoc/templates/`
  - Windows XP: `C:\Documents And Settings\USERNAME\Application Data\pandoc\templates`
  - Windows Vista or later: `C:\Users\USERNAME\AppData\Roaming\pandoc\templates`

### Usage

Once all the necessary material is installed and configured you can use `pancv` through the `--template` flag.

In the following example all variables have been set within the `cv.yaml` file and `cv.pdf` has been chosen as the output file.

```bash
pandoc cv.yaml --template pancv -o cv.pdf
```

### Variables

- `europass` (*boolean*) equal to `true` if you want a curriculum in *europass* format
- `name`
  - `first` (*string*) name.
  - `family` (*string*) surname.
- `address`
  - `first` (*string*) address.
  - `second` (*string*) [optional] address.
- `email` (*string*) email address.
- `mobile` (*string*) mobile phone number.
- `phone` (*string*) phone number.
- `cron-sections` (*list*) chronological sections.
  - `section` (*string*) section name.
  - `entries` (*list*) elements of the section.
    - `year` (*string*) duration.
    - `degree` (*string*) 
    - `institution` (*string*)
    - `city` (*string*) [optional].
    - `grade` (*string*) [optional].
    - `description` (*string*) [optional].
- `sections` (*list*) sections.
  - `section` (*string*) section name.
  - `items` (*list*) elements of the section.
    - `left` (*string*) left part of the section.
    - `right` (*string*) right part of the section.

## Italiano

**Pancv** è un template per [pandoc](https://pandoc.org/) per la realizzazione di *curriculum vitae*.

*Pancv* utilizza il pacchetto [moderncv](https://launchpad.net/moderncv) e il pacchetto [europasscv](https://github.com/gmazzamuto/europasscv).

***Attenzione***: Il supporto al formato europass è ancora in fase sperimentale.

### Installazione

- Installare pandoc e una distribuzione LaTeX.
- Scaricare l'ultima versione di questo tema dalla [pagina delle release](https://git.norangeb.it/norangebit/pancv/releases).
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
