# Ghosts-FlashLights
> A game with Ghosts and FlashLights

## Game overview
**Ghosts & FlashLights** (*working title*) è un gioco nel quale il giocatore controlla una torcia che si muove sullo schermo, mentre un personaggio, bimbo, si muove dall'inizio del livello verso la fine, e viene assalito da dei fantasmi ed altri mostri, questi fantasmi sono sensibili alla luce, quindi con la trocia si deve illuminarli per farli lentamente scomparire. La batteria della torcia va risparmiata, perchè si consuma rapidamente, mentre il bimbo si muove cercando di evitare sempre il fantasma più vicino e più debole. Mentre si muove il bambino può collezionare vari oggetti collezionabili che permettono di ricaricare la torcia o potenziarla temporaneamente, o rendere il bimbo stesso invulnerabile per un breve periodo. La grafica è in pixel-art ed il gioco è simile ad un platform 2d, con componenti di puzzle solving, nel quale il personaggio (bambino) si muove autonomamente ed il giocatore può gestire solo la torcia.

## Unique selling points
- Puzzle game divertente ed unico con una storia coinvolgente
- Tensione e difficoltà crescente per raggiungere la fine dei livelli
- Il gioco può essere giocato su pc o anche su smartphone e tablet
- Futura possibilità di multiplayer

## Minimum requirements

For Mobile:
- OS: Android 10
- Model: Samsung S9

For PC:
- OS: Windows 10
- Graphics card: Intel UHD 620

## Game synopsis

Un bimbo durante la notte viene catturato e mandato in un mondo parallelo, oscuro e minaccioso, con pericoli di ogni sorta oltre a fantasmi e mostri, che vogliono catturarlo e trasformarlo in uno di loro. In questo sogno lucido il bimbo non ha la capacità di controllare sempre le proprie paure e si muove in modo sconsiderato guidato da esse. La luce sicuramente è una forza potente contro gli incubi da affrontare, ma ci sono anche personaggi buoni che possono dare una mano durante il cammino.
La torcia è una delle poche fonti di luce che riescono ad indebolire i mostri ed i fantasmi, ma non ha certo energia infinita, sarà necessario maneggiarla con attenzione e parsimonia per evitare di sprecare il suo potere. Il povero bimbo in questo caso potrebbe soffrirne o addirittura trasformarsi lui stesso in un fantasma.

## Game objectives
The list of core objectives (a.k.a. player goals) are the following:
- L'obiettivo principale è quello di far giungere il bimbo sano e salvo alla fine di ogni livello, o almeno di farlo spaventare il meno possibile durante il percorso.
- Un obiettivo secondario è quello di tenere a distanza i fantasmi ed i mostri di ogni livello usando la torcia in modo da accenderla e spegnerla nei momenti giusti, ma evitando che si consumi completamente
- Collezionare vari oggetti durante il percorso permette di ricaricare la torcia o cambiarne il tipo di luce (che può essere più o meno efficace in base al mostro o fantasma che viene illuminato)
- collezionare oggetti speciali, fa raggiungere dei passaggi altrimenti non raggiungibil
- ogni livello ha una percentuale di completamento, completarlo tutto richiede vari giri nei quali si sbloccano nuove possibilità
- ci sono delle classifiche sul tempo impiegato per ogni livello e per aver completato il gioco nel tempo minore possibile
The player can fail (a.k.a. fail state) at achieving the core objectives with the following
actions:
- lasciare che i mostri o i fantasmi si avvicinino per troppo tempo al bimbo, che perde quando il livello di paura raggiunge il limite
- in certi livelli è possibile che, a causa di scelte sbagliate con la torcia, il bimbo intraprenda il percorso sbagliato cadendo o incontrando altri spaventosi preicoli che portino al limite la paura

## Game rules

- il giocatore può muovere la torcia in tutto lo schermo, scegliendo se accenderla o no in ogni momento
- i mostri ed i fantasmi possono essere visibilito invisibili, ma vengono bloccati o rallentati dalla luce, oltre a perdere parte della loro energia, fino a scomparire quando finiscono l'energia
- il bimbo inizia a camminare da sinistra a destra appena inizia il livello e si muove seguendo alcuni perscorsi per cercare di avvicinarsi alla fine del livello, andando sempre nella direzione del mostro/fantasma con meno energia
- quando il bimbo si scontra con degli oggetti li raccoglie fornendo un bonus o un malus alla sua velocità, o alla durata o alla luce della torica
- quando il bimbo entra in contatto con un mostro o un fantasma accresce la sua paura e se giunge al limite, il livello è fallito e va ricominciato

## Game loop

![GameLoop](readme_images/game_loop.png?raw=true "Game Loop")
*Image 1 - Diagram of the core game loop*

The game has five pillars in its core game loop:
- **Walk**: Quando inizia un livello, il bimbo inizia a camminare seguendo uno dei percordi verso la fine del livello
- **Torch**: Il giocatore muove la torcia per illuminare la strada del bimbo, e fermare/combattere i mostri ed i fantasmi
- **Avoid**: Illuminando e colpendo i fantasmi cercare di evitare che il bimbo li colpisca o giunga in zone pericolose del livello
- **Collect**: Nel suo percorso il bimbo raccoglie dei powerup o altri oggetti che forniscono dei bonus temporanei alla torcia o altre migliorie temporanee/permanenti, o ancora degli Oggetti collezionabili per la storia
- **Upgrade**: Grazie a questi oggetti raccolti, vengono aggiornate temporaneamente o definitivamente altre componenti del gioco come la torcia, il bimbo, i mostri, la percentuale di completamento di un livello o la storia in se. 

## Game environment

I setting nei quala si svolgono i vari livelli sono oscuri dungeon di pietra o caverne scavate nella roccia, e luoghi all'aperto come cimiteri e foreste ma sempre di notte con poca luce. Si incontrano ostacoli come muri, piattaforme, lapidi e alberi. Gli oggetti che si possono incontrare e raccogliere sono batterie per la torcia, piccoli giochi per diminuire la paura del bimbo, lampadine di veri colori che modificano la luce della torcia, vestiti o copertine speciali che proteggono temporaneamente il bimbo dai mostri, machingegni fotosensibili che attivano o disattivano porte o fanno muovere piattaforme 

## Camera, control, character (3Cs)

Balancing this 3 componentes makes the game experience more fluid and immersive for the player

### Camera

L'inquadratura seguirà sempre il bimbo lasciandolo al centro della scena, in una inquadratura classica da platform 2d. La torcia sarà come in un layer superiore e si potrà muovere liberamente su tutto lo schermo. Gran parte della scena sarà nera, e sarà visibilie l'ambiente illuminato intorno al bimbo, ai mostri o ad altri punti di luce. Accendendo la torcia in ogni punto si crea un raggio di luce che illumina parzialmente una zona dello schermo.
L'inquadratura si muove quasi sempre solo orizzontalmente ma possono esserci anche dei livelli in verticale, quindi potrà muoversi anche verticalmente, sempre lasciando il bimbo più al centro possibile, ma l'inquadratura deve rispettare i liminiti di dimensioni del livello.
Quando il bimbo viene a contatto con un fantasma l'inquadratura potrebbe vibrare o inclinarsi per far comprendere il pericolo e l'aumento di spavento del bimbo

### Character

In questo gioco il protagonista si muove in modo semi autonomo mentre il giocatore controlla solo la torcia che si muove come un layer sovrapposto su tutto lo schermo.

#### Character description

Il personaggio principale è un bimbo o una bimba, spaventati che si trovano in ambienti bui e spaventosi.
Il giocatore all'inizio del gioco può scegliere uno degli avatar proposti, tra bimbo e bimba.

![MaleChild](readme_images/male_child.png?raw=true "Male Child")
*Image 2 - Male Child*
![FemaleChild](readme_images/female_child.png?raw=true "Female Child")
*Image 3 - Female Child*

La torcia elettrica è rossa ed ha un bottone laterale, quando accesa emette un fascio di luce in direzione corretta, che illumina ad una certa distanza quello che la circonda.

![FlashLight](readme_images/torcia.png?raw=true "FlashLight")
*Image 5 - FlashLight*
![FlashLightOn](readme_images/torcia-accesa.png?raw=true "FlashLight On")
*Image 6 - FlashLight On*

#### Character metrics

Gli sprite del bimbo e della torcia sono in pixel art, dimensioni 32x32 pixel.
La **velocità del bambino** di default è lenta, mentre raccogliendo  alcuni oggetti può aumentare temporaneamente
Il bimbo ha **un'indicatore di spavento** che decresce a contatto con i mostri/fantasmi e si ripristina con alcuni oggetti o ad inizio livello
La torcia segue il mouse senza particolari limiti di velocità ma può **inclinarsi** (ruotare il fascio di luce) in base alla posizione sullo schermo
La torcia ha un **indicatore di carica**, che si consuma velocemente quando accesa, e si ripristina raccogliendo alcuni oggetti.
In base al **colore della luce**, la torcia ha una **potenza di illuminazione** diversa, che fa scomparire più o meno velocemente i mostri ed i fantasmi, alcune lampadine raccolte rallentano temporaneamente il **consumo di carica** della torcia

#### Character states
The following section outlines the primary child character states:
- **Idle**: fermo prima di iniziare il livello di gioco
- **Walking**: cammina scegliendo il percorso migliore verso la fine del livello
- **Jumping**: salta su una piattaforma o su un gradino
- **Scared**: spaventato per il contatto con un fantasma o un mostro
- **Happy**: raggiunto il fine livello

The following section outlines the primary flashlight states:
- **Disabled**: non può essere mossa
- **TurnedOff**: spenta
- **TurnedOn**: accesa
- **Discharged**: scarica

### Controller
The following section outlines the **mouse** controller scheme:
Muovere il mouse, durante il gioco, significa muovere la torcia sullo schermo, la punta della torcia viene rivolta in automatico verso il fantasma o il mostro piu vicino, quando si tiene premuto il tasto sinistro del mouse la torcia si accende e non si può muovere ne ruoterà in nessun modo, quando è spenta si può muovere liberamente per tutto lo schermo, semplicemente seguendo la posizione del mouse

The following section outlines the **touchscreen** controller scheme:
La torcia rimane ferma e ruota verso il mostro o il fantasma più vicini, muovendo la torcia con il dito essa si muove, ruotando sempre automaticamente verso i mostri, Sarà presente un tasto in basso a sinistra dello schermo a forma di bottone di accensione della torcia, tenendolo premuto la torcia si accende, e non può essere spostata con il dito, mentre rilasciadolo si potrà spostare e ruoterà di nuovo

## Game ingredients
The following section outlines the core game ingredients:
- **Child**: è il personaggio principale del gioco e si muove in automatico cercando di raggiungere la fine del livello evitando i fantasmi ed i mostri più potenti
- **Fanatasmi/Mostri**: sono gli antagonisti che possono far provare paura al bimbo e paralizzarlo completamente se entrano per troppo tempo a contatto con lui; sono fermi, si muovono lungo percorsi prestabiti o inseguono il bimbo
- **Flashlinght**: la torcia è lo strumento che usa il giocatore per combattere e sconfiggere i fantasmi ed i mostri sullo schermo, può restare accesa per poco tempo prima di scaricarsi, quindi la sua energia va conservata ed utilizzata il meno possibile
- **Pickups**: oggetti che il bimbo può raccogliere nel suo percorso e che danno un benefit, come ricaricare la batteria, proteggere il bimbo, velocizzarlo o rallentare i mostri
- **Obstacles**: altri ostacoli che possono aumentare la paura del bimbo, bloccarlo o farlo cadere, ad esempio delle porte possono aprirsi con un pannello solare, o delle piattaforme si possono muovere con la luce per evitare la caduta del bimbo
- **Terreno e Piattaforme**: sono la base sulla quale il bimbo cammina, salta e si muove verso la fine del livello, possono muoversi automaticamente o manualmente in orizontale o verticale per permettere di raggiungere zone altrimenti inaccessibili. Se si muovono manualmente, sarà la luce della torcia a controllarle con dei piccoli pannelli solari posti in alcune zone del livello
- **Fine livello**: un oggetto speciale che conforta il bimbo quando viene raggiunto

## Game systems
The following section outlines the core game systems:
- **Child Movement System**: il bimbo cercherà sempre di restare in movimento e dirigersi verso la fine livello, evitando i mostri più forti, saltando sulle piattaforme e attendendo di poter raggiungere quelle successive
- **FlashLight System**: la torcia interagisce con i mostri indebolendoli, e con alcuni oggetti per attivarli, ha diversi possibili colori di luce più o meno efficaci con diversi mostri o oggetti
- **Platforms System**: le piattaforme si muovono in automatico o con l'aiuto della luce della torcia
- **Monsters System**: i mostri hanno un loro comportaento in base al livello e al tipo

## Game Menu
In this section, we'll outline the game's menus:

**Main Menu**: The main menu will be accessible at the start of the game. The menu options are as follows:
- Play: This option loads the levels submenu.
  - Levels: level list, only the completed levels and the first uncompleted level are unlocked and available to be played
- Scores: This option displays the latest top 10 scores.
- Exit: This option closes the game's window.

**In-Game Menu**: The in-game menu is only accessible while playing levels, apearing when "Esc"/"Back" is pressed/tapped. The menu options are as follows:
Restart Level: Restarts the level from the beginning
Exit Level: Returns the player back to the main menu scene

## Game HUD
The following section outlines the game's **Head-up Display** (HUD):
The HUD will only be displayed while the game is in a level and will include the following interface components:
- **Fear Meter**: indica il livello di paura del bimbo
- **Charge Meter**: indica il livello di carica della batteria della torcia
- **Power Merter**: indica per ogni mostro e fantasma, il livello di potenza residua
- **Level Progress Bar**
- **Countdown**: prima dell'inizio di ogni livello un contatore da 3 a 0 per preparare il giocatore ad iniziare
