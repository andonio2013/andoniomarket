# Manuale utente — AnDonio Market

Manuale completo del gestionale **AnDonio Market** e del sito del negozio.
Va bene sia per la versione **Illimitato** (quella del negozio) sia per le
versioni con **licenza** (Cassa Libera, Cassa & Catalogo, Magazzino, Negozio,
Completo): le funzioni sono le stesse, la chiave di licenza decide quali si
aprono.

Indice:

1. [Installazione e primo avvio](#1-installazione-e-primo-avvio)
2. [La cassa](#2-la-cassa)
3. [Prodotti, magazzino ed etichette](#3-prodotti-magazzino-ed-etichette)
4. [Clienti, tessere e compleanni](#4-clienti-tessere-e-compleanni)
5. [Appuntamenti dal sito](#5-appuntamenti-dal-sito)
6. [Gratta e vinci](#6-gratta-e-vinci)
7. [Offerte del giorno e sconti](#7-offerte-del-giorno-e-sconti)
8. [Coupon, buoni regalo e punti](#8-coupon-buoni-regalo-e-punti)
8-bis. [AnDoPay — la carta del negozio](#8-bis-andopay--la-carta-del-negozio)
9. [Ordini con ritiro](#9-ordini-con-ritiro)
10. [Self-checkout](#10-self-checkout)
11. [Riconoscimento del volto](#11-riconoscimento-del-volto)
12. [Sito del negozio](#12-sito-del-negozio)
12-bis. [Impostazioni del negozio](#12-bis-impostazioni-del-negozio-pannello-web)
13. [Sincronizzazione con il sito](#13-sincronizzazione-con-il-sito)
13-bis. [Ruoli con limiti e seconda cassa](#13-bis-ruoli-con-limiti-e-seconda-cassa)
14. [Backup](#14-backup)
15. [Domande frequenti](#15-domande-frequenti)

---

## 1. Installazione e primo avvio

### Cosa scaricare

| File | A cosa serve |
|---|---|
| `AnDonioMarket_Setup.exe` | **Consigliato.** Installa il programma per l'utente corrente (non serve essere amministratore), crea i collegamenti nel menu Start e sul Desktop. |
| `AnDonioMarket.exe` | Versione **portabile**: un solo file, non si installa. Mettilo in una cartella e fai doppio clic. |

Requisiti: Windows 10 o 11 a 64 bit. Internet serve la prima volta per
attivare la licenza; poi il programma funziona anche senza connessione.

### Attivazione della licenza

1. Apri il programma.
2. Inserisci la chiave ricevuta (formato `ANDM-XXXXX-XXXXX-XXXXX-XXXXX`) e premi
   **Attiva licenza**. I trattini si possono anche omettere.
3. La chiave viene legata a quel computer. Per spostarla su un altro PC scrivi
   all'assistenza: viene sbloccata e la riattivi sul computer nuovo.

Il programma ricontrolla la licenza all'avvio e poi ogni 15 minuti. Se il PC
resta offline hai 30 minuti di tempo per tornare online; dopo, il programma si
blocca finché non torna la connessione.

### Dove finiscono i dati

Tutti i dati restano sul tuo computer, accanto al programma:

```
data\        prodotti, clienti, storico, punti, utenti, regole, cassa
SCONTRINI\   documenti TXT e PDF
BACKUP\      backup automatici e manuali
logs\        registro tecnico
```

Disinstallare il programma **non** cancella i dati.

### Le schede del programma

In alto ci sono i pulsanti di servizio (**Oggi**, **Self-checkout**, **Coda**,
**Apri cassa**), sotto le schede:

- **Cassa** — le vendite.
- **Prodotti** — catalogo, giacenze, etichette.
- **Sconti** — sconti temporanei, bundle, scadenze.
- **Clienti** — anagrafica, punti, tessere, compleanni.
- **Scontrini** — storico e ristampa.
- **Statistiche** — incassi, esportazioni, report IVA.
- **Registro**, **Utenti**, **Impostazioni** (solo amministratore).
- **Appuntamenti** — le richieste di meeting arrivate dal sito.
- **Gratta&Vinci** — regole del gioco, premi in palio e premi da ritirare.

---

## 2. La cassa

### Una vendita normale

1. Cerca il prodotto per nome, scansiona il codice a barre con lo scanner o
   premi **F4** per usare la fotocamera.
2. I prodotti finiscono nel carrello; con **F1** si salta alla ricerca.
3. Se il prodotto è **a peso**, il programma chiede i kg.
4. Premi **F8** (o **Emetti documento**) per chiudere lo scontrino.

Nella colonna destra della cassa trovi cliente, punti, buoni regalo, offerte e
coupon.

### Cliente e punti

- Scansiona la tessera, digita il **codice cliente** oppure premi
  **🙂 Riconosci cliente dal volto**.
- Il codice cliente si può scrivere come vuoi: `201307`, `2013 07` o
  `20-13-07` funzionano tutti, perché il confronto ignora spazi e trattini.
- Se il cliente è registrato al sito, i punti si allineano da soli alla
  sincronizzazione.

### Sconti, buoni, coupon e offerte

- **🏷️ Offerta di oggi** — applica i prodotti dell'offerta del giorno con il
  loro prezzo scontato (vedi [capitolo 7](#7-offerte-del-giorno-e-sconti)).
- **🎟️ Applica coupon** — scansiona un codice `CPN…` (compleanno, benvenuto,
  inattivi, Gratta&Vinci): lo sconto si applica subito e il coupon risulta usato
  sullo scontrino.
- **Buoni regalo** (`BUO…`) — scalano dal saldo del buono.
- **🎲 Biglietto fortunato** — uno sconto a sorpresa sulla vendita.
- I **premi del Gratta&Vinci** sono coupon come gli altri: il cliente ti mostra
  il codice `CPN…` e lo sconto si applica da solo.
- **Codici creati online**: se scrivi o scansiona un codice `BUO…`, `GRA…` o
  `CPN…` che la cassa non ha ancora ricevuto con la sincronizzazione, il
  programma lo chiede al sito e lo applica subito. Non serve far rifare il
  codice al cliente né ricaricare la pagina del pannello. Il saldo dei buoni e
  i premi consegnati restano allineati da sole due parti.

### Ritiro di un ordine del sito

1. Scansiona il codice `ORD…` nella cassa.
2. Il programma carica da solo i prodotti e il cliente dell'ordine.
3. Premi **Emetti documento**: l'ordine passa a *Ritirato* con il numero dello
   scontrino.

### Metodi di pagamento, resto e fattura

- Scegli il metodo (contanti, carta, bancomat, buoni…) e, con i contanti,
  scrivi l'importo ricevuto: il resto viene calcolato da solo.
- Con un cliente che ha **P.IVA / C.F.** spunta **📄 Emetti fattura**: il
  documento è intestato a suo nome, con numerazione propria (`1/2026`, …) che
  riparte da 1 ogni anno.

### Scontrini sospesi e ristampe

- **F2 Sospendi scontrino** mette da parte il carrello, **F3 Riprendi scontrino**
  lo riprende (utile quando il cliente dimentica qualcosa).
- Dalla scheda **Scontrini** cerchi un documento passato e lo ristampi in TXT o
  PDF, oppure ne fai uno **storno** (reso).

---

## 3. Prodotti, magazzino ed etichette

Nella scheda **Prodotti**:

- **Nome, prezzo, IVA, giacenza, barcode** (se lo lasci vuoto il programma
  genera un EAN-8), **costo**, **scorta minima**, **lotto** e **scadenza**.
- **Giacenza illimitata** per i prodotti che non vuoi contare.
- **A peso** per frutta, verdura e sfusi: in cassa si chiedono i kg.
- Da qui si possono anche **importare** ed **esportare** i prodotti in CSV.

**Reparto, fornitore, prezzo di acquisto e margine.** Ogni prodotto può avere
un **reparto** (la categoria) e un **fornitore**: si scelgono nell'editor del
prodotto e compaiono in elenco, dove i filtri in alto mostrano un reparto o un
fornitore alla volta (accanto c'è la ricerca libera per nome o barcode).
Scrivendo il **prezzo di acquisto** il programma calcola da solo il **margine**
in percentuale: così vedi quanto rende un articolo prima di scontarlo.

**📦 Lista di riordino (CSV per fornitore)** prepara l'ordine al fornitore: un
file con i prodotti sotto scorta minima (o tutti quelli selezionati), divisi per
fornitore, pronto da inviare per email. I fornitori con telefono ed email si
possono registrare nella scheda **Fornitori** e nelle impostazioni del pannello
web (*Impostazioni → Reparti, fornitori e livelli fedeltà*).

**🏷️ Etichette prezzo (PDF A4)** stampa cartellini con nome, prezzo, nome del
negozio e barcode Code128, tre per riga: puoi stampare i prodotti selezionati,
tutti, oppure solo quelli sotto scorta minima.

**📦 Inventario** apre il conteggio guidato: si scansiona quello che c'è nella
scaffale e il programma calcola le differenze con la giacenza a sistema, poi
allinea con un pulsante.

I prodotti vicini alla **scadenza** finiscono nella bacheca **📌 Oggi** e possono
essere scontati in automatico con la regola impostata in *Sconti*.

---

## 4. Clienti, tessere e compleanni

Ogni scheda cliente ha: nome, email, telefono, **codice cliente**, **P.IVA /
C.F.**, **data di compleanno**, punti e **tessera fedeltà** (EAN-8).

- **Codice cliente**: è il codice che il cliente vede nel sito come "Codice
  cliente" e che si può digitare in cassa. È quello scritto nel tuo programma:
  alla sincronizzazione la sua versione vince su quella del sito. Se un altro
  cliente del sito (o uno importato da Loyverse) aveva lo stesso codice, dopo la
  sincronizzazione vale il tuo e il codice resta su una sola scheda.
- **Tessera fedeltà**: il programma assegna un EAN-8 (`2000…`) a ogni cliente.
  Si stampa la tessera, si mostra il codice a barre oppure il **QR** dal sito.
- **Compleanno** (formato `GG/MM` o `MM-GG`): il giorno stesso il sito crea in
  automatico il coupon di compleanno con lo sconto che hai impostato e lo invia
  per email al cliente.
- **Punti**: si assegnano alla vendita (1 punto per euro, configurabile) e si
  possono correggere a mano dal pulsante **Modifica punti**.
- **Codice invito** e **invitato da**: per il programma referral (punti a chi
  invita e a chi si iscrive).

### Livelli fedeltà

I livelli (per esempio *Base*, *Argento*, *Oro*) si impostano dal pannello web
in *Impostazioni → Reparti, fornitori e livelli fedeltà*: per ogni livello
decidi **nome**, **punti** a cui scatta e **sconto %** da applicare. Sono le
tue scelte: nessun valore è fissato dal programma.

Con la casella **Sconto automatico per livello (alla cassa)** attiva, quando un
cliente passa in cassa il sito guarda i suoi punti e applica lo sconto del
livello raggiunto: nella cassa online lo vedi scritto nella riga del cliente.
Nella stessa pagina imposti anche i **punti doppi** nei giorni che scegli
(per esempio il martedì) e il moltiplicatore dei punti.

---

## 5. Appuntamenti dal sito

I clienti registrati al sito possono chiedere un **meeting** dal negozio.

### Dal lato cliente — pagina `/prenota`

![Prenota un meeting](immagini/sito-prenota.png)

1. Il cliente apre `/prenota` e fa **accesso** con l'account del sito (è
   obbligatorio: così la richiesta arriva con nome, email e telefono già
   verificati).
2. Sceglie **l'argomento** (Consulenza, Problema con un ordine, Assistenza
   prodotto, Altro), **quando preferisce** (facoltativo), il **telefono** e
   scrive le **note**.
3. Premendo **Invia la richiesta** compare sotto l'elenco **Le tue richieste**
   con lo stato: *In attesa*, *Confermato*, *Annullato*, *Fatto*, insieme alla
   risposta del negozio.
4. Ogni cliente può avere al massimo **tre richieste aperte**: evita di
   riempire l'agenda con lo stesso appuntamento.

### Dal lato negozio — scheda **Appuntamenti**

Nell'app del negozio c'è la scheda **Appuntamenti** con l'elenco delle
richieste (data, cliente, telefono, argomento, preferenza, stato, note) e i
pulsanti:

- **🔄 Aggiorna dal sito** — scarica subito le richieste nuove.
- **✅ Conferma** — il cliente legge *Confermato*.
- **❌ Annulla** — la richiesta sparisce dall'elenco.
- **✔️ Fatto** — meeting concluso.
- Nel campo **Risposta al cliente** puoi scrivere un messaggio (per esempio
  l'orario concordato): arriva nell'area personale del cliente.

Le richieste arrivano anche da sole con la **sincronizzazione** (all'avvio del
programma e con **☁ Sincronizza tutto col sito**), quindi non serve tenere
aperto il pannello web.

### Dal lato negozio — pannello web

Nel pannello del sito c'è la voce **📅 Appuntamenti** (solo amministratore),
con il badge del numero di richieste **da rispondere**: stessi dati dell'app
(cliente, telefono, argomento, note, preferenza, stato) e gli stessi pulsanti
**Conferma**, **Fatto**, **Annulla** e **Rispondi** con il messaggio per il
cliente. L'elenco delle richieste concluse non ingombra: restano solo quelle
ancora aperte.

---

## 6. Gratta e vinci

Il sito ha una pagina **`/grattasubito`** dove i clienti registrati grattano un
biglietto virtuale: se vincono, il premio finisce sulla loro carta fedeltà.

![Gratta e vinci](immagini/sito-grattasubito.png)

### Dal lato cliente

1. Il cliente apre `/grattasubito` e fa **accesso** (senza account non si può
   grattare: il premio deve poter arrivare sulla sua carta).
2. Vede il **messaggio del negozio**, quanti **biglietti gli restano oggi** e
   l'elenco dei **premi in palio**.
3. Premendo **Gratta il biglietto** il programma decide subito l'esito; il
   biglietto si scopre grattando con il dito o con il mouse (o premendo
   **Scopri subito**).
4. Se ha vinto:
   - per uno **sconto** compare un codice `CPN…`: il cliente lo mostra alla
     cassa e lo sconto si applica scansionandolo;
   - per **punti** il saldo della carta aumenta subito;
   - per un **premio in natura** compare un codice `GRA…` da mostrare alla
     cassa, dove il negozio lo segna come ritirato.
5. Tutti i biglietti grattati restano in **I tuoi biglietti**, con il premio,
   il codice e la data.

### Dal lato negozio — scheda **Gratta&Vinci**

Nell'app trovi due parti.

**Regole del gioco** (solo amministratore):

| Impostazione | Cosa fa |
|---|---|
| Gioco attivo | Spegne o accende il gioco sul sito. |
| Probabilità di vincita % | Quante possibilità su 100 ha ogni biglietto di vincere (per esempio 25). |
| Biglietti al giorno per cliente | Quanti biglietti può grattare ogni cliente in un giorno (0 = senza limite). |
| Biglietti totali al giorno | Limite per tutto il negozio (0 = senza limite). |
| Premi al giorno per cliente | Quante volte al giorno lo stesso cliente può vincere (0 = senza limite). |
| Pausa dopo una vincita | Quanti biglietti bisogna grattare dopo un premio prima di poter vincere di nuovo. |
| Messaggio in cima alla pagina | Il testo che i clienti leggono sulla pagina del gioco. |

**Premi in palio** — quanti premi vuoi, ognuno con:

- **Nome** (per esempio "Buono 5 euro");
- **Tipo**: *Sconto in percentuale*, *Sconto in euro*, *Punti fedeltà*,
  *Premio in natura (omaggio)*;
- **Valore** (la percentuale, gli euro o i punti);
- **Peso**: quanto è probabile che esca rispetto agli altri premi (peso 60 esce
  molto più spesso di peso 5);
- **Massimo al giorno** (0 = senza limite) e **valido per giorni** (la scadenza
  del coupon creato);
- **Messaggio al cliente** e interruttore **Premio attivo**.

Premi **💾 Salva e invia al sito**: le regole vengono salvate nel programma e
mandate al sito, quindi valgono per il sito e per tutte le casse collegate.

**Premi vinti da ritirare** — l'elenco dei premi consegnabili (cliente, premio,
codice, email, data). Il pulsante **🔄 Aggiorna dal sito** li scarica subito e
**✅ Premio ritirato** segna il premio scelto come consegnato (e lo toglie
dall'elenco anche sul sito).

### Dal lato negozio — pannello web

Nel pannello del sito c'è la voce **🎰 Gratta e vinci** (solo amministratore):
le stesse impostazioni dell'app (gioco attivo, probabilità di vincita, gratta al
giorno per ogni cliente e per tutto il negozio, vincite al giorno, pausa dopo
una vincita, testo mostrato al cliente) e la tabella dei **premi in palio**
(nome, tipo, valore, peso, al giorno, validità, attivo), con **+ Aggiungi
premio** e **✕** per togliere un premio. Il pulsante **Salva tutto** manda le
regole al sito e a tutte le casse collegate.

Sotto, la parte **Oggi**: quanti biglietti sono stati grattati, quanti hanno
vinto e quanti premi sono **da consegnare**, con il pulsante **Consegnato** per
segnarli (l'elenco si aggiorna anche in cassa e nell'app).

---

## 7. Offerte del giorno e sconti

### Le nove offerte

Nella scheda **Offerte** del pannello (e nelle regole del programma) decidi
tutto, offerta per offerta:

- **Attiva / disattiva** la singola offerta.
- **Tipo**: percentuale oppure **importo fisso in euro**.
- **Valore**: la percentuale (o gli euro) da scontare.
- **Prodotti**: quali prodotti possono andare in quell'offerta (vuoto = tutti).
- **Quantità**: quanti prodotti mettere nell'offerta.
- **Peso manuale**: include anche i prodotti a peso.
- **Scadenza**: giorno e ora in cui l'offerta smette di valere (vuoto = fine
  giornata).
- Con **Ctrl/Shift** puoi selezionarne più di una e **attivare**,
  **disattivare** o dare la **stessa scadenza** in un colpo solo.

Dopo l'ora impostata (di base le **10:00**) il sistema genera da solo le offerte
del giorno e un **codice `OFF…`** per ciascuna, senza che nessuno apra il
programma o il pannello. Se l'invio email è attivo, i clienti iscritti ricevono
l'elenco in automatico (una sola volta al giorno).

Alla cassa si scansiona il codice `OFF…` e lo sconto si applica **solo a quei
prodotti**, per quella vendita, finché l'offerta non è scaduta. Un'offerta
spenta o scaduta viene rifiutata anche se il codice è ancora in giro.

I prezzi dell'elenco sono sempre quelli **attuali del catalogo**, non quelli
salvati il giorno in cui l'offerta è nata: l'email che ricevono i clienti, il
cartello che copi dal pannello e quello che vede la cassa mostrano perciò gli
stessi importi del negozio, anche se nel frattempo un prezzo è stato corretto.

### Sconti temporanei, bundle e scadenze

- **Sconti temporanei**: prezzo scontato su un prodotto per un periodo, con
  data di inizio e fine. Si applicano da soli in cassa e si vedono nel sito.
- **Bundle** (promozioni): *Prendi N, paghi N-1*, *secondo articolo scontato*,
  *gruppo a prezzo fisso*, scegliendo i prodotti.
- **Scadenze**: sconto automatico sui prodotti vicini alla scadenza.

Tutte queste regole si sincronizzano **a due vie** con la dashboard: vince
l'ultima modifica, da qualunque parte sia stata fatta.

---

## 8. Coupon, buoni regalo e punti

- **Coupon** (`CPN…`): compleanno, benvenuto, clienti inattivi, Gratta&Vinci e
  coupon manuali in euro o in percentuale. Si creano dal pannello *Coupon* e si
  applicano in cassa scansionandoli.
- **Buoni regalo** (`BUO…`): si vendono con un importo, hanno un saldo che
  scala a ogni uso e una scadenza.
- **Tutti i codici valgono in entrambi i posti**: un codice creato nel pannello
  web (coupon di compleanno, buono regalo, premio del Gratta&Vinci) funziona
  anche nella cassa del programma desktop e viceversa. Basta scriverlo o
  scansionarlo: se non è già arrivato con la sincronizzazione, la cassa lo
  legge dal sito al momento. Il saldo dei buoni e i premi già consegnati non si
  possono usare due volte.
- **Punti fedeltà**: si accumulano alla cassa (1 punto per euro, configurabile),
  si possono spendere come sconto e si vedono nell'area del cliente.
- **Livelli fedeltà**: li decidi tu. In *Impostazioni → Livelli fedeltà* scrivi
  per ogni livello **nome**, **punti a cui scatta**, **sconto riservato** e
  **moltiplicatore dei punti** (1 = punti normali, 2 = doppi, 1,5 = una volta e
  mezza). Il cliente che raggiunge la soglia riceve automaticamente lo sconto
  del livello e guadagna i punti moltiplicati; il livello e i punti che mancano
  al successivo compaiono nella sua area, e in cassa accanto al nome.
- **Referral**: chi invita un amico prende punti, chi si iscrive con il codice
  anche (valori configurabili).

---

## 8-bis. AnDoPay — la carta del negozio

AnDoPay è la carta di pagamento del negozio: un conto con saldo, PIN e CVC che
il cliente usa in cassa, nel self-checkout e per i prestiti. Non è una carta
bancaria: i soldi li gestisci tu dal pannello o dal programma, e ogni
movimento resta scritto con il saldo che ne risulta.

### I livelli della carta

Bronzo, Argento, Oro e quelli che aggiungi tu. Ogni livello ha **nome**,
**colore**, **punti a cui scatta**, **sconto in cassa** e un eventuale tetto di
saldo. Il livello sale da solo quando il cliente raggiunge la soglia di punti
fedeltà: il cambio resta nei movimenti (per esempio «Carta passata da bronzo a
oro»).

### Emettere una carta

Dal programma: scheda **AnDoPay → ➕ Emetti carta**, scegli cliente, livello,
numero (vuoto = lo genera il sistema), PIN e saldo iniziale. Dal pannello web:
**AnDoPay → + Emetti carta**, stessa cosa. Alla fine leggi **numero, PIN e CVC**
da comunicare al cliente: il PIN serve a pagare, il CVC è la conferma in cassa.

- Il numero può avere **8, 12 o 16 cifre** (lo decidi in *Impostazioni*), con il
  prefisso che vuoi.
- PIN di 4 cifre e CVC di 3: se non li scrivi tu vengono generati a caso.
- Una carta per cliente. **Blocca** e **Disattiva** fermano subito i pagamenti;
  **Gestisci** cambia numero, PIN, CVC, intestatario, livello e saldo.

### Saldo, ricariche e movimenti

In *Gestisci carta* scrivi il nuovo saldo: la differenza diventa una **ricarica**
(o una **rettifica**, se abbassi). Ogni movimento registra tipo, importo, saldo
risultante, chi l'ha fatto e l'ora. Il cliente vede gli stessi movimenti nella
sua area.

### Pagare con AnDoPay

Tre modi, tutti equivalenti:

1. **Numero + PIN + CVC** in cassa, nel POS web o nel self-checkout. Se la carta
   non ha saldo sufficiente il pagamento viene rifiutato e lo scontrino non
   parte.
2. **Codice monouso di 8 cifre**: il cliente lo genera su `/cartando`, tu lo
   digiti in cassa come se fosse un codice prodotto. Il sistema riconosce
   cliente e carta, imposta il pagamento, e il codice **si brucia**: vale per
   una sola transazione e scade dopo i minuti che imposti (15 di default).
3. **Addebito dal pannello o dal programma**, per correggere una vendita.

Sullo scontrino compare `AnDoPay ****1234 · saldo …`, così il cliente sa quanto
gli resta.

### L'area del cliente: `/cartando`

Con il login del sito il cliente vede la **carta disegnata** (colore del
livello, numero mascherato, intestatario, scadenza, CVC a richiesta), il saldo,
la barra verso il livello successivo, i movimenti, il pulsante per il **codice
monouso**, la richiesta di **prestito** e il **cambio PIN**. Il link è anche in
`/ilmioarket`, accanto a Listino, Prenota e Gratta e vinci.

### Prestiti

Il cliente può **chiedere** un prestito dalla sua area, oppure lo concedi tu dal
pannello (*Prestiti → Concedi*) o dal programma (*AnDoPay → 💰 Concedi
prestito*). La cifra entra **subito** nel saldo e il debito si restituisce in
**rate mensili trattenute in automatico dal saldo**; il residuo e la prossima
rata restano visibili sulla carta. Se il saldo non basta, la rata slitta al
mese dopo.

### Impostazioni AnDoPay

Nel pannello, **AnDoPay → Impostazioni**: lunghezza del numero, prefisso,
minuti di validità del codice, ricarica massima, prestito massimo e numero di
rate, PIN e CVC obbligatori, e se il cliente può crearsi la carta da solo.
Le stesse regole valgono per il programma desktop.

### Sincronizzazione

Carte, livelli, movimenti, prestiti e codici arrivano al programma con la
sincronizzazione (scheda **AnDoPay → 🔄 Aggiorna dal sito**). Il **saldo lo
muove solo il sito**: così cassa desktop, POS web, self-checkout e area del
cliente non possono mai divergere. Se il sito non è raggiungibile, AnDoPay non
incassa: meglio un pagamento con carta o contanti che un saldo sbagliato.

---

## 9. Ordini con ritiro

Il cliente riempie il carrello su `/listaprodotti` e preme **Ordina e ritira in
negozio**: riceve un codice `ORD…` con il suo codice a barre, lo trova anche in
IlMioMarket e può mostrarlo dal telefono.

Il negozio lo vede nella pagina **Ordini** del pannello (e riceve una email) e
può segnarlo *In preparazione* o *Pronto*: al cliente arriva l'avviso. Alla
cassa, in versione **Illimitato**, si scansiona il codice e il carrello si
carica da solo.

---

## 10. Self-checkout

Dalla barra in alto premi **🛒 Self-checkout**: si apre una schermata sola a
tutto schermo, pensata per il cliente, con:

- **prodotti** (ricerca o scansione con la fotocamera, anche dal telefono con
  Iriun Webcam);
- **carrello** e totale;
- **riconoscimento del volto** per prendere la tessera fedeltà;
- **ritiro di un ordine** fatto dal sito (codice `ORD…`);
- **metodo di pagamento** (carta o contanti, con importo ricevuto e resto);
- **anteprima dello scontrino** e pulsante per emetterlo.

I pulsanti sono grandi e restano visibili anche sugli schermi piccoli. Per
uscire serve il **PIN di un amministratore**: il cliente non può chiudere la
postazione.

---

## 11. Riconoscimento del volto

In **Impostazioni → 🙂 Riconoscimento volto clienti** registri il volto di un
cliente (una quindicina di foto dalla webcam). Poi in cassa basta premere
**🙂 Riconosci cliente dal volto** e il cliente viene selezionato da solo.

Funziona con la webcam del PC oppure con **Iriun Webcam**: apri l'app sul
telefono, collegalo alla stessa Wi-Fi e il programma usa "Iriun Webcam" da solo
(lo stesso vale per Camo Studio e DroidCam). Le foto restano solo su quel
computer, in `data\volti`. La **soglia** (30 = severa, 130 = permissiva) si
regola dalle stesse impostazioni.

---

## 12. Sito del negozio

Indirizzo di base: `https://iltuosito.freebuff.page`. Le pagine pubbliche e
private sono:

| Pagina | A cosa serve |
|---|---|
| `/listaprodotti` | **Listino** per i clienti registrati: prezzi, prezzo scontato, disponibilità, carrello e ordine per il ritiro. |
| `/ilmioarket` | **IlMioMarket**: carta fedeltà (codice a barre e QR), punti, coupon, ordini, dati del profilo, carrello salvato. |
| `/prenota` | **Prenota un meeting** con il negozio. |
| `/grattasubito` | **Gratta e vinci**: un biglietto al giorno (o quanti ne concedi). |
| pannello del negozio | Cassa web, prodotti, clienti, coupon, offerte, ordini, promo, licenze, impostazioni e backup cloud. |

Alla registrazione, se il cliente scrive il numero di una tessera che esiste già
(anche con spazi, per esempio `2000 0066`), l'account viene collegato a quel
cliente e ai suoi punti.

### L'area del cliente

Entrando in `/ilmioarket` il cliente vede e gestisce da solo:

- la **carta fedeltà** con codice a barre e QR da far scansionare alla cassa
  (nessun numero da dettare) e i **punti** aggiornati;
- i **coupon** attivi (compleanno, benvenuto, offerte, carrello abbandonato,
  Gratta&Vinci) con il codice da mostrare alla cassa;
- gli **ordini** con lo stato del ritiro e i **premi** vinti ancora da ritirare;
- i **dati del profilo**, compreso il **compleanno** (serve per il coupon
automatico) e il **carrello salvato** tra una visita e l'altra.

Tutto quello che il cliente muove qui arriva al programma con la
sincronizzazione: se il cliente si iscrive dal sito, in cassa lo trovi già con
il suo codice cliente.

---

## 12-bis. Impostazioni del negozio (pannello web)

Nel pannello, **Impostazioni**, ci sono tutte le regole che governano il sito e
la cassa. Ogni blocco ha il suo pulsante di salvataggio e quello che imposti qui
arriva anche al programma desktop con la sincronizzazione (e viceversa).

### Dati del negozio

Nome, indirizzo, P.IVA, aliquota IVA di partenza e **valore dei punti**: sono
gli stessi dati che finiscono su scontrini, etichette e fatture. Da qui cambi
anche la password del tuo account del pannello.

### 🎂 Coupon di compleanno

Attivi o disattivi il coupon automatico del compleanno, scegli se inviarlo per
**email** al cliente, il **valore in euro** oppure la **percentuale**, e la
**validità in giorni**. Il giorno del compleanno il sito crea il coupon e lo
invia da solo: in cassa si scansiona il codice e lo sconto si applica.

### Regole sconti, promozioni e referral

Le nove offerte del giorno (peso manuale, importo o percentuale, prodotti,
scadenze, attivazione una per una), bundle, buoni regalo, promozioni e referral:
sono descritte nella sezione 7 di questo manuale.

### Reparti, fornitori e livelli fedeltà

- **Reparti**: l'elenco delle categorie dei prodotti, uno per riga.
- **Fornitori**: nome, telefono ed email di ogni fornitore, da usare per la
  lista di riordino.
- **Livelli fedeltà**: nome, punti a cui scatta il livello e sconto %, più i
  **punti doppi** nei giorni scelti.

### 🛵 Consegna a domicilio

Accendi la consegna nel negozio online e imposta **costo**, **gratis sopra** un
certo importo, **raggio in km**, **fasce orarie**, **giorni** di consegna e una
**nota** che il cliente legge nel carrello.

### ✉️ Email automatiche

Tre automazioni, ognuna con i suoi valori e la sua validità:

- **Coupon di benvenuto** ai nuovi clienti iscritti.
- **Carrello abbandonato**: dopo tot ore il cliente riceve un coupon di
  recupero.
- **Clienti che non tornano da un po'**: dopo tot giorni parte un coupon per
  farlo tornare.

A queste si aggiungono il coupon di compleanno e l'email con le **offerte del
giorno**, che parte da sola una volta al giorno quando accendi l'invio nella
pagina *Offerte*. Se un invio fallisce il sito riprova e l'esito resta visibile
nel pannello.

### 🔔 Avvisi del sito

La campanella nel sito avvisa i clienti delle novità (nuove offerte, ordine
pronto, premio da ritirare). Si accende o si spegne da qui.

### Backup cloud

Carica lo ZIP dei backup fatti dal programma desktop e permette di scaricarlo,
o di chiedere al programma di **ripristinare** un backup scelto: il programma
lo scarica al primo collegamento e si riavvia con i dati ripristinati (prima
salva sempre una copia di sicurezza). Il sito tiene gli ultimi 14 backup.

---

## 13. Sincronizzazione con il sito

La sincronizzazione funziona nei due sensi e parte da sola all'avvio del
programma, oltre che col pulsante **☁ Sincronizza tutto col sito**.

### Come si configura

1. Nel programma apri **Clienti → ⚙️ Impostazioni sincronizzazione sito**
   (oppure *Impostazioni → Sincronizzazione gestionale desktop*).
2. Incolla il **token** che trovi nel pannello del sito in *Impostazioni →
   Sincronizzazione gestionale desktop* (pulsante **Copia token**). L'indirizzo è
   già compilato.
3. Premi **Verifica collegamento**: deve rispondere «Collegamento riuscito» con
   il numero di clienti e prodotti del sito.

Nel campo **Indirizzo del sito** va solo l'indirizzo; se incolli per errore un
indirizzo che finisce con `/api/sync/...` il programma lo corregge da solo.

### Cosa viaggia (nei due sensi)

- **Prodotti**: nome, prezzo, IVA, giacenza, barcode, a peso, eliminazioni.
- **Clienti**: anagrafica, **codice cliente**, tessera, **compleanno**,
  P.IVA, punti, inviti.
- **Sconti temporanei** e sconti rimossi.
- **Scontrini** emessi fuori tavola e **registro attività**.
- **Regole di sconto**: offerte (le nove, con scadenze e prodotti), bundle,
  buoni, promo, referral, coupon di compleanno, **regole del Gratta&Vinci**.
- **Impostazioni del negozio**: reparti, fornitori, livelli fedeltà, punti
  doppi, limiti di sconto, consegna a domicilio, email automatiche e avvisi:
  quello che imposti da una parte vale anche dall'altra.
- **Buoni regalo** (importo, saldo, scadenza).
- **Appuntamenti**: le richieste di meeting dal sito.
- **Premi del Gratta&Vinci** vinti e ancora da ritirare.

Per ogni voce **vince la modifica più recente**, da qualunque parte sia stata
fatta; le eliminazioni viaggiano come "pietre tombali" così non vengono
ricreate.

### Il codice cliente vince sempre

Il **codice cliente** impostato nel tuo programma è la fonte: alla
sincronizzazione sostituisce quello scritto sul sito, e da quel momento vale
ovunque (cassa, pannello, area del cliente). Scrivendo il codice in cassa puoi
usare indifferentemente il codice cliente o il numero della tessera, con o senza
spazi e trattini.

### Il token

Il token permette **solo** di leggere e aggiornare i dati di negozio (clienti,
punti, prodotti, scontrini, regole, appuntamenti e premi); non dà accesso alla
cassa web, alle licenze o alle impostazioni del sito. Se lo rigeneri dal
pannello, aggiornalo nel programma.

---

## 13-bis. Ruoli con limiti e seconda cassa

### Ruoli con limiti

Oltre ai permessi (vendere, sconti, resi, resoconti…), ogni cassiere può avere
**due limiti numerici**:

- **sconto massimo** che può applicare (in percentuale);
- **importo massimo** di un singolo documento.

Vuoto o zero significa *nessun limite personale*. Se esiste anche il limite del
negozio (*Impostazioni → Limite di sconto*), vale sempre il più basso dei due.
L'amministratore non ha limiti. Quando un cassiere supera il suo limite la cassa
lo blocca e scrive perché: serve un amministratore per quella vendita.

### Seconda cassa con un codice

Per mettere due casse nello stesso negozio, anche su due PC o un tablet:

1. Nella dashboard apri **Casse collegate** e premi **+ Nuova postazione**: dai
   un nome (es. «Cassa 2 · bancone»), scegli **il cassiere** che la userà e
   salva. Compare un **codice di sei caratteri** (es. `MZ7G4P`).
2. Sull'altro dispositivo apri il POS web: nella schermata di accesso premi
   **🔗 Collega questa cassa con un codice**, digita il codice, **Controlla
   codice** e poi **Collega e apri la cassa**.
3. Quella postazione lavora **come quel cassiere**: stessi prodotti, prezzi,
   offerte, magazzino e scontrini, con i suoi permessi e i suoi limiti. In alto
   compare il nome della postazione (`🖧 Cassa 2 · bancone`).

La cassa si stacca subito se premi **Disattiva**, se generi un **nuovo codice**
o se cambi il cassiere collegato; **Elimina** toglie la postazione. La seconda
cassa non deve stare per forza sulla stessa rete: basta il codice, che è
personale come una chiave.

**Dal programma del negozio (versione Illimitato e versione con licenza).**
Nella barra in alto c'è **🖧 Casse collegate**: si apre l'elenco delle postazioni
con il codice, il cassiere e lo stato, e da lì puoi **creare** una cassa nuova
(nome + cassiere), **generare un nuovo codice**, **riattivare** o
**disattivare** una postazione — sono le stesse della dashboard, quindi quello
che fai qui si vede anche sul sito e viceversa.

Con **🔗 Collega questo PC** digiti il codice e *quel* computer diventa la
seconda cassa: in alto compare `🖧 Nome postazione · cassiere`, e valgono i
permessi e i limiti di quel cassiere (sconto massimo e importo massimo del
documento, controllati anche dal programma). **🚫 Scollega** riporta il PC a
cassa principale.

---

## 14. Backup

Tre livelli, tutti attivi di default:

1. **Backup locale** — in `BACKUP\`, all'apertura del programma e ogni 15
   minuti; i vecchi backup non vengono sovrascritti.
2. **Backup su Google Drive** — la prima volta che usi il pulsante
   **☁️ Collega Google Drive** il programma chiede il permesso e crea la
   cartella **AnDonio Market Backup** nel tuo Drive. Da quel momento salva una
   copia **all'apertura** e **ogni 15 minuti**, ognuna in una sottocartella
   nuova con giorno, mese, anno, ora, minuti e secondi (per esempio
   `27-10-2026_15-20-45`): nessun backup precedente viene mai sovrascritto.
   Si accende o spegne da **Impostazioni & Backup**.
3. **Backup sul sito** — una volta al giorno il programma carica sul sito lo
   stesso ZIP dei backup locali (mai il file `.env`). Dal pannello web, pagina
   **Backup**, si vede l'elenco con data, PC e dimensione: si può **Scaricare**
   un file, **Eliminare** o **Ripristinare** direttamente.

### Ripristino dal sito

Dalla pagina **Backup** premi **Ripristina** accanto al backup che vuoi
rimettere: la richiesta resta *in attesa del gestionale*. Al giro di
sincronizzazione successivo il programma del negozio scarica quel backup e lo
rimette al posto dei dati attuali — prima crea da solo una copia di sicurezza
dello stato corrente, quindi si può sempre tornare indietro — poi riferisce
l'esito alla dashboard (*completato* o *errore* con il motivo) e si chiude: va
riaperto per lavorare con i dati ripristinati. La richiesta si può annullare
dalla dashboard finché il gestionale non l'ha presa in carico.

---

## 15. Domande frequenti

**Ho dimenticato la password del pannello web.**
Serve il codice di recupero (in *Impostazioni → Cambia codice di recupero* del
programma) oppure scrivi all'assistenza.

**La cassa dice "Codice non trovato" quando scrivo il codice cliente.**
Adesso il codice si confronta ignorando spazi e trattini: scrivi `201307`,
`2013 07` o `20-13-07` e funziona. Se ancora non lo trova, controlla che il
cliente esista (anche dopo una sincronizzazione) e che quel codice sia davvero
il suo **Codice cliente**.

**Ho sbagliato il codice cliente sul sito.**
Correggilo nel programma (scheda *Clienti*): alla sincronizzazione successiva la
versione del programma vince.

**I prezzi nell'email delle offerte erano sbagliati.**
È stato corretto: adesso i prezzi sono formattati in centesimi in modo unico
(`€1,35 invece di €1,50`) e c'è un controllo automatico che impedisce il ritorno
dell'errore.

**Non vedo le richieste di meeting.**
Controlla che la sincronizzazione sia configurata (token) e premi **🔄 Aggiorna
dal sito** nella scheda *Appuntamenti*. I clienti devono essere registrati al
sito: senza account la richiesta non parte.

**Un cliente dice di aver grattato ma non vedo il premio.**
Nella scheda *Gratta&Vinci* premi **🔄 Aggiorna dal sito**: il premio appare in
*Premi vinti da ritirare*. Se il cliente ha vinto uno sconto, il codice è anche
un coupon: te lo mostrerà alla cassa e lo scanner lo applica da solo.

**Il gioco non fa vincere nessuno.**
Guarda la **probabilità di vincita** (per esempio 25 = 1 biglietto su 4), il
limite di **premi al giorno per cliente** e la **pausa dopo una vincita**: sono
le tre regole che riducono le vincite.

**Ho spostato il programma su un altro PC.**
Installa di nuovo, attiva la licenza (dopo averla fatta sbloccare) e usa
**Ripristina da file…** con l'ultimo backup.

---

## Supporto

Problemi, licenze, upgrade di versione: **andonio2013@gmail.com**

---

*In questo repository non sono pubblicate chiavi di licenza, dati dei clienti né
il codice sorgente del programma.*
