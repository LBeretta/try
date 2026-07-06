# Geberit Experience Center - PDF Generator

Sito statico per generare inviti PDF personalizzati usando `assets/template.pdf` come sfondo ufficiale.

## Novità versione 6

- In testa al form è presente la scelta **1 giorno** oppure **2 giorni**.
- Se scegli 2 giorni, il sito mostra due blocchi di compilazione: **Giorno 1** e **Giorno 2**.
- Il PDF a 2 giorni usa lo stesso template e le stesse coordinate per entrambe le pagine.
- Per il Giorno 2:
  - `Data giorno 2` viene preimpostata al giorno successivo rispetto alla data del Giorno 1;
  - `RSVP entro` viene preimpostato uguale all'RSVP del Giorno 1;
  - entrambi i campi restano modificabili prima della generazione.

## Campi disponibili

Per ogni giorno puoi compilare:

- Data giorno
- Luogo fisso: `Via Tortona 31, Milano`
- 5 righe agenda con orario e attività
- RSVP entro

Gli orari sono menu a tendina da `07:30` a `23:00`, ogni 30 minuti.

Le attività sono menu a tendina con queste opzioni:

- Arrivo
- Arrivo e welcome coffee
- Visita all'Experience Center
- Pranzo
- Attività ludica
- Cena
- Pausa caffè
- Altro

Se scegli **Altro**, compare un campo libero per scrivere un'attività personalizzata.

## Formato date nel PDF

- Data giorno: `18 settembre 2026`
- RSVP: `RSVP entro il 16 settembre`

## Come provarlo in locale

Dalla cartella del progetto:

```bash
python3 -m http.server 8000
```

Poi apri:

```text
http://localhost:8000
```

## File principali

```text
index.html       Landing page e form
styles.css       Stili della landing page
app.js           Logica di compilazione e generazione PDF
template.json    Coordinate e configurazione del template
assets/template.pdf  Sfondo ufficiale del PDF
```
