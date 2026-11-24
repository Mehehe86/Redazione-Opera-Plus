# Opera+ — Procedura per le schede dei registi, direttori d'orchestra e altri professionisti (v1.0)

## Obiettivo
La scheda deve conservare **tutti i lavori artistici documentabili** di un professionista dell'opera e del teatro musicale, con **nome del teatro e città** per ciascuna esperienza verificata, anno o stagione quando disponibili. Si applica a registi, direttori d'orchestra, scenografi, costumisti, coreografi, responsabili delle luci e altre figure professionali. Una stessa persona può avere più professioni: non creare identità diverse soltanto perché assume incarichi differenti.

Non serve costruire uno storico dei singoli giorni di recita, dei cast, dei cointerpreti o delle collaborazioni ricorrenti; non creare collegamenti o dipendenze da Opera+ Atlas.

Lo schema è `schemi-json/artista-professionista.schema.json`; un esempio **interamente fittizio** è in `esempi-archivio/artista-professionista-esempio.json`.

## 1. Cerca l'identità corretta
Controlla se esiste già una scheda e verifica eventuali omonimi utilizzando biografie, formazione, professioni, attività e riferimenti ufficiali. Non fondere due persone solo perché hanno lo stesso nome o hanno collaborato con la stessa istituzione. Non ricercare né conservare indirizzi privati.

## 2. Cerca tutti i lavori, senza selezionare solo i più importanti
Parti dal sito dell'artista e dal suo curriculum, dai siti dei teatri e dei festival, dai programmi di sala, dagli archivi e dalle biografie di agenzia. Cerca **opera per opera e incarico per incarico**, includendo anche le produzioni meno conosciute; per una carriera internazionale ripeti le ricerche nelle lingue appropriate. Per ogni lavoro cerca **tutte le sedi documentabili**, incluse riprese e ritorni nello stesso teatro in stagioni differenti. Non fermarti alla prima sede trovata.

Se l'incarico è costruire una scheda, prova a ricostruire sistematicamente la carriera dalle fonti disponibili. Se è soltanto scrivere un articolo urgente, puoi aggiungere prima i dati pertinenti, segnalando che la scheda resta parziale. Non dichiarare «completo» ciò che non hai verificato.

**Registi:** registra ogni diverso allestimento firmato, anche quando riguarda la stessa opera. Quando è documentato che un allestimento è stato ripreso in teatri o anni differenti, registra quelle esperienze sotto lo stesso lavoro. Non considerare automaticamente due spettacoli dello stesso titolo due nuove regie o due riprese della stessa regia: l'identità dell'allestimento va verificata attraverso crediti di produzione e fonti ufficiali.

**Direttori d'orchestra:** registra l'opera e l'incarico di direzione musicale nelle produzioni documentate; non attribuire automaticamente al direttore la paternità dell'allestimento. Due esecuzioni della stessa opera in teatri diversi sono due esperienze, senza bisogno di ricostruire la lista delle recite.

**Scenografi, costumisti e altri professionisti:** registra la **specifica funzione** che hanno svolto per una produzione. Non dedurre che abbiano svolto anche altri incarichi solo perché il loro nome ricorre nei crediti artistici. Se una persona firma sia scene sia costumi, registra entrambi gli incarichi in modo distinguibile.

La combinazione *opera + incarico* non basta sempre per identificare un lavoro unico: due regie diverse di `La traviata` dello stesso regista sono lavori distinti, mentre una ripresa della stessa regia in un altro teatro è una nuova esperienza del medesimo lavoro. Se le fonti non consentono di stabilire il legame, usa `identificativo_allestimento: null` e una nota di incertezza; evita di unire o moltiplicare arbitrariamente le produzioni.

## 3. Come registrare teatro, città e periodo
Quando la sede è nota, registra **nome del teatro, città in cui si trova e Paese**. Teatro Regio di Torino e Teatro Regio di Parma devono essere distinguibili; non basta «Teatro Regio». Se la fonte documenta la città ma non l'edificio, conserva la città e lascia `teatro` a `null`. Non scambiare il teatro produttore con la sede che ha ospitato lo spettacolo. Se la fonte indica soltanto un festival, usa le note anziché inventare un teatro.

Registra `anno` soltanto quando è documentato; se è nota soltanto una stagione come `2023/2024`, conserva `stagione` e lascia `anno` a `null`. Se il lavoro è annunciato ma non documentato come realizzato, usa `annunciato`, anche se la data prevista è passata. Mantieni traccia di annullamenti e sostituzioni senza trasformare un programma in una partecipazione accertata.

## 4. Conserva le fonti per ogni fatto
Per ogni lavoro e per ogni esperienza includi almeno un identificativo in `fonti_ids`, collegato a una voce presente nell'elenco `fonti`. Registra titolo della fonte, URL diretto, data di consultazione e descrizione esatta di ciò che prova. Per esempio, una scheda di stagione annunciata dimostra un incarico programmato, non che sia stato eseguito; una recensione successiva può invece confermare l'avvenuta rappresentazione.

Se una fonte documenta un incarico senza teatro o anno, registra il dato certo lasciando sconosciuti quelli non verificabili. Non inventare prime assolute, debutti, collaborazioni o caratteristiche di una produzione.

## 5. Visualizzazione approvata: un elenco cronologico, senza suddivisioni
Quando il redattore chiede la scheda, presentala **come un unico elenco continuo di righe di testo**, dal lavoro più antico documentato al più recente, **senza raggruppamenti per anno, titolo, incarico o teatro**.

Formato:

`ANNO O STAGIONE – INCARICO – OPERA – TEATRO – CITTÀ`

Esempio interamente inventato:

```text
2021 – Regia – La traviata – Teatro Regio – Torino
2024 – Regia – La traviata – Teatro Regio – Parma
Stagione 2026/2027 – Regia – La traviata – Teatro Comunale – Bologna [annunciato]
```

In questo esempio le prime due righe sono la stessa regia ripresa in due teatri, mentre la terza si riferisce a un nuovo allestimento. L'elenco cronologico **non deve necessariamente mostrare questa distinzione in ogni riga**: i dati strutturati e le fonti devono tuttavia conservarla. Quando è necessario per la comprensione, una breve nota dopo l'elenco può spiegare che una specifica produzione è stata ripresa.

Ordina le **esperienze** presenti nei singoli `lavori`, non le voci del repertorio nel loro insieme. Se lo stesso lavoro torna nello stesso teatro in un anno diverso, crea una riga per ciascuna esperienza documentata. Non creare invece una riga per ogni data di recita nella medesima serie di rappresentazioni.

Se due esperienze hanno soltanto lo stesso anno, non inventare l'ordine preciso: usa un criterio stabile per le righe a pari data. Per stagioni o periodi non precisamente datati, non attribuire arbitrariamente un anno; segnalane l'incertezza. Colloca le esperienze senza qualsiasi data in fondo, con «Anno da verificare». Per sedi o città sconosciute usa rispettivamente «Teatro da verificare» o «Città da verificare». Contrassegna gli incarichi futuri con **[annunciato]** e quelli incerti con una dicitura esplicita.

**Le fonti restano nei dati**, non vanno incollate dopo ogni riga dell'elenco. Il redattore deve poterle richiedere quando vuole verificare una voce. Il formato di lettura non determina la struttura JSON: si genera l'elenco dai dati conservati, senza duplicarli o perdere la tracciabilità.

## 6. Revisione e approvazione
Prima di salvare o modificare schede nell'archivio condiviso, presenta al redattore le modifiche proposte e le fonti. Dopo l'approvazione verifica la validità JSON rispetto allo schema, i riferimenti alle fonti, i possibili doppioni, la distinzione fra incarichi annunciati e realizzati e la presenza della città per ogni teatro documentato.

Non trattare l'assenza di un lavoro in archivio come prova che non sia mai stato realizzato. Durante la scrittura giornalistica utilizza soltanto gli elementi pertinenti e ricontrolla le informazioni importanti.
