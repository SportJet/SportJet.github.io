# SportJet

Une création "**original**" - Lycée de Lorgues
**SportJet** est un Mini projet de BTS Snir.

## Utilisation
**SportJet** est un ensemble matériel.
![enter image description here](https://github.com/SportJet/SportJet.github.io/raw/master/img/shem1.png)un Arduino est connecter au réseau via une connexion Ethernet et peut etre controler via un Appareil Android.

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
```mermaid
sequenceDiagram
Arbitre ->> IHM Tablette: apuis démarer partie
IHM Tablette ->>C_Rasp: ResevoirSocket()
C_Rasp ->> C_Partie: DémarrerPartie()
C_Partie ->> C_chronometre: DémarrerChrono()

Arbitre ->> IHM Tablette: apuis incrémenté score
IHM Tablette ->>C_Rasp: ResevoirSocket()
C_Rasp ->> C_Partie: IncrémenterScore()

Arbitre ->> IHM Tablette: apuis arret partie
IHM Tablette ->>C_Rasp: ResevoirSocket()
C_Rasp ->> C_Partie: ArreterPartie()
C_Partie ->> C_chronometre: stopper_Chrono()
```
<details> 
<summary>Version Bouml</summary>
<div>
![Diagramme de sequence partie](https://github.com/SportJet/SportJet.github.io/raw/master/img/fig128125.png)
</div> 
</details>



## Diagramme de sequence chrono
![Diagramme de sequence chrono](https://github.com/SportJet/SportJet.github.io/raw/master/img/fig134670.png)
# BDD
![DDB](https://github.com/SportJet/SportJet.github.io/raw/master/img/Untitled.png)



# Publication

Publishing in StackEdit makes it simple for you to publish online your files. Once you're happy with a file, you can publish it to different hosting platforms like **Blogger**, **Dropbox**, **Gist**, **GitHub**, **Google Drive**, **WordPress** and **Zendesk**. With [Handlebars templates](http://handlebarsjs.com/), you have full control over what you export.

> Before starting to publish, you must link an account in the **Publish** sub-menu.

## Publish a File

You can publish your file by opening the **Publish** sub-menu and by clicking **Publish to**. For some locations, you can choose between the following formats:

- Markdown: publish the Markdown text on a website that can interpret it (**GitHub** for instance),
- HTML: publish the file converted to HTML via a Handlebars template (on a blog for example).

## Update a publication

After publishing, StackEdit keeps your file linked to that publication which makes it easy for you to re-publish it. Once you have modified your file and you want to update your publication, click on the **Publish now** button in the navigation bar.

> **Note:** The **Publish now** button is disabled if your file has not been published yet.


# Markdown extensions

StackEdit extends the standard Markdown syntax by adding extra **Markdown extensions**, providing you with some nice features.

> **ProTip:** You can disable any **Markdown extension** in the **File properties** dialog.


## SmartyPants

SmartyPants converts ASCII punctuation characters into "smart" typographic punctuation HTML entities. For example:

|                |ASCII                          |HTML                         |
|----------------|-------------------------------|-----------------------------|
|Single backticks|`'Isn't this fun?'`            |'Isn't this fun?'            |
|Quotes          |`"Isn't this fun?"`            |"Isn't this fun?"            |
|Dashes          |`-- is en-dash, --- is em-dash`|-- is en-dash, --- is em-dash|


## KaTeX

You can render LaTeX mathematical expressions using [KaTeX](https://khan.github.io/KaTeX/):

The *Gamma function* satisfying $\Gamma(n) = (n-1)!\quad\forall n\in\mathbb N$ is via the Euler integral

$$
\Gamma(z) = \int_0^\infty t^{z-1}e^{-t}dt\,.
$$

> You can find more information about **LaTeX** mathematical expressions [here](http://meta.math.stackexchange.com/questions/5020/mathjax-basic-tutorial-and-quick-reference).


## UML diagrams

You can render UML diagrams using [Mermaid](https://mermaidjs.github.io/). For example, this will produce a sequence diagram:

```mermaid
sequenceDiagram
Alice ->> Bob: Hello Bob, how are you?
Bob-->>John: How about you John?
Bob--x Alice: I am good thanks!
Bob-x John: I am good thanks!
Note right of John: Bob thinks a long<br/>long time, so long<br/>that the text does<br/>not fit on a row.

Bob-->Alice: Checking with John...
Alice->John: Yes... John, how are you?
```

And this will produce a flow chart:

```mermaid
graph LR
A[Square Rect] -- Link text --> B((Circle))
A --> C(Round Rect)
B --> D{Rhombus}
C --> D
```
