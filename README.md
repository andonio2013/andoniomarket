# AnDonio Market

**Gestionale di cassa per negozi** — funziona su Windows, senza installare Python e senza Internet (tranne la prima attivazione della licenza).

Cassa, catalogo prodotti, magazzino, clienti e punti fedeltà, scontrini in PDF, backup automatici: tutto in un unico programma.

---

## Download

| File | A cosa serve |
|---|---|
| **[AnDonioMarket_Setup.exe](https://github.com/andonio2013/andoniomarket/raw/main/AnDonioMarket_Setup.exe)** — 94 MB | Installer per Windows — **consigliato**. Installa il programma per l'utente corrente (non servono permessi di amministratore), crea i collegamenti nel menu Start e sul Desktop e, se trova una cartella con i dati di AnDonio Market, può importarli. |
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
