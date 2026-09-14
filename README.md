# La Fabbrica delle Meraviglie

Un gioco di tabelline per Nora e Amal: missioni da sei domande, un mix casuale, un percorso completo in ordine dall'1×1 al 10×10, quattro mini-giochi diversi, un laboratorio per creare collane, indizi visivi, lettura vocale facoltativa, nessun timer né penalità e progressi conservati sul dispositivo. Funziona su tablet, anche senza connessione dopo la prima visita quando il browser ha installato la modalità offline.

## Pubblicazione con GitHub Pages

1. Crea un repository GitHub, per esempio `tabelline-nora`.
2. Carica **tutti e cinque i file** di questa cartella nella radice del repository: `index.html`, `sw.js`, `manifest.webmanifest`, `app-icon.svg`, `README.md`.
3. Nel repository apri **Settings → Pages**. In **Build and deployment**, scegli **Deploy from a branch**, poi `main` e `/ (root)`, e salva.
4. Apri l'indirizzo che appare in Pages (di solito `https://TUO-NOME.github.io/tabelline-nora/`) dal tablet. Se vuoi un'icona nella schermata iniziale, usa la funzione **Aggiungi a schermata Home** del browser.

Non servono account, database, pacchetti o chiavi. Per cambiare il gioco basta modificare `index.html`. All'apertura si sceglie il profilo di Nora o Amal; stelle, missioni, collane, frasi e giro completo sono salvati separatamente nel `localStorage` dello stesso browser. I progressi esistenti di Nora rimangono nella chiave originale. Il pulsante con il nome in alto permette di cambiare giocatrice. «Ricomincia da zero» cancella solo il profilo selezionato. I progressi restano nel browser di quel tablet, non su GitHub e non si sincronizzano fra dispositivi. GitHub Pages pubblica il codice e rende il gioco accessibile a chi conosce il link; non inserire dati privati nel repository.

## Come funziona l'apprendimento

Il gioco suggerisce prima le tabelline 2, 5 e 10 e poi le altre, ma ciascuna può scegliere liberamente. I punti di avanzamento di un fatto aumentano quando lo trova al primo tentativo senza indizi né costruzioni guidate; una risposta con aiuto dà comunque una stella. La missione termina dopo sei risposte trovate, senza scadenze.

Per ogni profilo, i messaggi di incoraggiamento cambiano dopo le risposte, i tentativi, le missioni e le tabelline completate. Le frasi ruotano senza ripetersi finché ciascun gruppo non è stato mostrato interamente; la rotazione riprende anche se si chiude e si riapre il gioco. Usare un indizio riceve un messaggio positivo dedicato.

Ogni mondo usa una meccanica diversa: nell'**Atelier delle gemme** si montano ciondoli da un certo numero di gemme e si digita il totale; nel **Prato degli unicorni** si fanno salti di una quantità fissa sulle nuvole e si sceglie la destinazione; sul **Palco delle stelle** si accendono battute di luci e si digita il totale; nella **Giungla delle tigri** si cerca il numero di piste a partire dal totale delle impronte. Le costruzioni sono facoltative per chi ricorda già il risultato. Gli indizi mostrano gruppi e addizioni ripetute usando simboli diversi in ciascun mondo. Il laboratorio permette di aggiungere e togliere gemme da una collana di otto elementi; le ultime tre gemme si sbloccano con le prime tre missioni. Nella sezione «I miei progressi» si possono vedere i risultati, attivare una modalità più calma e azzerare i dati con conferma.

**Mix sorpresa** propone sei moltiplicazioni scelte tra tutte le tabelline. **Il giro completo** propone le 100 moltiplicazioni in ordine: 1×1, 1×2, …, 10×10. La giocatrice inserisce il risultato con grandi tasti numerici, senza poter scegliere fra risposte già scritte. Si può fare una tabellina da dieci domande per volta, fermarsi in qualsiasi momento e riprendere sullo stesso dispositivo. Nella sezione «I miei progressi» il rapporto distingue le risposte immediate senza indizi da quelle trovate con aiuto o dopo un tentativo errato, e indica quali prodotti ripassare. Un giro unico non è un test diagnostico né una misura definitiva delle sue conoscenze. Rifare il giro sostituisce solo il rapporto precedente; le stelle e le missioni restano.

Per una verifica locale, avvia `python3 -m http.server 8000` in questa cartella e apri `http://localhost:8000`.
