## <font color=8A5BA6>Introduzione</font>
### <font color=B292D6>Definizioni generale</font>

- **Proposizione:** frase sui cui ha senso interrogarsi se valga o meno;
- **Linguaggio formale:** linguaggio artificiale creato per poter descrivere le dimostrazioni senza ambiguità, composto da:
	- Formule logiche;
	- **Enunciato:** proposizione da dimostrare tramite prova;
	- **Teorema:** enunciato dimostrato corretto;
	- **Lemma:** teorema ancillare, sotto-teorema introdotto solo per una dimostrazione più importante;
	- **Corollario:** teoremi secondari dalla dimostrazione semplice una volta che il teorema principale è stato dimostrato;
	- **Conclusione:** enunciato da dimostrare;
	- **Premessa:** Enunciato che assumiamo in quanto ipotesi o dimostrato in precedenza;
- **Ragionamento ipotetico:** Nelle dimostrazioni vado a restringere i casi i in cui una certa proposizione (P) valga tramite ipotesi. Se ipotizzo (o suppongo) P non mi interrogo se P vale o meno perché non è di mio interesse al momento.
	- Esempio: per dimostrare $P\to Q$ posso ipotizzare P, non mi interessa dimostrare che P valga, mi interessa dimostrare che se P vale allora vale anche Q

### <font color=B292D6>Sintassi della logica del prim'ordine</font>

- $\top$ : vero, vale in qualsiasi caso;
- $\bot$: falso, assurdo, non vale mai;
- **Predicati applicati (**$\leq, \geq, =...$**):** se applicati a delle proposizione possono valere o meno;
- $P\land Q$: e, congiunzione, vale se sia $P$ che $Q$ valgono;
- $P\lor Q$: o, disgiunzione, vale almeno una delle due formule valgono;
- $P\to Q$: se $P$ allora $Q$, implicazione logica, vale se sotto l'ipotesi $P$ vale sempre $Q$. Non indica un rapporto di causalità!!
- $\lnot P$: non $P$, vale se $P\to \bot$;
- $P\iff Q$: se e solamente, sse, coimplicazione, vale se valgono sia $P\to Q$ che $Q\to P$;
- $\forall x\ P$: per ogni $x\ P$, quantificatore universale, vale se $P$ vale per ogni $x$;
- $\exists x\ P$: esiste $x\ P$, quantificatore esistenziale, vale se $P$ vale per almeno un $x$

Questa è una spiegazione Tarskiana della logica, utile come introduzione. Non è eccellente perché per spiegare le formule della logica ci rifacciamo alle stesse ($P\land Q$  vale se vale $P$ e $Q$)
### <font color=B292D6>Precedenza e associatività</font>

- **Precedenza** (in ordine decrescente: $\lnot,\land,\lor,\to,\iff$;
- **Associatività a destra:** $\land,\lor,\to,\iff$
### <font color=B292D6>Connettivi e quantificatori</font>

- **Connettivo:** costruisce una nuova proposizione a partire da elementi dati;
- **Arietà:** numero di proposizioni che un connettivo prende in "input";
- **Connettivi 0-ari:** $\top,\bot$;
- **Connettivi unari:** $\lnot$;
- **Connettivi binari:** $\land,\lor,\to,\iff$;
- **Quantificatori:** $\forall,\exists$.

### <font color=B292D6>Regole d'introduzione e di eliminazione</font>

- **Introduzione:** se devo dimostrare un enunciato con un certo connettivo  posso (o devo) usare una delle sue regole d'introduzione per ridurmi a poter dimostrare cose più semplici:
	- Esempio: per dimostrare $P\land Q$ posso dimostrare $P$ e $Q$ singolarmente.
- **Eliminazione:** se ho un ipotesi con un certo connettivo, posso (o devo) usare una delle sue d'eliminazioni per aiutarmi nella dimostrazione:
	- Esempio: se so $P\land Q$ allora saprò (come ipotesi locale) che sia $P$ sia $Q$ valgono singolarmente

## <font color=8A5BA6>Regole per ogni connettivo</font>

### <font color=B292D6>Per ogni </font> $\forall x\ P(x)$
 - Introduzione: Se devo dimostrare $\forall x\ P(x)$ posso assumere una $x$ di cui non so niente e limitarmi a dimostrare $P(x)$  
	 - Nelle dimostrazioni: "Sia $x$ (un insieme fissato); ..."
	 - In Lean: "Assume $x$: set"
 - Eliminazione: Se so che $\forall x$ vale $P(x)$ allora posso prendere un qualsiasi elemento e concludere che $P$ 
### <font color=B292D6>Implicazione </font> $P\to Q$
 - Introduzione: 
	 - Nelle dimostrazioni: 
	 - In Lean: 
 - Eliminazione:  
	 - Nelle dimostrazioni: 
	 - In Lean: 
### <font color=B292D6>Comimplicazione </font> $P\iff Q$
 - Introduzione: 
	 - Nelle dimostrazioni: 
	 - In Lean: 
 - Eliminazione:  
	 - Nelle dimostrazioni: 
	 - In Lean: 
### <font color=B292D6>Assurdo </font> $\bot$
 - Introduzione: 
	 - Nelle dimostrazioni: 
	 - In Lean: 
 - Eliminazione:  
	 - Nelle dimostrazioni: 
	 - In Lean: 
### <font color=B292D6>Negazione </font>  $\lnot P$
 - Introduzione: 
	 - Nelle dimostrazioni: 
	 - In Lean: 
 - Eliminazione:  
	 - Nelle dimostrazioni: 
	 - In Lean: 
### <font color=B292D6>Congiunzione </font> $P\land Q$
 - Introduzione: 
	 - Nelle dimostrazioni: 
	 - In Lean: 
 - Eliminazione:  
	 - Nelle dimostrazioni: 
	 - In Lean: 
### <font color=B292D6>Or </font> $P\lor Q$
 - Introduzione: 
	 - Nelle dimostrazioni: 
	 - In Lean: 
 - Eliminazione:  
	 - Nelle dimostrazioni: 
	 - In Lean: 
### <font color=B292D6>Esiste </font> $\exists x\ P(x)$
 - Introduzione: 
	 - Nelle dimostrazioni: 
	 - In Lean: 
 - Eliminazione:  
	 - Nelle dimostrazioni: 
	 - In Lean: 
	 - 
## <font color=8A5BA6>Annotazioni generali</font>

### <font color=B292D6>Abbreviazioni </font>


