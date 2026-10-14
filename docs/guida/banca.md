[Indice della guida](README.md) · [Presentazione](../../README.md) · [Scarica il setup](https://github.com/brn78/BlackHole-Workspaces/releases/latest)

# <a id="banca"></a>Banca

**Azienda → Banca** (dalla 1.119.0) tiene i **conti correnti** con il saldo e i **movimenti** importati dagli estratti conto, e li **abbina** agli incassi delle fatture emesse e ai pagamenti delle fatture dei fornitori. Va bene per qualunque banca: il file si scarica dall'internet banking nel formato che c'è. La pagina compare a chi ha *Vedere la banca* o *Importare e abbinare i movimenti*; per abbinare gli incassi serve anche *Gestire le vendite*, per i pagamenti *Pagare le fatture dei fornitori*. Sono dati riservati.

## <a id="banca-conti"></a>I conti

- **Nuovo conto**: il nome, l'**IBAN** (controllato), la banca e il BIC, il **saldo iniziale** con il suo giorno. Senza conti, la pagina propone quelli scritti nei dati dell'azienda.
- Con la [contabilità](contabilita.md) attiva si sceglie il suo conto di banca: gli incassi e i pagamenti abbinati vanno lì, e la prima nota segue da sola.
- Per le [distinte](#banca-distinte) (dalla 1.120.0) il conto tiene anche i codici che dà la banca: il **codice SIA** (5 caratteri, per le RiBa), il **CUC** (8 caratteri, se la banca lo chiede nei file SEPA) e il **codice creditore SEPA** (per gli addebiti diretti). Si scrivono quando la banca li comunica: finché mancano, la distinta di quel tipo dice che cosa serve e non si crea.
- Il **saldo** è il saldo iniziale più i movimenti importati; se il file della banca scrive il saldo (una colonna Saldo, o il saldo finale del CAMT) si vede accanto, in rosso se non torna: vuol dire che manca un pezzo di estratto conto. Un conto chiuso si **archivia**; eliminato, va nel [cestino](cestino.md) con i suoi movimenti (gli incassi e i pagamenti registrati restano).

## <a id="banca-importare"></a>Importare l'estratto conto

- **Importa l'estratto conto**, scegli il conto e il file: **Excel** (.xlsx, .xls, .ods), **CSV** o **CAMT XML** (camt.053 o camt.052, l'«estratto conto CBI XML» delle banche italiane). Fino a 5.000 movimenti per volta.
- Nei fogli si sceglie la **riga con i nomi delle colonne** (proposta da sola: molte banche scrivono sopra la tabella il conto, il periodo, i saldi) e **che cosa c'è in ogni colonna**: la data, l'importo con il segno oppure le uscite e le entrate in due colonne (Dare e Avere), oppure l'importo con una colonna del segno (D/C, +/−); poi la descrizione, la causale, l'ordinante o il beneficiario, il suo IBAN, il riferimento, il saldo. Con l'assistente attivo, **Proponi con l'assistente** le sceglie lui. L'anteprima mostra le prime righe con entrate e uscite: controlla i segni.
- La scelta delle colonne si **ricorda per il conto**: la volta dopo, con lo stesso tipo di file, si va avanti e basta. Gli importi si leggono anche con il punto delle migliaia e la virgola dei decimali, con il meno in fondo o tra parentesi; le date anche come «12 ott 2026». Le righe senza data (totali, saldi in fondo) si saltano.
- **Controlla** dice quanti movimenti sono nuovi e quanti erano già stati importati: due estratti conto che si sovrappongono non fanno doppioni (due movimenti uguali nello stesso file restano due). Se l'IBAN del CAMT non è quello del conto, avvisa.
- Nella linguetta **Importazioni** ogni file resta con il periodo e i numeri; **Annulla l'importazione** toglie i suoi movimenti ancora da abbinare.

## <a id="banca-abbinare"></a>Abbinare i movimenti

- La linguetta **Da abbinare** mostra per ogni movimento la **proposta** migliore: le entrate con le rate delle fatture emesse, le uscite con quelle delle fatture dei fornitori. Contano l'importo uguale alla rata, il **numero della fattura** nella descrizione («FT 12», «fattura n. 12», «12/2026»), la **partita IVA** o il codice fiscale, l'**IBAN** della controparte (quello del cliente o della fattura del fornitore), il **nome**, la scadenza vicina. Si propongono anche **più rate** dello stesso cliente pagate con un bonifico solo e gli incassi o i pagamenti **già registrati a mano** con lo stesso importo.
- **Abbina** registra l'incasso (o il pagamento) con il giorno del movimento e la nota «Dalla banca»: la fattura risulta incassata, il recupero crediti e la contabilità lo vedono. Una proposta con l'importo uguale e il numero della fattura, la partita IVA o l'IBAN, senza altre vicine, è **sicura** (lo dice la parola in verde davanti alla proposta): **Abbina quelli sicuri** le fa tutte da sola. Nelle righe senza proposta **Cerca…** apre il movimento sulla ricerca a mano; dal menu della riga anche **Segna non da abbinare…**. Se un movimento senza proposte **sembra** una spesa, una commissione, un F24, un giroconto, uno stipendio o un prelievo (dalle parole della banca, oppure perché uno uguale o della stessa controparte è già stato segnato) la riga lo dice, con **Non da abbinare…** che apre il movimento con la categoria già scritta; **Segna le spese riconosciute** (in **Altro**) li segna tutti insieme, dopo la conferma con il conto per categoria (dalla 1.125.0). Il saldo in alto è quello **degli estratti conto**; quello della contabilità è nella Home. Nelle finestre più strette entrate e uscite stanno in una colonna sola, **Importo**, con il segno.
- Un clic sul movimento apre la sua scheda: tutte le proposte con il perché, **Cerca a mano** (una o più rate, anche con un importo diverso: un acconto o un bonifico che paga in parte) e **Non da abbinare** per quello che non riguarda fatture (spese bancarie, giroconti, F24, stipendi, prelievi) con la categoria, che poi si ripropone.
- Due movimenti che si annullano (un **giroconto** tra due conti, un **insoluto** o uno **storno** che riporta indietro un accredito) si propongono insieme: **Compensa** li abbina l'uno all'altro senza registrare incassi o pagamenti. La proposta è più forte se la descrizione dice insoluto, storno o giroconto, se i conti sono due e se i giorni sono vicini.
- **Togli l'abbinamento** toglie gli incassi e i pagamenti registrati dall'abbinamento; quelli che c'erano già restano. La linguetta **Movimenti** li mostra tutti, con i filtri per entrate, uscite, abbinati e non da abbinare.

## <a id="banca-distinte"></a>Distinte: RiBa, addebiti SEPA e bonifici ai fornitori

Una **distinta** (dalla 1.120.0) mette in un file solo le rate da presentare alla banca: si carica nell'home banking invece di scriverle una per una, e quando arriva l'accredito (o l'addebito) il movimento si abbina alla distinta intera.

- **Distinte → Nuova distinta** e il tipo:
   - **RiBa**: le rate delle fatture emesse con il metodo RIBA (MP12). Il file è il tracciato **CBI** delle ricevute bancarie. Servono il codice SIA nel conto, la **banca d'appoggio** del cliente (il suo IBAN italiano nella scheda del cliente), l'indirizzo e la partita IVA o il codice fiscale nella fattura.
   - **Addebito SEPA**: le rate con il metodo SDD (MP19) dei clienti con il **mandato** firmato. Il file è l'XML SEPA (pain.008) con il codice creditore del conto; il primo addebito di un mandato va come FRST, i successivi come RCUR, da soli.
   - **Bonifici ai fornitori**: le rate da pagare delle fatture dei fornitori con l'IBAN (non le note di credito né i contanti, gli assegni e le RiBa del fornitore). Il file è l'XML SEPA dei bonifici (pain.001).
- Si sceglie il periodo delle scadenze (per gli addebiti e i bonifici anche il **giorno** in cui la banca deve eseguirli) e si spuntano le rate. Quelle con qualcosa che manca si vedono in grigio con il motivo: si sistema la scheda del cliente, la fattura o il mandato e si riapre. Una rata già in una distinta non si ripropone.
- Nella scheda della distinta: **Scarica il file**, caricalo nell'home banking, poi **Segna presentata**. Una distinta ancora da presentare si può **eliminare** (le rate tornano libere); una già abbinata no.
- Quando arriva il movimento con il totale della distinta, in **Da abbinare** si propone la distinta intera (sicura se la descrizione parla di RiBa, SDD o effetti): **Abbina** registra l'incasso o il pagamento di ogni rata e chiude la distinta. Togliendo l'abbinamento la distinta torna presentata.
- Una rata che torna indietro: nella distinta **Insoluto** toglie il suo incasso (la fattura torna da incassare e il [recupero crediti](crediti.md) la vede) e lo scrive nella storia della fattura. Il movimento dell'insoluto nell'estratto conto si abbina con **Compensa** o si segna *Non da abbinare* (le spese).

## <a id="banca-mandati"></a>I mandati SDD

- La linguetta **Mandati SDD** tiene i mandati firmati dai clienti: il cliente, l'**IBAN** da addebitare (controllato), il **riferimento** del mandato (unico, fino a 35 caratteri), il giorno della **firma**, lo schema (**CORE** per tutti, **B2B** solo tra imprese) e lo stato.
- Un mandato **revocato** non si propone più nelle distinte; uno già usato in una distinta non si elimina, si revoca. L'*ultimo addebito* dice se il prossimo sarà il primo (FRST) o uno dei successivi (RCUR).

---

[← Mezzi e attrezzature](mezzi.md) · [Indice](README.md) · [Contabilità →](contabilita.md)
