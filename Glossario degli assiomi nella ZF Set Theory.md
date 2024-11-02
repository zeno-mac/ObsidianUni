### <font color=B292D6>Assioma di estensionabilità</font>

$\forall X,\forall Y,(X=Y\iff \forall Z,(Z\in X\iff Z\in Y)$
### <font color=B292D6>Definizione di sottoinsieme</font>
$A\subseteq B \overset{\text{def}}{=}\forall Z,(Z\in A\to Z\in Y)$
### <font color=B292D6>Assioma di separazione</font>
$\forall X, \exists Y, \forall Z,(Z\in Y\iff Z\in X \land P(Z))$
Se $Y=(Z\in X|P(Z))$ allora:  $\forall X, \forall Z,(Z\in \{W\in X|P(W\}) \iff Z\in X \land P(Z))$
###  <font color=B292D6>Assioma dell’insieme vuoto</font>
$\exists X,\ \forall Z,\ Z\notin X$ oppure $\forall Z,\ Z\notin \varnothing$
##### <font color=C8A2C8>Definizione dell’insieme vuoto</font>
Assioma presente per la didattica: nella vera ZF Set Theory:
$\varnothing \overset{\text{def}}{=}\{X\in Y|false\}$
### <font color=B292D6>Intersezione</font>
$A\cap B \overset{\text{def}}{=}\{X\in A|X\in B\}$
##### <font color=C8A2C8>Teorema dell'intersezione binara</font>
$X\in A\cap B\iff X\in A\land X\in B$
##### <font color=C8A2C8>Intersezione n-aria</font>
$A_1\cap...\cap _n=(...((A_1\cap A_2)\cap A_3)...\in A_n)$
##### <font color=C8A2C8>Definizione di intersezione generale</font>
$\bigcap F\overset{\text{def}}{=}\varnothing \quad se\quad   F=\varnothing \\\bigcap F\overset{\text{def}}{=}\{ X\in A|\forall Y,\ (Y\in F \to X\in Y)\} \quad dove \quad A\in F$
$\bigcap F = \bigcap _{Y\in F}Y$,   _Esempio_:  $\bigcap _{Y\in \{A,B,C\}}Y=A\cap B\cap C$
### <font color=B292D6>Assioma dell’unione</font>
$\forall F,\  \exists X, \ \forall Z, \ (Z\in X\iff \exists Y, (Y\in F\land Z\in Y))$
$\bigcup F=\bigcup_{Y\in F}Y$
##### <font color=C8A2C8>Teorema dell’unione binaria</font>
$\forall A, \ \forall B,\ \forall Z,(Z\in A\cup B\iff Z\in A \lor Z\in B)$
### <font color=B292D6>Assioma del singoletto</font>
$\forall X,\ \exists Y, \ \forall Z,\ (Z\in Y \iff Z=X)$  oppure  $\forall X,\ \forall Z,\ (Z\in \{ X\}\iff Z=X)$
##### <font color=C8A2C8>Teorema dell’unione binaria</font>
Assioma presente per la didattica, dimostrazione del vero teorema omesso
### <font color=B292D6>Costruzione dei numeri naturali</font>
$[\![0]\!] \overset{\text{def}}{=} \varnothing \qquad[\![n]\!] \overset{\text{def}}{=} [\![n]\!]\cup \{[\![n]\!]\}$
### <font color=B292D6>Assioma dell'infinito</font>
$\exists Y,(\varnothing \in Y\land \forall N,\ (N\in Y\to N\ \cup \{N\}\in Y ))$
### <font color=B292D6>Assioma dell'insieme potenza </font>
$\forall X,\exists Y,\forall Z,\ (Z\in Y\iff Z\subseteq X)$
$Y=2^x\ o \ \rho (X)$ 
### <font color=B292D6>Assioma di regolarità (o fondazione)</font>
Ogni insieme non vuoto ha un elemento dal quale è disgiunto.
### <font color=B292D6>Assioma di rimpiazzamento </font>
L'immagine di un insieme descritto tramite una funzione applicata ad un altro insieme è anche quello un insieme.
