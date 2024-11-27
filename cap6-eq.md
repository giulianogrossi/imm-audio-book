Equalizzazione
====

---

## Introduzione


L'equalizzazione audio si riferisce al processo di modellazione delle frequenze di un segnale audio. Con l'equalizzatore è possibile utilizzare dei filtri per aumentare o ridurre selettivamente determinate frequenze al fine di ottenere il suono desiderato. Il processo di equalizzazione è sia una scienza che un'arte: un'attenta regolazione può eliminare i rumori indesiderati, aggiungere ariosità e chiarezza alle voci, enfatizzare il suono di una grancassa o ridurre la confusione causata da più strumenti che si scontrano nella stessa gamma di frequenze. Inoltre, l'equalizzazione può essere utilizzata per effetti creativi, come l'emulazione del suono distinto di una telefonata nella voce. La versatilità dell'equalizzatore è vastissima ed esploreremo le sue numerose applicazioni nelle prossime discussioni. Per il momento, concentriamoci sulle basi di questo strumento fondamentale.  

Gli equalizzatori (EQ) sono onnipresenti negli apparecchi audio, che si tratti di un semplice controllo dei toni su uno stereo, un equalizzatore grafico multibanda hi-fi, una banda di equalizzazione parametrica in un pedale per chitarra, oppure si tratti di sistemi audio analogici, digitali, domestici, automobilistici, pubblici o di registrazione/mixaggio in studio.
Sebbene basati sugli stessi principi, gli equalizzatori hanno scopi diversi a seconda del contesto. Nei sistemi di riproduzione, gli equalizzatori servono a cancellare eventuali effetti di filtraggio indesiderati dovuti all'attrezzatura coinvolta (altoparlanti, amplificatori, ecc.) o all'acustica della stanza. I musicisti utilizzano gli equalizzatori per modellare il proprio suono, ovvero come parte di un'espressione musicale. Gli equalizzatori sono costruiti utilizzando filtri lineari tempo-invarianti (a condizione che i controlli non vengano modificati). Esistono due tipi di equalizzatori: `grafici` e `parametrici`. 
 
 ```{card}
:header: EQ Grafici
:footer: 
Gli equalizzatori grafici sono il tipo più comune, in cui la banda audio è divisa in un numero fisso di bande di frequenza e la quantità di equalizzazione in ciascuna banda è controllata da un filtro passa-banda il cui guadagno può essere variato verso l'alto e verso il basso. Le frequenze centrali delle bande e le larghezze 3-dB del filtro sono fisse e l'utente può variare solo il guadagno complessivo di ciascuna banda. In genere, i filtri passa-banda del secondo ordine sono adeguati per le applicazioni audio. Negli equalizzatori grafici, pertanto, una risposta in frequenza desiderata (ovvero l'attenuazione e l'amplificazione di determinate frequenze) si ottiene modificando il guadagno su un insieme di frequenze centrali fisse.
```

```{card}
:header: EQ Parametrici
:footer: 
Negli equalizzatori parametrici, la risposta in frequenza desiderata viene ottenuta utilizzando un certo numero di bande, ognuna delle quali può essere controllata tramite una frequenza centrale, una larghezza di banda e un guadagno (o altri parametri simili). Collegando in cascata quattro o cinque filtri di questo tipo è possibile ottenere quasi tutti gli effetti di equalizzazione desiderati.
```

---

## Equalizzazione audio

L’equalizzazione è uno strumento fondamentale nella produzione audio e svolge ruoli diversi a seconda delle fasi di lavorazione. Può essere considerato il “coltellino svizzero” dell’audio, capace sia di realizzare regolazioni sottili che di apportare cambiamenti radicali in vari momenti della produzione. In ogni contesto, l’EQ risponde a esigenze specifiche: creare nuovi suoni, bilanciare le tracce o perfezionare il mix finale per gli ascoltatori. Di seguito una panoramica:

**Equalizzazione nel Sound Design**

Nel sound design, l’equalizzazione è uno strumento estremamente versatile che va oltre il semplice miglioramento o pulizia dell’audio. Viene usato per modellare creativamente i suoni in modo da adattarli al contesto narrativo o evocare atmosfere specifiche. Ad esempio, l’EQ può simulare ambienti diversi, come far sembrare che un suono provenga da dietro una porta chiusa attenuando le alte frequenze. Un’altra tecnica comune è l’effetto “telefono”, ottenuto con un filtro passa-banda per imitare la risposta in frequenza limitata di un vecchio telefono. I sound designer utilizzano frequentemente l’EQ per creare illusioni di distanza o riprodurre l’acustica di spazi differenti, rendendolo essenziale nella costruzione di ambienti audio immersivi.

**Equalizzazione nel Mixing**

Durante la fase di mixaggio, l’equalizzazione viene utilizzato principalmente per bilanciare le singole tracce all’interno di una canzone. Permette di ritagliare uno spazio unico per ogni strumento o parte vocale, evitando che si sovrappongano nello stesso intervallo di frequenze. Con l’EQ, si può migliorare la chiarezza, rimuovere le frequenze “fangose” e modellare il tono di ciascun elemento per contribuire in modo efficace al mix complessivo. L’obiettivo è creare coesione tra i vari componenti, assicurandosi che ognuno sia udibile chiaramente senza sovrastare gli altri.

**Equalizzazione nel Mastering**

Nel mastering, l’equalizzazione assume un ruolo leggermente diverso. Viene utilizzato per perfezionare il suono complessivo di una traccia o di un album. L’obiettivo è ottenere una risposta in frequenza bilanciata sull'intero mix, garantendo che suoni bene su tutti i sistemi di riproduzione. L’equalizzazione nel mastering implica regolazioni sottili per migliorare il tono generale del mix, correggere piccoli squilibri e garantire coerenza tra i brani di un album.

Come abbiamo visto, l’equalizzazione è uno strumento imprescindibile per qualsiasi produttore musicale, essenziale per modellare e perfezionare il suono delle tracce. Dall'analisi delle bande di frequenza all’utilizzo dei parametri e delle tecniche dell’equalizzazione, si rammenta che l’efficacia dell’equalizzazione si basa su equilibrio e sottigliezza. Non si tratta solo di far suonare bene gli elementi singolarmente, ma di garantire che lavorino insieme per creare un mix coeso e armonioso. Che si stia aumentando le frequenze per aggiungere brillantezza o tagliando per ridurre le frequenze indesiderate, ogni regolazione dovrebbe servire il fine ultimo di migliorare il paesaggio sonoro complessivo.

Di seguito vengono presentati, in linea teorica, i principali modelli di filtro utilizzati per questo scopo, tra cui i filtri peak e notch, l’EQ parametrico e i filtri shelving passabasso e passaalto.

##### Filtri peak e notch del II ordine

Nel capitolo precedente abbiamo visto il progetto del filtro risonatore utilizzando la tecnica del posizionamento di poli e zeri. L'idea base è quella di collocare una coppia di poli con raggio $R$ e angolo $\pm \omega_0$ all'interno della circonferenza unitaria, cioè 

$$
p = R e^{j \omega_0} \quad \text{e} \quad p^* = R e^{-j \omega_0}
$$

dove $^*$ indica il complesso coniugato. Una leggera generalizzazione del filtro a risonatore consiste nel posizionare anche una coppia di zeri vicino ai poli lungo le stesse direzioni dei poli, cioè in corrispondenza delle posizioni:

$$
\rho=r e^{j \omega_0} \quad \text{e} \quad \rho^* = r e^{-j \omega_0}
$$

dove $r$ è ristretto al range $0 \leq r \leq 1$. La funzione di trasferimento diventa così:


\begin{align}
H(z) &= \frac{(1 - \rho z^{-1})(1 - \rho^* z^{-1})}{(1 - p z^{-1})(1 - p^* z^{-1})}\\
&=\frac{(1 - r e^{j \omega_0} z^{-1})(1 - r e^{-j \omega_0} z^{-1})}{(1 - R e^{j \omega_0} z^{-1})(1 - R e^{-j \omega_0} z^{-1})}\\
&= \frac{1 + b_1 z^{-1} + b_2 z^{-2}}{1 + a_1 z^{-1} + a_2 z^{-2}} 
\end{align}

dove i coefficienti del filtro sono dati in funzione dei parametri $r$, $R$ e $\omega_0$:

\begin{align}
&b_1=-2r\cos(\omega_0),&\qquad &b_2=r^2&\\
&a_1=-2R\cos(\omega_0),&\qquad &a_2=R^2&
\end{align}

La posizione di zeri e poli è mostrata figura. 

![](images/risonatoreII.png)

La figura mostra il comportamento del filtro per un dato fasore $e^{j\omega}$ in relazione alla sua prossimità o meno alla coppia polo/zero. Quando $r < R$, il polo “vince” sullo zero, nel senso che è più vicino al cerchio unitario rispetto allo zero, dando luogo a un picco nella risposta in frequenza a $\omega= \omega0$. Il caso del risonatore può essere considerato come un caso speciale con $r = 0$. Quando $r > R$, lo zero vince sul polo, dando luogo a una caduta nella risposta in frequenza. In particolare, se $r = 1$, si ottiene uno zero esatto, una tacca, in corrispondenza di $\omega= \omega0$. Quando il polo e lo zero sono molto vicini, cioè $r\approx R$, la risposta in frequenza rimane essenzialmente piatta per frequenze lontane da $\omega=±\omega_0$, perché le distanze del fasore $e^{j\omega}$ dalle coppie polo/zero sono pressoché uguali, il che fa pensare che un filtro di questo tipo può essere considerato un semplice equalizzatore parametrico, che fornisce un “boost” se $r < R$, o un “cut” se $r > R$. L'altezza del boost o del cut rispetto a 1 è controllata dalla vicinanza di $r$ a $R$. L'ampiezza dei picchi o delle cadute è controllata dalla vicinanza di $R$ al cerchio unitario.

I filtri qui descritti sono semplici, offrono un'dea chiara su come il filtro opera, tuttavia questa tecnica è adeguata solo nel caso di larghezza di banda ridotta. Ma diventa complicata per larghezze di picco maggiori, come quelle che potrebbero essere utilizzate negli equalizzatori audio grafici e parametrici. Il metodo della trasformazione bilineare (non discusso qui) offre un controllo preciso sulle specifiche desiderate per tali filtri. Descriviamo da qui in poi pertanto una famiglia di filtri notch e peak ottenuti con detta tecnica e che rivelano caratteristiche più adeguate all'equalizzazione generale.  

Se denotiamo con $H_{\text{notch}}(z)$ e $H_{\text{peak}}(z)$ le funzioni di trasferimento dei filtri `notch` e `peak`, e con $G_0$ e $G$ i loro guadagni alle varie frequenze, allora $G$ rappresenta l'amplificazione alla frequenza centrale del filtro rispetto a $G_0$. Quest'ultimo è spesso scelto come costante negli equalizzatori e può essere semplicemente impostato a 1, ovvero $G_0 = 1$, e viene talvolta chiamato livello. Si ottiene un `boost` selezionando $G > G_0$ e un `cut` con $G < G_0$. Come mostrato figura, i guadagni relativi devono essere scelti come segue, a seconda che si tratti di un boost o di un cut:

$$G^2_0 < G^2_B < G^2 \text{ (boost)}$$ 
$$G_2 < G^2_B < G^2_0 \text{ (cut)}$$ 

![](images/boostcut.png)

I filtri peak e notch condividono un certo numero di parametri (da qui il termine parametrico), ovvero la larghezza di banda $\Delta \omega$, la frequenza centrale $\omega_0$ e $G$, che possono essere regolati dall'utente. Queste quantità digitali sono legate a quelle analogiche secondo le relazioni:

$$\label{eq:omega}
\omega_0 = 2\pi \frac{f_0}{f_s} \qquad \text{e} \qquad \Delta \omega = 2\pi \frac{\Delta f}{f_s},
$$

dove $F_s$ è la frequenza di campionamento e $f_0$ e $\Delta f$ sono la frequenza centrale e la larghezza di banda (in Hz). In un equalizzatore grafico, queste quantità sono fissate per ogni banda e l'utente può solo modificare $G$. La frequenza centrale e la larghezza di banda sono legate ai bordi della banda, chiamati frequenze di taglio $\omega_1$ e $\omega_2$ (con $\omega_2 > \omega_1$), come segue:

$$
\omega_0 = \sqrt{\omega_1 \omega_2} \quad \text{e} \quad \Delta \omega = \omega_2 - \omega_1, 
$$

cioè, la frequenza centrale è la media geometrica di $\omega_1$ e $\omega_2$, mentre la larghezza di banda è semplicemente la differenza tra le due. Si noti che gli equivalenti analogici di queste quantità, ovvero $f_1$ e $f_2$, sono correlati a $\omega_1$ e $\omega_2$ in modo simile a quanto indicato in [](eq:omega).


![](images/bandwidth.png)


Un filtro notch con frequenza centrale $\omega_0$ ha una funzione di trasferimento che si presenta come segue:

$$
H_{\text{notch}}(z) = \frac{b \big(1 - 2 \cos \omega_0 z^{-1} + z^{-2} \big)}{1 - 2b \cos \omega_0 z^{-1} + (2b - 1)z^{-2}},
$$

che può essere visto come un filtro IIR di secondo ordine. La quantità $b$, che rappresenta il guadagno, è data da:

$$
b = \frac{1}{1 + \beta},
$$

dove

$$
\beta = \frac{\sqrt{1 - G_B^2}}{G_B} \tan \frac{\Delta \omega}{2},
$$

e $G_B$ è il guadagno alle frequenze di taglio $\omega_1$ e $\omega_2$. Per ottenere frequenze di taglio a -3 dB, possiamo semplicemente scegliere $G_B^2 = 0.5$. 

Il filtro notch è definito dalla seguente equazione alle differenze:

$$
y(n) = b x(n) - 2b \cos \omega_0 x(n-1) + b x(n-2) + 2b \cos \omega_0 y(n-1) - (2b - 1)y(n-2). 
$$

Per implementarlo, è sufficiente scegliere $\omega_0$ e calcolare $b$, che viene determinato selezionando una larghezza di banda $\Delta \omega$. 

In figura sono mostrati alcuni esempi di risposte in modulo di filtri notch. Questi sono rappresentati per una frequenza centrale di $\omega_0 = \pi / 2$ e per larghezze di banda variabili con $G_B^2 = 0.5$.

![]()

Una analoga descrizione può essere data per il filtro peak. Esso  amplifica il segnale a una determinata frequenza, che corrisponde alla frequenza centrale $\omega_0$ del filtro. La sua funzione di trasferimento è la seguente:

$$
H_{\text{peak}}(z) = \frac{(1 - b)(1 - z^{-2})}{1 - 2b \cos \omega_0 z^{-1} + (2b - 1)z^{-2}},
$$

dove, similmente al filtro notch, il guadagno $b$ è dato da:

$$
b = \frac{1}{1 + \beta},
$$

con

$$
\beta = G_B \frac{\sqrt{1 - G_B^2}}{\tan \frac{\Delta \omega}{2}}.
$$

Come si può vedere, il filtro peak è anch'esso un filtro IIR di secondo ordine. Si noti che il termine $z^{-1}$ non compare nel numeratore di questo filtro. Il parametro $\Delta \omega$ rappresenta, come nel caso del filtro notch, la larghezza di banda del filtro peak alla frequenza centrale $\omega_0$, e $G_B$ è il guadagno alle frequenze di taglio, che può essere scelto come $G_B^2 = 0.5$ per ottenere frequenze di taglio a -3 dB. 

Anche il filtro peak è ottenuto da un filtro analogico tramite la cosiddetta trasformazione bilineare $z$. Esso soddisfa la seguente equazione alle differenze:

$$
y(n) = (1 - b)x(n) - (1 - b)x(n-2) + 2b \cos \omega_0 y(n-1) - (2b - 1)y(n-2), 
$$

che può essere facilmente implementata una volta scelte $\Delta \omega$ e $\omega_0$, e calcolato $b$ a partire dall'espressione sopra. 

In figura sono mostrati alcuni esempi di risposte in modulo per il filtro peak.

![]()

Le risposte dei filtri peak sono mostrate. Sono rappresentate le risposte per una frequenza centrale di $\omega_0 = \pi/2$ e per larghezze di banda variabili con $G_B^2 = 0.5$.

##### Filtro Equalizzatore Parametrico

Procediamo ora a combinare i filtri \textit{peak} e \textit{notch} che abbiamo appena introdotto, come descritto in (10.1). Questo si ottiene inserendo (10.4) e (10.7) in (10.1). Tuttavia, prima osserviamo che possiamo combinare i due filtri come segue: sia

$$
H_{\text{notch}}(z) = \frac{A(z)}{B(z)}\qquad \text{e}\qquad H_{\text{peak}}(z) = \frac{C(z)}{D(z)},
$$

allora possiamo combinare i due filtri in un unico filtro come

$$
H_{\text{eq}}(z) = G_0 H_{\text{notch}}(z) + G H_{\text{peak}}(z),
$$

cioè

$$
H_{\text{eq}}(z) = G_0 \frac{A(z)}{B(z)} + G \frac{C(z)}{D(z)},
$$

che può essere ulteriormente scritto come

$$
H_{\text{eq}}(z) = \frac{G_0 A(z)D(z) + G C(z)B(z)}{B(z)D(z)}.
$$

Quando si combinano i due filtri, è interessante notare che

$$
H_{\text{notch}}(z) + H_{\text{peak}}(z) = 1,
$$

il che significa che i due filtri con $G_0 = 1$ e $G = 1$ non alterano il segnale in ingresso. I filtri sono quindi detti complementari. Se scegliamo $G_0 = 0$ e $G = 1$, otteniamo un filtro peak; viceversa, impostando $G_0 = 1$ e $G = 0$, otteniamo un filtro notch dal nostro filtro equalizzatore parametrico. Pertanto, il filtro è molto flessibile e include, come casi speciali, i filtri peak e notch, oltre a un'impostazione neutra che non altera il segnale.

Prima di procedere alla combinazione dei due filtri, dobbiamo considerare come scegliere il parametro di guadagno $G_B$. Esistono diversi modi per farlo. Tuttavia, è utile (e comune) impostarlo in relazione a $G$ e $G_0$ come media aritmetica o media geometrica delle due, cioè:

$$
G_B^2 = \frac{G^2 + G_0^2}{2}.
$$

oppure

$$
G_B^2 = G G_0.
$$

Utilizzando il principio menzionato in precedenza per combinare i due filtri, otteniamo:

$$
H_{\text{eq}}(z) = 
\frac{
\frac{G_0 + G \beta}{1 + \beta} 
- \frac{2 G_0 \cos \omega_0}{1 + \beta} z^{-1} 
+ \frac{G_0 - G \beta}{1 + \beta} z^{-2}
}{
1 - \frac{2 \cos \omega_0}{1 + \beta} z^{-1} 
+ \frac{1 - \beta}{1 + \beta} z^{-2}
}, 
$$

dove $\beta$ è ora definito come

$$
\beta = 
\frac{G_B^2 - G_0^2}{G^2 - G_B^2} 
\tan \frac{\Delta \omega}{2}. 
$$

Se $G_0^2 < G_B^2 < G^2$, abbiamo un boost alla frequenza $\omega_0$, mentre se $G^2 < G_B^2 < G_0^2$, abbiamo un cut. 

Se utilizziamo la media aritmetica in (10.16) per la definizione di $G_B$, si può facilmente vedere che:

$$
\frac{G_B^2 - G_0^2}{G^2 - G_B^2} = 1, 
$$

in tal caso si ha che $\beta = \tan \frac{\Delta \omega}{2}$. Una volta scelti $\omega_0$ e $\Delta \omega$, è relativamente semplice calcolare i coefficienti del filtro. La differenza risultante è data da:

$$
y(n) = \frac{G_0 + G \beta}{1 + \beta} x(n) 
- \frac{2 G_0 \cos \omega_0}{1 + \beta} x(n-1).
$$

$$
y(n) = \frac{G_0 + G \beta}{1 + \beta} x(n) 
- \frac{2 G_0 \cos \omega_0}{1 + \beta} x(n-1) 
+ \frac{G_0 - G \beta}{1 + \beta} x(n-2) 
+ \frac{2 \cos \omega_0}{1 + \beta} y(n-1) 
- \frac{1 - \beta}{1 + \beta} y(n-2).
$$

In figura sono mostrati alcuni esempi di risposte in frequenza di filtri equalizzatori parametrici per diversi valori di guadagno, $G$. I filtri mostrati hanno tutti una frequenza centrale di $\omega_0 = \pi/2$, una larghezza di banda di $\Delta \omega = \pi/4$ con $G_B = \sqrt{G G_0}$ e $G_0 = 1$.

![]()


##### Filtro Shelving 

Per trattare le frequenze molto basse e molto alte nel segnale audio, è utile introdurre i cosiddetti filtri shelving. Questi sono filtri che presentano una risposta piatta e un guadagno regolabile rispettivamente a basse o alte frequenze. Il filtro con risposta piatta alle basse frequenze è spesso chiamato `low-pass shelving filter`, mentre quello per le alte frequenze è chiamato `high-pass shelving filter`. Questi possono essere ottenuti dal filtro equalizzatore parametrico generale in (10.17) sostituendo la frequenza centrale, $\omega_0$, con $0$ o $\pi$.

Per il filtro `low-pass (LP) shelving`, inseriamo $\omega_0 = 0$ in (10.17). Poiché $\cos \omega_0 = 1$, otteniamo un filtro più semplice, cioè:

$$
H_\text{lp}(z) = 
\frac{G_0 + G \beta}{1 + \beta} 
- \frac{G_0 - G \beta}{1 + \beta} z^{-1} 
\Bigg/ 
\left( 1 - \frac{1 - \beta}{1 + \beta} z^{-1} \right),
$$

che è un filtro del primo ordine. Al posto della larghezza di banda $\Delta \omega$, ora abbiamo una singola frequenza di taglio, che chiamiamo $\omega_c$, e un corrispondente guadagno $G_C$, che sostituisce $G_B$ ma viene calcolato allo stesso modo usando (10.16). La quantità $\beta$ nelle equazioni sopra è quindi determinata da questa relazione:

$$
\beta = 
\frac{G_C^2 - G_0^2}{G^2 - G_C^2} 
\tan \frac{\omega_c}{2}.
$$

Tuttavia, come in precedenza, con la definizione di $G_C$ in (10.16), questa espressione si semplifica a qualcosa di più semplice che dipende solo dalla larghezza di banda. Va sottolineato che il filtro equalizzatore parametrico generale in (10.17) può essere utilizzato direttamente con le modifiche sopra descritte.

Le sostituzioni descritte qui permettono di non dover utilizzare una implementazione separata per i filtri shelving. Per il filtro low-pass shelving, l'equazione alle differenze risultante è quindi:

$$
y(n) = \frac{G_0 + G \beta}{1 + \beta} x(n) 
- \frac{G_0 - G \beta}{1 + \beta} x(n-1) 
+ \frac{1 - \beta}{1 + \beta} y(n-1).
$$

Per il filtro high-pass shelving (HP), inseriamo $\omega_0 = \pi$ in (10.17). Considerando che $\cos \omega_0 = -1$, si ottiene:

$$
H_\text{hp}(z) = 
\frac{G_0 + G \beta}{1 + \beta} 
+ \frac{G_0 - G \beta}{1 + \beta} z^{-1} 
\Bigg/ 
\left( 1 + \frac{1 - \beta}{1 + \beta} z^{-1} \right).
$$

La definizione della larghezza di banda è leggermente diversa in questo caso. Qui è data da $\Delta \omega = \pi - \omega_c$. Considerando che $\tan \frac{\pi - \omega_c}{2} = \cot \frac{\omega_c}{2}$, $\beta$ per il filtro high-pass shelving risulta:

$$
\beta = 
\frac{G_C^2 - G_0^2}{G^2 - G_C^2} 
\cot \frac{\omega_c}{2}.
$$

Infine, l'equazione alle differenze per il filtro high-pass shelving è:

$$
y(n) = \frac{G_0 + G \beta}{1 + \beta} x(n) 
+ \frac{G_0 - G \beta}{1 + \beta} x(n-1) 
- \frac{1 - \beta}{1 + \beta} y(n-1).
$$

Infine, in Fig. 10.6 sono mostrati alcuni esempi di risposte in frequenza di filtri shelving per guadagni $G$ variabili. Sono mostrati sia i filtri low-pass che high-pass. Per il filtro low-pass shelving, la frequenza di cutoff è $\omega_c = \frac{\pi}{4}$, mentre per il filtro high-pass shelving è $\omega_c = \frac{3\pi}{4}$. In entrambi i casi, il guadagno $G_C$ è dato da:

$$
G_C = \sqrt{G G_0},
$$

con $G_0 = 1$.

---

## Pratica comune

Tutti i filtri che abbiamo considerato in questo capitolo sono casi speciali di un filtro IIR generale del secondo ordine, della forma:
\[
y(n) = b_0 x(n) + b_1 x(n-1) + b_2 x(n-2) + a_1 y(n-1) + a_2 y(n-2).
\]
L'unica differenza tra i vari filtri risiede nella scelta dei coefficienti.

Un diagramma a blocchi della struttura del filtro che può essere utilizzata per implementare i filtri equalizzatori è mostrato in figura. 

![]()

Nella Tabella 1, sono elencati i coefficienti dei filtri per i vari casi insieme alla definizione appropriata di \(\beta\). Se scegliamo la definizione di \(G_B\) in \((10.16)\), ossia:
\[
G_B^2 = \frac{G^2 + G_0^2}{2},
\]
le varie definizioni di \(\beta\) risultano semplificate. Inoltre, con una scelta del livello unitario, ossia \(G_0 = 1\), l'espressione è ulteriormente semplificata, e i coefficienti risultanti del filtro sono riportati in Tabella~10.2. Per un rapido riferimento, i parametri utente dei vari filtri sono elencati in Tabella~10.3.

Si noti che, invece della larghezza di banda, \(\Delta \omega\), è possibile utilizzare il cosiddetto fattore \(Q\), definito come:
\[
Q = \frac{\omega_0}{\Delta \omega},
\]

![](images/tabelle_eq.png)



un approccio utilizzato in alcune implementazioni di equalizzatori parametrici. Il fattore \(Q\) controlla la selettività del filtro rispetto alla frequenza centrale. Ciò significa che per una bassa frequenza centrale, un valore costante di \(Q\) risulterà in una larghezza di banda inferiore rispetto alle frequenze più alte. Questo è ben in linea con le proprietà del sistema uditivo umano, in particolare il modo in cui la larghezza di banda è percepita in funzione della frequenza centrale.

Per concludere, osserviamo che, come già detto, i filtri progettati in base ai principi qui descritti devono essere collegati in serie. Se vengono collegati in parallelo, i filtri non daranno il risultato desiderato a causa dell'effetto della risposta di fase dei filtri. Esistono tuttavia altri tipi di filtri equalizzatori che possono essere collegati in parallelo. Inoltre, esistono anche progetti di equalizzatori FIR per l'audio, sebbene i filtri IIR qui presentati siano in genere più efficienti dal punto di vista computazionale.