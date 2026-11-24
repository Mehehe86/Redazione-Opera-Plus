# Opera+ — Procedura redazionale per le schede dei cantanti (v1)

## A che cosa serve la scheda
La scheda deve permettere al giornalista di ritrovare **tutti i ruoli documentati** di un cantante e, quando le fonti lo consentono, **in quale teatro e in quale città** ogni ruolo è stato interpretato. Va alimentata progressivamente durante il normale lavoro giornalistico. Non è necessario registrare tutte le date di recita, i cast, gli altri interpreti, le coppie artistiche o le collaborazioni ricorrenti. Non introdurre collegamenti a Opera+ Atlas.

Il tracciato tecnico si trova in `schemi-json/artista-cantante.schema.json`. L'esempio di compilazione, interamente fittizio, è in `esempi-archivio/artista-cantante-esempio.json`.

## 1. Cercare la persona giusta
Prima di creare una scheda verifica se ne esista già una, cercando nome professionale e possibili varianti. Per gli omonimi confronta biografie, professione, formazione e fonti ufficiali: non fondere due persone sulla base del solo nome, della città o del settore di lavoro. In caso di dubbio mantieni schede separate e una nota di omonimia. Non raccogliere indirizzi privati o altri dati personali irrilevanti.

## 2. Ricostruire biografia e repertorio
Consulta anzitutto i siti degli artisti, dei teatri e dei festival, i programmi di sala e gli archivi; integra, quando utili, agenzie, interviste e testate giornalistiche attendibili. Collega le affermazioni su formazione e incarichi alle fonti utilizzate. Una biografia discorsiva deve essere una sintesi di fatti verificabili, non un testo riempito di informazioni plausibili.

Registra **ogni combinazione opera–compositore–personaggio una sola volta**. Se il soprano ha interpretato Gilda in più città, non duplicare la voce Gilda: aggiungi le esperienze sotto lo stesso ruolo. Conserva tutti i ruoli che riesci a documentare, anche se non pertinenti all'articolo del momento. Non devi però ricostruire una carriera completa prima di completare ogni incarico.

## 3. Distinguere i ruoli interpretati da quelli annunciati
Non supporre che «in repertorio» significhi «già interpretato pubblicamente». Talvolta le biografie includono ruoli studiati, disponibili o futuri.

Usa `interpretato` quando una fonte documenta un'esecuzione effettivamente avvenuta. Usa `annunciato` per una partecipazione programmata non ancora confermata come realizzata. Usa `in_preparazione` per un ruolo che l'artista dichiara di stare studiando; usa `repertorio_dichiarato_non_verificato` quando non puoi stabilire se sia stato cantato. Non convertire automaticamente un annuncio in interpretazione soltanto perché la data è trascorsa.

`stato_documentato` descrive la condizione complessiva del ruolo in base alle prove disponibili. Le esperienze mantengono ciascuna il proprio `stato`, quindi sotto un ruolo già interpretato possono comparire anche impegni futuri soltanto annunciati. Per una preparazione o un repertorio genericamente dichiarato senza teatro accertato, conserva il ruolo, le fonti e una nota, lasciando vuoto l'elenco delle esperienze.

## 4. Registrare teatro e città
Per ogni esperienza documentata registra il **nome del teatro**, la **città in cui si trova** e il **Paese**, oltre all'anno quando noto. Il Teatro Regio di Torino e il Teatro Regio di Parma non sono la stessa istituzione: un nome apparentemente riconoscibile non basta.

Se il cantante è documentato nel ruolo ma il teatro è sconosciuto, puoi registrare il ruolo senza inventare il luogo. Se un'esperienza ha teatro conosciuto, la città è obbligatoria; viceversa una città da sola può essere conservata quando la fonte non precisa la sede. Non confondere il luogo che ha ospitato la rappresentazione con il soggetto che l'ha prodotta. Non inventare anni o teatri per completare i campi.

Le date esatte delle recite non sono richieste, e non serve ricostruire i cast.

## 5. Conservare la prova di ciascuna informazione
Ogni ruolo e ogni esperienza devono rimandare ad almeno una fonte tramite `fonti_ids`. Gli identificativi devono corrispondere a voci effettivamente presenti in `fonti`. Usa preferibilmente il collegamento diretto alla pagina o al documento, non la homepage del teatro. Conserva data di consultazione e una frase nel campo `attesta` che dica **esattamente che cosa la fonte dimostra**.

Esempio: un programma di stagione preliminare prova che una cantante è stata *annunciata* nel cast, non che abbia effettivamente cantato. Una biografia può attestare che ha interpretato Gilda senza documentare il teatro; conserva allora il ruolo, ma non inventare la sede. Per scrivere che un artista debutta assolutamente in un ruolo non basta che quel ruolo sia assente dal nostro archivio.

## 6. Aggiornare senza perdere informazioni
Quando emerge una nuova fonte, cerca prima il ruolo già registrato e controlla se l'esperienza sia nuova o già documentata. Aggiungi teatri e anni verificati senza creare doppioni. Se un annuncio viene annullato o il cantante viene sostituito, conserva la storia documentaria con una nota e lo stato appropriato: non registrare una recita non avvenuta.

Se una nuova fonte corregge un dato errato, descrivi il cambiamento e lascia che la cronologia di GitHub ne mantenga traccia. Le informazioni non accertate restano esplicitamente incerte, senza essere trasformate in fatti. «Non risulta nella nostra scheda» non significa «non è mai successo».

## 7. Approvare e verificare
Prima di scrivere nell'archivio condiviso, sottoponi al redattore le proposte di creazione e modifica, indicando esattamente i dati aggiunti o corretti e le loro fonti. Dopo l'approvazione, verifica che il file sia JSON valido e conforme allo schema, che ogni `fonti_ids` faccia riferimento a una fonte reale, che non siano duplicati ruoli o esperienze e che ogni teatro noto abbia una città esplicita.

Il giornalista potrà poi utilizzare la scheda per selezionare le informazioni pertinenti a un articolo o a un'intervista, controllando le fonti prima di riportare affermazioni importanti. Non deve trasformare l'intero repertorio in un elenco da inserire automaticamente negli articoli.
