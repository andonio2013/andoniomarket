# AnDonio Market

**Gestionale di cassa per negozi** — funziona su Windows, senza installare Python e senza Internet (tranne la prima attivazione della licenza).

Cassa, catalogo prodotti, magazzino, clienti e punti fedeltà, scontrini in PDF, self-checkout, riconoscimento del volto per la tessera, bacheca "Oggi" con compleanni e scorte, inventario con scanner, conteggio cassa guidato, backup automatici: tutto in un unico programma.

---

## Download

| File | A cosa serve |
|---|---|
| **[AnDonioMarket_Setup.exe](https://github.com/andonio2013/andoniomarket/raw/main/AnDonioMarket_Setup.exe)** — 95 MB | Installer per Windows — **consigliato**. Installa il programma per l'utente corrente (non servono permessi di amministratore), crea i collegamenti nel menu Start e sul Desktop e, se trova una cartella con i dati di AnDonio Market, può importarli. |
| **[AnDonioMarket.exe](https://github.com/andonio2013/andoniomarket/raw/main/AnDonioMarket.exe)** — 92 MB | Versione **portable**: un solo file, non si installa. Mettilo in una cartella e fai doppio clic. Crea i propri dati accanto a sé. |

Requisiti: Windows 10 o 11 a 64 bit, connessione a Internet per la prima attivazione.

📘 **Manuale utente completo** (con immagini): [MANUALE.md](MANUALE.md) — spiega passo per passo la cassa, il pannello online, le offerte, i coupon, il self-checkout, il gratta e vinci e gli appuntamenti.

---

## Licenza

**Il programma richiede una chiave di licenza.** Non ci sono chiavi di prova né chiavi incluse in questo repository.

Per acquistare una licenza (o per assistenza) scrivi a:

> **andonio2013@gmail.com**

Indica nella email:

- la **versione** che ti interessa (vedi tabella sotto);
- il **nome del negozio** e quanti **computer** devono usarla.

Riceverai una chiave nel formato `ANDM-XXXXX-XXXXX-XXXXX-XXXXX`. Al primo avvio il programma la chiede, la verifica online e la lega al PC. La licenza non distingue maiuscole e minuscole e i trattini possono essere omessi.

### Versioni disponibili

| Versione | Chiave | Funzioni incluse |
|---|---|---|
| **Cassa Libera** | `ANDM-L…` | Solo cassa con articolo libero: importo digitato a mano, nessun catalogo. |
| **Cassa & Catalogo** | `ANDM-C…` | Cassa con catalogo prodotti, sconti, metodi di pagamento e storico scontrini. |
| **Magazzino** | `ANDM-M…` | Solo magazzino: prodotti, prezzi, scorte minime, riordino, codici a barre. |
| **Negozio** | `ANDM-N…` | Cassa con catalogo **+** magazzino **+** clienti e punti fedeltà. |
| **Completo** | `ANDM-F…` | Tutte le funzioni: cassa, catalogo, magazzino, clienti, statistiche, utenti e permessi. |

Il programma installato è sempre lo stesso: la chiave decide quali funzioni si aprono. Le funzioni non incluse nella versione acquistata restano visibili ma bloccate con un lucchetto; premendole compare un avviso con il recapito per richiedere l'upgrade.

### Cosa sapere sulla licenza

- Ogni chiave vale per il numero di computer concordato all'acquisto (di norma uno). Per cambiare PC scrivi all'assistenza: la chiave viene sbloccata e puoi riattivarla sul nuovo computer.
- Il programma controlla la licenza all'avvio e poi ogni 15 minuti. Se il PC resta offline hai 30 minuti di tempo per tornare online; dopo, il programma si blocca e protegge i dati finché non torna la connessione con una licenza valida.
- Se la licenza viene sospesa, revocata o fatta scadere, il programma si blocca al controllo successivo: in quel caso scrivi a **andonio2013@gmail.com**.

---

## Sito del negozio (online)

Il programma si collega al sito del negozio:

- **Listino online** (`/listaprodotti`): tutti i prodotti con prezzo, prezzo scontato e disponibilità, riservato ai clienti registrati.
- **IlMioMarket**: l'area personale del cliente con la **carta fedeltà** (codice a barre EAN-8), i punti, i dati del profilo e il carrello salvato. Alla registrazione, se il numero di carta esiste già, l'account viene collegato a quel cliente e ai suoi punti.
- **Ordini con ritiro**: il cliente ordina dal sito, riceve un codice a barre e lo mostra alla cassa; il negozio vede l'ordine nel pannello e lo segna pronto o ritirato.
- **Promozioni via email**: dal pannello si invia un avviso con le promozioni della giornata o un testo personalizzato, a tutti i clienti o solo ad alcuni.
- **Clienti**: il negoziante vede i clienti registrati e la loro email e può assegnare una nuova password oppure chiederne il cambio al prossimo accesso.

### Sincronizzazione con il sito

La sincronizzazione funziona nei due sensi e parte anche da sola all'avvio del programma.

Nel programma apri **Clienti → ⚙️ Impostazioni sincronizzazione sito** e incolla il **token** che trovi nel pannello del sito in *Impostazioni → Sincronizzazione gestionale desktop* (pulsante **Copia token**; l'indirizzo è già compilato). Premi **Verifica collegamento**: deve rispondere «Collegamento riuscito» con il numero di clienti e prodotti del sito. Poi premi **☁ Sincronizza tutto col sito**:

- dal sito arrivano i clienti iscritti online e i prodotti aggiunti dal pannello;
- dal programma partono i clienti creati alla cassa, il saldo punti, i prezzi e le giacenze.

Nel campo **Indirizzo del sito** va solo l'indirizzo (per esempio `https://iltuosito.freebuff.page`): se incolli per errore un indirizzo che finisce con `/api/sync/...` il programma lo corregge da solo.

I punti del gestionale sono la fonte: alla prima sincronizzazione i saldi online non vengono mai diminuiti (si può scegliere di sostituirli con quelli della cassa con l'opzione nella finestra), poi il sito applica solo le differenze, quindi i punti assegnati online non vengono mai azzerati. Il token permette solo di leggere e aggiornare clienti, punti e prodotti: non dà accesso alla cassa, alle licenze o agli altri dati del negozio.

**Il codice cliente è quello della cassa.** Ogni cliente ha un *codice cliente* (quello che si digita o si scansiona al banco). Quello impostato nel gestionale è l'unico valido: la sincronizzazione lo porta al sito e lo riporta al gestionale, quindi dopo un allineamento non si vedono più codici diversi fra pannello, sito e cassa. Se due programmi hanno lo stesso cliente, vince il codice del gestionale.

**Cosa viaggia nella sincronizzazione** (a due vie, ogni volta che si apre il programma, ogni 15 minuti e a richiesta): prodotti, prezzi e giacenze, clienti con compleanno e codice, punti fedeltà, coupon (compresi quelli di compleanno), offerte del giorno con le loro regole, scontrini e registro attività del desktop, ordini con ritiro, appuntamenti richiesti dal sito e partite di gratta e vinci. Per ogni voce vince la modifica più recente; le cancellazioni non vengono mai riportate indietro.

## Ordini con ritiro in negozio

Il cliente riempie il carrello su `/listaprodotti` e preme **Ordina e ritira in
negozio**: riceve un codice (`ORD…`) con il suo codice a barre, lo trova anche in
IlMioMarket e può mostrarlo dal telefono. Il negozio lo vede in **Ordini** nel
pannello (e riceve una email) e può segnarlo *In preparazione* o *Pronto*: al
cliente arriva l'avviso.

Nella versione **Illimitato** basta scansionare il codice nella cassa: il
gestionale carica da solo i prodotti e il cliente dell'ordine, così resta solo
da premere **Emetti documento**. Dopo lo scontrino l'ordine passa a *Ritirato*,
con il numero del documento. Se un prodotto non è più in catalogo viene segnalato
e le altre righe si caricano comunque.

## Etichette prezzo

Da **Prodotti → 🏷️ Etichette prezzo (PDF A4)** si stampano cartellini con nome,
prezzo, nome del negozio e codice a barre Code128, tre per riga su A4. Si può
scegliere fra i prodotti selezionati, tutti o solo quelli sotto scorta minima, e
quante copie per prodotto.

## Backup sul sito

In **Impostazioni & Backup → ☁️ Backup sul sito** il programma carica una volta al
giorno lo stesso ZIP dei backup locali (dati, utenti, registro documenti — mai il
file `.env`). Dal pannello web, *Impostazioni → Backup cloud*, si scarica l'ultimo
file per ripristinarlo da **Ripristina da file…** se il PC si guasta. Il sito
tiene gli ultimi 14 backup.

## Coupon e tessera sul telefono

In IlMioMarket il cliente vede la tessera anche come **QR** e i suoi **coupon**.
Dal pannello, pagina *Coupon*, si creano coupon in euro o in percentuale e i
coupon di compleanno (basta il compleanno nella scheda cliente, formato `MM-GG`).
Alla cassa si scansiona il codice `CPN…` (o si usa **🎟️ Applica coupon**): lo
sconto viene applicato subito e il coupon risulta usato sullo scontrino. Dalla
stessa pagina si possono anche far scadere i punti dei clienti inattivi, con
anteprima prima di confermare.

## Fattura ai clienti azienda

Nella scheda cliente si annotano **P.IVA / C.F.** e **compleanno**. In cassa, con
un cliente selezionato, la casella **📄 Emetti fattura** produce un documento
intestato *FATTURA* con la partita IVA del cliente e numerazione propria
(`1/2026`, `2/2026`, …); la numerazione riparte da 1 ogni anno. Il riepilogo IVA
per il commercialista resta in **Statistiche → Esporta report**.

## Compleanni e coupon

In **Clienti** ogni scheda ha la **data di compleanno** (visibile anche
nell'elenco). Il cliente può aggiungerla da solo registrandosi al sito oppure
dalla sua area personale. Il giorno del compleanno il sito crea in automatico un
coupon con lo sconto impostato dal negozio (in euro o in percentuale) e lo invia
per email al cliente; in cassa basta scansionare il codice `CPN…` e lo sconto si
applica da solo, al banco come in IlMioMarket.

## Offerte del giorno

Nella scheda **Offerte** del pannello decidi tutto: quante offerte al giorno
(fino a nove), l'ora, i prodotti e l'intervallo di sconto. Ogni offerta ha la
sua regola indipendente: percentuale oppure importo fisso in euro, prodotti
scelti, peso manuale per la vendita a peso, quantità, scadenza e interruttore
per accenderla o spegnerla. Con Ctrl/Shift puoi selezionarne più di una e
attivarle, disattivarle o dare la stessa scadenza in un colpo solo.

Dopo l'ora impostata (di base le 10:00) il sistema genera da solo le offerte e
crea un codice `OFF…` per ciascuna. Se l'invio email è attivo, i clienti
iscritti ricevono l'elenco in automatico, anche se nessuno apre il pannello o
la cassa. Alla cassa si scansiona il codice e lo sconto si applica solo a quei
prodotti, per quella vendita, finché l'offerta non è scaduta.

Le nove regole, l'ora, i prodotti e tutte le impostazioni di sconto sono
sincronizzate **a due vie** tra la dashboard e il gestionale: vince l'ultima
modifica, e ciò che è possibile allineare con Loyverse (prodotti, prezzi,
clienti e scontrini) viaggia con la stessa sincronizzazione.

## Il cervello del negozio

Nel pannello c'è la sezione **Cervello**: quattro strumenti che lavorano sui dati
veri del negozio.

- **Previsioni e riordino**: per ogni prodotto la media venduta al giorno sugli
  ultimi 28 giorni, i giorni di copertura delle scorte, la quantità da ordinare
  (14 giorni più la scorta minima) e lo stato *esaurito / urgente / esaurimento /
  ok*. Il riordino è già diviso per fornitore, con il totale a costo d'acquisto e
  il pulsante per registrare l'ordine.
- **Regole sconto automatiche**: percentuale, 3×2, 2×1, bundle e scaglioni, con
  prodotti, categorie, giorni della settimana, **fascia oraria**, periodo di
  validità e priorità. Non serve digitare codici: la cassa applica la regola da
  sola e lo sconto compare sullo scontrino come `CODICE AUTO`. Una regola con
  fascia `18:00`–`23:59` è, per esempio, lo sconto anti-spreco della sera.
- **Missioni cliente**: obiettivi per periodo (tre visite in una settimana, una
  spesa minima nel mese, un certo numero di punti) con premio in punti accreditato
  una volta sola al raggiungimento della soglia.
- **Turni e chiusura Z**: timbratura entrata/uscita e report per operatore con
  scontrini, incasso, contanti, sconti, annullati e ore lavorate.

Regole e missioni stanno sul server, quindi valgono sia per la cassa del
pannello web sia per la cassa del gestionale desktop: l'app ha la stessa scheda
**🧠 Cervello** e, appena il carrello cambia, chiede al sito quali sconti
automatici valgono per quella spesa. Senza collegamento al sito il programma
continua a vendere con le regole locali e la scheda lo segnala.

## Appuntamenti in negozio (`/prenota`)

Nel sito c'è la pagina **/prenota**: il cliente sceglie giorno e ora, scrive cosa
vuole discutere (un prodotto da ordinare, un preventivo, un problema) e invia la
richiesta. Serve l'accesso, così la richiesta arriva già con nome, email e
telefono e il negozio può rispondere.

Il negoziante vede le richieste in **Appuntamenti**, sia nel pannello del sito
sia nel gestionale desktop (anche in versione Licenza), e può fissare l'appuntamento,
segarlo come *Fatto*, *Annullato* o *Non presentato* e rispondere al cliente
(la risposta parte per email). Le richieste in attesa sono evidenziate con un
avviso all'apertura del programma; gli appuntamenti sono sincronizzati fra sito e
gestionale insieme a tutto il resto.

## Gratta e vinci online (`/grattasubito`)

In **/grattasubito** il cliente registrato trova il suo gratta e vinci: tocca le
caselle, scopre il risultato e, se vince, riceve un premio. **Serve l'accesso**
per giocare: senza login il pulsante resta bloccato e la pagina invita a
registrarsi.

Il negoziante decide tutto da **Gratta e vinci** (pannello online e gestionale
desktop): se attivare il gioco, quanti gratta al giorno per ogni cliente (o il
valore generale per tutti), quali premi esistono (sconto in euro, sconto in
percentuale, omaggio), il valore di ciascun premio, le probabilità di vittoria, il
numero di caselle e i giorni di validità del premio. Il cliente può fare un solo
gratta al giorno per ogni livello di premio.

I premi vinti diventano **tagliandi** con un codice `GRA…`: il cliente li vede in
IlMioMarket e alla cassa si digita o si scansiona il codice, così lo sconto si
applica da solo e il tagliando risulta utilizzato sullo scontrino (non si può
usare due volte). Le impostazioni e i premi sono sincronizzati a due vie, quindi
valgono allo stesso modo sul sito e al banco.

## Backup su Google Drive

Il programma salva una copia dei dati all'apertura e poi ogni 15 minuti nella
cartella **Il mio Drive → AnDonio Market Backup**, dentro una sottocartella nuova
con data e ora (`25-10-2026_14-32-05`): nessun backup precedente viene mai
sovrascritto. Si accende o spegne da **Impostazioni & Backup**.

## Self-checkout

Dalla barra in alto premi **🛒 Self-checkout**: si apre una schermata sola, a
tutto schermo, pensata per il cliente. Ci sono solo i prodotti (ricerca o
scansione con la fotocamera, anche dal telefono con Iriun Webcam), il carrello,
il riconoscimento del volto per la tessera fedeltà, il **ritiro di un ordine**
fatto dal sito, la scelta del **metodo di pagamento** (carta o contanti, con
l'importo ricevuto e il resto), l'anteprima dello scontrino e il pulsante per
emetterlo.

I pulsanti sono grandi e restano sempre visibili anche sugli schermi piccoli;
i messaggi (peso, PIN, errori, scontrino emesso) compaiono sopra la postazione
e non dietro la finestra principale.

Per uscire serve il **PIN di un amministratore**: il cliente non può chiudere
la postazione né tornare al gestionale completo.

## Riconoscimento del volto

In **Impostazioni → 🙂 Riconoscimento volto clienti** puoi registrare il volto
di un cliente (una quindicina di foto dalla webcam) e poi alla cassa basta
premere **🙂 Riconosci cliente dal volto**: il cliente e i suoi punti fedeltà
vengono selezionati da soli, senza digitare il codice della tessera.

Funziona con la webcam del PC oppure con **Iriun Webcam**: apri l'app sul
telefono, collegalo alla stessa Wi-Fi del computer e il programma trova e usa
"Iriun Webcam" da solo (lo stesso vale per Camo Studio e DroidCam).

Le foto restano solo su quel computer, nella cartella `data\volti`, e non
vengono mai inviate a Internet. Se un cliente viene riconosciuto troppo spesso
o troppo poco, si regola la **soglia** dalle stesse impostazioni (30 = severa,
130 = permissiva).

## AnDoPay: la carta del negozio

**AnDoPay** è la carta di pagamento interna: saldo, PIN e CVC, livelli
(Bronzo, Argento, Oro e quelli che crei tu) che scattano con i punti, ricariche,
rettifiche, blocchi e prestiti a rate. La emetti dal pannello o dal programma,
con numero da 8, 12 o 16 cifre, e il cliente la richiede da solo su
**[`/cartando`](https://site-0d25e51ac1fb4bf1bddfc61dd626b1bc.freebuff.page/cartando)**:
lí vede la carta disegnata con il colore del suo livello, il saldo, i movimenti,
il **codice monouso di 8 cifre** e il pulsante per chiedere un prestito.

Si paga in tre modi: **numero + PIN + CVC**, **codice monouso di 8 cifre**
(digitato in cassa come un codice prodotto, vale una volta sola) oppure con un
addebito dal pannello. Funziona nella cassa desktop, nel POS web e nel
self-checkout; il saldo lo muove il sito, quindi cassa, web e area cliente
restano sempre allineati e sullo scontrino compare il saldo rimasto.

## Ruoli con limiti e seconda cassa

Ogni cassiere può avere i suoi **permessi** (vendere, sconti, resi, resoconti,
prodotti…) e **due limiti numerici**: sconto massimo applicabile e importo
massimo del singolo documento. Se esiste anche il limite del negozio vale il più
basso dei due; l'amministratore non ha limiti.

Per una **seconda cassa** (altro PC o tablet) dal pannello web apri *Casse
collegate* e crea una postazione scegliendo il cassiere: ottieni un **codice di
sei caratteri** da digitare sull'altra postazione in *🔗 Collega questa cassa con
un codice*. Quella cassa lavora come quel cassiere, con i suoi permessi e i suoi
limiti. Le stesse funzioni sono anche nel programma desktop (**🖧 Casse
collegate**), e quello che fai da una parte si vede dall'altra.

## Reparti, fornitori, livelli fedeltà

Nelle impostazioni del sito imposti **reparti** (categorie), **fornitori**
(nome, telefono, email) e **livelli fedeltà**: nome del livello, punti a cui
scatta, moltiplicatore dei punti e sconto. Da *Prodotti* vedi anche il **prezzo
di acquisto** e il **margine** di ogni articolo. Tutto arriva al programma
desktop con la sincronizzazione.

## Consegna a domicilio ed email automatiche

La **consegna** si accende dal pannello con costo, soglia per la gratuità,
raggio, fasce orarie, giorni e una nota per il cliente. Le **email automatiche**
sono tre: coupon di benvenuto, carrello abbandonato e clienti che non tornano da
un po'; a queste si aggiungono il coupon di compleanno e l'email delle offerte
del giorno.

## Ripristino da backup

Dalla pagina **Backup** del pannello puoi scaricare un backup caricato dal
gestionale oppure premere **Ripristina**: la richiesta resta in attesa e al giro
di sincronizzazione successivo il programma scarica quel backup, salva prima una
copia di sicurezza dello stato attuale e lo rimette al posto dei dati.

## Primo avvio

1. Installa con `AnDonioMarket_Setup.exe` (oppure apri `AnDonioMarket.exe`).
2. All'avvio inserisci la chiave ricevuta via email e premi **Attiva licenza**.
3. Inserisci i tuoi prodotti da *Prodotti* (o importali) e inizia a vendere.

I dati restano sul tuo computer, nelle cartelle accanto al programma:

```
data\        prodotti, clienti, storico, punti, utenti, cassa
SCONTRINI\   documenti TXT e PDF
BACKUP\      backup automatici e manuali
logs\        registro tecnico
```

La disinstallazione rimuove il programma ma **non cancella i dati**. Fai comunque backup regolari da *Impostazioni → Backup*.

---

## Supporto

Problemi, licenze, upgrade di versione: **andonio2013@gmail.com**

---

*In questo repository non sono pubblicate chiavi di licenza, dati dei clienti né il codice sorgente del programma.*
