---
tipo: guida
---
# Software del corso

Tutto quello che useremo, con il link alla pagina ufficiale di download. La maggior parte degli strumenti è gratuita (eventuali eccezioni o servizi con piani a pagamento sono indicati nelle singole schede).

## Dotazione hardware e requisiti

> [!IMPORTANT]
> **Dotazione hardware e periferiche**
> - **Computer portatile personale** (Mac o Windows) da portare a ogni incontro, con permessi di amministratore e almeno 10 GB di spazio libero su disco
> - **Cuffie o auricolari con microfono**: obbligatori per il lavoro laboratoriale in aula e le prove audio
> - **Webcam** (integrata o esterna): necessaria per le esercitazioni di visione artificiale e sensori
> - **Smartphone personale** (Android o iOS): necessario per il protocollo di raccolta dati e le app di tracciamento
> - **Mouse esterno con rotellina** (consigliato): facilita notevolmente la navigazione in Obsidian Canvas e l'interazione con diagrammi e codice

> [!WARNING]
> **Requisiti minimi di sistema**
> - **Gemini CLI** richiede **macOS 15** o successivo, oppure **Windows 11 versione 24H2** o successiva
> - **Claude Code** richiede macOS 13 o successivo, oppure Windows 10 versione 1809 o successiva
>
> Per sapere che versione hai:
> - **Mac:** menu Apple (la mela in alto a sinistra) → *Informazioni su questo Mac*
> - **Windows:** tasto Windows + R, scrivi `winver`, premi Invio

---

## Sul computer

### Obsidian
Scrivere e organizzare le note: il tuo Quaderno, il vault del corso.
- Download: https://obsidian.md/download
- Mac (Homebrew): `brew install --cask obsidian`
- Windows (winget): `winget install -e --id Obsidian.Obsidian`

### GitHub Desktop
Salvare e sincronizzare il Quaderno su GitHub. **È l'unico modo in cui useremo git nel corso, per tutti.**
- Download: https://desktop.github.com/download/
- Mac (Homebrew): `brew install --cask github`
- Windows (winget): `winget install -e --id GitHub.GitHubDesktop`

### Node.js
Il motore che serve a far girare Gemini CLI. Non lo userai direttamente.
- Download (versione **LTS**): https://nodejs.org/it/download
- Mac (Homebrew): non serve installarlo a parte, arriva con Gemini CLI
- Windows (winget): `winget install -e --id OpenJS.NodeJS.LTS`

### Gemini CLI
L'intelligenza artificiale di Google nel terminale, dentro il tuo Quaderno. Si usa con il proprio account Google, con un limite gratuito di 60 richieste al minuto e 1.000 al giorno.
- Sito e documentazione: https://geminicli.com
- Codice sorgente: https://github.com/google-gemini/gemini-cli
- Mac (Homebrew): `brew install gemini-cli`
- Windows (dopo Node.js): `npm install -g @google/gemini-cli`

### Claude Code *(opzionale)*
L'agente di Anthropic nel terminale. **Richiede un abbonamento a pagamento** (Claude Pro o superiore, oppure un account API): il piano gratuito non basta. Nel corso lo vedremo probabilmente solo come dimostrazione.
- Installazione: https://code.claude.com/docs/it/setup
- Mac (Homebrew): `brew install --cask claude-code`
- Windows (winget): `winget install -e --id Anthropic.ClaudeCode`
- Su Windows è consigliato anche **Git per Windows**: https://git-scm.com/downloads/win (`winget install -e --id Git.Git`)

### Telegram
Comunicazioni veloci con la classe: il corso ha un **gruppo Telegram**, il link per entrare è su Classroom. Sul computer usiamo *Telegram Desktop*, identico su Mac, Windows e Linux.
- Download: https://desktop.telegram.org
- Tutte le versioni: https://telegram.org/apps
- Mac (Homebrew): `brew install --cask telegram-desktop`
- Windows (winget): `winget install -e --id Telegram.TelegramDesktop`

### Ente Auth
App per l'autenticazione a due fattori: gratuita, open source, disponibile su iPhone, Android, Mac, Windows, Linux e web. Può fare un backup cifrato dei codici, così se perdi il telefono non perdi gli accessi. Funziona anche senza account. Vedi [Guida - Account GitHub e 2FA](Guida%20-%20Account%20GitHub%20e%202FA.md).
- Download: https://ente.com/auth/
- Mac (Homebrew): `brew install --cask ente-auth`
- Windows (winget): `winget install -e --id ente-io.auth-desktop`

### Browser
Qualunque browser recente va bene. Per gli sketch che usano webcam e microfono consigliamo Chrome o Firefox.
- Chrome: https://www.google.com/chrome/
- Firefox: https://www.mozilla.org/it/firefox/new/

### Già presenti sul computer

| | Mac | Windows |
|---|---|---|
| **Terminale** | *Terminale* (Applicazioni → Utility) | *PowerShell*. Su Windows 11 si apre dentro *Terminale Windows*: https://apps.microsoft.com/detail/9n0dx20hk701 |
| **Blocco note** | *TextEdit*, ma prima va messo in modalità testo semplice: menu *Formato → Converti in formato Solo testo*, oppure in *Impostazioni → Nuovo documento → Solo testo* | *Blocco note* |

Se si scrive al computer, si scrive in **Obsidian** o in un **blocco note**. Mai in Word.

---

## Sullo smartphone

| App | A cosa serve | Download |
|---|---|---|
| **Ente Auth** | Autenticazione a due fattori | https://ente.com/auth/ |
| **phyphox** | Leggere i sensori del telefono (movimento, suono, luce) ed esportare i dati | https://phyphox.org/download/ |
| **Telegram** | Il gruppo della classe | https://telegram.org/apps |

### Da conoscere

Non vanno installate per forza: le citiamo in L01 e le vediamo da vicino in L09, come esempi di come le app raccolgono e raccontano i dati del corpo. Chi le usa già può portarne i dati nel progetto.

| App | Che cosa fa | Da sapere | Download |
|---|---|---|---|
| **Daylio** | Diario dell'umore e delle attività: un tocco al giorno, senza scrivere | Gratuita. L'esportazione dei dati in **CSV** è gratuita (*Altro → Esporta voci*), il PDF è a pagamento | https://daylio.net |
| **Google Health** | L'app che dal maggio 2026 ha preso il posto dell'app Fitbit: sonno, movimento, battito | Il *Google Health Coach*, l'assistente basato su Gemini, richiede un orologio Fitbit o Pixel Watch e l'abbonamento Premium. I dati si esportano dalle impostazioni dell'app o dall'account Google | https://play.google.com/store/apps/details?id=com.fitbit.FitbitMobile · https://apps.apple.com/app/id462638897 |

---

## Sul web (niente da installare)

| Servizio | A cosa serve | Indirizzo |
|---|---|---|
| **GitHub** | Dove vive il tuo Quaderno | https://github.com |
| **Google Classroom** | Avvisi, consegne, valutazioni (codice: `kmxdszhf`) | https://classroom.google.com/c/ODEyMDMxMTQ2NTk2?cjc=kmxdszhf |
| **Gemini** | IA di Google: testo, immagini, video | https://gemini.google.com |
| **NotebookLM** | Dialogare con le fonti | https://notebooklm.google.com |
| **Notebook del corso** | Le fonti del corso in NotebookLM (*Cibernetica e Teoria dell'Informazione*) | https://notebook.google.com/notebook/cacdef8c-c81e-48b2-93c2-8bb25f7e336a |
| **Google AI Studio** | Prototipare con l'IA | https://aistudio.google.com |
| **p5.js Web Editor** | Scrivere ed eseguire sketch | https://editor.p5js.org |
| **p5.js** | Documentazione ed esempi | https://p5js.org |
| **ml5.js** | Visione artificiale nel browser (corpo, volto, mani) | https://ml5js.org |

---

## Gestori di pacchetti

Un [Gestore di pacchetti](../04_Glossario/Gestore%20di%20pacchetti.md) installa e aggiorna i programmi con un solo comando nel terminale. Nel corso usiamo **Homebrew** su Mac e **winget** su Windows. Le procedure complete, passo per passo, sono in [Guida - Installazioni Mac](Guida%20-%20Installazioni%20Mac.md) e [Guida - Installazioni Windows](Guida%20-%20Installazioni%20Windows.md).

| | Mac | Windows |
|---|---|---|
| **Gestore** | Homebrew | winget (già presente in Windows 10 e 11) |
| **Pagina** | https://brew.sh/it/ | https://learn.microsoft.com/it-it/windows/package-manager/winget/ |
| **Aggiornare tutto** | `brew update` poi `brew upgrade` | `winget upgrade --all` |

### Tutto in una volta: Mac
Dopo aver installato Homebrew:
```
brew install --cask obsidian github telegram-desktop ente-auth
brew install gemini-cli
```

### Tutto in una volta: Windows
Un comando alla volta:
```
winget install -e --id Obsidian.Obsidian
winget install -e --id GitHub.GitHubDesktop
winget install -e --id OpenJS.NodeJS.LTS
winget install -e --id Telegram.TelegramDesktop
winget install -e --id ente-io.auth-desktop
```
Poi:
```
Set-ExecutionPolicy -Scope CurrentUser RemoteSigned
```
Chiudi e riapri il terminale, e infine:
```
npm install -g @google/gemini-cli
```
