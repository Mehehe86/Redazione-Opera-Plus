# Opera+ — Procedura per le schede dei teatri, dei festival e delle istituzioni musicali (v1.0)

## A che cosa serve
La scheda è un riferimento giornalistico essenziale e documentato sull'identità, la storia, la sede e il campo di attività di un teatro, di un festival o di un'organizzazione musicale. Serve a evitare errori di denominazione, città e ricostruzione storica nella preparazione di notizie, interviste e recensioni. **Non è una copia del programma delle stagioni, un catalogo di tutti gli artisti o una banca dati dei singoli spettacoli.**

Il modello è in `schemi-json/teatro-festival.schema.json`. L'esempio fittizio si trova in `esempi-archivio/teatro-festival-esempio.json`.

## 1. Identifica senza ambiguità
Prima di creare una scheda, cerca nomi equivalenti e schede già presenti. Controlla sempre nome ufficiale, città e Paese: «Teatro Regio» da solo non distingue Torino da Parma. Accerta l'eventuale presenza di nomi storici, variazioni di denominazione o traduzioni del nome; registra soltanto varianti documentate.

Per i festival, distingui nome della manifestazione, città o territorio di riferimento e organizzazione promotrice. Non presumere che il nome dell'evento coincida con quello dell'ente organizzatore.

## 2. Distingui istituzione, organizzazione e sede
Un teatro può avere una storia istituzionale più lunga dell'edificio attuale. Un festival può utilizzare più sale, cambiare luogo nel tempo oppure svolgersi in diversi comuni. **Non trasformare automaticamente la sede dell'istituzione nel luogo di ogni spettacolo.**

Nel campo `soggetto_gestore` inserisci, quando verificato, il nome dell'organizzazione. Nel campo `sedi` registra i luoghi fisici documentati, con nome, città, Paese ed eventuale indirizzo pubblico. Ogni sede è classificata come attuale, storica, occasionale o da verificare; se i dati sono incompleti, non inventare indirizzi o luoghi.

Se l'istituzione è stata fondata in una data e l'edificio attuale inaugurato in un'altra, **conserva separatamente i due fatti** nella storia. Non indicare l'anno di ricostruzione come anno di fondazione.

## 3. Verifica la storia senza accumulare cronologie inutili
Parti dal sito ufficiale, dalla sezione «storia» e dai documenti istituzionali. Integra archivi pubblici, siti di enti territoriali, cataloghi di architettura, pubblicazioni scientifiche e altre fonti affidabili quando servono a chiarire un passaggio.

Registra i principali snodi accertati, per esempio fondazione, inaugurazione del primo edificio, incendio, chiusura, trasferimento, apertura della nuova sede o trasformazione istituzionale. Per ogni evento storico conserva la data o il periodo come riportato dalla fonte e una spiegazione sintetica. Non moltiplicare dettagli che non aiuterebbero una redazione a raccontare l'istituzione.

Se fonti autorevoli offrono cronologie o denominazioni differenti, approfondisci e segnala il dubbio prima di archiviare una versione come certa.

## 4. Descrivi le attività senza confonderle con il cartellone
Indica le forme di attività continuative documentate: opera, balletto, concerti, formazione, produzioni per famiglie, attività educative e così via. Per un festival registra la disciplina, le caratteristiche riconoscibili della manifestazione e l'eventuale periodicità, soltanto se verificata.

Non registrare in questa scheda cast, titoli di singole stagioni o un calendario esaustivo. Eventuali incarichi attuali dei vertici o informazioni organizzative mutevoli devono essere ricontrollati per ciascun articolo; non trasformarli in attributi storici permanenti.

## 5. Conserva le fonti e ciò che dimostrano
Registra per ciascuna fonte titolo, URL preciso, data di consultazione e un'indicazione esatta di ciò che documenta. Collega ogni sede, attività e passaggio storico alle fonti con `fonti_ids`. Se una scheda ufficiale documenta il teatro come luogo fisico, non dedurre da essa automaticamente chi lo gestisse in epoche precedenti.

Distingui dati verificati, interpretazioni e formulazioni promozionali. Non prendere per certo un primato dichiarato da una sola fonte promozionale senza controllarne il significato.

## 6. Aggiorna e presenta le informazioni
La scheda cresce per aggiunte documentate e correzioni approvate. Prima di salvare una scheda condivisa, presenta al redattore i dati e i collegamenti alle fonti; dopo l'approvazione controlla che gli ID delle fonti siano coerenti e che le denominazioni delle città non siano omesse.

Quando il redattore chiede di vedere una scheda, presentane in modo leggibile l'identità, le sedi, le attività e una breve cronologia dei passaggi storici. **Il formato a righe cronologiche continue approvato per le carriere dei cantanti non si applica automaticamente alle schede istituzionali.** Per richieste mirate rispondi direttamente, attingendo ai dati pertinenti.

Non introdurre collegamenti a Opera+ Atlas o sistemi di tracciamento di collaborazioni fra artisti.
