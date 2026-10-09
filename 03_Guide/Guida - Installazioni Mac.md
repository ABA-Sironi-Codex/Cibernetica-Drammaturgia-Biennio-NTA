---
tipo: guida
---
# Installazioni Mac

Questa guida installa tutti i programmi del corso con **Homebrew**, un [Gestore di pacchetti](../04_Glossario/Gestore%20di%20pacchetti.md): un negozio a cui si chiedono i programmi per nome. È la stessa procedura della L02, da seguire a casa se in aula non hai finito o se qualcosa è andato storto.

Ti servono: il Mac collegato alla corrente e a internet, la **password con cui accendi il Mac**, una mezz'ora di tempo.

> [!WARNING]
> **Prima di cominciare**
> - **macOS 15 (Sequoia) o successivo** serve per Gemini CLI. Per sapere che versione hai: menu Apple (la mela in alto a sinistra) → *Informazioni su questo Mac*. Con un macOS più vecchio puoi installare tutto il resto, ma salta il passo 5
> - Il tuo utente deve essere **amministratore** del Mac. Se il Mac è di un'altra persona o di un'azienda, potresti non esserlo: in quel caso vai direttamente al [Piano B](#piano-b)
> - Almeno **10 GB liberi** sul disco

## 1. Aprire il terminale

`Cmd + Spazio`, scrivi *Terminale*, premi Invio. Vedi anche [Guida - Terminale minimo](Guida%20-%20Terminale%20minimo.md).

## 2. Installare Homebrew

1. Vai su https://brew.sh/it/
2. Sotto *Installa Homebrew* c'è un comando che comincia con `/bin/bash -c`. Copialo con il pulsante accanto
3. Incollalo nel terminale (`Cmd + V`) e premi Invio

> [!IMPORTANT]
> **La password invisibile**
> Il terminale ti chiede la password del Mac. **Mentre la scrivi non compare niente**: né lettere, né pallini. Sembra che la tastiera non funzioni, invece funziona. Scrivila tutta e premi Invio.

4. Homebrew ti chiede di premere **Invio** per continuare: premilo
5. Se compare una finestra che propone di installare gli *strumenti per sviluppatori da riga di comando*, premi **Installa**
6. Aspetta. Può durare da 5 a 20 minuti

## 3. I *Next steps*

Alla fine Homebrew scrive **Next steps** e, sotto, due o tre righe di comandi. **Copiale e incollale nel terminale una alla volta**, premendo Invio dopo ognuna. Servono a dire al terminale dove si trova Homebrew.

Su un Mac con processore Apple (M1, M2, M3, M4…) sono simili a queste, con il tuo nome utente al posto di `nome`:

```
echo >> /Users/nome/.zprofile
echo 'eval "$(/opt/homebrew/bin/brew shellenv)"' >> /Users/nome/.zprofile
eval "$(/opt/homebrew/bin/brew shellenv)"
```

Usa quelle che vedi **sul tuo schermo**, non queste. Sui Mac con processore Intel di solito non ci sono: va bene così.

Verifica:
```
brew --version
```
Deve rispondere con un numero di versione, per esempio `Homebrew 4.6.0`.

## 4. I programmi con le finestre

```
brew install --cask obsidian github telegram-desktop ente-auth
```

Installa in una volta sola Obsidian, GitHub Desktop, Telegram ed Ente Auth. Può chiederti di nuovo la password (invisibile).

## 5. Gemini CLI

```
brew install gemini-cli
```

Installa Gemini CLI e, insieme, **Node.js**, che gli serve per funzionare. Può durare qualche minuto.

## 6. Verificare

```
node --version
gemini --version
```

Tutti e due devono rispondere con un numero. Poi apri dal Launchpad o dalla cartella **Applicazioni**, una alla volta:

- [ ] **Obsidian** si apre sulla schermata iniziale. Non creare ancora nessun vault: lo facciamo in L03
- [ ] **GitHub Desktop** si apre
- [ ] **Telegram** si apre. Se vuoi, accedi con il QR code dal telefono
- [ ] **Ente Auth** si apre. Se in L01 hai creato l'account Ente, accedi e ritrovi i codici

**Non avviare ancora Gemini CLI**: il primo accesso lo facciamo insieme, in L07.

## 7. GitHub Desktop: il primo accesso

1. Apri GitHub Desktop → **Sign in to GitHub.com**
2. Si apre il browser: entra con la password e il codice di Ente Auth
3. Il browser chiede se autorizzare GitHub Desktop: **sì**
4. Tornato in GitHub Desktop, alla voce **Configure Git** scrivi nome e cognome

Poi rendi privata la tua email: su https://github.com → la tua foto in alto a destra → *Settings* → *Emails* → spunta **Keep my email addresses private**. GitHub ti mostra un indirizzo del tipo `12345678+nomeutente@users.noreply.github.com`. In GitHub Desktop: menu *GitHub Desktop* → *Settings* → *Git* → scegli quell'indirizzo nel menu dell'email.

Vedi anche [Guida - Account GitHub e 2FA](Guida%20-%20Account%20GitHub%20e%202FA.md).

## Aggiornare, ogni tanto

Una volta al mese, nel terminale:

```
brew update
brew upgrade
```

Aggiorna tutti i programmi installati con Homebrew, Gemini CLI compreso.

## Se qualcosa va storto

| Problema | Soluzione |
|---|---|
| Alla richiesta della password sembra che la tastiera non funzioni | È normale: la password non si vede. Scrivila e premi Invio |
| `Sorry, try again` | Password sbagliata. Controlla il blocco maiuscole |
| `... is not in the sudoers file` o Homebrew dice che serve un amministratore | Il tuo utente non è amministratore: vai al [Piano B](#piano-b) |
| Gli strumenti per sviluppatori si scaricano lentissimi | Lasciali andare, oppure interrompi e installali più tardi con `xcode-select --install` |
| `zsh: command not found: brew` | Non hai eseguito i *Next steps* (passo 3). Scorri in su nel terminale e copiali |
| `brew install --cask` dice che un'app esiste già | È già installata: va bene così |
| *Impossibile aprire l'app perché proviene da uno sviluppatore non identificato* | *Impostazioni di Sistema* → *Privacy e sicurezza* → scorri in fondo → **Apri comunque** |
| `gemini-cli` non si installa e parla della versione di macOS | Il tuo macOS è più vecchio di 15: salta Gemini CLI, in aula useremo l'alternativa via web |

Se non riesci a risolvere: fai una foto dello schermo con l'errore e mandala su Classroom o nel gruppo Telegram.

## Piano B

Se Homebrew non funziona, ogni programma si può scaricare e installare come al solito: apri il file `.dmg` e trascina l'app nella cartella **Applicazioni**.

| Programma | Download |
|---|---|
| Obsidian | https://obsidian.md/download |
| GitHub Desktop | https://desktop.github.com/download/ |
| Telegram | https://desktop.telegram.org |
| Ente Auth | https://ente.com/auth/ |
| Node.js (versione **LTS**, file `.pkg`) | https://nodejs.org/it/download |

Gemini CLI, dopo aver installato Node.js, si installa dal terminale:

```
npm install -g @google/gemini-cli
```

Se compare un errore `EACCES` (permessi), non insistere: chiedi in aula.

Vedi anche: [Software del corso](Software%20del%20corso.md)
