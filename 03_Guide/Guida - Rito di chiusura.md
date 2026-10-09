---
tipo: guida
---
# Rito di chiusura

Gli ultimi dieci minuti di ogni incontro servono a mettere al sicuro il lavoro. Sempre, senza eccezioni, dalla L03 alla fine del corso.

Il suo gemello, all'inizio dell'incontro, è il [rito di apertura](Guida%20-%20Rito%20di%20apertura.md).

## I passi

1. **Salva** tutto in Obsidian. Di solito lo fa da solo: basta che non ci siano finestre di altri programmi con modifiche aperte
2. Apri **GitHub Desktop**
3. In alto a sinistra, in *Current repository*, controlla che ci sia il tuo Quaderno, con il tuo **Nome-Cognome**, non il vault del corso
4. A sinistra compare l'elenco dei file cambiati. Clicca su uno: a destra vedi in verde ciò che hai aggiunto, in rosso ciò che hai tolto
5. In basso a sinistra, nel campo **Summary**, scrivi in una frase **che cosa hai fatto oggi**
6. Premi **Commit to main**
7. Premi **Push origin**, in alto

Fatto. Il tuo lavoro ora esiste in due posti: sul tuo computer e su GitHub.

## La frase del commit

La frase del *Summary* è il tuo diario. Fra tre mesi, leggendo l'elenco dei tuoi [Commit](../04_Glossario/Commit.md), rivedrai tutta la storia del tuo lavoro. Per questo:

- **dice che cosa è successo**, non *"aggiornamento"* o *"modifiche"*
- **una frase sola**, al passato o al presente: *Primo giorno del Quaderno: il personaggio che sono*
- se vuoi aggiungere qualcosa, c'è il campo **Description**, sotto

| No | Sì |
|---|---|
| `update` | *Trascritti i dati dal 14 al 20 ottobre* |
| `modifiche varie` | *Il mio GEMINI.md: un dramaturg più severo* |
| `asdf` | *Canvas del corpo-dati, prima versione* |

## Non solo in aula

Il rito si fa **ogni volta che lavori sul Quaderno**, anche a casa: dopo aver trascritto i dati, dopo un esercizio, dopo aver lavorato con l'agente. Meglio tanti commit piccoli che uno grande a fine mese.

Anche i file creati o modificati da **Gemini CLI** vanno salvati con il rito: GitHub Desktop li mostra come tutti gli altri. Prima di fare il commit, guarda che cosa ha cambiato.

## Che cosa vede il docente

Il tuo Quaderno è pubblico e il docente è collaboratore. Dopo il *Push*, il docente vede il lavoro su GitHub e, se ha qualcosa da dirti, apre una **Issue**: una nota nella scheda *Issues* del tuo Quaderno, sul sito. Il docente non scrive mai nei tuoi file.

Se ricevi una Issue, rispondi lì sotto. Quando hai sistemato, chiudila con **Close issue**.

## Se qualcosa va storto

| Problema | Soluzione |
|---|---|
| L'elenco dei file cambiati è vuoto | Hai già fatto il commit, oppure hai lavorato in un altro vault. Controlla il nome del vault in basso a sinistra in Obsidian |
| *Commit to main* è grigio | Manca la frase nel *Summary* |
| Dopo il commit non compare *Push origin* | Guarda in alto: il pulsante si chiama ancora *Push origin* con un numero accanto. Premilo |
| *Push* rifiutato (*rejected*) | Su GitHub c'è qualcosa di più nuovo. Premi **Fetch origin**, poi **Pull origin**, poi di nuovo **Push origin** |
| Compaiono file `.obsidian/…` | È normale: sono le impostazioni di Obsidian. Si salvano anche quelle |
| Compare un file `.DS_Store` o `desktop.ini` | Non dovrebbe: avvisa il docente |
| Hai fatto il commit nel vault del corso | Non premere *Push*. Chiama il docente |
| GitHub Desktop chiede di nuovo di accedere | Rifai *Sign in* con password e codice di Ente Auth |

Vedi anche: [Commit](../04_Glossario/Commit.md), [Push](../04_Glossario/Push.md), [Repository](../04_Glossario/Repository.md), [Guida - Rito di apertura](Guida%20-%20Rito%20di%20apertura.md)
