## <font color=8A5BA6>Introduzione</font>
Verso la fine del XIX secolo, i matematici iniziarono a esplorare come fornire una base solida per tutta la matematica sviluppata fino a quel momento. Il loro obiettivo era ricreare un sistema matematico a partire da un numero limitato di assunzioni e ipotesi. In questo contesto, la teoria degli insiemi è emersa come uno degli approcci più utilizzati, anche se non è l'unico possibile.

Nella teoria degli insiemi, il concetto fondamentale è l'insieme stesso; in altre parole, tutto è considerato un insieme. Altri elementi della matematica, come numeri, funzioni e operazioni, vengono definiti successivamente.
##### <font color=C8A2C8>Perché la teoria degli insiemi? </font>
La teoria degli insiemi è efficace nel descrivere la matematica attraverso un numero ridotto di assiomi e offre una rappresentazione rigorosa degli infiniti. Tuttavia, presenta alcune limitazioni, in particolare nel campo della computazione. Se un calcolatore dovesse utilizzare la teoria degli insiemi, avrebbe bisogno di oltre 100 insiemi per rappresentare il numero 10, rispetto ai soli 5 bit necessari in altre rappresentazioni.
## <font color=8A5BA6>Teoria naive degli insiemi di Cantor</font>

Una delle primissime teorie degli insiemi, ormai obsoleta perché dimostrata inconsistente da Russell. Alcune caratteristiche:
- Posso formare insiemi in qualsiasi modo, per esempio:
	- **Assioma di comprensione:**  $A =\{X|P(X)\}$, posso scegliere una proprietà qualsiasi.
	- **Elenco:** $A=\{1,\{a,34,\Gamma\}, 4, 5\}$.
- Non c'è nessuna richiesta di omogeneità all'interno di un insieme, in quanto tutto è un insieme.
- L'appartenenza $\in$ e l'uguaglianza $=$ sono gli unici predicati di base.
- Le ripetizioni e l'ordine non contano, l'unica discrimante è l'appartenenza.
- Alcuni esempi sull'appartenenza:
	- $1\notin 1$
	- $1\in\{1,2,3\}$
	- $\{1,2\}\notin\{1,2,3\}$
	- $\{1,2\}\in\{\{1,2\},3\}$
- Alcuni esempi sull'inclusione:
	- $1\subseteq 1$
	- $1\subseteq\{1,2,3\}$
	- $\{1,2\}\subseteq\{1,2,3\}$
	- $\{1,2\}\not\subseteq\{\{1,2\},3\}$
### <font color=B292D6>Paradosso di Russell</font>
Russel dimostra inconsistente la teoria di Cantor proponendo un insieme tramite l'assioma di comprensione.
$$X=\{Y|Y\notin Y\}$$
Da questa proprietà deriva $X\in X\ \iff\ X\notin X$.
##### <font color=C8A2C8>Inconsistente vuol dire sbagliato? No </font>
Inconsistente indica semplicemente che in una certa teoria è affermabile $A$ e  $\lnot A$, per cui descrive un universo a cui noi non siamo interessati.
##### <font color=C8A2C8>Quindi cosa facciamo? </font>
Nel momento in cui la teoria naive è scartata è necessario creare un'altra teoria degli insiemi, con alcune cose a cui stare attenti:
- Non dobbiamo avere l'assioma di comprensione
- Andrà introdotto il concetto di "classe", cioè insiemi "troppo grandi" per essere definiti tali
## <font color=8A5BA6>Teoria assiomatica degli insiemi</font>

### <font color=B292D6>Premesse</font>

- Esistono tante teorie assiomatiche degli insiemi, noi studiamo la teoria di Zermelo-Fraenkel (ZF Set Theory), che sta alla base di tante altre teorie ma permette comunque di sviluppare gran parte della matematica.
- I concetti di **Insieme, appartenenza** e **uguaglianza** non vengono definiti, sono **enti primitivi** di tutte le teorie assiomatiche degli insiemi. (Per vedere alcune misconception su appartenenza e inclusione vedasi il paragrafo sulla teoria naive).
- Gli assiomi sono ipotesi globali, non vengono dimostrati in quanto noi siamo interessati solo alle situazioni (agli “universi”) in cui valgono.
- Le definizioni sono abbreviazioni, non aggiungono informazioni (non restringono gli universi analizzati), ma vanno soltanto ad abbreviare concetti già presenti
- La ZF Set Theory non è mai stata dimostrata né consistente né inconsistente

### <font color=B292D6>Assioma di estensionabilità</font>

$$
\forall X,\forall Y,(X=Y\iff \forall Z,(Z\in X\iff Z\in Y)
$$

Due insiemi vengono definiti uguale se e solo se ogni elemento di uno appartiene anche all’altro.

### <font color=B292D6>Definizione di sottoinsieme</font>

$$
A\subseteq B \overset{\text{def}}{=}\forall Z,(Z\in A\to Z\in Y)
 
$$

Non è un assioma, non va ad introdurre concetti nuovi o definire cos’altro è un insieme o meno, semplicemente permette di indicare più velocemente se un insieme è sottoinsieme dell’altro.

NB: Il concetto di sottoinsieme in teoria degli insiemi è diverso rispetto a quello a cui si potrebbe pensare intuitivamente. Affermare che $A\subseteq B$ da informazioni sui singoli elementi contenuti in A e B, non sui due insiemi A e B nel totale;  allo stesso modo affermare $A\in B$ non da informazioni sui singoli elementi contenuti in A e B, ma solo sui due insiemi nel totale.

### <font color=B292D6>Assioma di separazione</font>

$$
\forall X, \exists Y, \forall Z,(Z\in Y\iff Z\in X \land P(Z))
$$

Dato un insieme X posso formare un sottoinsieme Y contenente tutti gli elementi Z in X che soddisfano una certa proprietà P().

##### <font color=C8A2C8>Cosa cambia dall’assioma di comprensione? </font>

L’assioma di comprensione permetteva di creare insiemi da zero da una qualsiasi proprietà, l’assioma di separazione permette soltanto di creare sottoinsieme partendo da insiemi già esistenti. Per replicare il paradosso di Russel servirebbe avere un insieme U che contiente tutti gli insiemi, nessun assioma ci permetterà mai di farlo.

##### <font color=C8A2C8>Come mai non scrivo anche </font> $\forall P$ <font color=B292D6>?</font>

P() non è un insieme, ma una proprietà. In logica del prim’ordine il quantificatore universale $\forall$ e quello esistenziale $\exists$ sono applicabili solo agli elementi della teoria discussa, in teoria degli insiemi tutti gli elementi sono insiemi, non proprietà. Per scrivere $\forall P$ è necessario usare una logica del second’ordine. 

Per mantenerci in logica del prim’ordine si può descrivere P() come una collezione di infiniti assiomi, uno per ogni proprietà. In questo modo l’assioma di separazione è solo una schematizzazione di infiniti assiomi diversi, uno di questi potrebbe essere 

$$
\forall X, \exists
Y, \forall Z,(Z\in Y\iff Z\in X \land Z\in\  Insieme\ dei \ numeri \ pari)
$$


Se indichiamo Y come $(Z\in X|P(Z))$ possiamo riscrivere l’assioma di separazione in questo modo

$$
\forall X, \forall Z,(Z\in \{W\in X|P(W\}) \iff Z\in X \land P(Z))
$$

NB: Questa notazione è un abuso, al momento non sarebbe corretto riscrivere l’assioma di separazione in questo modo. Diventa più avanti dimostrabile tramite logiche e teorie più avanzate, a un livello che in questo corso non raggiungeremo.

###  <font color=B292D6>Assioma dell’insieme vuoto</font>

$$
\exists X,\ \forall Z,\ Z\notin X
$$

L’insieme per chiarezza non viene chiamato $X$ ma $\varnothing$ , in questo modo l’assioma diventa 

$$
\forall Z,\ Z\notin \varnothing
$$

Questo è un assioma molto importante, essendo il primo assioma che ci permette di creare un nuovo insieme senza dover partire da insiemi già esistenti .

##### <font color=C8A2C8>Definizione dell’insieme vuoto</font>

L’assioma viene presentato per motivi didattici, in realtà nella vera teoria degli insiemi ZF non esiste e l’insieme vuoto viene definito a partire da un insieme la cui esistenza è dimostrata in futuro.
Con Y un qualunque insieme la cui esistenza è definita da un altro assioma (e.g. l’assiome dell’infinito), si può scrivere (usando l’assioma di separazione):

$$
\varnothing 
\overset{\text{def}}{=}\{X\in Y|false\}
$$

### <font color=B292D6>Definizione di intersezione binaria</font>

$$
A\cap B \overset{\text{def}}{=}\{X\in A|X\in B\}
$$

Come con la definizione di sottoinsieme, non vado ad affermare nuovi assiomi, semplicemente abbrevio un concetto già possibile. Usando l’assioma di separazione, ponendo $A$ l’insieme di partenza, $A\cap B$ il sottoinsieme e $X\in B$ la proprietà, posso dimostrare questo teorema: 
$$
X\in A\cap B\iff X\in A\land X\in B 
$$
Entrambe le formule descrivono un’intersezione binaria, cioè tra due insiemi. Posso scrivere una formula generalizzata in questo modo: 

##### <font color=C8A2C8>Intersezione n-aria</font>


$$
A_1\cap...\cap _n=(...((A_1\cap A_2)\cap A_3)...\in A_n)
$$

*NB:* Questo non è un assioma o una formula corretta! In logica non è possibile sottindere parti dei teoremi fino a un elemento n generalizzato, questa è semplicemente una dicitura informale per indicare come l’intersezione binaria può essere con più di due insiemi.

*NB2:* L’intersezione permette di intersecare un numero n di insiemi, non un numero infinito!

##### <font color=C8A2C8>Definizione di intersezione generale</font>

Dato un insieme, è possibile definire un insieme che è l’unione di tutti i suoi elementi (altri insiemi): 

$$
\bigcap F\overset{\text{def}}{=}\varnothing \quad se\quad   F=\varnothing \\
\bigcap F\overset{\text{def}}{=}\{ X\in A|\forall Y,\ (Y\in F \to X\in Y)\} \quad dove \quad A\in F
 
$$

*Parafrasi 1*: per qualsiasi insieme A appartente ad F, ogni elemento X appartenente ad $\bigcap F$ appartiene anche ogni altro insieme Y appartenente ad F
*Parafrasi 2 (informalissima):  $A\in F\ \land \ X\in A\ \land X\in \bigcap F\quad \to \quad \forall Y,\ X\in Y$*

$\bigcap F$ viene anche scritto come $\bigcap _{Y\in F}Y$

*Esempio*:  $\bigcap _{Y\in \{A,B,C\}}Y=A\cap B\cap C$

### <font color=B292D6>Assioma dell’unione</font>

$$
\forall F,\  \exists X, \ \forall Z, \ (Z\in X\iff \exists Y, (Y\in F\land Z\in Y))
$$

*Parafrasi*: indicando X come $\bigcup F$. Per qualsiasi insieme Y appartente ad F, ogni elemento Z appartenente ad $\bigcap F$ appartiene anche ad almeno un altro insieme Y.

$\bigcup F$ si scrive anche come  $\bigcup_{Y\in F}Y$

##### <font color=C8A2C8>Teorema dell’unione binaria</font>

Una volta dimostrato che per qualsiasi A e B esiste un insieme contiene solo A e B, si può dimostrare: 

$$
\forall A, \ \forall B,\ \exists X, \ \forall Z,(Z\in X\iff Z\in A \lor Z\in B)
$$

Se scriviamo X come $A\cup B$, allora abbiamo: 

$$
\forall A, \ \forall B,\ \forall Z,(Z\in A\cup B\iff Z\in A \lor Z\in B)
$$
### <font color=B292D6>Assioma del singoletto</font>

$$
\forall X,\ \exists Y, \ \forall Z,\ (Z\in Y \iff Z=X)
$$

L’insieme Y è quindi un insieme che a cui appartiene l’insieme X, per questo motivo viene indicato come $\{ X\}$, in questo modo l’assioma può essere riscritto come: 

$$
\forall X,\ \forall Z,\ (Z\in \{ X\}\iff Z=X)
$$

##### <font color=C8A2C8>Teorema del singoletto</font>

Anche l’assioma del singoletto è presentato per motivi didattici, in realtà è ridondante e può essere dimostrato a partite dall’assiome di rimpiazzamento (presentato in seguito)

### <font color=B292D6> Abuso di notazione </font>

Scrivendo $\{A_1,...,A_n\}$ indicheremo l’insieme $\{A_1\}\cup...\cup\{A_n\}$, che esiste grazie all’assioma del singoletto (esiste $\{A_n\}$ )e dell’unione (esiste $\{A_{n-1}\}\cup\{A_n\}$ ). Abbiamo qundi: 

$$
X\in\{A_1,...,A_n\}\ sse \ X=A_1\lor ...\lor X=A_n
$$

### <font color=B292D6>Costruzione dei numeri naturali</font>

Rifacendosi al concetto meta-matematico, andiamo a codificare i numeri naturali all'intermo della nostra teoria degli insiemi.
$$[\![0]\!] \overset{\text{def}}{=} \varnothing \qquad
[\![n]\!] \overset{\text{def}}{=} [\![n]\!]\cup \{[\![n]\!]\}
$$
Per queste due definizioni andiamo ad unire:
- L'assioma dell'insieme vuoto: esiste $\varnothing$
- L'assiome del singoletto: se esiste $\varnothing$ esiste anche $\{\varnothing\}$, così anche $\{\{\varnothing\}\}$...
- L'assioma dell'unione: esiste $[\![n]\!]\cup \{[\![n]\!]\}$
Di nuovo, questa è soltanto una definizione, una codifica di un concetto che abbiamo intuitivamente tramite questa teoria degli insiemi. Non è nemmeno l'unico modo per implementare i numeri naturali, è stato scelto questo metodo perché facilmente scalabile ad altri insiemi di numeri in seguito.
Seguendo la definizione, qualche esempio:
$$[\![0]\!] = \varnothing \qquad indicato\ con\ 0$$
$$[\![1]\!] = \{\varnothing\}\qquad indicato\ con\ 1$$
$$[\![2]\!] = \{\varnothing,\{\varnothing\}\} \qquad indicato\ con\ 2$$
$$[\![3]\!] = \{\varnothing,\{\varnothing\},\{\varnothing,\{\varnothing\}\}\} \qquad indicato\ con\ 3$$
Si può dimostrare che ogni numero è diverso, cfr _Logica del prim'ordine_

### <font color=B292D6>Assioma dell'infinito</font>
$$\exists Y,(\varnothing \in Y\land \forall N,\ (N\in Y\to N\ \cup \{N\}\in Y ))
$$
$Y$ è un insieme infinito che per ora chiameremo $\mathcal{N}$.
L'assioma afferma che esiste un insieme $\mathcal{N}$ con queste proprietà:
$\varnothing$ appartiene ad $\mathcal{N}$ e se un qualsiasi altro insieme ci appartiene, allora ci apparterrà anche l'unione col suo singoletto, creando una "successione infinita" 
NB: $\forall N$ nell'assioma non è né $\mathcal{N}$ né un numero naturale, ma semplicemente un insieme qualsiasi!
##### <font color=C8A2C8>Insieme infinito? E il paradosso di Russell?</font>
Per la prima volta un'assioma afferma l'esistenza di un insieme infinito. Per quanto possa sembrare affine all'insieme U (insieme che contiene tutti gli insiemi) che ci siamo ripromessi di non creare, in realtà c'è una differenza fondamentale: $\mathcal{N}$ è infinito sì, ma non contiene tutti gli insiemi, solo la $\varnothing$ e la "successione" di insieme a partire da N.

##### <font color=C8A2C8> Teorema dell'esistenza di ℕ </font> 
Al momento $\mathcal{N}$ è sì un insieme infinito, ma non è ancora l'insieme ℕ che stiamo cercando. Tramite una dimostrazione omessa è possible dimostrare l'esistenza di un insieme ℕ infinito che contiene solo le codificazioni dei numeri naturali.

### <font color=B292D6>Assioma dell'insieme potenza </font>
$$\forall X,\exists Y,\forall Z,\ (Z\in Y\iff Z\subseteq X) $$
L'assioma afferma l'esistenza di un insieme Y (chiamato o $2^x$ o $\rho (X)$) a cui appartengono tutti i sottoinsiemi (Z) di X
Esempio: $2^{\{1,2\}}=\{\varnothing ,\{1\},\{2\},\{1,2\}\}$
### <font color=B292D6>Assioma di regolarità (o fondazione)</font>
Infine gli ultimi due assiomi vengono presentati solo in maniera discorsiva, entrambi introducono concetti importanti ma non sono il focus del corso.

L'assioma di regolarità afferma ogni insieme non vuoto ha un elemento dal quale è disgiunto.

Conseguenze: Nessun insieme contiene ricorsivamente sé stesso, per cui ha senso andare ad analizzare la taglia di un insieme (cardinalità). 
### <font color=B292D6>Assioma di rimpiazzamento </font>
L'immagine di un insieme descritto tramite una funzione applicata ad un altro insieme è anche quello un insieme.
Se A è un insieme "piccolo" e vado a descrivere una funzione che mette in una relazione molti-a-uno gli elementi di un altro insieme, l'insieme immagine è altrettanto "piccolo".

