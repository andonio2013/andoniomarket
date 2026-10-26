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
