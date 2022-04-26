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

## Camera, control, character (3Cs)

### Camera

### Character

#### Character description

#### Character metrics

#### Character states

### Controller

## Game ingredients

## Game systems

## Game menu

## Game HUD
