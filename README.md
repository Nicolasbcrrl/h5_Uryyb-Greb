# h5_Uryyb-Greb

## Schneier 2015: Applied Cryptography

### 10.1 CHOOSING AN ALGORITHM

- Le choix d'un algorithme est une chose délicate où le risque zéro n'est pas grantie.

- Choisir un algorithme publié ou open source, vous offre "une garantie" que l'algorithme a pu être examiné et évaluer par d'autres utilisateurs et cryptographes. De plus, l'open source vous donne l'accès à l'enssemble du code source.Ce qui vous permet d'effectuer une analyse de l'algorithme et d'éventuellement le modifier (si la licence le permet) afin qu'il corresponde au mieux à vos besoins.

- Choisir un algorithme par rapport la réputation d'une entreprise, n'est absolument pas un gage de sécurité. Au même titre que faire appel à un consultant en sécurité. Dans les deux cas vous pouvez avoir affaire à des entités avec des connaissances limitées, voire inexistantes dans le domaine de la cryptography.  

- Faire confiance à son gouvernement fait partie des solutions les moins viables. Les gouvernements n'ont généralement aussi développé dans le domaine que les organisations privées. Cela étant dû à un manque d'investissements. De plus, des organisations étatiques comme la NSA préfèrent garder leurs connaissances pour leurs usages.

- Écrire et utiliser votre propre algorithme peuvent être une solution. Cependant, en faisant cela vous laissez la porte grande ouverte à des potentielles failles de sécuriser. Car votre solution n'a pas été tester par d'autres spécialistes dans le domaine et donc elle sera testée que dans le cas de figure dans lequel vous l'avez créé.

- Des organismes gouvernemental comme le FBI ou la NAS préfére garder secret leur capacité à cracker un algorithme, plutôt que de montrer des informarions qu'il aurais obtenu en crackant l'algorithme utilisé par le suspect.

- Comme lors de la seconde guerre mondial, les alliés interdisait l'utilisation du German Ultra traffic, afin de ne pas montrer aux Allemands qu'ils avaient cassé leur cryptage. La seule exception était si les alliés pouvait prouvé qu'ils ont trouvé les information par un autre moyen crédible.

- Le seul moyen de prouver que la NSA peut casser un algorithme est de crypter un information si importante que sa diffusion mérite de prouvé que la NSA peut venir à bout de l'alogorithme.

- Comme le dit l'auteur dans son livre, "**A good working assumption is that the NSA can read any message that it chooses, but that it cannot read all messages that it chooses.**".

- Tout algorithmes exportés hors des Etats-Unis doivent être approuvés par le gouvernement américain.

- Il est admis que les alogorithm validé par le gouvernemennt américain, peuvent être cassé par la NSA.

- La NSA détient tous les codes sources des algorithms approuvé par le gouvernement pour l'exportation.

### 10.2 PUBLIC-KEY CRYPTOGRAPHY VERSUS SYMMETRIC CRYPTOGRAPHY

- La cryptographie à clé publique et la cryptographie symétrique ne peuvent pas être comparé, car elles sont différente et résolvent des problèmes différents. 

- Pour le cryptage de données, l'utilisation de la cryptographie est la meilleurs solution. Elle est plus rapide et n'est pas soumise au risque des attaque par choix de texte chiffré. 

- La cryptographie à clé publique peut être utilisé pour la gestion des clés et un grand nombre de protocole, chose pour laquel la cryptographie symétique ne peut pas être utilisé. 

### 10.3 ENCRYPTING COMMUNICATIONS CHANNELS

- Le cryptage des données peut intervenir dans n'importe quelle couche du model de communication OSI.

- En pratique le cryptage à lieu dans les couches le plus basse, les couches 1 et 2, soit dans les couches les plus haute. Dans les couches les plus basse, on va parler de link-by-link encryption. Pour les couches supérieurs, on parle alors de end-to-end encryption.

#### Link-by-Link Encryption

- Ce type de cryptage est mis en place dans la couche physique du réseau. Cela est dû au fait que c'est l'endroit le plus simple pour le mettre en place, grâce à la nomalisation des interrfaces et à facilité de connection avec des dispositifs de chiffrement matériel.

- L'encryption link-by-link est très efficace, car il va encrypter toutes les données, les information de routage et les informations protocolaires qui passent par lui.

- Ce type de cryptage est appelé **traffic-flow security**. 

- Un adversaire face à ce type de cryptage ne pourra pas acceder à l'information mais il ne pourra également pas l'endroit et la quantité des données en circulation sur le réseau.

- Cependant, pour que cette solution fonctionne il faut que chaque lien physique du réseau doivent être protéger. 

- Le fait de possèder un gros réseau peut également mettre un frein à la mise en place de cette solution, car elle devient très vite très coûteuse.

#### End-to-End Encryption

- L'encryption end-to-end va crypter des données de manière sélective et premanante, jusqu'à ce que le destinataire les reçoivents.

- L'équipement de cryptage est placé entre la couche réseau et la couche transport.

- L'encryption end-to-end permet d'éviter le cryptage et décryptage au niveau de la couche physique.

- les information d'achminement ne sont pas cryptés. Ce qui permet de les analyser.

- L'opération de cryptage peu être rendue transparante pour l'utilisateur et un seul jue de clé par liaison suffi.

- La mis en place d'un équipement de cryptage end-to-end peut être compliqé en raison des protocoles spécifique à chaque système de communication. 

- Une alternative serait d'effectuer le cryptage à des couches supérieurs de l'architecture de communication, mais cela peut également poser des problème en terme de compatibilité.

#### Combining the Two

- Avec la combinaison des deux approche on obtient un niveau de sécurité plus élevé.

- Tout les liens physique sont crypté. Cela empèche toutes exposition des données aux noeuds intermédaire et également toute analyse du trafic. 

- Afin de simplifier la gestion des clés, la charge peut être répartie pour les deux systèmes.

- Cependant, cette approche est la plus coûteuse en raison de la nécessité de mettre en œuvre les deux systèmes de cryptage.


### 10.4 ENCRYPTING DATA FOR STORAGE

## Sources

---
