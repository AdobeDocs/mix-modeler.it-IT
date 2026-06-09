---
title: Mix Modeler Deep Dive
description: Esplora la metodologia tecnica alla base di Adobe Mix Modeler, tra cui l’attribuzione multi-touch, la modellazione del marketing mix, l’apprendimento del trasferimento e l’ottimizzazione del budget.
feature: Administration
hide: true
feature_v2:
  - id: a234aebd-3855-4376-a64d-29b38411e0c5
  - id: fe1c9ae8-a908-4ae1-a0b6-fcf35177b134
level_v2:
  - id: d378ca77-2da1-4f39-ad92-1917fe974a38
topic_v2:
  - id: bbbea26f-9621-49eb-9ab8-e06fb3bbce8c
source-git-commit: 4f4fe68694c81ddb258656eb05d62ef057f200cb
workflow-type: tm+mt
source-wordcount: 2747
ht-degree: 0%

---


# Approfondimento


Adobe Mix Modeler è una piattaforma di misurazione unificata basata su AI/ML che combina l’attribuzione multi-touch (MTA) e la modellazione marketing mix (MMM) per fornire informazioni di marketing precise, scalabili e a prova di futuro. Questo articolo presenta una scomposizione dettagliata della metodologia, delle scelte di progettazione e delle innovazioni tecniche alla base di Mix Modeler. E si basa su [questa sessione del Summit 2025](https://business.adobe.com/it/summit/2025/sessions/marketing-mix-modeling-at-adobe-learn-to-predict-s602.html){target="_blank"}, che presenta una suddivisione dettagliata della metodologia, delle scelte di progettazione e delle innovazioni tecniche alla base di Mix Modeler.

Con la crescita della complessità del marketing, gli approcci di misurazione tradizionali non sono all’altezza delle aspettative. La frammentazione dei dati, l’evoluzione dei vincoli di privacy e la necessità di velocità e rigore rendono necessario ripensare al modo in cui vengono valutate le prestazioni di marketing. La risposta di Adobe è Mix Modeler: un sistema integrato che utilizza l’apprendimento automatico per sintetizzare più origini di dati e paradigmi di modellazione in una strategia coesa.


>[!TIP]
>
>Uno dei vantaggi principali di Mix Modeler è l&#39;accessibilità della soluzione per gli esperti di marketing. L’applicazione semplifica le complessità della data science tramite un’interfaccia di facile utilizzo che non richiede conoscenze scientifiche. Se sei interessato a un approfondimento, questo articolo esplora le scelte tecniche effettuate durante lo sviluppo di Mix Modeler. L’articolo presuppone una certa familiarità con i concetti (avanzati) di data science.

Questo articolo spiega più dettagliatamente i componenti fondamentali. I componenti fondamentali sono:

* [attribuzione multi-touch](#multi-touch-attribution-mta)
* [modellazione marketing mix](#marketing-mix-modeling-mmm)
* [trasferisci apprendimento](#transfer-learning) (scambio intelligente di risultati tra attribuzione multi-touch e modellazione marketing mix)



## Attribuzione multi-touch (MTA)


### Panoramica

Il modello di attribuzione multi-touch (MTA) che alimenta Mix Modeler si basa su un modello di sopravvivenza in tempo discreto addestrato sui dati a livello di evento. I dati includono ricerche, clic, visualizzazioni di prodotti, aggiunte ai carrelli e checkout. Utilizzando l&#39;apprendimento supervisionato, il modello stima la probabilità condizionale di conversione in ogni fase del percorso del cliente. Il modello considera sia i percorsi di percorso dei clienti di conversione che quelli di non conversione per misurare in che modo i diversi punti di contatto di marketing influenzano il comportamento dei clienti nel tempo. Il percorso di non conversione è importante quanto il percorso di conversione. Il contrasto tra i due percorsi consente di comprendere se un particolare tipo di punto di contatto di marketing determina in modo efficace la conversione. Ad esempio, se un tipo di punto di contatto sembra probabile su un percorso di non conversione e su un percorso di conversione, tale punto di contatto non ha alcun impatto sulla conversione. Questo comportamento è contrario a un punto di contatto che viene visualizzato spesso su un percorso di conversione e non su un percorso di non conversione.

![Dati a livello di evento](/help/assets/event-level-data.png)

### Concetti chiave

I concetti chiave dell’attribuzione multi-touch sono:

* **Modellazione interessi**: la conversione del cliente viene modellata come un accumulo di interessi nel tempo.

  ![Interesse per aumento esposizione](/help/assets/exposure-increases-interest.jpg)

  In questo approccio, una serie di segnali di interesse determina la probabilità di conversione, ciascuno influenzato da

   * precedenti esposizioni ai mezzi di comunicazione,
   * l&#39;impatto dei media adstock (un modello di risposta alla creazione di pubblicità e al declino nei mercati dei beni di consumo), e
   * altri fattori basali.



  Questi segnali sono rappresentati come *ϴ<sub>BL</sub>* + *ϴ<sub>E,tc-t1</sub>* + *ϴ<sub>E,tc-t2</sub>* e *ϴ<sub>S, tc-t3</sub>*, dove:

   * *ϴ*: illustra i parametri del modello (ciò che viene appreso dal modello).
   * *tc*: ora della conversione.
   * *tc-tx: il tempo che intercorre tra l&#39;esposizione e la conversione, pertinente per il modello.
   * *BL*: baseline.
   * *E*: e-mail.
   * *S*: ricerca.

  Nel framework di modellazione, l&#39;obiettivo è tenere conto esplicitamente del tempo tra ogni esposizione multimediale e il momento della conversione (*tc-tx*), riconoscendo che le interazioni più recenti hanno più peso di quelle più vecchie.

* **Mappatura probabilità**: la probabilità di conversione è derivata dal livello di interesse utilizzando una funzione logistica a forma di S.

  ![Probabilità di conversione](/help/assets/probability-of-conversion.jpg)

  Attraverso l’apprendimento automatico supervisionato che utilizza un modello di sopravvivenza in tempo discreto, l’illustrazione precedente visualizza il percorso del cliente A alla conversione. Il livello di interesse viene visualizzato sull&#39;asse X e la probabilità di conversione sull&#39;asse Y. Questa mappatura mostra che la seconda esposizione e-mail (*ϴE, tc-t2*) ha il maggiore impatto sulla conversione. Come indicato da un aumento significativo della probabilità di conversione al momento di tale passaggio.

* **Rendimenti in diminuzione**: punti di contatto aggiuntivi hanno un impatto meno incrementale con la crescita degli interessi.

  La curva a forma di S, come illustrato in precedenza, mostra anche che l’esposizione del cliente a punti di contatto aggiuntivi ha un impatto meno incrementale con livelli di interesse in crescita.

* **Modello di sopravvivenza a tempo discreto**: l&#39;utilizzo di un modello di sopravvivenza a tempo discreto introduce maggiore flessibilità nel modello, che consente al modello di acquisire sfumature temporali nel comportamento del cliente. Il modello di sopravvivenza a tempo discreto attenua anche alcune delle ipotesi più restrittive richieste dai modelli di sopravvivenza a tempo continuo.

  ![Modello di sopravvivenza temporale discreto](/help/assets/discrete-time-survival-model.jpg)

  Una funzione a tempo continuo modella l&#39;impatto di e-mail adstock sul livello di interesse, in qualsiasi momento dal momento dell&#39;esposizione: *ϴ<sub>E</sub>(Δt;⋋)*
Una funzione a tempo discreto modella l&#39;impatto di e-mail adstock sul livello di interesse come intervalli di tempo discreti utilizzando parametri scalari: *ϴ<sub>E,i</sub> ≥ 0<sub>E,i+1</sub>*


### Vantaggi

L’approccio di attribuzione multi-touch selezionato per Mix Modeler presenta diversi vantaggi chiave.

* Tenere conto sia dei percorsi di conversione che di quelli di non conversione, garantendo in tal modo una stima più accurata dell’impatto reale dei contenuti multimediali.
* Incorpora adstock e rendimenti ridotti che modellano il comportamento reale del cliente ed evita supposizioni eccessivamente semplificate che si trovano spesso nei modelli basati su regole.
* Scalabilità efficiente per dataset di grandi dimensioni grazie all&#39;ottimizzazione per il calcolo distribuito e l&#39;elaborazione parallela.
* Supporta l’attribuzione intuitiva dei punti di contatto che consente un’interpretazione chiara, contraria ad altri metodi come i modelli Markov nascosti.
* Prestazioni elevate e alta precisione predittiva rispetto ad altri algoritmi di classificazione.

Mix Modeler fornisce una [interfaccia intuitiva](/help/models/insights.md#attribution) per gli addetti al marketing per le informazioni derivanti dall&#39;attribuzione multi-touch.

![Informazioni sull&#39;attribuzione modello](/help/assets/model-insights-attribution.png)


Anche se l’attribuzione multi-touch offre tutti questi vantaggi, Mix Modeler non si basa completamente sulle informazioni di conversione dai dati a livello di evento. La modellazione del marketing mix è un altro componente fondamentale per prendere in considerazione i dati a livello aggregato.

## Modellazione marketing mix (MMM)

La modellazione del marketing mix (MMM) si basa su dati a livello aggregato e utilizza una struttura di modello moltiplicativo, piuttosto che additiva, per riflettere le interazioni di marketing reali.

![Dati a livello di aggregazione](/help/assets/mmm-aggregate-data.jpg)

L’illustrazione mostra i dati a livello aggregato in formato tabulare. Ogni riga corrisponde a un periodo di tempo, in genere una settimana o un giorno, e ogni colonna rappresenta una variabile. La tabella include:

* la colonna di conversione (variabile di risultato del modello),
* colonne multimediali (ad esempio: ricerca, visualizzazione) e
* le colonne dei fattori (ad esempio, stagionalità, promozioni) per acquisire influenze interne o esterne al di fuori della spesa dei supporti che ancora influiscono sulle prestazioni dei supporti.

Il modello prevede le conversioni alla settimana 4 utilizzando i dati evidenziati in verde chiaro, inclusi i fattori della settimana e gli input storici dai canali multimediali.

### Concetti chiave

I concetti chiave alla base della modellazione del marketing mix sono:

* **Modello moltiplicativo**: le vendite o le conversioni sono il prodotto di una linea di base e di moltiplicatori multimediali.

  Quindi, invece di utilizzare un modello additivo:
  *Conversioni settimanali = Domanda prevista **+**&#x200B;Moltiplicatore della ricerca **+**&#x200B;Moltiplicatore della visualizzazione **+**....*
utilizza un modello moltiplicativo:
  *Conversioni settimanali = Domanda prevista **x**&#x200B;Moltiplicatore della ricerca **x**&#x200B;Moltiplicatore della visualizzazione **x**....*

  Oppure in una formula: ** Y = ⨍<sub>BL</sub>(X<sub>fattori</sub>;<sub>fattori</sub>) x ⨍<sub>S</sub>(X<sub>S</sub>;<sub>S</sub>) x ⨍<sub>D</sub>(X<sub>D</sub>;<sub>D</sub>)*

  Ad esempio:

   * Conversioni effettive settimanali: 1730.
   * Conversioni previste settimanali: 1787,5 = 1100 x 1,25 x 1,3, dove:
      * 1100: domanda basale prevista alla settimana 4, una funzione per i dati dei fattori 1 e 2 della settimana 4.
      * 1.25: moltiplicatore di ricerca previsto per la settimana 4, una funzione dei dati di ricerca dalla settimana 1 alla settimana 4.
      * 1.3: moltiplicatore di visualizzazione previsto dalla settimana 4, una funzione per visualizzare i dati dalla settimana 1 alla settimana 4.

  La differenza prevista tra ciò che il modello prevede (1787.5) e le conversioni effettive (1730) è il residuo, che è spesso di piccole dimensioni e non qualcosa di cui preoccuparsi.


* **Acquisizione di adstock e diminuzione del rendimento**: Adstock viene acquisito utilizzando le funzioni di decadimento esponenziale e alimentazione.

  ![Acquisizione dei rendimenti in diminuzione delle azioni pubblicitarie](/help/assets/capturing-adstock-diminishing-return.jpg)


  Il decadimento esponenziale per adstock può essere sia a una coda che a due code, a seconda della posizione in cui si verifica il picco di impatto dopo l&#39;investimento nel supporto.

  Per ridurre i rendimenti, viene applicata la funzione di risparmio energia: *x<sup></sup>* per *∈ (0,1*). Questa funzione di potenza genera un grafico concavo a forma di grafo per catturare il rendimento decrescente. Il ritorno in diminuzione viene quindi acquisito nella funzione moltiplicatore all&#39;interno del modello MMM.


### Vantaggi

I vantaggi dell’approccio basato sulla modellazione del marketing mix si basano sul fatto che il modello moltiplicativo supporta meglio i comportamenti di marketing attesi nel mondo reale. Ad esempio:

* Sinergia mediatica in cui i canali mediatici spesso funzionano meglio insieme che isolatamente.
* Impatto variabile nel tempo, in cui lo stesso livello di investimento di marketing può produrre rendimenti diversi in momenti diversi a causa di fattori esterni.
* Raccomandazioni di budget nel tempo laddove le condizioni di mercato previste o le fluttuazioni di base contribuiscono a determinare l&#39;allocazione del budget nel tempo.

Mix Modeler fornisce una [interfaccia intuitiva per gli addetti al marketing](/help/models/insights.md#attribution) per le varie informazioni derivanti dalla modellazione del marketing mix. Ad esempio, una disaggregazione dei contributi dei fattori per mostrare la proporzione delle conversioni di base che possono essere attribuite a vari fattori inclusi nel modello.


![Analisi stratificata contributi fattore](/help/assets/factors-example.png)


#### Esempio

Questo esempio semplificato illustra come un approccio di modellazione moltiplicativa per un negozio online di sneakers fittizio consenta una migliore allocazione di budget rispetto al modello additivo.

![Approccio del modello moltiplicativo](/help/assets/benefits-mmm.jpg)

##### Presupposti

* La domanda di scarpe da ginnastica è più elevata in estate e più bassa in inverno, come illustrato dai contributi totali al basale.

* La strategia predefinita per la pianificazione del marketing consiste nel spendere una quantità fissa di budget di marketing ($ 840) per l&#39;intero anno, dove ogni mese ottiene lo stesso budget.

* Adstock viene ignorato e i supporti a pagamento vengono trattati come un&#39;unità. Tali ipotesi sono indipendenti dal modello scelto e non influenzano il confronto.

* Un budget costante nel modello additivo indica un contributo costante in ogni mese, che si riflette per il modello additivo sul grafico superiore nella colonna centrale.

* Nel modello moltiplicativo, un budget costante significa moltiplicatori costanti ogni mese. Per ottenere un impatto variabile nel tempo per la stessa spesa mensile, il moltiplicatore funziona con la domanda di base. Questo effetto moltiplicatore viene visualizzato sul grafico inferiore nella colonna centrale.

##### Spostare i budget

Esiste la capacità di passare da un budget fisso a un budget variabile, mantenendo il budget totale a 840 dollari?

* Nel modello additivo, dal punto di vista della modellizzazione, non vi è alcun incentivo ad apportare un cambiamento in quanto non vi è alcuna interazione con il basale. Avere una spesa piatta è ottimale. Se trasferisci $1 da novembre a maggio, il guadagno in maggio è inferiore al calo di novembre a causa di rendimenti in diminuzione.
* In un modello moltiplicativo, c&#39;è spazio per spostarsi. In base alla linea di base, è possibile spostare i budget dai mesi invernali ai mesi estivi. Il guadagno nel mese estivo è più della perdita nel mese invernale a causa dell&#39;effetto moltiplicatore. L&#39;estensione del turno e dove passare è inclusa negli [algoritmi di ottimizzazione del budget](#budget-optimization) utilizzati nella modellazione del marketing mix.



## Trasferisci apprendimento

Accanto alla modellazione di attribuzione multi-touch e marketing mix, la sperimentazione è un altro pilastro importante per risolvere i problemi di misurazione del marketing. Anche se la sperimentazione non viene implementata nel quadro di Mix Modeler, è possibile utilizzare la sperimentazione, come disattivare il marketing in alcuni mercati, per comprendere l&#39;impatto causale del marketing sulle vendite.

Adobe consiglia e utilizza il trasferimento dell’apprendimento per combinare informazioni provenienti dall’attribuzione multi-touch, dalla modellazione del marketing mix, dalla sperimentazione e da altre fonti di conoscenza precedenti.  Questa fusione può essere descritta come un approccio a più livelli. Ogni livello presenta delle lacune per illustrare i limiti della produzione di un modello coeso. Ma se impilate i livelli nel modo giusto, potete compensare gli spazi nel modello combinato.
Applica questa analogia quando utilizzi la combinazione di attribuzione multi-touch, modellazione di marketing mix, sperimentazione e origini di conoscenza precedenti. Blend questi componenti in modo tale che la combinazione soffra il meno dei difetti in ciascuno dei componenti.

In sostanza, l’apprendimento mediante trasferimento è un algoritmo di ottimizzazione numerica sul lavoro. Nell&#39;ambito dell&#39;apprendimento del modello, viene impostata una funzione di perdita (per quantificare la differenza tra l&#39;output previsto di un modello e il valore effettivo (verità del suolo)). Viene inoltre determinata una buona misura della metrica di adattamento (per valutare se le previsioni di un modello si allineano con i dati osservati). Trasferisci l’apprendimento, quindi risolve l’ottimizzazione numerica per ottenere i metadati (parametri del modello). Se esistono una o più fonti di informazione, quella funzione di ottimizzazione originale viene potenziata con un altro termine. Questo termine misura la distanza tra ciò che hai fornito come conoscenza precedente e ciò che il modello produce da confrontare.


### Apprendimento del trasferimento bidirezionale

Quando disponi sia di dati a livello di evento che di dati a livello di aggregato, l’apprendimento del trasferimento bidirezionale coinvolge il seguente flusso di lavoro.

![Apprendimento del trasferimento bidirezionale](/help/assets/bi-directional-transfer-learning.jpg)

| Passaggio | Descrizione |
|:---:|---|
| 1a | Il modello MTA predefinito viene addestrato sui dati. In genere, un modello MTA viene addestrato su un intervallo di tempo più breve rispetto al modello MMM. I dati coprono i dati dell’evento dai canali online. |
| 1b | Il modello MTA viene addestrato. In genere, un modello MMM viene addestrato su un intervallo di tempo di almeno due anni. I dati riguardano fattori, canali online e offline. |
| 2 | Il modello MTA viene valutato. |
| 3 | I risultati del modello MTA con punteggio vengono inseriti in MMM come apprendimento del trasferimento. |
| 4 | Il modello MMM viene aggiornato con i dati di apprendimento del trasferimento. Questo aggiornamento significa che viene utilizzato un nuovo set di stime di parametri per ulteriori informazioni approfondite e per l’ottimizzazione del budget. I canali e la copertura temporale non cambiano. |
| 5 | Il modello MMM viene valutato utilizzando i dati aggregati settimanali per i canali. |
| 6 | Il risultato del modello MMM con punteggio viene inserito nell’MTA come apprendimento del trasferimento. |
| 7 | I punteggi MTA per i dati a livello di evento vengono aggiornati utilizzando i risultati del trasferimento di apprendimento e vengono utilizzati per ulteriori informazioni. |

Considera i seguenti aspetti:

* L’MTA è limitato per quanto riguarda la copertura dei canali (ad esempio solo i dati a livello di evento provenienti da dati web e mobili), ma è vantaggioso a causa della grande quantità di dati. L’aspetto chiave dell’MTA è la prestazione relativa.
* MMM comprende il quadro più olistico con fattori, canali online e offline.
* Il trasferimento dell’apprendimento da MTA a MMM aggiorna il modello MMM. I risultati del trasferimento di apprendimento influenzano i parametri che guidano il *modello* moltiplicativo. Il trasferimento dell&#39;apprendimento da MMM a MTA aggiorna i *punteggi* dell&#39;MTA. Non è necessario influenzare il modello MTA, in quanto i punteggi iniziali sono già statisticamente sufficienti.

## Conoscenze precedenti

Quindi oltre a MTA, MMM e sperimentazione, ci sono molte altre fonti diverse di conoscenze precedenti che puoi facoltativamente sfruttare per la pianificazione della misurazione di marketing. Diverse aziende hanno fonti diverse di conoscenza preventiva. Alcuni esempi includono la quota di spesa, i modelli interni precedenti o l’esperienza del settore.

![Conoscenza precedente](/help/assets/prior-knowledge.jpg)

Il processo di creazione del modello può sfruttare tutte queste fonti di informazioni attraverso lo stesso processo di trasferimento. Queste origini di conoscenza precedenti sono facoltative. Non è necessario disporre di origini di conoscenza precedenti per il funzionamento della modellazione del marketing mix. Se non disponi di alcuna conoscenza precedente, viene utilizzato il modello predefinito per generare informazioni sul punteggio e quindi l’ottimizzazione del budget. Se si dispone di un input di conoscenza precedente, è possibile utilizzare l&#39;apprendimento del trasferimento per aggiornare il modello MMM.


## Ottimizzazione del budget

L’ottimizzazione del budget si basa sul modello MMM moltiplicativo illustrato in precedenza,

In un semplice esempio, sono disponibili due canali: ricerca e visualizzazione. E hai un budget totale. L&#39;obiettivo è quello di suddividere il budget tra i due canali per massimizzare la conversione. L’ottimizzazione numerica viene utilizzata per trovare il mix di budget ottimale che massimizza la conversione in base al vincolo di budget totale. Ad esempio, immagina che il tuo vincolo di budget totale sia di $130.000.

La formula di ottimizzazione del budget è: *Max ⨍(X<sub>S</sub>, X<sub>D</sub>) = ⨍<sub>BL</sub>(X<sub>fattori</sub>) x ⨍<sub>S</sub>(X<sub>S</sub>) x ⨍<sub>D</sub>(X<sub>D</sub>)*, dove *X<sub>S</sub>* e *X<sub>D</sub>* sono parametri e *X<sub>fattori</sub>* previsti.

![Vincoli budget](/help/assets/budget-constraints.png)


### Vincoli a livello di canale

Immagina di avere vincoli aggiuntivi a livello di canale:

* $10.000 - $80.000 per la ricerca.
* $5.000 - $70.000 per la visualizzazione.
* 130.000 dollari in totale.

Di conseguenza, il mix di budget idoneo determina il vincolo della superficie di ottimizzazione. L’algoritmo di ottimizzazione numerica consente quindi di determinare l’allocazione di budget ottimale.

### In più conversioni

Oltre ai vincoli a livello di canale, pianifica un’allocazione ottimale del budget tra più conversioni.

![Ottimizzazione del budget tra conversioni](/help/assets/planning-across-multiple-conversions.jpg)

Per adattare l’allocazione ottimale del budget tra le conversioni, viene utilizzata una media ponderata della funzione precedente per ciascuna delle conversioni. La formula diventa *⨍<sub>new</sub>(X) = w<sub>1</sub>f<sub>1</sub>(X) + w<sub>2</sub>f<sub>2</sub>(X)*

Esempi di ottimizzazione del budget in più conversioni sono:

* Desideri massimizzare i ricavi totali derivanti dalle vendite online e dalle conversioni in-store.
* Desideri ottimizzare per il successo a lungo termine utilizzando sia i KPI di brand awareness che le conversioni di vendita.

Nel secondo esempio, le unità delle due conversioni non sono simili (KPI di brand awareness rispetto alle conversioni), ma questo non importa. Le conversioni o i modelli non devono fare riferimento agli stessi canali e possono anche sovrapporsi. L’ottimizzazione numerica trova la soluzione migliore al problema entro i vincoli specificati.


## Riepilogo

Adobe Mix Modeler è più di uno strumento di misurazione; Mix Modeler è un motore di supporto decisionale e i suoi punti di forza sono:

* La capacità di modellare la complessità reale con rigore statistico
* Un&#39;integrazione unificata di diversi dati e paradigmi di modellazione
* Architettura a prova di futuro in grado di adattarsi alle tendenze di deprecazione dei dati

La combinazione di interpretabilità e prestazioni ha reso Mix Modeler fondamentale per la trasformazione del marketing basata sui dati di Adobe. Mix Modeler consente ai team di marketing di prendere decisioni di investimento più rapide, intelligenti e allineate.
