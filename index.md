---
layout: default
---
<h1 id="sportjet">SportJet</h1>

<p>Une création "<strong>original</strong>" - Lycée de Lorgues
<strong>SportJet</strong> est un Mini projet de BTS Snir.</p>

<h2 id="utilisation">Utilisation</h2>

<p><strong>SportJet</strong> est un ensemble matériel.
<img src="https://github.com/SportJet/SportJet.github.io/raw/master/web/img/shem.png" alt="shem" />
un Arduino est connecter au réseau via une connexion Ethernet et peut etre controler via un Appareil Android.</p>

<h1 id="miseenplacelancementendev">Mise en place - Lancement ( En Dev)</h1>

<h2 id="serveurbdd">Serveur BDD</h2>

<p>le Serveur BDD permet d'enregistré le score des match.</p>

<h2 id="raspberrypi">Raspberry Pi</h2>

<p>le Raspberry Pi controle en I2C le panneux LED, il recois via des Socket les commande a exercé sur le Panneux.</p>

<h2 id="applicationandroid">Application Android</h2>

<p>Permet d'envoier des ordres via des Socket sur le réseau, il permet donc de controler le panneau LED.</p>

<h1 id="uml">UML</h1>

<h2 id="diagramdedploiment">Diagram de déploiment</h2>

<p><img src="https://github.com/SportJet/SportJet.github.io/raw/master/web/img/usecase.png" alt="use case" /></p>

<h2 id="scnarii">Scénarii</h2>

<ul>
<li>L&#39;arbitre assistant démarre une partie. Le chronomètre démarre. Le score s&#39;initialise à 0:0.</li>

<li>L&#39;arbitre assistant peut stopper le chronomètre et le relancer.</li>

<li>L&#39;arbitre assistant peut incrémenter ou décrémenter le score d&#39;une des deux équipes.</li>

<li>Si un problème de connexion réseau à lieu alors l&#39;arbitre assistant utilise le boîter de commande.</li>

<li>L&#39;arbitre assistant enregistrer le score de la partie, puis le transmettre à la fédération.</li>

<li>Il signale la fin d&#39;une période.</li>
</ul>

<h2 id="diagrammedesequencepartie">Diagramme de sequence partie</h2>

<p><img src="https://github.com/SportJet/SportJet.github.io/raw/master/web/img/sec1.png" alt="Diagramme de sequence partie" /></p>

<h2 id="diagrammedesequencechrono">Diagramme de sequence chrono</h2>

<p><img src="https://github.com/SportJet/SportJet.github.io/raw/master/web/img/sec2.png" alt="Diagramme de sequence chrono" /></p>

<h1 id="bdd">BDD</h1>

<p><img src="https://github.com/SportJet/SportJet.github.io/raw/master/web/img/bdd.png" alt="DDB" /></p>
