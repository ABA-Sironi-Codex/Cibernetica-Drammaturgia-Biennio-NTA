---
tipo: guida
---
# Installazioni Windows

Questa guida installa tutti i programmi del corso con **winget**, il [Gestore di pacchetti](../04_Glossario/Gestore%20di%20pacchetti.md) che Windows ha già al suo interno: un negozio a cui si chiedono i programmi per nome. È la stessa procedura della L02, da seguire a casa se in aula non hai finito o se qualcosa è andato storto.

Ti servono: il computer collegato alla corrente e a internet, una mezz'ora di tempo.

> [!WARNING]
> **Prima di cominciare**
> - **Windows 11, versione 24H2 o successiva** serve per Gemini CLI. Per sapere che versione hai: tasto Windows + R, scrivi `winver`, premi Invio. Con Windows 10 o un Windows 11 più vecchio puoi installare tutto il resto, ma salta i passi 5 e 6
> - Il tuo utente deve essere **amministratore** del computer. Se il computer è di un'altra persona o di un'azienda, potresti non esserlo: in quel caso vai direttamente al [Piano B](#piano-b)
> - Almeno **10 GB liberi** sul disco

## 1. Aprire il terminale

Tasto Windows, scrivi *Terminale* (oppure *PowerShell*), premi Invio. Non usare il vecchio *Prompt dei comandi*. Vedi anche [Guida - Terminale minimo](Guida%20-%20Terminale%20minimo.md).

## 2. Controllare winget

```
winget --version
```

Deve rispondere con un numero di versione, per esempio `v1.11.400`.

Se risponde che `winget` *non è riconosciuto*: apri il **Microsoft Store**, cerca **Programma di installazione app** (*App Installer*) e premi **Aggiorna** o **Installa**. Poi chiudi e riapri il terminale.

## 3. I programmi

Scrivi i comandi **uno alla volta**, premendo Invio dopo ognuno e aspettando che finisca:

```
winget install -e --id Obsidian.Obsidian
winget install -e --id GitHub.GitHubDesktop
winget install -e --id OpenJS.NodeJS.LTS
winget install -e --id Telegram.TelegramDesktop
winget install -e --id ente-io.auth-desktop
```

- Alla prima installazione winget chiede se accetti i termini delle sue fonti: scrivi `Y` e premi Invio
- Alcuni programmi aprono una finestra che chiede *Consentire a questa app di apportare modifiche al dispositivo?*: rispondi **Sì**. Se la finestra non compare, cercala nella barra delle applicazioni: a volte resta dietro le altre
- `-e` vuol dire *exact*: installa esattamente quel programma, non uno con un nome simile

## 4. Permettere a npm di funzionare

Windows, per sicurezza, blocca alcuni tipi di programmi scaricati. Questo comando gli dice di fidarsi di quelli firmati, solo per il tuo utente:

```
Set-ExecutionPolicy -Scope CurrentUser RemoteSigned
```

PowerShell chiede conferma: scrivi `S` e premi Invio.

**Adesso chiudi il terminale e riaprilo.** Il terminale si accorge dei programmi nuovi solo quando viene riaperto.

## 5. Gemini CLI

```
npm install -g @google/gemini-cli
```

Può durare qualche minuto e stampare molte righe gialle che cominciano con `npm warn`: sono normali. Contano solo le righe rosse con `npm error`.

## 6. Verificare

```
node --version
gemini --version
```

Tutti e due devono rispondere con un numero. Poi apri dal menu Start, uno alla volta:

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

Poi rendi privata la tua email: su https://github.com → la tua foto in alto a destra → *Settings* → *Emails* → spunta **Keep my email addresses private**. GitHub ti mostra un indirizzo del tipo `12345678+nomeutente@users.noreply.github.com`. In GitHub Desktop: *File* → *Options* → *Git* → scegli quell'indirizzo nel menu dell'email.

Vedi anche [Guida - Account GitHub e 2FA](Guida%20-%20Account%20GitHub%20e%202FA.md).

## Aggiornare, ogni tanto

Una volta al mese, nel terminale:

```
winget upgrade --all
npm update -g @google/gemini-cli
```

La prima riga aggiorna tutti i programmi che winget conosce, la seconda Gemini CLI.

## Se qualcosa va storto

| Problema | Soluzione |
|---|---|
| `winget` non riconosciuto | Microsoft Store → *Programma di installazione app* → Aggiorna. Poi riapri il terminale |
| `npm` non riconosciuto | Non hai riaperto il terminale dopo aver installato Node.js. Chiudilo e riaprilo |
| `npm.ps1 non può essere caricato perché l'esecuzione di script è disabilitata` | Hai saltato il passo 4 |
| `EPERM` o `EACCES` durante `npm install -g` | Chiudi tutti i terminali, riaprine uno e ripeti. Se continua, può essere l'antivirus: chiedi in aula |
| Un pacchetto winget fallisce e parla di permessi | Il tuo utente non è amministratore: usa il [Piano B](#piano-b) per quel programma |
| Avviso blu di *SmartScreen* su un installer | *Ulteriori informazioni* → *Esegui comunque*. Solo per i programmi di questo elenco |
| Gemini CLI non parte e parla della versione di Windows | Il tuo Windows è più vecchio di 11 24H2: in aula useremo l'alternativa via web |

Se non riesci a risolvere: fai una foto dello schermo con l'errore e mandala su Classroom o nel gruppo Telegram.

## Piano B

Se winget non funziona, ogni programma si può scaricare e installare come al solito, con un doppio clic sul file scaricato e le opzioni predefinite.

| Programma | Download |
|---|---|
| Obsidian | https://obsidian.md/download |
| GitHub Desktop | https://desktop.github.com/download/ |
| Telegram | https://desktop.telegram.org |
| Ente Auth | https://ente.com/auth/ |
| Node.js (versione **LTS**, file `.msi`) | https://nodejs.org/it/download |

Poi riprendi dal passo 4 di questa guida: i passi 4, 5 e 6 sono uguali.

Vedi anche: [Software del corso](Software%20del%20corso.md)
