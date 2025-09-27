Lezione dedicata a dispositivi di input: tutti quei dispositivi che, nel nostro sistema di realtà virtuale consentono all'utente di interagire con il sistema, dando dei comandi.
I dispositivi di input sono tanti e di diverso tipo.
![[image01_001.png]]
Un'applicazione è un ciclo infinito, che oltre a gestire la grafica (che deve essere aggiornata ad ogni ciclo), il computer deve calcolare altre cose (suono, feddback, sensore, etc...) e interpretare i comandi che manda l'utente.
I dispositivi di input si possono classificare in diversi modi:
	- gradi di libertà (*DOF*);
	- discreti o continui;
	- Desktop o non-Desktop
	- per le tecnologie pre cui funziona.

### **DoF**
Il numero di gradi di un sensore è la dimensione è la dimensione del vettore di input che il sensore gli dà. 
Es: se un sensore vi da in ingresso soltanto un numero ogni volta che lo interrogate, allora questo è un sensore ad un grado di libertà.
Es: il mouse è un sensore in input a due gradi di libertà, perchè ogni volta che viene letto da due numeri: *x* e *y* del mouse stesso.
Ovviamente pochi gradi di libertà, nella realtà virtuale non sono abbastanza, sono necessari dispositivi tipicamente a *6* gradi di libertà che combinano sia la posizione, che l'orientamento.
### **Discreti o Continui**
I dispositivi di input si possono classificare anche sul fatto che sono discreti o continui.
- Discreto: dispositivo che quando viene attivato fornisce un input ad eventi, per esempio un tasto di una tastiera è discreto, può essere soltanto premuto o non premuto.
- Continuo: Dispositivo il cui tracciamento del movimento è continuo, ovviamente il computer lo discretizza, ma questo continua ad aggiornare posizione e orientamento del dispositivo.
### **Desktop o non-Desktop**
I dispositivi desktop hanno il cavo, e quindi vincolano il loro uso alla scrivania, da seduti
I dispositivi non-desktop, al contrario, non hanno cavi e quindi possono essere portati in giro quando si naviga in una stanza con la realtà virtuale.

### **Che cosa rende la programmazione dell'interfaccia utente articolata?**
Partendo dal fatto che non ci sono standard, cioè tutti i dispositivi sono diversi, prodotti da diversi produttori, ciascuno con le sue librerie di programmazione.
Un altro aspetto che potrebbe creare una barriera è il costo che può raggiungere cifre elevate e quindi poco usufruibile.
## **Quali sono i task principali che utente può eseguire in ambiente di realtà virtuale?**
In realtà sono tanti, ma i principali da ricordare sono:
1. **Selezionare** oggetti: essere in un ambiente virtuale, avere il proprio avatar e si può selezionare un oggetto, scegliere un oggetto ed eseguirci un'azione.
2. **Manipolare** oggetti: dopo aver selezionato un oggetto. viene attaccato virtualmente alla mano virtuale e da li si possono modificare le proprietà dell'oggetto.
3. **Navigare nell'ambiente virtuale**: significa muoversi e di conseguenza muovere l'avatar all'interno del mondo virtuale.
#### 1. Selezione
La selezione che significa scegliere, selezionare un oggetto serve per renderlo attivo, così da poterci fare delle altre operazioni.
Due modi tipici di fare selezione sono:
- Toccare l'oggetto con una mano virtuale o con proxy virtuale. Il difetto è che la limitazione della selezione è data da ciò che è nel raggio di azione della mano o del proxy.
- Rey casting: dal proxy virtuale viene sparato un raggio e, quando questo colpisce un oggetto a distanza, l'oggetto viene selezionato.
La selezione può essere di due tipi:
- isomorfa: c'è una corrispondenza diretta tra il movimento della mano nella realtà e nella realtà virtuale. Il movimento è 1:1.
- non-isomorfa: al contrario quando il movimento della mano reale *non* corrisponde in scala 1:1 alla realtà .
	- Esempio: *go-go technique*: un'estensione artificiale della mano con una scalatura non lineare tra la mano reale e la mano virtuale.
		![[image01_002.png]]
	- Esempio: *naming*: selezionare un oggetto tramite voce (più complesso perché serve anche un analizzatore vocale.

Se decomponiamo la selezione:
1. 'indicazione' dell'oggetto tramite pointing, touching, selezione indiretta;
2. conferma di selezione tramite un bottone, un gesto, un suono;
3. Feedback: grafico, tattile, audio, testuale.
#### 2. Manipolazione
Solitamente dopo la selezione, avviene la manipolazione.
La cosa più tipica è muoverlo, in modo semplice l'oggetto 3D viene attaccato alla mano virtuale e portato in giro, così che l'oggetto segua il movimento delle mano reale.
Il modo più accurato per questo tipo di manipolazione sarebbe quello di usare un modello 3D della mano che corrisponde alla mano reale, riuscire a fare il tracking di tutte le dita e far una manipolazione che è consistente con la fisica del contatto di tutte le dita. 
Questo è molto complicato da realizzare in modo stabile.
#### 3. Navigazione
L'obbiettivo è quello di modificare il punto di vista dell'osservatore: cambiarne posizione e orientamento.
Navigare in un ambiente virtuale è fondamentale e può essere fatto in diversi modi diversi:
- Naturale: è il modo più semplice, ogni movimento del corpo, della testa viene mappato dai sensori del visore e direttamente trasmesso nella realtà virtuale.
- Steering: tecnica basata su vari modi, per esempio sullo sguardo: stando fermi, guardando la direzione desiderata di movimento e premendo comandi sul joystick, l'avatar si sposta verso la direzione 'guardata'.
- Target-based (teletrasporto): con il joystick viene selezionata la meta da raggiungere e l'avatar viene trasportato nel punto puntato.   
## **Dispositivi di input**
### **CyberGlove**
Guanto professionale, ai tempi molto costoso.
Sono guanti che possono essere con o senza filo. All'interno del guanto ci sono tante cuciture con delle resistenze variabili che al flettere delle falangi cambiano, vien convertito il segnale e con la mappatura di tali cambiamenti si ottengono risultati.
![[image01_003.png]]
## **Dispositivi Aptici**
Sono dispositivi sia di input che di output, con la limitazione che hanno un cavo che vi vincola.
*Haptics* rientra nella robotica ed è una disciplina che si occupa di studiare gli stimoli tattili di una persona.
I dispositivi aptici sono quei dispositivi che hanno a che fare con la stimolazione tattile delle persone.
Si possono distinguere in due modi:
1. **Dispositivi di feedback tattile**: agiscono sui recettori tattili sotto pelle. Permettono alla mente di percepire vibrazioni, pressioni, texture, etc...
2. **Dispositivi di feedback cinestetico**: rimandano una forza contraria che agisce su muscoli, articolazioni, tendini del corpo umano.

I dispositivi aptici vengono classificati in base ai gradi di libertà (*DoF*)
- *Bassa DoF* : fino a 3 gradi di libertà (forza);
- *Alta DoF*: fino a 6 gradi di libertà (forza e coppie);
- *Molto alta DoF*: oltre 6 gradi di libertà (quando è necessario applicare più punti di contatto).

Esistono altre categorie di distinzione, per esempio, come sono fatti meccanicamente:
- in serie;
- paralleli.
e vengono divisi per come cambia la cinematica di come sono fatti i bracci.

Altre classificazioni dei dispositivi aptici si basano anche sul numero di punti a contatto con il corpo:
- *a singolo punto*: con un solo punto di contatto;
- *multi-punto*: con almeno due punti di contatto;
- *task replica*: dispositivo aptico che ha la forma che riproduce un tool reale:

Un'altra categoria di classificazione si basa sulla strategia di controllo:
- Impedenza: i comandi che l'utente fornisce al computer sono le coordinate di posizione del dispositivo e riceve in output una forza. Sono i più comuni.
- Ammettenza: l'utente trasmette una forza che viene applicata sui joystick e riceve come output delle coordinate.

Ultimi parametri dei dispositivi aptici da tenere in considerazione sono quelli che li rendono più o meno costosi e di conseguenza più o meno sofisticati.
- *Motion Range*: range in cui si può muovere il dispositivo
- *Peak Force*: forza massima che l'utente può applicare sui dispositivo;
- *Resolution*: minimo spostamento che il dispositivo è in grado di misurare;
- *Accuracy*: l'errore che commette il sensore nel misurare la posizione del dispositivo.
#### **Utilizzo**
Il tipico utilizzo consiste nel muovere con il joystick un proxy virtuale, l'input viene letto e mandato continuamente al computer, esso lo usa per disegnare 'il pallino' che si vede a schermo.
Viene calcolato se si verifcano delle collisioni tra 'il pallino' e l'oggetto all'interno della schermata (*collision detection*)
![[image01_004.png]]
Gli algoritmi che calcolano un feedback di forza si chiama di **rendering aptico**
Il **rendering aptico** è il processo di calcolo e generazione di forza in risposta all'interazione dell'utente con l'ambiente virtuale. 
Un dispositivo aptico solitamente consente ad un utente di spostare un oggetto 3D appartenente all'ambiente virtuale.
L'oggetto virtuale manipolato è chiamato *proxy*.
Una frequenza di aggiornamento di 1KHz è necessaria per un'esperienza confortevole per quasi tutte le applicazioni di rendering tattile.
Es: Il proxy è una sfera, in input il dispositivo ha 3 DoF e posizione e l'output è una forza:
![[image01_005.png]]
Es: il provy è un oggetto 3D, in input il dispositivo ha 6 DoF, posizione e orientazione; mentre in output si ottengono 3 forze e 3 coppie:
![[image01_006.png]]
#### **Tecniche di rendering**
##### 1. Rendering Diretto:
La posizione/ orientamento misurata dal sensore tattile viene applicata direttamente al proxy virtuale con una relazione lineare.
La forza restituita all'utente è calcolata come direttamente proporzionale alla profondità di penetrazione del proxy virtuale con gli altri oggetti dell'ambiente grafico.
Es: contatto tra il proxy con una sfera
![[image01_007.png]]
	1. Controllare se si verifica una collisione: 
		- Avendo le coordinate del centro della sfera $(x_s, y_s, z_s)$ e del suo raggio $R$;
		- Avendo le coordinate del proxy dell'utente $(x_u, y_u, z_u)$
		$$
d = \sqrt{(x_u-x_s)^2+(y_u-y_s)^2+(z_u-z_s)^2}
$$
	2. Come applicare la forza:
		$$
			F =
			\begin{cases}
			  0 & \text{if } d > R\\
			  k(R-d)\vec{N} & \text{otherwise}
			\end{cases}
		$$
		dove 
		$$\vec{N} = \frac{1}{d} \begin{bmatrix}
x_u-x_s \\
y_u-y_s \\
z_u-z_s
\end{bmatrix} $$
			e $k$ scelta 

Il rendering diretto per oggetti 3D più complessi invece ha qualche accortezza in più:
1. dividere l'oggetto in sotto-volumi;
2. ogni sotto-volume è associato ad una porzione della superficie dell'oggetto;
3. La forza di feedback è calcolata in modo proporzionale alla profondità di penetrazione del proxy virtuale nelle sottoparti dell'oggetto. 
Questo metodo funziona sia con oggetti semplici ma può generare discontinuità nella forza percepita.
![[image01_008.png]]
##### 2. Virtual Coupling:
Per poterla applicare è necessario avere a disposizione un simulatore della fisica.
In questa tecnica non c'è più la lettura della posizione del joystick e l'applico al pallino, perchè l'ambiente di sviluppo in cui si lavora segue le regole della fisica e viene quindi scritto un controllo con cui vengono determinate le forza dal applicare al proxy virtuale affinché seguano i movimenti dell'utente, questi si chiamano modelli *molla-smorzatore*.
Quindi non si deve più imporre la posizione del proxy, ma si deve scrivere una forza che, se applicata al mio pallino virtuale, fa in modo che il pallino virtuale insegua i nuovi movimenti.
Formula di una formula tipica:
$$
F= k_Ld+\delta_Lv
$$
dove
$k_L, \delta_L$ sono rigidità e costante di smorzamento della molla lineare
$d$ è l'offset della molla per la distanza lineare
$v$ è la velocità lineare relativa dell'oggetto dinamico.

Che vantaggi porta questo metodo? 
- se ci si trova in un ambiente basato sulla fisica, quando il pallino virtuale colpisce un oggetto, vengono gestiti automaticamente anche gli urti.