# SportJet

Une création "**original**" - Lycée de Lorgues
**SportJet** est un Mini projet de BTS Snir.

## Utilisation
**SportJet** est un ensemble matériel.
![shem](https://github.com/SportJet/SportJet.github.io/raw/master/img/shem1.png)
un Arduino est connecter au réseau via une connexion Ethernet et peut etre controler via un Appareil Android.

# Mise en place - Lancement ( En Dev)
## Serveur BDD
le Serveur BDD permet d'enregistré le score des match.
## Raspberry Pi
le Raspberry Pi controle en I2C le panneux LED, il recois via des Socket les commande a exercé sur le Panneux.
## Application Android
Permet d'envoier des ordres via des Socket sur le réseau, il permet donc de controler le panneau LED.

# UML
## Diagram de déploiment
![use case](https://github.com/SportJet/SportJet.github.io/raw/master/img/fig128014.png)

## Scénarii
- L&#39;arbitre assistant démarre une partie. Le chronomètre démarre. Le score s&#39;initialise à 0:0.
- L&#39;arbitre assistant peut stopper le chronomètre et le relancer.
- L&#39;arbitre assistant peut incrémenter ou décrémenter le score d&#39;une des deux équipes.
- Si un problème de connexion réseau à lieu alors l&#39;arbitre assistant utilise le boîter de commande.
- L&#39;arbitre assistant enregistrer le score de la partie, puis le transmettre à la fédération.
- Il signale la fin d&#39;une période.

## Diagramme de sequence partie
![Diagramme de sequence partie](https://github.com/SportJet/SportJet.github.io/raw/master/img/fig128125.png)

## Diagramme de sequence chrono
![Diagramme de sequence chrono](https://github.com/SportJet/SportJet.github.io/raw/master/img/fig134670.png)

# BDD
![DDB](https://github.com/SportJet/SportJet.github.io/raw/master/img/Untitled.png)
