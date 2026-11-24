# Opera+ — Procedura per le schede delle opere liriche (v1.0)

## A che cosa serve la scheda
La scheda di un'opera lirica è un riferimento storico-editoriale per il giornalista AI. Contiene informazioni verificabili sull'opera, indipendenti da una rappresentazione particolare: titolo, autori, prima rappresentazione, libretto, personaggi, versioni, contesto storico e riferimenti utili. Non è una cronologia di recite, una scheda dei cast o una guida all'ascolto da preparare obbligatoriamente. Il giornalista la usa per orientarsi, poi verifica sulle fonti i fatti importanti prima di pubblicarli.

Il formato è in `schemi-json/opera-lirica.schema.json`. L'esempio tecnico in `esempi-archivio/opera-lirica-esempio.json` è **interamente inventato** e non deve essere usato per scrivere articoli.

## 1. Individua l'opera giusta
Prima di creare un file, cerca eventuali schede esistenti, includendo titoli alternativi, traduzioni e grafie storiche. Non fondere due opere soltanto perché condividono un titolo o un soggetto: confronta compositore, librettista, prima rappresentazione e versioni. Identifica chiaramente il titolo di riferimento e le eventuali denominazioni alternative.

Cerca e verifica compositore o compositori, librettista o librettisti, genere (se documentato), lingua del libretto, struttura in atti, parti o quadri e fonti letterarie. Non trasformare una definizione critica successiva in una categoria che gli autori abbiano usato senza prova.

## 2. Documenta la prima rappresentazione
Consulta fonti autorevoli e individuabili: archivi teatrali, istituzioni musicali, cataloghi scientifici, edizioni critiche, libri e studi musicologici. Verifica data, **nome del teatro e città**, e Paese. Distinzione essenziale: la prima assoluta dell'opera non coincide necessariamente con la prima della versione riveduta o con la prima in un Paese.

Se manca un dato, lascia il campo a `null`, spiegando il limite, anziché completarlo per plausibilità. Se le fonti divergono su una data o sull'identificazione del teatro, registra il dubbio e ricontrolla prima di approvare.

## 3. Consulta il libretto e ricostruisci i personaggi
Per personaggi, registro vocale, ambientazione e vicenda, individua un libretto attendibile e identifica la versione alla quale si riferisce. Quando le fonti divergono tra edizioni, non correggere silenziosamente una con l'altra: indica a quale versione appartiene ogni dato.

Scrivi una sinossi breve, aderente agli avvenimenti. Non inserire automaticamente giudizi sul carattere dei personaggi o interpretazioni psicologiche non sostenute dal testo. Se sono rilevanti, conserva queste letture come **interpretazioni attribuite** a fonti precise, non come fatti incontrovertibili.

## 4. Distingui le versioni storiche dalle scelte di allestimento
Alcune opere hanno versioni autorizzate o revisioni sostanziali che incidono su struttura, musica, testo o personaggi. Registra le versioni note e documentate, con denominazione, anno quando accertato, differenze principali e fonti. Non moltiplicare le versioni a partire da un taglio occasionale di un direttore o di una singola produzione.

Quando prepari un articolo su uno spettacolo specifico, accerta quale versione venga eseguita; la scheda dell'opera non dimostra da sola quale materiale abbia utilizzato un determinato teatro.

## 5. Raccogli solo contesto utile e verificabile
Quando la ricerca ne offre l'occasione, conserva circostanze della composizione, vicende censorie, rapporti con la fonte letteraria, revisioni, particolarità musicali e osservazioni drammaturgiche che aiutano a comprendere l'opera.

Non trasformare però ogni scheda in un'enciclopedia e non riempirla di formule generiche. Distingui **documentazione** (un fatto attestato da libretto, partitura o documento storico) e **interpretazione attribuita** (lettura di uno studioso o di un critico). Per le interpretazioni specifica autore, opera o pubblicazione e riferimento verificabile.

Le note musicali tecniche sono materiale di riferimento: il giornalista non deve inserirle automaticamente nel parlato, negli articoli o nelle interviste. Se il redattore chiede una ricerca musicale o letteraria approfondita, svolgila con fonti specifiche anziché fingere che la scheda breve ne esaurisca il contenuto.

## 6. Link alle fonti e alle risorse
Per ogni fonte conserva il titolo, l'URL diretto, la data di consultazione e la descrizione esatta di **che cosa attesta**. Collega i dati puntuali agli identificativi delle fonti pertinenti. Le liste di personaggi, le versioni, i fatti di contesto e le note interpretative devono avere i rispettivi `fonti_ids`.

Se è utile conservare un libretto, una partitura, un'edizione critica o uno studio, registra il collegamento alla risorsa verificata. Prima di dichiarare che il documento è consultabile o scaricabile, controlla davvero la pagina di destinazione e le condizioni di accesso. Un catalogo che descrive un'edizione non equivale a un PDF liberamente disponibile.

Se una fonte non è più accessibile, non sostituirla silenziosamente con una fonte generica: segnala la necessità di nuova verifica.

## 7. Aggiorna progressivamente senza inventare
Una scheda può nascere parziale e crescere durante il normale lavoro redazionale. Non è necessario completare ogni approfondimento per scrivere un breve articolo, ma non definire «completa» una scheda che conserva soltanto dati di base.

Prima di aggiungere informazioni cerca se siano già presenti, controlla l'attendibilità delle nuove fonti e segnala le divergenze. Presenta al redattore le modifiche proposte e i relativi riferimenti prima di scriverle nell'archivio condiviso. Dopo l'approvazione controlla che il JSON rispetti lo schema e che ogni ID di fonte richiamato esista realmente.

## 8. Presentazione al redattore
La scheda delle opere **non segue il formato cronologico continuo delle schede dei cantanti**: non contiene la carriera di un artista né il calendario delle rappresentazioni.

Quando viene richiesta una consultazione generale, presenta in modo leggibile l'identità dell'opera e i suoi dati essenziali, una breve sinossi e, quando utili, versioni documentate e informazioni di contesto. Se il redattore chiede soltanto una data, il libretto o la differenza fra due versioni, rispondi direttamente alla domanda usando la parte pertinente della scheda e le relative fonti.

Non trasferire automaticamente ogni informazione della scheda in un articolo: seleziona ciò che serve alla notizia e verifica ciò che utilizzi.
