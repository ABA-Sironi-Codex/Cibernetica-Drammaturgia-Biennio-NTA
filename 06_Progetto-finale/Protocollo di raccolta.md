---
tipo: progetto
---
# Protocollo di raccolta

Il protocollo è l'insieme delle regole con cui raccogliamo i dati: che cosa si misura, come, quando. Cresce con il corso: ogni fase aggiunge uno strato, e ogni versione viene discussa e riscritta dalla classe.

| Versione | Da quando | Come |
|---|---|---|
| v0 · carta | L01 | Un quaderno fisico, alla maniera di *Dear Data* |
| v1 · testo | L05 | Nota giornaliera nel Quaderno, con le proprietà come dati |
| v2 · moduli e sensori | Fase C | App, moduli, sensori del telefono |
| v3 · dal vivo | Fase D | Webcam, microfono, sensori letti in tempo reale e non salvati |

## Regole per tutte le versioni

- **La partecipazione è volontaria.** Ognuno sceglie che cosa misurare; valgono anche dati poetici o inventati. Chi non vuole condividere dati personali può inventarli tutti
- **Il voto non dipende** dalla quantità o dalla natura dei dati condivisi
- **Un dato dimenticato non si inventa a posteriori.** Sulla carta si scrive *dimenticato*; nel Quaderno la proprietà resta vuota. Anche i vuoti sono un dato
- **Le persone non si nominano.** Nelle note, chi compare ha un soprannome o un ruolo, mai il nome vero: il Quaderno è pubblico
- **Le note già scritte non si correggono** quando il protocollo cambia: la storia del protocollo resta visibile nei dati

## v0 · Carta (dalla L01)

Ogni giorno, sul quaderno di carta, con la data in cima alla pagina:

1. **un dato del corpo** (per esempio: ore di sonno, passi, bicchieri d'acqua, rampe di scale)
2. **un dato dell'umore** (per esempio: una parola, un colore, un numero da 1 a 5)
3. **un dato inventato**, poetico, che riguarda solo te (per esempio: quante volte hai guardato fuori dalla finestra)

Dalla L04 i dati della carta vengono trascritti nel Quaderno, una nota per giorno, con tre proprietà: `corpo`, `umore`, `inventato`.

## v1 · Testo (dalla L05)

*Si scrive insieme in aula, nella L05, dopo la revisione delle prime settimane.*

La revisione parte da quattro domande:
1. Che cosa ha funzionato?
2. Che cosa è stato noioso?
3. Che cosa non si riusciva a misurare?
4. Che cosa manca?

E da un problema: il corpo della classe è **unico** e **proteiforme**. Unico vuol dire che qualcosa deve essere in comune: se ognuno misura una cosa diversa, non c'è un corpo, ci sono sei persone. Proteiforme vuol dire che ognuno resta diverso. Per questo il protocollo ha **due livelli**: dati in comune, misurati da tutti nello stesso modo, e dati personali.

### Dopo la revisione, nel Quaderno
- [ ] aggiorna il modello `99_Sala-Macchine/Template/nota-giornaliera` con le proprietà nuove
- [ ] imposta il tipo *numero* per le proprietà numeriche
- [ ] aggiorna `03_Progetto/il-mio-protocollo`
- [ ] aggiungi le colonne nuove alla base `i-miei-dati`

## v2 · Moduli e sensori (Fase C)

La carta resta possibile, ma i dati possono arrivare anche da altre fonti. Ogni strumento produce un file di dati, quasi sempre un **CSV**: una tabella in testo semplice che p5.js sa leggere.

| Strumento | Che cosa raccoglie | Come si esportano i dati |
|---|---|---|
| **phyphox** | movimento, suono, luce, dai sensori del telefono | CSV, dall'app |
| **contapassi del telefono** | passi, distanze | dall'app Salute (iPhone) o da Google Health (Android) |
| **Daylio** | umore e attività, con un tocco | CSV, gratuito |
| **Google Health** | sonno, movimento, battito, con un orologio Fitbit o Pixel Watch | dalle impostazioni dell'app o dall'account Google |
| **modulo Google** | i dati in comune della classe, ogni giorno, dalla L09 | Foglio Google → CSV |
| **bot Telegram** | i dati in comune, con un messaggio al giorno | *in un secondo momento* |

Vedi [Software del corso](../03_Guide/Software%20del%20corso.md).

## v3 · Dal vivo (Fase D)

Dati che esistono solo nel momento della performance: la webcam che vede un corpo, il microfono che sente una voce, il telefono che sente un movimento. Vengono letti in tempo reale e **non vengono salvati**.
