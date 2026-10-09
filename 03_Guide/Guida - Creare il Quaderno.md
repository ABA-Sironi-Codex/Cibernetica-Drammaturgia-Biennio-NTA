---
tipo: guida
---
# Creare il Quaderno

Il Quaderno è l'archivio di tutto il tuo lavoro dell'anno. È una cartella sul tuo computer, dentro `Corso`, e un [Repository](../04_Glossario/Repository.md) pubblico sul tuo account GitHub. Lo crei una volta sola, in L03, con GitHub Desktop e Obsidian.

Ti servono: GitHub Desktop collegato al tuo account (vedi [Guida - Installazioni Mac](Guida%20-%20Installazioni%20Mac.md) o [Guida - Installazioni Windows](Guida%20-%20Installazioni%20Windows.md), passo 7), Obsidian, la cartella `Corso`.

## 1. Creare il repository

In GitHub Desktop: menu **File** → **New repository…**

| Campo | Che cosa scrivere |
|---|---|
| **Name** | il tuo nome e cognome, con le iniziali maiuscole, separati da un trattino, senza accenti: `Anna-Rossi`, `Nicolo-Pinna`, `Anna-Maria-Sanna` |
| **Description** | *Drammaturgia Multimediale, ABA Sassari* (facoltativo) |
| **Local path** | premi *Choose…* e scegli la cartella **Corso** |
| **Initialize this repository with a README** | ✔ spuntato |
| **Git ignore** | *None* |
| **License** | *None* |

Premi **Create repository**.

Controlla: nel Finder o in Esplora file, dentro `Corso` c'è ora la cartella con il tuo nome, per esempio `Anna-Rossi`. Il percorso completo è `/Users/nome/Corso/Anna-Rossi` (Mac) oppure `C:\Users\nome\Corso\Anna-Rossi` (Windows).

È l'unica eccezione alla regola delle minuscole: il nome del Quaderno è il tuo nome.

## 2. I file da non salvare

Alcuni file non vanno mai su GitHub: quelli che Obsidian riscrive di continuo, quelli che Mac e Windows creano da soli, i video pesanti.

In GitHub Desktop: menu **Repository** → **Repository settings…** → **Ignored files**. Incolla questo testo e premi **Save**:

```
.obsidian/workspace.json
.obsidian/workspace-mobile.json
.trash/
.DS_Store
Thumbs.db
desktop.ini
*.mp4
*.mov
*.avi
*.mkv
*.wav
*.aif
*.aiff
*.psd
.env
*.key
```

I video e gli audio lunghi vanno su Google Drive; nella nota si scrive il link.

## 3. Pubblicarlo su GitHub

1. In alto, premi **Publish repository**
2. **Togli la spunta** da *Keep this code private*: il Quaderno è pubblico
3. Premi **Publish repository**

Controlla: su `github.com/nomeutente/Nome-Cognome` c'è il tuo Quaderno, con il file `README.md`.

## 4. Invitare il docente

1. Su GitHub, nella pagina del tuo Quaderno → **Settings** (l'ingranaggio in alto)
2. A sinistra → **Collaborators**
3. GitHub può chiederti di confermare chi sei: codice di Ente Auth
4. **Add people** → scrivi il nome utente del docente → selezionalo → **Add to repository**

Il docente può leggere tutto, ma non scrive mai nei tuoi file: se ha qualcosa da dirti, apre una [Issue](../04_Glossario/Issue.md).

## 5. Aprirlo in Obsidian

1. Apri Obsidian → **Apri cartella come vault** (*Open folder as vault*)
2. Scegli la cartella del tuo Quaderno dentro `Corso` (per esempio `Corso/Anna-Rossi`) → *Apri*
3. Se Obsidian chiede se fidarti dell'autore: **Fidati** (*Trust author*). Il vault è tuo

## Le cartelle

Le cartelle si creano **quando servono**, in Obsidian: clic destro nell'elenco dei file → **Nuova cartella**. Alla fine del corso il Quaderno sarà fatto così:

| Cartella | Che cosa contiene | Da quando |
|---|---|---|
| `02_Esercizi/` | gli esercizi del corso | L03 |
| `01_Diario/` | una nota per giorno, con i tuoi dati | L04 |
| `03_Progetto/` | il tuo protocollo, il corpo-dati, il progetto finale | L04 |
| `99_Sala-Macchine/` | modelli delle note e impostazioni | L04 |
| `GEMINI.md` | le istruzioni per l'agente (un file, non una cartella) | L07 |
| `04_Fonti/` | fonti, letture, appunti | quando ti serve |
| `_dati-privati/` | i dati grezzi esportati da app e sensori | Fase C |
| `_allegati/` | immagini e altri file usati nelle note | quando ti serve |

Una cartella vuota non arriva su GitHub: compare lì solo quando dentro c'è almeno una nota. È normale.

Nomi di cartelle e file: minuscole, niente spazi (al loro posto `-` oppure `_`), niente accenti.

## Se qualcosa va storto

| Problema | Soluzione |
|---|---|
| Il Quaderno è finito in `Documenti/GitHub/Nome-Cognome` | Il *Local path* non è stato cambiato. In GitHub Desktop: *Repository* → *Remove* (senza cancellare), sposta la cartella in `Corso`, poi *File* → *Add local repository* |
| *Publish* dice che il nome esiste già | Hai già un repository con quel nome su GitHub. Chiama il docente |
| Il Quaderno su GitHub è privato | Su GitHub: *Settings* → in fondo, *Change visibility* → *Public* |
| Obsidian mostra la cartella `Corso` invece del Quaderno | Hai aperto come vault la cartella sbagliata. Riapri `Corso/Nome-Cognome` |
| Nell'elenco dei file cambiati compaiono `.obsidian/…` | È normale: sono le impostazioni di Obsidian. Si salvano anche quelle |

Poi, ogni volta: [Guida - Rito di chiusura](Guida%20-%20Rito%20di%20chiusura.md).
