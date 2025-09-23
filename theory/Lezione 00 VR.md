**Cos'è la realtà virtuale?**
	È un enviroment artificiale che è creato con software e si presenta all'utente in modo che egli lo accetti come enviroment reale.
Le aree di applicazione della realtà virtuale sono molteplici: industriali, di visualizzazione (medico, scientifico, etc...), di intrattenimento, di training (es. simulatori di guida), riabilitazione e terapia, modellazione, design e architettura.
**Elementi Chiave della VR**
![[image001.png|400]]
VR è costituito dal computer, con installato Unity
L'utente utilizza dei dispositivi per interagire con la simulazione. Questi possono essere sia di input che di output.
Il calcolatore per costruire l'ambiente di simulazione si appoggia a delle librerie create esternamente per generare l'ambiente operativo.
![[image002.png|400]]
È presente un computer dove gira l'applicazione che si occupa di varie cose (render grafico, render audio, render aptico, etc...)
Tra il computer e l'utente ci sono delle interfacce/dispositivi di input/output.
Sono di input i dispositivi che consentono di inviare dei comandi all'applicazione.
Sono di output i dispositivi che consentono di ricevere feedback e dati sensoriali
Esistono dispositivi che entrano in contemporanea in entrambe le categorie.
Il dispositivo di output per antonomasia è un visore, che si occupa di fornire all'utente la sua grafica.
**Propercezione**
	È la percezione che l'utente ha di sé una volta immerso in questa realtà virtuale.
	Più è alta e più è elevato il senso di immersione nell'ambiente virtuale.
Quando c'è un livello basso di propercezione, un'applicazione di realtà virtuale può dare fastidio e può portare ad affaticamento, nausea e mal di testa.
**Cyber Sickness**
	È una forma di motion sickness che comporta sintomi quali nausea, vomito, disorientamento, vertigini, etc...
La cyber sickness si crede sia correlata all'incongruenza sensoriale che si presenta quanto c'è un conflitto tra sensi differenti.
	Es: 
			- **errori di tracking** che inducono a dei miss-match tra l'utente e l'avatar di gioco;
			- **lag di sistema** che producono dei delays tra l'azione dell'utente e il risultato a schermo;
			- **risoluzione dell'immagine HMD e FOV**: scarsa risoluzione e FOV piccolo non sono accettabili, anche grandi FOV possono essere problematici.
	
**Modellare un mondo virtuale**
I modelli grafici sono modelli a poligoni: tutto ciò che viene rappresentato, rappresenta il contorno della superficie approssimato a poligoni. Si usa un modello *poligonale*.
**Il colore**
Ogni pixel dello schermo ha un colore ed è rappresentato da un vettore (red, green, blue).
I colori sono vettori in uno spazio 3D.
![[image003.png|400]]
==minuto 18:30==