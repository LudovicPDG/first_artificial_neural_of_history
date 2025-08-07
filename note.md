# Reproduction du papier A logical calculus of the idea immanent in nervous activity

## context

ce papier a était écris par waren McCulloch et Walter pitts en 1943 alors que walter pitts n'avait que 20 ans. Le character tout ou rien d'un nerf stipule qu'un nerf emet ou n'emet pas de l'information cela n'est donc pas continue. Cette affirmation est toujours considérée comme vrai aujourd'huie mais elle est relativisée car en sait qu'il existe des phenenomene continue au niveau des dentrite ou des soma se qui peut influencer le seil d'activation d'un nerf. toute fois, aujourd'huie en utilise des neuronne qui emet de l'information continue comme avec les fonction d'activation sigmoide et relu.

dans ce papier ils essayent de traiter les neuronne comme des systeme logique.

pour eux tous reseaux peut etre vue comme un system logique et l'inverse tous systeme logique peut etre vue comme un réseau

il est plus compliqué de d'écrire des reseau cerculaire.

le fait que l'activation passé d'un neuronne influence sans seuil d'activation cela rend la modelisation compliqué. Mais c'est surement ca qui est a l'origine de l'apprentissage.

du fait caractere tout ou rien d'un neuronne on peut considéré un neuronne sous forme de logique propositionnel (vrai ou faux)

a chaque fois q'un neuron s'active cela correspond a une logique propositionnel vrai

l'activation d'un neuron peut etre vue comme le resultat logiquede l'activation ou non d'autre neuron ex: Le neurone A s’active si B ET C sont actifs → A = B ∧ C

on peut donc d'un point de vue spacial voir les reseau de neuronne comme formant des systeme plus logique

pour un meme reseau on peut le voire comme plusieur systeme logique mais chaque systeme logique ne s'équivalent pas en terme de temps d'éxécution.

d'un point de vue fonctionnel un neuronne fonctionnant avec des synapse electrique ou chimique se comporte de la meme manière

Pour resoudre le probleme de l'apprentissage, ils propose d'utiliser un reseau de neuronne. meme si dans la réalité le nombre de connexion change dans notre cerveaux, ils propose ici d'utiliser un reseau fixe

on peut utiliser des fonction recursive pour s'occuper des reseau de neuronne recursive

leur modele se base sur 5 hypothèse

📐 Hypothèse (1) : Loi du tout ou rien
L’activité d’un neurone est tout ou rien : il s’active complètement ou pas du tout.
C’est ce qui permet de le représenter par une valeur booléenne (vrai/faux ou 1/0).

📐 Hypothèse (2) : Seuil fixe et sommation spatiale
Un neurone s’active si un nombre fixe de synapses sont excitées dans une courte période (appelée période de sommation).

Peu importe quels synapses précisément sont excités.

Ce nombre est indépendant du passé et de la position sur le neurone.

📐 Hypothèse (3) : Seul délai synaptique est significatif
Le seul délai temporel important dans le calcul est celui de la synapse, pas la vitesse de conduction dans les axones.

📐 Hypothèse (4) : Les synapses inhibitrices sont absolues
Si un inhibiteur est actif, il empêche totalement le neurone de s’activer, même si d'autres synapses sont excitées.

📐 Hypothèse (5) : La structure du réseau est fixe dans le temps
Les connexions ne changent pas.
Cela permet un modèle logique stable, sans plasticité.

Ils utilisent un langage logique inspiré de Carnap, Russell et Whitehead (les auteurs des Principia Mathematica).

À cause des contraintes de typographie, ils adaptent certains symboles :

∃ (existence) est remplacé par un E droit.

L’implication logique ⊃ devient une flèche →.

on peut utiliser un foncteur pour transmet les expression d'écrivant les propriété d'un neuronne par rapport a ses propriété précédente. ex: P(x) est une propriété (exemple : "le neurone A s’active au temps x")

Alors S(P)(x) signifie :

"la propriété P est vraie au temps x–1"

Donc S(P)(x) = P(x–1)

l'ordre du reseau et le nombre de groupe de neuronne qu'il faut retirer pour que le reseau ne soit plus cyclique.

un TPE est une proposition logique portant sur une variable temporelle Z

Si S1 et S2 sont des TPE avec la même variable, alors on peut former :

S(S1) → valeur de S1 au temps précédent

S1 ∨ S2 → disjonction (OU logique)

S1 ∧ S2 → conjonction (ET logique)

¬S1 → négation (NON logique)

Un reseau simple peut totalment etre représenté par un TPE simple

un ci a un seil ei chaque neuronne recoit des synapse excitatrice ci1, ci2 etc.. avec des poid ni1, ni2 etc... et des synapse inhebatrice cj1, cj2

pour qu'un neuronne s'active il doit dépasser son seil sans recevoir de d'information par le synapse enibateur

ex:

### notation

pour ce qui est de la notation on note n le reseau de neuronne c1, c2 etc... le reseau de neuronne qui la compose. le comportement d'un neuronne ci est noté ni(t) ou t est le temps et ducoup ni l'action du neuronne ci (la proposition logique). i peut etre un nombre ou un operateur logique (pour par exemple dire tous les neuronne de 1 a 10)

les neuronne pérépherique sont les neuronne d'entrée cela peut etre vur comme des neuronne sensoriel.

une serie d'equation logique d'écris le comportement d'écris le comportement de chaque neuronne interne ex: Ni(z) = Pri(...) ou pris est la precondition necessaire pour que le neuronne s'active.

une propriété peu etre réalisé soit en narrow sense c'est a dire avec quelque neuronne soit en extended sense avec beaucoup de neuronne.

### fonctionnement du cerveau

Le cerveaux peut etre présentée comme un réseau de neuronne. Un réseau de neuronne comme son nom l'indique est composée de neuronne. un neuronne est composée de trois partie. les dendrite qui sont comme des recepteur il recoive soit de l'information chimique (neuro transmetteur, c'est ce qu'il y'a de plus commun) ou electrique (rare, souvent présent dans les fonction moteur). le soma ou préricaryon (nom souvent utiliser en francais) qui en quelque sorte la partie central du neronne, c'est la que le neuronne va "decider" d'emmetre ou non de l'information, il fait la somme de tous les signaux qu'il recoit et si cela franchit un certain seil (~-55 milivolt) il emet de l'information (les soma peuvent aussi recevoir de l'information, c'est rare). les axone est la partie qui est la partie qui va envoyer de l'information. les axone sont comme une tige qui se ramifie en plein de terminaison axonal

On appelle synapse la zone entre deux neuronne, ce n'est pas un organe mais juste une zone.

les neurotransmetteur peuvent etre exebitteur (+) ou annilateur (-) ou modulateur (+ ou -) on peut leur associé un coefficient d'infleunce ex: +0.8, -0.2, +0.5
Pour ce qui est de l'information electrique on addition le voltage electrique.

le soma a un potentiel de repo (~-70 milivolt) ces le voltage normal d'un soma. Si le soma n'atteint pas son seil d'activation, il revient a son potentiel de repo a partir d'un certain temps.

les synapase electrique communique 10 a 50 fois plus rapidement qu'un synapse chimique.(cela depend de la taille de l'axon et la myéline)
un neuronne artifficiel transmet de l'information 100 000 fois plus vite qu'un synapse electrique. (cela depend du processeur et de l'algorithme)

la myeline et une gaine isolente qui accelere la transsmission d'inforamtion.

somata et le pluriel de soma

il existe différent classe de neuronne generalement en les classe par fonction

- les neuron sensoriel (apporte de l'information)
- les neuron interneuron (transmette de l'information)
- les neuron moteur (donne l'ordre)

les nerf sont en ensemble d'axone parrallele très long.

quand je touche quelque chose l'information est transmis au nerf de mon doigt dans les somata sont situé dans des ganglions nerveaux proche de la moelle epiniare (neuronne sensoriel), qui est transmis a des neuronne dans ma moelle epiniaire jusqu'au neironne dans mon cerveaux.

un neuronne ne peut pas etre activée par un seul neuronne.

un neuronne a ce qu'on appelle une période refractaire absolue ces a dire qu'il ne peut plus activer pendant pendant une certaine periode après qu'il est était activé ou relative cela veut dire que c'est plus compliqué.

au contraire quand un neuronne n'a pas été activer pendant un certain temps il rentre dans une phase de sur activation.

un neuronne generalment libere qu'un seul type de neurotransmetteur, et cela generalement tout le long de ca vit. Par contre un neuronne peut recevoir plusieur type de neurotransmetteur sur ses dendrite ou directement sur son soma.

un neuron comme je les dit peut recevoir plusieur information mais peut aussi emettre plusieur information, car malgrès le fait qu'un neuron ne possede qu'un seul axone il a plusieur terminaison axonal ce qui lui permet d'avoir plusieur synapse.

Le cerveau est plastique, c'est a dire qu'il peut créer de nouveaux neuronne neuro-synthèse (uniquement dans l'hippocampe et les zone sub-ventriculaire), créer des nouvelle synapse en créant de nouvelle dendrite, et nouvelle terminaison axonal. Et renforcant ses synapse (LTP) ou affablissant ses synapse (LTD).
