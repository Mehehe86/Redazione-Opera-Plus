# Opera+ — Procedura per le schede degli allestimenti lirici (v1.0)

## Scopo e criterio di identificazione
La scheda documenta **una specifica realizzazione scenica di un'opera**, dal momento in cui nasce alle successive riprese. Non confonderla con l'opera musicale e letteraria in sé: *Rigoletto* di Verdi ha una scheda come opera, mentre ogni differente progetto di regia ha una propria scheda di allestimento.

Non creare automaticamente una nuova scheda perché un teatro ripropone la stessa regia, perché cambiano cantanti o direttore d'orchestra o perché una produzione torna dopo alcuni anni. Viceversa, due regie differenti della stessa opera vanno tenute separate, anche quando appartengono allo stesso regista. L'identità di un allestimento deve derivare da comunicati, crediti, coproduzioni, descrizioni e documenti verificati, non dalla sola coincidenza di titolo e regista.

Lo schema si trova in `schemi-json/allestimento-lirico.schema.json`; il file `esempi-archivio/allestimento-lirico-esempio.json` è integralmente fittizio e serve soltanto a testare il formato.

## 1. Parti dai materiali ufficiali e ricostruisci l'origine
Cerca schede del teatro, comunicati stampa, programmi di sala, dossier di produzione, interviste e materiali visivi ufficiali. Individua l'opera, il compositore, il regista e gli altri responsabili. Cerca l'indicazione «nuovo allestimento», «ripresa», «coproduzione» o il riferimento a un precedente debutto: queste formule sono indizi importanti, ma verifica **quale produzione precisa** si stia indicando.

Cerca poi l'origine dell'allestimento: teatro, città, anno o stagione della prima presentazione **della regia**, non della prima assoluta dell'opera. Se la data di origine non è documentata, registra il dubbio anziché inventare la prima.

Non confondere il soggetto produttore con il luogo in cui l'allestimento è stato rappresentato. Se esistono coproduttori documentati, registrali nell'elenco separato `coproduttori`.

## 2. Conserva ogni ripresa documentata, senza censire le singole recite
Nel campo `presentazioni` registra ogni serie documentata di rappresentazioni in un teatro e in una stagione, identificando **teatro, città e Paese**, anno o stagione. Un allestimento nato al Teatro Regio di Torino e ripreso al Teatro Regio di Parma non deve essere confuso in un'unica sede. Se la produzione torna nello stesso teatro in anni differenti, le esperienze devono restare distinguibili.

Non occorre archiviare tutte le date di recita né i singoli cast. Quando una sede non è documentata, conserva la città o il festival se disponibile e indica nelle note ciò che manca. Non inferire un edificio specifico dalla sola denominazione di un festival.

Distingui presentazioni `realizzata`, `annunciata`, `annullata` o `da_verificare`. Una pagina di stagione prova che una ripresa è prevista, non che abbia avuto luogo. Quando ricevi una conferma successiva, aggiorna lo stato conservando la tracciabilità delle fonti.

## 3. Crediti artistici: attribuzioni precise
Registra i responsabili della creazione originaria con **incarico e nome**, per esempio regia, scene, costumi, luci, video, coreografia o drammaturgia. Non attribuire automaticamente tutte le scelte scenografiche al regista. Se in una ripresa cambiano il responsabile del riallestimento o componenti artistiche, annota i `crediti_specifici` della presentazione e, quando documentate, le `variazioni_documentate`.

La direzione musicale di una singola serie e i cantanti non definiscono necessariamente l'identità della regia. Non costruire un elenco di cointerpreti o di collaborazioni ricorrenti. Registra un direttore soltanto quando abbia un ruolo pertinente al progetto da descrivere e non dedurre che abbia partecipato a tutte le riprese.

## 4. Descrivi ciò che è verificabile, senza scrivere la recensione al posto del recensore
Consulta le note di regia, le interviste, le fotografie e i video, distinguendo le caratteristiche riscontrabili dalle intenzioni dichiarate. La frase «il regista vuole evidenziare il rapporto fra potere e violenza» è un'intenzione **attribuita al regista**, non una dimostrazione dell'efficacia della messinscena.

Per ogni elemento importante registra una descrizione concreta e l'identificativo della fonte. Evita aggettivi valutativi automatici come «straordinario», «originale» o «commovente». Quando la produzione cambia per ragioni di spazio o riallestimento, distingui quali caratteristiche appartengono alla versione rappresentata in un determinato teatro.

## 5. Ricostruisci la ricezione critica senza appiattirla
Se la produzione è già stata rappresentata, cerca le recensioni specifiche di quello stesso allestimento. Consulta fonti indipendenti, anche in lingue diverse quando la produzione ha una storia internazionale. **Cerca giudizi favorevoli e rilievi critici**, ma non inventare un dissenso dove le fonti non ne mostrano.

Per ciascuna osservazione conserva autore, testata, data se disponibile, teatro e città della recita recensita, aspetto esaminato e sintesi del giudizio **attribuito al critico**, insieme all'ID della fonte precisa. Non presentare come giudizio di Opera+ la combinazione delle opinioni di altri giornalisti.

Una critica a un cantante o a un direttore di una particolare recita **non va trasferita a tutte le riprese della stessa regia**. Per il dossier preparatorio di una recensione, privilegia gli elementi riguardanti la messinscena e segnala chiaramente quando le valutazioni musicali dipendono da cast e direzione differenti.

Se lo spettacolo deve ancora debuttare, non fingere l'esistenza di recensioni precedenti di quell'allestimento: puoi documentare il lavoro precedente del regista, precisando che si tratta di altre produzioni.

## 6. Fonti e incertezze
Ogni affermazione strutturata importante deve avere un `fonti_ids` coerente con l'elenco `fonti`; per la ricezione critica è previsto un `fonte_id`. Registra titolo, URL diretto, data di consultazione e nel campo `attesta` l'esatta informazione provata. Non limitarti a rinviare alla homepage di un teatro quando la pagina del singolo spettacolo è disponibile.

Quando trovi due produzioni con il medesimo titolo e lo stesso regista, **non unirle finché non hai una prova della loro identità**. Se le fonti sono ambigue, conserva separatamente i dati verificati e segnala il dubbio in `nota_identificazione`. Un cast differente, da solo, non prova né nega che sia la stessa regia. Se una fotografia sembra simile a quella di un altro allestimento, non assumerne l'identità soltanto sulla base delle immagini.

Non affermare che un documento o video sia pubblicamente accessibile senza averne verificato il collegamento.

## 7. Come utilizzare la scheda nella redazione
Per preparare la recensione di uno spettacolo ancora da vedere, il giornalista deve partire dai materiali ufficiali e dalle precedenti recensioni **dello stesso allestimento**, quando esistono. Produce un dossier che spiega cosa osservare, perché e su quali fonti si basa, senza anticipare il giudizio del recensore. Questa procedura integra, ma non sostituisce, le istruzioni della Parte 4 del Manuale editoriale.

Per un articolo di presentazione, utilizza le informazioni pertinenti: la storia della regia, il debutto, le riprese, la concezione artistica e gli eventuali cambiamenti. Non trasferire automaticamente nella notizia tutte le annotazioni della scheda.

## 8. Come mostrare e aggiornare la scheda
Quando il redattore chiede la scheda completa, presenta anzitutto l'identità dell'allestimento, i responsabili, la prima documentata e le caratteristiche dichiarate. Segui con **una cronologia sintetica di tutte le presentazioni documentate**, dal passato al futuro, una riga per stagione o ripresa: `ANNO O STAGIONE – OPERA – REGIA – TEATRO – CITTÀ`. Contrassegna gli eventi annunciati e le origini incerte. La cronologia non deve essere confusa con le singole date di recita.

Le recensioni precedenti, quando richieste o utili per preparare un dossier, vanno presentate con fonte e motivazione delle osservazioni, non soltanto con etichette «positivo» o «negativo». La forma di lettura non modifica il JSON conservato.

Prima di salvare una scheda nell'archivio condiviso, mostra i dati e le fonti al redattore per approvazione. Controlla che non esistano duplicati, che l'opera sia identificata correttamente, che teatri e città siano accoppiati, che la distinzione fra annunci e rappresentazioni realizzate sia mantenuta e che gli ID delle fonti siano risolti. La scheda cresce progressivamente e non deve essere dichiarata completa senza una ricerca adeguata.
