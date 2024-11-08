Spettro del segnale audio
====

---

##### Introduzione

La trasformata di Fourier è uno strumento matematico che ci permette di capire quali frequenze compongono un segnale, come un’onda sonora o un segnale elettrico. Immagina di avere una canzone e di poter “vedere” le singole note musicali che la compongono: la trasformata di Fourier fa proprio questo, prendendo un segnale e scomponendolo nelle sue parti fondamentali, le frequenze, che sono come le singole note della canzone.

In pratica, quando ascoltiamo un suono complesso (come un accordo di chitarra o il rumore del traffico), le nostre orecchie e il cervello lo scompongono automaticamente nelle frequenze dei suoni che lo compongono. La trasformata di Fourier è una versione matematica di questa operazione: prende un segnale variabile nel tempo e lo rappresenta in funzione della frequenza, rivelandoci quali componenti a frequenza bassa, media e alta sono presenti e in che quantità.

Grazie a questo, possiamo passare da una rappresentazione nel tempo (dove vediamo il segnale cambiare momento per momento) a una rappresentazione in frequenza (dove vediamo solo le “note” fondamentali che compongono il segnale). Questo è fondamentale in tanti campi, come la musica, l’ingegneria audio, le telecomunicazioni, e l’elaborazione delle immagini, perché ci permette di analizzare e manipolare i segnali in modo molto efficiente e mirato.

La Short-Time Fourier Transform (STFT) è un’estensione della trasformata di Fourier usata per analizzare segnali che cambiano nel tempo, come una traccia audio o un segnale vocale. Mentre la trasformata di Fourier classica ci dà una visione globale delle frequenze presenti in un segnale, la STFT ci permette di vedere come queste frequenze variano nel tempo. Per fare questo servirà  operare un finestramento del segnale: La STFT divide il segnale in piccole porzioni, chiamate finestre, ognuna delle quali contiene un piccolo intervallo temporale del segnale. La durata della finestra è fondamentale: deve essere abbastanza breve per catturare le variazioni del segnale, ma non così corta da rendere imprecisa l’informazione sulle frequenze.	Per ogni finestra, viene poi calcolata la trasformata di Fourier, producendo una rappresentazione in frequenza di quel breve intervallo del segnale. Questo ci dice quali frequenze sono presenti e con quale intensità in quel preciso istante temporale. Ripetendo il processo su tutto il segnale e spostando la finestra di analisi (a intervalli sovrapposti), otteniamo una serie di trasformate di Fourier locali. Il risultato è una rappresentazione in 2D detta spettrogramma, dove l’asse orizzontale rappresenta il tempo, l’asse verticale rappresenta le frequenze, e i colori o le intensità mostrano la potenza di ogni frequenza in ogni intervallo temporale.

La STFT è particolarmente utile quando abbiamo segnali non stazionari, cioè segnali le cui caratteristiche cambiano nel tempo. Esempi tipici sono: la musica in cui le frequenze cambiano nelle diverse parti di un brano musicale, l'elaborazione vocale in cui si vuole analizzare come i suoni e le parole variano nel tempo, facilitando compiti come il riconoscimento vocale; altre discipline come la sismologia, le telecomunicazioni o la biomedicina.

In sintesi, la STFT permette di ottenere una visione dinamica del contenuto in frequenza di un segnale, fornendo una rappresentazione tempo-frequenza che ci dice non solo “quali” frequenze sono presenti, ma anche “quando” esse appaiono.

---

## Frequenza, timbro e pitch nei suoni

##### Pitch
Il `pitch` (o `“altezza”`) di un suono è una qualità percepita che ci permette di distinguere se un suono è acuto o grave. È ciò che ci fa riconoscere, ad esempio, che la voce di una persona è più alta (acuta) o più bassa (grave) rispetto a un’altra, oppure che una nota suonata su un violino è più acuta di una suonata su un contrabbasso. Sebbene la frequenza sia una misura fisica e oggettiva, il pitch è una percezione umana e può variare da persona a persona o con l’età. Ad esempio, alcune persone possono percepire differenze molto sottili tra frequenze simili, mentre altre no. Inoltre, il pitch percepito può essere influenzato dal contesto sonoro e dall'esperienza dell’ascoltatore.

I fattori che influenzano il pitch sono i seguenti.
1. Frequenza: Il pitch è strettamente legato alla frequenza del suono, ovvero al numero di oscillazioni al secondo dell’onda sonora, misurato in Hertz (Hz). In generale:
   - Suoni a frequenze più alte (come quelli prodotti da un fischio o un soprano) vengono percepiti come acuti.
	- Suoni a frequenze più basse (come quelli prodotti da un tamburo o un basso) vengono percepiti come gravi. 
   - Ad esempio, la nota La standard per l’accordatura ha una frequenza di 440 Hz. Se aumentiamo la frequenza, il pitch aumenta; se la riduciamo, il pitch diminuisce.
2. Intensità: L’intensità del suono, o volume, può influenzare leggermente la percezione del pitch, soprattutto a livelli estremi. Suoni molto forti tendono a sembrare leggermente più acuti.
3.	Struttura dell’Onda Sonora: La presenza di armoniche e la forma dell’onda influenzano il pitch percepito. Alcuni strumenti, come l’organo e la chitarra, producono armoniche che fanno percepire il pitch in modo leggermente diverso, anche se la frequenza fondamentale è la stessa.

In sintesi, il pitch è una delle proprietà fondamentali del suono che ci permette di distinguere le note musicali e di identificare la tonalità di una voce o di un suono.

##### Suoni armonici

I `suoni armonici` sono suoni prodotti da onde che includono una frequenza fondamentale e una serie di armoniche, ovvero frequenze multiple della fondamentale che conferiscono un timbro caratteristico. Ecco alcuni esempi:

1.	Corde di strumenti musicali: La vibrazione di una corda (come quella di una chitarra o di un pianoforte) produce un suono armonico. Quando la corda vibra, la frequenza fondamentale si combina con le armoniche superiori, creando il suono complesso che riconosciamo come il timbro dello strumento.
2.	Voci umane: Quando parliamo o cantiamo, le corde vocali generano un suono con una frequenza fondamentale (pitch percepito) e armoniche. Queste armoniche variano a seconda della struttura e della forma del tratto vocale, dando ad ogni voce il proprio timbro unico.
3.	Fiati e ottoni: Strumenti come il flauto, il clarinetto o la tromba producono suoni armonici grazie alla vibrazione dell’aria al loro interno. La lunghezza del tubo e il modo in cui l’aria viene soffiata creano una frequenza fondamentale e armoniche che danno a ciascun strumento il proprio suono distintivo.
4.	Campane: Anche se la forma d’onda delle campane è più complessa, il suono prodotto contiene armoniche che conferiscono al suono il caratteristico timbro metallico e risonante. A differenza di strumenti a corda o fiato, le armoniche delle campane non sono perfetti multipli della fondamentale, dando loro un suono unico e inconfondibile.
5.	Organo: Gli organi creano suoni armonici combinando diverse canne, ognuna delle quali suona una frequenza fondamentale e armoniche specifiche. Variando l’insieme di canne attivate, l’organista può produrre un’ampia gamma di timbri complessi.

La seguente figura illustra lo spettro di un Do ottenuto dall'arpeggio della corda della chitarra che genera un'onda stazionaria di diverse frequenze. Si possono notare infatti al fondamentale di circa $261$ Hz e le armoniche correlate distribuite nello spettro limitato dalla frequenza di campionamento $F_s=10$ kHz.   

![do](images/do-chitarra.png)

Come si nota dalla figura, nello spettro sono presenti degli `ipertoni`, che sono le componenti di un suono complesso dotate di una frequenza superiore a quella della fondamentale. Se le frequenze degli ipertoni sono multipli interi della frequenza della fondamentale, essi si dicono armoniche. Nello spettrogramma del suono, gli ipertoni sono evidenziati dai massimi del grafico. In natura è estremamente difficile trovare un suono che contenga una sola frequenza, pertanto le note suonate dagli strumenti classici sono come degli accordi di più note, solo con l'avvento degli strumenti elettronici è possibile produrre agilmente suoni monofrequenza. In particolare, gli ipertoni si presentano negli strumenti a corda, nei fiati e nella voce umana.

In tutti questi esempi, gli ipertoni e le armoniche giocano un ruolo fondamentale nel definire la “colorazione” o timbro del suono, rendendo il suono di ciascun strumento o voce riconoscibile e unico.

##### Timbro

La `colorazione` o `timbro` del suono è la qualità che ci permette di distinguere tra suoni di uguale altezza (o pitch) e intensità, ma provenienti da sorgenti diverse. È ciò che ci fa capire, ad esempio, la differenza tra un violino e una chitarra che suonano la stessa nota, oppure tra la voce di due persone diverse. Il timbro è determinato dalle componenti armoniche e dalle caratteristiche dell’onda sonora prodotta da ciascuna sorgente sonora: la relazione tra il livello della fondamentale, i livelli delle armoniche o degli ipertoni, e la loro evoluzione nel tempo. I suoni puri tendono ad avere solo poche armoniche a bassi livelli, mentre i suoni brillanti tendono ad avere molte armoniche a livelli elevati. Anche le armoniche mancanti possono essere importanti e possono produrre timbri che suonano “vuoti”. Se i rapporti tra la frequenza della fondamentale e le altre frequenze non sono numeri interi, allora il timbro può suonare simile a quello di una campana o persino al rumore.

La capacità dell’orecchio umano di percepire il timbro è correlata alla frequenza. A basse frequenze, l’orecchio può rilevare differenze di fase e seguire i cambiamenti di un gran numero di armoniche. Man mano che la frequenza aumenta, la capacità dell’orecchio di discriminare la fase diminuisce sopra A4 (440 Hz), e il numero di armoniche udibili si riduce a causa della risposta dell’orecchio. Ad esempio, un suono con una frequenza fondamentale di 100 Hz ha armoniche a intervalli di 100 Hz, quindi la 150ª armonica si trova a 15 kHz. Ma un suono con una fondamentale di 1 kHz ha la sua 15ª armonica a 15 kHz. Il numero di armoniche udibili risulta quindi limitato all’aumentare della frequenza fondamentale. I sintetizzatori forniscono un controllo completo sulla frequenza, fase e livello delle armoniche, consentendo all’utente di controllare il timbro. Le caratteristiche del timbro si possono osservare nella seguente figura in cui la fondamentale del suono è alla frequenza $f$, mentre c’è un’armonica al doppio di questa frequenza, $2f$ e poi compare anche un ipertono o frequenza parziale a $3.75f$. 

```{image} images/timbro.png
:alt: long
:class: bg-primary mb-1
:width: 500px
:align: center
```

Alcuni dei principali fattori che contribuiscono al timbro sono:

1.	Armoniche: Quando un oggetto vibra per produrre un suono, genera una frequenza fondamentale (quella del pitch percepito) e una serie di frequenze superiori (armoniche) che sono multipli della fondamentale. La distribuzione e l’intensità di queste armoniche creano un’impronta unica per ogni strumento o voce.
2.	Forma dell’Onda Sonora: Diverse sorgenti producono onde sonore con forme diverse (onda sinusoidale, triangolare, quadra, ecc.). Queste differenze influiscono sul timbro, dando una qualità unica al suono.
3.	Attacco e Decadimento: Ogni suono ha una fase di attacco (iniziale) e di decadimento (finale). La velocità con cui il suono inizia e termina influisce sul timbro. Ad esempio, un pianoforte ha un attacco rapido, mentre un violino suona più dolcemente.
4.	Risonanze: Ogni strumento ha una particolare struttura fisica che amplifica certe frequenze più di altre. Questa risonanza naturale influenza il timbro e rende unico ogni strumento.
5.	Distorsione e Rumore Aggiuntivo: In alcuni strumenti, il rumore o la distorsione contribuiscono al timbro. Ad esempio, il soffio in un flauto o le impurità nel suono di una tromba possono aggiungere carattere al timbro.

Esempi di Timbro sono i seguenti. Un Do suonato da un pianoforte, da un flauto e da un clarinetto: anche se la nota è la stessa, la qualità del suono sarà molto diversa. Questo perché ogni strumento produce una combinazione unica di armoniche e ha un attacco e un decadimento caratteristici che ne modificano il timbro.

Il timbro è quindi fondamentale per riconoscere e differenziare le sorgenti sonore, sia negli strumenti musicali che nelle voci, arricchendo la nostra percezione sonora del mondo.

##### Suoni inarmonici

I `suoni inarmonici` sono suoni in cui le componenti frequenziali (cioè le onde che lo compongono) non sono multipli interi di una frequenza fondamentale, come avviene nei suoni armonici. Mentre nei suoni armonici le armoniche sono distribuite in modo regolare e conferiscono al suono un timbro stabile e riconoscibile, nei suoni inarmonici la distribuzione delle frequenze è irregolare, dando un timbro più complesso o, talvolta, “metallico” e “disordinato”. Esempi di suoni inarmonici sono i seguenti.

1.	Campane: Le campane producono suoni inarmonici perché le vibrazioni del loro materiale non generano frequenze multiple della fondamentale. Questo conferisce loro un suono risonante e talvolta “disperso”.
2.	Piatti e Gong: Quando si colpisce un piatto o un gong, le vibrazioni che si generano sono altamente irregolari e producono molte frequenze che non seguono una relazione armonica. Il risultato è un suono ricco, ma anche caotico e inarmonico.
3.	Bacchette e Barre Metalliche: Colpendo una barra metallica o una bacchetta, si ottiene una vibrazione complessa che non segue le armoniche naturali. I metallofoni (strumenti a barre metalliche), come il vibrafono, generano suoni che hanno una certa componente inarmonica, specialmente quando le barre non sono accordate con precisione.
4.	Suoni Naturali come il Rombo del Tuono o il Fruscio delle Foglie: Molti suoni naturali sono inarmonici, poiché non hanno una frequenza fondamentale dominante o un sistema regolare di armoniche.

I suoni inarmonici sono percepiti dall'orecchio umano come “più ruvidi” o “disordinati” rispetto ai suoni armonici. A volte vengono descritti come privi di una nota chiara o “distonici”, poiché mancano di quella chiarezza e stabilità tipica dei suoni armonici. Tuttavia, i suoni inarmonici sono molto usati in musica, specialmente per ottenere effetti specifici di tensione, mistero o drammaticità, come nelle percussioni orchestrali o nella musica elettronica.

In sintesi, i suoni inarmonici sono caratterizzati dalla mancanza di armoniche regolari e hanno un timbro complesso, spesso associato a suoni metallici, percussivi o naturali che creano un senso di instabilità o di “caos musicale.”


##### Inviluppo
I suoni non iniziano e non terminano istantaneamente. Ci vuole un tempo finito affinché una corda inizi a vibrare e un certo tempo perché essa riduca la vibrazione a uno stato stazionario. Il tempo necessario affinché un oggetto inizi a vibrare si chiama `tempo di attacco`, mentre il tempo impiegato dalla vibrazione per decrescere a uno stato stazionario è detto `tempo di decadimento`. Per gli strumenti che possono produrre un suono continuo, come l’organo, il tempo di decadimento è definito come il tempo necessario affinché il suono decresca fino al livello di sostegno stazionario, mentre la fine della vibrazione si chiama `tempo di rilascio` (in figura).

```{image} images/ADSR.png
:alt: long
:class: bg-primary mb-1
:width: 500px
:align: center
```

Alcuni strumenti hanno tempi di attacco, decadimento e rilascio lunghi: per esempio, gli strumenti a corda ad arco. Gli strumenti a corda pizzicata hanno tempi di attacco più brevi. Alcuni strumenti, come il pianoforte o le percussioni, hanno tempi di attacco molto rapidi. Tempi molto brevi sono spesso chiamati transienti. La combinazione di tutte le fasi di un suono è chiamata inviluppo e rappresenta il cambiamento del volume del suono tracciato nel tempo. Il termine inviluppo può anche essere utilizzato in un senso più ampio.

---

## Note musicali

Nella musica, il termine nota è spesso usato in modo piuttosto generico e può riferirsi sia a un simbolo musicale (quando si parla di rappresentazioni in notazione) sia a un suono con `altezza` definita (quando si parla di rappresentazioni audio). In questa sezione, utilizziamo il termine per riferirci ai simboli musicali utilizzati nella notazione musicale occidentale. Ogni nota ha diversi attributi che determinano la `durata` relativa e l’altezza del suono che il musicista deve eseguire. Ad esempio, nel caso del pianoforte, l’altezza di una nota indica al musicista quale tasto deve essere premuto sulla tastiera, e la durata della nota stabilisce per quanto tempo quel tasto deve essere tenuto premuto.

Il concetto di altezza non è rigido e si riferisce a una proprietà percettiva che permette a un ascoltatore di ordinare un suono su una scala legata alla frequenza. Come si vedrà in seguito, suonare una nota su uno strumento produce un suono (più o meno) periodico di una certa frequenza fondamentale. Questa frequenza fondamentale è strettamente legata a ciò che si intende per altezza di una nota. Nel seguito, usiamo il termine “altezza” in modo intuitivo, per ordinare i suoni con altezza da “più bassa” a “più alta” — in modo simile ai tasti di una tastiera di pianoforte ordinati da sinistra a destra.

Due note con frequenze fondamentali in rapporto pari a una qualsiasi potenza di due (ad esempio, metà, doppio o quattro volte) sono percepite come molto simili. Per questo motivo, tutte le note con questo tipo di relazione possono essere raggruppate nella stessa classe di altezza. Questa osservazione porta anche alla nozione fondamentale di `ottava`, definita come l’intervallo tra una nota musicale e un’altra con metà o doppia della sua frequenza fondamentale. Con questa definizione, una classe di altezza è un insieme di tutte le altezze o note che distano un numero intero di ottave.

Per descrivere la musica usando un numero finito di simboli, è necessario discretizzare lo spazio di tutte le possibili altezze. Questo porta alla nozione di `scala musicale`, che può essere considerata come un insieme finito di altezze rappresentative. A causa della stretta relazione di ottava delle altezze, le scale sono generalmente considerate in un’unica ottava, con ottave superiori o inferiori che semplicemente ripetono il modello. Una scala musicale può quindi essere specificata da una divisione dello spazio di un’ottava in un certo numero di passi di scala. Gli elementi di una scala sono spesso chiamati semplicemente le note della scala e sono ordinati secondo le rispettive altezze.

Nella storia della musica, sono state proposte e utilizzate molte scale differenti, e ci sono state accese discussioni sull'idoneità di scale specifiche. L'appropriatezza di una scala dipende molto dal tipo di musica da descrivere, dagli strumenti usati, dal genere musicale o dal contesto culturale. Una scala adatta a rappresentare la musica per pianoforte occidentale potrebbe non essere adatta a rappresentare la musica per sitar indiano. Una scala usata per il canto gregoriano del X secolo potrebbe non essere una buona scelta per descrivere la musica sperimentale del XX secolo. Non esiste una scala musicale universalmente valida, e la scelta di una scala musicale comporta inevitabilmente delle semplificazioni imposte dalle considerazioni pratiche.

Qui consideriamo solo il caso della `scala cromatica temperata` a dodici toni, in cui un’ottava è suddivisa in dodici passi di scala. Le frequenze fondamentali di questi passi sono equidistanti su una scala logaritmica di frequenze. La differenza tra le frequenze fondamentali di due passi successivi nella scala è detta `semitono`, che rappresenta l’intervallo più piccolo possibile in questa scala. Nella scala temperata a dodici toni, ci sono dodici classi di altezza. Nella notazione musicale occidentale, queste classi di altezza sono indicate combinando una lettera con un’alterazione. Sette di queste classi (corrispondenti alla scala di Do maggiore) sono rappresentate dalle lettere `C, D, E, F, G, A, B`. Queste classi corrispondono ai tasti bianchi di una tastiera di pianoforte. Le restanti cinque classi di altezza corrispondono ai tasti neri del pianoforte e sono rappresentate da una combinazione di una lettera e di un’alterazione (♯, ♭). Un diesis (♯) alza la nota di un semitono, mentre un bemolle (♭) la abbassa di un semitono. Le alterazioni sono scritte dopo il nome della nota. Ad esempio, D♯ rappresenta il Re diesis e D♭ il Re bemolle. Nella scala temperata, le restanti cinque altezze possono essere indicate come C♯, D♯, F♯, G♯, A♯ o come D♭, E♭, G♭, A♭, B♭. Per esempio, C♯ e D♭ rappresentano la stessa classe di altezza, anche se musicalmente si distingue tra i due concetti.

Per nominare le note della scala temperata a dodici toni, oltre a indicare la classe di altezza, è necessario fornire un identificatore per l’ottava. Seguendo la Notazione Scientifica, ogni nota è specificata dal nome della classe di altezza, seguito da un numero che indica l’ottava. La nota A4 ha una frequenza fondamentale di 440 Hz e serve da riferimento. Il numero dell’ottava aumenta di uno passando da una nota con classe di altezza B a una con classe di altezza C. Ad esempio, la nota B4 è seguita dalla nota C5. Analogamente, il numero dell’ottava diminuisce di uno passando da una C a una B. La nota più bassa, C0, ha una frequenza fondamentale intorno ai 16 Hz, al di sotto della soglia di percezione acustica umana. La figura seguente mostra le note da C3 a C5, insieme ai tasti corrispondenti di una tastiera di pianoforte.

![tastiera](images/tastiera.png)

Ordinando tutte le note della scala temperata secondo le loro altezze, si ottiene una scala cromatica temperata, in cui tutte le note della scala sono equidistanti. Il termine cromatico deriva dal greco chroma, che significa colore. Nel contesto musicale, il termine `croma` è strettamente legato alle dodici differenti Classi di altezza. Ad esempio, le note C2 e C5 hanno entrambe lo stesso valore di croma, C. In altre parole, tutte le note che hanno lo stesso valore di croma appartengono alla stessa classe di altezza. Ricordiamo che le note che appartengono alla stessa classe di altezza (o che hanno lo stesso valore di croma) vengono percepite come simili in un certo modo. Al contrario, le note che appartengono a classi di altezza diverse (o che hanno valori di croma diversi) vengono percepite come dissimili. Questo giustifica l’uso del termine “croma” nel senso che note con valori di croma differenti hanno un “colore sonoro” differente.

Nella figura seguente si vede la lista delle frequenze in Hertz dei tasti di un moderno pianoforte standard a 88 tasti in temperamento graduale a dodici toni, dove il quarantanovesimo tasto, il LA centrale (o A4), ha la sua fondamentale a $440$ Hz (in evidenza). Ogni ottava divide la frequenza in dodici passi identici (per esempio, il quinto LA è $440$ Hz e la sua ottava superiore è $880$ Hz), ogni frequenza successiva si deriva moltiplicando (in crescendo) o dividendo (in descrescendo) per la radice dodicesima di due (come mostrato di seguito). Per esempio, la frequenza del semitono superiore al la centrale A4 (A4\#), si ottiene moltiplicando $440$ per la radice dodicesima di due. Per passare dal la centrale A4 al $SI$ centrale $B4$ (salendo di un tono, o due semitoni), si moltiplica $440$ per la radice dodicesima di due, due volte. Per passare da A4 a C5 (il DO superiore), si moltiplica $440$ tre volte per la radice di due.

![key](images/piano_key.png)

##### Scala temperata

La differenza in altezza tra due suoni musicali, costituita dalla differenza di numero delle loro vibrazioni, si chiama `intervallo`. L'intervallo si determina contando le linee e gli spazi che separano le due note sul rigo musicale. Due intervalli sono uguali se è uguale il rapporto (e non la differenza) delle frequenze dei suoni dell'intervallo.

Alla fine del XVII sec. Andreas Werckmeister adottò, per costruire una scala, un procedimento matematico molto rigido rispetto ai criteri di ricerca precedenti: partendo dall'intervallo di un'ottava divise la scala in dodici parti uguali. Trovò in tal modo la costante dta dalla radice dodicesima di due, il cui valore è approssimato a 1.059.

Il rapporto fra la frequenza di una nota e la successiva è costante ed è detto semitono temperato. Indicando con $x$ il valore del semitono temperato, possiamo scrivere:

$$ 
\frac{f_\text{C4\#}}{f_\text{C4}}=\frac{f_\text{D4}}{f_\text{C4\#}}=\cdots=\frac{f_\text{B4}}{f_\text{A4\#}}=\frac{f_\text{A4\#}}{f_\text{C5}}=x
$$

Se inoltre si aggiunge il vincolo che la frequenza di una qualsiasi nota di un’ottava raddoppia nell’ottava successiva:

$$ 
\frac{f_\text{C5}}{f_\text{C4}}=\frac{f_\text{C4}}{f_\text{C3}}=\cdots=\frac{f_\text{A5}}{f_\text{A4}}=\frac{f_\text{A4}}{f_\text{A3}}=2\qquad \text{etc.}
$$

allora si ricava che la ragione $x$ di una progressione geometrica che in 12 passi porta al raddoppio di una frequenza rispetto ad un'altra è data da:

$$
2=\frac{f_\text{C5}}{f_\text{C4}}=x^{12}\frac{f_\text{C4}}{f_\text{C4}}\quad \Rightarrow \quad x^{12}=2 \quad \Rightarrow \quad x=\sqrt[12]{2}=2^\frac{1}{12}
$$

che si può approssimare a 1.06.

Dunque, moltiplicare la frequenza di una nota per $2^{1/12}$ corrisponde a salire di un semitono nella scala temperata, mentre moltiplicare la frequenza di una nota per $2^{k/12}$ corrisponde a salire di $k$ semitoni nella scala temperata, come rappresentato in figura.

![scala](images/scala.png)


Inoltre, per la proprietà dei logaritmi (il logaritmo di un quoziente è uguale alla differenza dei logaritmi del dividendo e del divisore) la scala logaritmica trasforma i rapporti di frequenza in differenze, così un’ottava si traduce in un intervallo costante fra i logaritmi delle frequenze. Per esempio (ma vale per tutte le coppie di note con lo stesso nome, ma appartenenti a ottave contigue):

$$
1=\log_2 2=\log_2\left(\frac{f_\text{C5}}{f_\text{C4}}\right)
=\log_2 \left(f_\text{C5}\right)-\log_2\left(f_\text{C4}\right)
$$

La musica occidentale si basa sul sistema temperato equabile. La sua scala si distingue anzitutto in `cromatica` e `diatonica`. La scala cromatica è la scala che comprende tutti i suoni possibili del sistema, quindi nel temperamento equabile è definita dalla successione di 12 semitoni contigui (in figura). Il semitono cromatico è formato da due note con lo stesso nome ma diversa altezza (es: Do - Do\#, Mi$\flat$ - Mi).

```{image} images/scala_do_maggiore.png
:alt: long
:class: bg-primary mb-1
:width: 400px
:align: center
```

La scala diatonica è una scala di 7 note e ad essa appartengono due grandi tipi di scale: la scala maggiore (in figura sotto), costituita da 5 toni e 2 semitoni, e diverse forme di scale minori. Il semitono diatonico è formato con due note consecutive con diverso nome e diversa altezza (es: Mi - Fa , Si - Do)

```{image} images/scala_diatonica.png
:alt: long
:class: bg-primary mb-1
:width: 250px
:align: center
```

:::{figure} video/do_major.mp4
:width: 30%
:align: left
:::

---

## Analisi in frequenza del segnale audio

Come abbiamo visto in precedenza, i segnali musicali sono generalmente complessi mix sonori che consistono in una moltitudine di componenti sonore differenti. A causa di questa complessità, l’estrazione di informazioni musicalmente rilevanti da un’onda costituisce un problema difficile. Un primo passo per comprendere meglio un segnale dato è scomporlo in blocchi costitutivi che siano più accessibili per i successivi passaggi di elaborazione. Nel caso in cui questi blocchi siano costituiti da funzioni sinusoidali, tale processo è anche chiamato `analisi di Fourier`. Le funzioni sinusoidali sono particolari in quanto possiedono un significato fisico esplicito in termini di frequenza. Di conseguenza, la scomposizione risultante rivela lo spettro di frequenze del segnale, simile a un prisma che può essere usato per scomporre la luce nei suoi colori spettrali costituenti. La trasformata di Fourier converte un segnale dipendente dal tempo in una rappresentazione che dipende dalla frequenza. Essendo uno degli strumenti più importanti nell’elaborazione dei segnali, incontreremo la trasformata di Fourier in una varietà di compiti di elaborazione musicale.

Per comprenderne la portata, iniziamo con un segnale audio che rappresenta il suono di un brano musicale. Ad esempio, analizziamo il suono di una singola nota suonata su un pianoforte il cui tracciato temporale è mostrata in figura. 

![C4](images/C4_piano.png)

Per comprendere quale nota sia stata effettivamente suonata, ricordiamo che l’altezza di un suono musicale è strettamente legata alla sua frequenza fondamentale, ovvero la frequenza della componente parziale più bassa del suono. Pertanto, dobbiamo determinare il contenuto in frequenza, ossia le principali oscillazioni periodiche del segnale. Ingrandiamo il segnale considerando solo una sezione di circa 20 ms e di 220 campioni (come in figura). 

![](images/clip_C4.png)

La figura mostra che il segnale si comporta in modo quasi periodico in questa sezione. In particolare, si possono osservare 5 creste principali di un’oscillazione simile a una sinusoide. La presenza di circa 5 cicli di oscillazione in una sezione di 20 ms indica che il segnale contiene una componente di frequenza di circa 262 Hz.

L'idea principale dell'analisi di Fourier è confrontare il segnale con sinusoidi di varie frequenze $f\in\mathbb{R}$ (in Hz). Ciascuna di queste sinusoidi, o toni puri, può essere vista come un'oscillazione prototipo (o appartenente alla base - potenzialmente infinita - di Fourier). Come risultato, otteniamo per ogni frequenza considerata $f \in \mathbb{R}$ un coefficiente di ampiezza $c_f \in \mathbb{R}$ che ne caratterizza il "peso" nella scomposizione (o composizione additiva) del segnale. Nel caso in cui il coefficiente $c_f$ sia elevato in magnitudine, vi è un'alta somiglianza tra il segnale e la sinusoide di frequenza $f$, e il segnale contiene un'oscillazione periodica a quella frequenza. Nel caso in cui $c_f$ sia molto basso o quasi nullo, il segnale non contiene una componente periodica a quella frequenza. 

Tracciamo ora i coefficienti $c_f$ rispetto ai vari parametri di frequenza $f \in \mathbb{R}$. Questo genera un grafico come quello mostrato nella prossima figura. In questo grafico, il valore massimo si trova per il parametro di frequenza $f_0=261.7$ Hz che rappresenta all'incirca la `frequenza fondamentale` della nota C4. Infatti, questa è esattamente la nota suonata nell'esempio al pianoforte. Inoltre, attraverso i coefficienti che spiccano nel grafico, si può anche osservare la presenza di numerose sinusoidi di frequenza multipla della fondamentale ad indicare, all’incirca, le componenti in frequenza delle parziali del tono C4, anche detto `spettro di frequenza` del segnale.

![mag](images/magnitude_C4.png)

Per osservare nel dettaglio il contributo delle armoniche nell'approssimazione del segnale si osservi la figura seguente. Come detto il segnale è un segnale quasi periodico in cui si possono osservare oscillazioni che rimandano all'dea di una sovrapposizione di sinusoidi di varia frequenza ed ampiezza. Infatti si nota direttamente dal secondo grafico in figura il peso della prima armonica, o fondamentale, di frequenza $f_0$. Le creste tra segnale e fondamentale mostrano una indubbia corrispondenza. Tuttavia sono necessarie altre armoniche per ottenere migliore ricostruzione: nella seconda e nella terza immagine sono infatti riportati i grafici con rispetivamente 3 e 10 armoniche linermente combinate con i coefficienti mostrati prima. Le armoniche sono multiple della fondamentale secondo la legge $f_k=(k+1)f_0$, con $k=0,1,2,\cdots$.

![harm](images/harmonics.png)

Con questo esempio, abbiamo già visto l'idea principale della trasformata di Fourier. La trasformata di Fourier scompone un segnale nelle sue componenti di frequenza. Per ciascuna frequenza $f$, la trasformata di Fourier fornisce un coefficiente $c_f$ (e una fase $\varphi_f$) che ci dice in che misura il segnale dato corrisponde a un'oscillazione prototipo sinusoidale di quella frequenza. Sotto ipotesi molto larghe dunque, un qualsiasi segnale può essere visto come somma di un numero, eventualmente infinito, di componenti armoniche.  Ad ogni componente armonica è associata una frequenza di oscillazione. Quindi è possibile studiare quali e quante frequenze siano presenti in un dato segnale. La trasformata di Fourier è una trasformazione matematica reversibile che permette tutto questo: aumentando il numero di componenti armoniche, ovvero il numero dei segnali armonici a diversa frequenza, si può migliorare l’approssimazione del segnale fino a ridurre a zero la differenza.
Questa sovrapposizione ponderata viene anche chiamata rappresentazione di Fourier del segnale originale. Il segnale originale e la trasformata di Fourier contengono la stessa quantità di informazioni. Queste informazioni, tuttavia, sono rappresentate in modi diversi. Mentre il segnale visualizza le informazioni nel dominio del tempo, la trasformata di Fourier le visualizza nel dominio della frequenza. Come affermato da Hubbard [9], il segnale ci dice quando determinate note vengono suonate nel tempo, ma nasconde le informazioni sulle frequenze. Al contrario, la trasformata di Fourier della musica mostra quali note (frequenze) vengono suonate, ma nasconde le informazioni su quando le note vengono eseguite.

---

##### Trasformata di Fourier di segnali analogici

Senza seguire una trattazione rigorosa, ricordiamo qui l'importante risultato relativo alla trasformata di Fourier di un segnale audio analogico. Richiamaimo poi che per calcolare lo spettro di un segnale analogico in digitale, si campiona una registrazione di durata finita del segnale e i campioni risultanti vengono trasformati nel dominio della frequenza mediante un algoritmo DFT o FFT. La frequenza di campionamento $F_s$ deve essere sufficientemente veloce da minimizzare gli effetti dialiasing. Se necessario, un prefiltro analogico antialiasing può precedere l'operazione di campionamento.
