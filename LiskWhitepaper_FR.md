## Table of Contents

1. [Introduction](#1-introduction)
	1. [Qu'est ce que Lisk ?](#1-what-is-lisk)
	2. [Aspects techniques](#2-technical-background)
	3. [Les innovations clés](#3-key-innovation-factors)
	4. [Les composants de Lisk](#4-lisk-components)
2. [Clients](#2-clients)
	1. [Lisk (client lourd)](#1-lisk)
	2. [Lisk Lite (client léger)](#2-lisk-lite)
	3. [Lisk Mobile](#3-lisk-mobile)
3. [Consensus](#3-consensus)
	1. [Délégués](#1-delegates)
	2. [Taxes de réseau](#2-network-fees)
	3. [Peer-to-Peer](#3-peer-to-peer)
4. [Fonctionnalités centrales](#4-core-features)
	1. [Les noms d'utilisateur](#1-usernames)
	2. [Contactes](#2-contacts)
	3. [Multi-signatures](#3-multi-signatures)
5. [Applications décentralisées](#5-decentralized-applications)
	1. [Machine Virtuelle](#1-virtual-machine)
	2. [Dapps](#2-dapps)
	3. [Développement de Dapps](#3-dapps-development)
	4. [Exécution d'une Dapp](#4-dapps-computation)
	5. [Consensus des Dapps](#5-dapps-consensus)
	6. [Les noeuds maîtres](#6-dapps-master-nodes)
	7. [L'enregistrement de Dapps](#7-dapps-storage)
	8. [Le crédit et le débit avec une Dapp](#8-dapps-deposits-withdrawals)
	9. [La monnaie d'une Dapp](#9-dapps-tokens)
6. [Appendix](#6-appendix)
7. [Sources](#7-sources)

## 1. Introduction

### 1. Qu'est ce que Lisk ?

Lisk est une plateforme nouvelle génération permettant de développer et distribuer des applications JavaScript décentralisées à l'aide d'un écosystème complet et facile à prendre en main. Avec Lisk, les développeurs peuvent publier, distribuer et monétiser leurs applications avec une cryptomonnaie adaptée qui utilise un système de blockain modifié, des smart contracts, cloud storage et des computing nodes; le tout dans une seule solution.

### 2. Aspects techniques

La partie serveur de Lisk est développée en Node.js[[1]](http://nodejs.org), la partie client est en HTML5 et CSS3. Tout cela fonctionne en asynchrone, ce qui permet de gérer les transactions au sein du réseau rapidement. La base de données est SQLite pour gérer les requêtes complexes.

### 3. Les innovations clés

Lisk est la première solution d'applications décentralisées entièrement développée en Node.js. L'écosystème de Lisk s'ouvre alors à des milliers de développeurs ayant les compétences adaptées. N'importe quel développeur qui connait JavaScript et Node.js peut immédiatement commencer à développer une application décentralisée, dès le premier jour.

Notre premier but avec Lisk est de produire un environnement plug&play qui permettrait aux développeurs de tout faire que ce soit le design, le développement, la publication et la monétisation d'une application, le tout depuis une seule plateforme. En utilisant Lisk, les développeurs peuvent rapidement déployer leurs applications JavaScript sur l'hébergeur Lisk & Noeuds de stockage, être référencé dans le Lisk Dapp Store, et avoir directement accès à Lisk Compute Nodes qui exécute le code des applications. Le tout étant sécurisé par l'intégrité et la sécurisation du consensus [sidechain](https://bitcoin.fr/blockchain-et-sidechains/) de Lisk. 

Pour couronner le tout, toutes ces fonctions en cloud sont exécutées par des utilisateurs et des délégués de Lisk qui sont payés grâce à un système de facturation interne (ou par le réseau lorsque c'est un délégué) et sont payés en LISK (la cryptomonnaie propre à Lisk) ou en Bitcoin. C'est typiquement l'endroit parfait pour les applications techniques, accéssibles et en avance dans l'innovation.

### 4. Les composants de Lisk

- Hébergement décentralisé en P2P pour Dapps
- Stockage décentralisé en P2P pour Dapps
- Calculs décentralisés
- Consensus sidechain pour toutes les Dapps
- Interface API pour Lisk et Bitcoin
- Outils de développement : Lisk CLI / Lisk Dapp SDK

## 2. Clients

### 1. Lisk (client lourd)

Le client lourd est la meilleure solutions pour les supers-utilisateurs, les délégués et les développeurs. C'est disponnible pour Windows, Mac OS et Linux. Cependant être délégué n'est que possible sur Linux. Le client léger peut être connecté au client lourd pour accéder au réseau.

Ils peuvent être utilisés pour réaliser des appels API, si c'est autorisé par le propriétaire du client lourd. Tous les clients lourds téléchargent la blockchain en P2P.

### 2. Lisk Lite (client léger)

La plupart des utilisateurs utiliseront le client léger pour accéder à leur compte Lisk, c'est une version alléger du client Lisk.

Le client léger est disponnible sur Windows et Mac OS. Il ne nécessite pas d'installation puisqu'il est lancé directement sur le navigateur. Ce n'est pas un noeud de réseau, ce client est connecté à Internet et communique avec le protocole HTTP. Cela apporte quelques avantages.

L'utilisateur n'a pas besoin de télécharger la blockchain, ce qui veut dire que l'application est très légère. La clé secrète n'est pas envoyée à travers le réseau, toutes les données sont signées depuis la machine locale. Il est possible de réaliser tout type de transaction.

Si on souhaite déléguer un noeud, il est possible de l'enregistrer avec le client léger. Cependant, il n'est pas possible d'exécuter un noeud depuis ce client, c'est à dire créer de nouveaux bloques. Pour cela il est nécessaire d'utiliser le client lourd.

Les utilisateurs de Dapp peuvent utiliser le client léger pour accéder à leurs Dapp applications. L'API Dapp et les APIs connexes sont accéssibles par les développeurs.

C'est ce qui permet de facilement créer des Dapps JavaScript avec nw.js[[2]](https://github.com/nwjs/nw.js) ou Electron[[3]](https://github.com/atom/electron).

### 3. Lisk Mobile

Le client mobile de Lisk permet aux utilisateurs d'accéder à leur compte depuis n'importe où. Le client sera disponnible sur iOS et Android, publié sur Apple Store et Google Play.

L'infrastructure serveur pour le client mobile sera une copie de celui utilisé pour le client lourd. Le vrai changement réside dans l'apparence du client afin d'améliorer l'expérience utilisateur sur petit écran. L'application a été adapté à une interface mobile, comme Bitcoin ou les applications de banque qu'on utilise déjà. Cela permettra de lancer toutes les Dapps depuis le client mobile. Nous projettons de développer des fonctionnalités propres au mobile tel que l'empreinte digitale ou l'empreinte rétinienne pour accroître la sécurité.

## 3. Consensus

Lisk est basé sur le DPoS[[4]](http://wiki.bitshares.org/index.php/BitShares) (Delegated Proof of Stake) mécanisme de consensus. Cette méthode de consensus a été créée par l'équipe BitShares.

DPoS est basé sur des délégués pouvant créer des bloques. Les délégués sont des comptes de confiance qui sont élus comme "Délégués Actifs". Les 101 délégués avec le plus de votes peuvent créer des bloques. Les autres délégués, n'étant pas dans le top 101, sont des "Délégués en Attente", ils peuvent atteindre le top 101 de la liste des délégués en recevant des votes par les détenteurs de LSK. Tous les utilisateurs de Lisk ont 101 votes disponnibles pour déléguer leurs candidats favoris. Le poids de vote est proportionnel au montant que possède le votant dans son portefeuille Lisk. Le montant total est affiché dans la liste des délégués avec le status "Approuvé", et est listé en pourcentage selon un ratio du total de montant voté pour le délégué et les 100 millions de Lisk disponnibles.

La promotion des délégués au top 101 ou la déstitution des délégués intervient lors de la réalisation d'un cycle de 101 bloques. Chaque cycle de 101 bloques est créé dans un ordre aléatoire par les délégués du top 101. Le temps d'un bloque est de 10 secondes. Les bloques fraîchement créés sont diffusés dans le réseau et ajoutés à la blockchain. Après 6 à 10 confirmations, un bloque, avec également ses transactions, peut être considéré comme "confirmé". Un cycle de 101 bloques prend approximativement 16 minutes.

Avec DPoS, des mises à jour lourdes peuvent exister, mais la mise à jour la plus longue est prioritaire. Les délégués doivent être en ligne en même temps et avoir un temps d'activité suffisament long. Le temps d'activité est utilisé pour définir le niveau de confiance d'un noeud en journalisant chaque instant où ce noeud "rate" un bloque pour lequel il était assigné. Les utilisateurs votent pour le top 101 selon plusieurs facteurs, le temps d'activité étant un facteur clé pour déterminer le vote. Si un délégué diminue son activité, les utilisateurs peuvent supprimer leur vote pour cause de mauvaise performance. 

### 1. Délégués

La fonction des délégués est expliquée dans la section sur le consensus.

Pour être délégué, un utilisateur doit enregistrer un compte de délégué. Cela peut être fait depuis le client lourd ou le client léger. Il faut garder à l'esprit la généreration de bloques n'est possible qu'avec un portefeuille complet. Cela signifie qu'il est possible d'enregistrer un délégué avec n'importe quelle version de portefeuille mais qu'il ne pourra entrer en activité qu'avec un client complet. Le numéro de compte et le nom d'utilisateur sera le même après l'enregistrement comme délégué. Tous les comptes Lisk sont peuvent s'inscrire comme délégués.

Les nouveaux délégués commencent comme délégués en attente. Les délégués en attante débutent avec un approbation équivalente à 0% et auront besoin de votes de la communauté Lisk afin de monter dans la liste de top 101 des délégués. La génération de bloques est seulement réalisée par les délégués du top 101. Un délégué en attente ne pourra forger de bloques.

### 2. Taxes de réseau

Toutes les transaction valides au sein du réseau doivent être opérées. Les délégués opèrent les transactions et les enregistre dans de nouveaux bloques. Pour que tout fonctionne, les délégués recoivent une taxe. Toutes les transactions du réseau doivent contenir un montant de taxe pour éviter les spammes.

La taxe par défault dans le réseau est de 0,1 LISK. Par exemple, un transaction de 100 LISK inclut un taxe de 0,1 LISK pour une transaction équivalente à 100,1 LISK.

Ci-dessous une liste des différents types de transaction :

- 0,1 LISK de taxe pour un envoi de transaction
- 5 LISK pour enregister un second mot de passe
- 100 LISK pour enregistrer un nom d'utilisateur
- 100 LISK pour enregistrer un délégué
- 1 LISK pour ajouter une contact
- 500 LISK pour enregistrer une Dapp
- 5 LISK par membre pour enregistrer une multi-signature par groupe.

Les délégués recoivent les taxes de toutes les transactions du dernier cycle de bloques (101 bloques). Les taxes sont partagées équitablement entre les délégués qui ont créé des bloques dans le cycle. Les délégués qui manquent de créer des bloques dans le cycle alors qu'ils leur étaient assignés ne seront pas payés.

### 3. Peer-to-Peer

Nous utilisons un réseau standard de P2P[[5]](https://en.wikipedia.org/wiki/Peer-to-peer) qui fonctionne avec le protocol HTTP et utilise le format JSON pour échanger les données. Le module P2P récupère les informations de chaque pair suivantes :

- Version  
- Système d'opération  
- Adresse IP  
- Numéro de Port  

## 4. Fonctionnalités centrales

### 1. Les noms d'utilisateur

Lisk permet aux utilisateurs d'enregistrer des noms d'utilisateur qui sert d'alias à un compte. Les autres utilisateurs peuvent envoyer des transactions vers le nom d'utilisateur et les comptes liés la recevront. Cette fonctionnalité permet de simplement retenir des comptes avec des adresses longues.

La taxe pour enregistrer un nom d'utilisateur est de 100 LISK. Les noms d'utilisateur peuvent contenir les caractères suivants :

- Alphabet traditionnel (minuscule et majuscule) : A-Z, a-z
- Des nombres de 0 à 9 : 0-9
- Des caractères spéciaux : !, @, $, &, et .

Chaque nom d'utilisateur est unique. La taille est actuellement limités à 16 caractères. Ce n'est pour l'instant pas possible de supprimer un nom d'utilisateur.

### 2. Contactes

Lisk permet de gérer une liste de contactes ou d'amis. Cette fonctionnalité peut être utilisée pour enregistrer des comptes fréquemment utilisés, mais il peut aussi être utilisé comme système à réputation. Si un compte possède des contactes confirmés, il pourrait être considéré comme plus populaire que d'autres qui n'en ont pas.

Les contactes fonctionnent comme les "followers" dans Twitter. Un utilisateur est ajouté à la liste de contactes qui sera alors affiché comme contacte en attente dans le portefeuille de l'utilisateur. Le contacte ajouté sera affiché dans la liste des contactes, que l'utilisateur ajouté ait accepté ou non. Lorsque l'utilisateur ajouté accepte la demande de contacte, l'envoyeur de la requête sera alors ajouté dans sa liste de contactes. Les deux utilisateurs ont alors chacun un nouvel utilisateur confirmé. 

La taxe de réseau pour ajouter un nouvel utilisateur ou accepter une requête est de 1 LISK.

### 3. Multi-signatures

Lisk permet aux utilisateurs de créer des groupes de multi-signatures. Un groupe de multi-signatures consistes en un groupe d'utilisateurs, appellés les membres du groupe. Les transactions avec un groupe de multi-signatures peut être configuré pour nécessiter l'approbation des tous les membres pour effectuer une transaction.

Pour effectuer cela, une achitecture M à N multi-signatures a été implémentée. Tous les membres du groupe de multi-signatures (N) sont ajoutés, limité à un maximum de 16 signataires, et le nombre requis (M) de signatures pour approuver une transaction est paramétré.

M doit être supérieur à 1 et inférieur ou égal à N. N étant le nombre de membres du groupe de multi-signatures.

Lorque une transaction d'un groupe de multi-signatures est initialisée, tous les membres verront un transaction en attente et seront aptes à l'approuver ou l'ignorer. Une fois le nombre de confirmation atteint, le groupe permet la transaction et peut être validée pour envoi à la blockchain.

Le propriétaire du groupe de multi-signatures peut changer les règles du groupe lorsqu'il le souhaite à condition d'avoir l'approbation de M signataires. 

## 5. Application Décentralisées  

### 1. Machine virtuelle  

Les applications Lisk sont exécutées par les noeuds Lisk, une version NodeJS spécialisée offre un environnement bac-à-sable dans lequel on peut exécuter des Dapps. Les communications internes sont effectuées avec Names Pipes qui n'impose pas de limite en taille de message.

Dès le lancement d'une nouvelle Dapp, le client Lisk démarre une nouvelle instance de noeud Lisk comme processus enfant. Lorsqu'une Dapp rencontre une erreur fatale, le processus enfant est arrêté dans le but de ne pas impacter le client Lisk parent.

**Il est à noter qu'actuellement il n'y a pas de protection contre les appels non-autorisés d'une Dapp en court de lancement. C'est pourquoi il n'est pas conseillé de lancer des programmes non-sécurisés au risque de perdre des fonds. Nous travaillons au développement d'un environnement bac-à-sable pour les programmes non-sécurisés.** 

### 2. Dapps

Une Dapp est une application décentralisée[[8]](https://github.com/DavidJohnstonCEO/DecentralizedApplications/blob/master/README.md) écrite en Node.js et JavaScript. Une Dapp fonctionne avec la machine virtuelle (VM) Lisk qui utilisé l'algorithme de consensus de Lisk ou bientôt celui de Bitcoin. La VM de Lisk une application Node.js scalable qui permet aux développeurs compétents en JavaScript de produire des Dapps. Avec les technologies du web actuelles (HTML5/CSS3/JavaScript) les développeurs peuvent créer des interfaces utilisateur performantes. Dapp utilise des paquets modifiés de Node.js avec NPM (Node.js Package Manager, gestionnaire de paquets de Node.js).

### 3. Développement de Dapps

Les développeurs écrivent des Dapps en JavaScript qui permet de profiter entièrement de l'écosystème de Node.js et de son gestionnaire de paquets NPM. La VM de Lisk est intégrée avec l'API de Lisk. Cette API est une interface de la blockchain de Lisk et également de la blockchain de Bitcoin. Chaque Dapps est exécuté dans une VM Lisk, ce qui supprimer toutes attaques possibles et isole le développement d'un Dapp pour la sécurité. L'API de Lisk est accéssible par la Dapp.

Pour rendre le développement de Dapp facile, l'équipe de Lisk a publié lisk-cli, une interface en ligne de commande qui créé son propre testnet et un environnement Dapp. Également nous préparons une boîte à outils Dapp, qui offre aux développeurs une référence pour l'implémentation des fonctionnalités importantes de Dapp, et qui sert de base solide pour commencer à produire une Dapp.

Plusieurs librairies ont été écrites pour offrir toutes les fonctionnalités de l'API de Lisk.

L'API inclut :  

* L'algorithme de consensus  
* L'API de Lisk  
* L'API de Bitcoin  
* L'API de la base de données  

Pour ouvrir une Dapp, le format : `http://ip:port/dapps/<dapp_id/username>` est utilisé.

### 4. Exécution d'une Dapp

L'équipe de Lisk est en train de développer un système qui permet de facturer de temps de calcul. La VM de Lisk analyse le temps de calcul nécessaire à un processeur pour lancer une Dapp. Cela a pour effet de permettre aux propriétaires de noeuds de lancer une Dapp maîtresse pour recevoir des LISK ou des Bitcoins en retour.

L'objectif de Lisk est de créer une écosystème unique, où le calcul n'est qu'une partie. À l'avenir, Lisk fournira un mécanisme de publication de Dapps pour des noeuds candidats, capables alors d'exécuter des Dapps, selon les ressources nécessaire pour une Dapp afin d'obtenir un meilleur rendement (prix/performance). Le propriétaire du noeud recevra un revenu pour son service de calcul, de mémoire et d'autres ressources.

Cela est appelé Dapps Billing. On peut comparer cela à la plateforme Heroku qui déploie des applications.

### 5. Consensus des Dapps

Chaque Dapp possède son propre sidechain qui opère en parallèle avec les bloques de Lisk.

Les sidechains de Dapp sont gérées par le groupe des top 101 noeuds maîtres, chacun peut générer des bloques pour une Dapp. Le rôle premier de chaque noeud maître est de contrôller les transactions et valider chaque bloque générés dans une sidechain.

La signature des bloques par un noeud maître peut être restreint par le propriétaire de la Dapp. Il est capable alors de sélectionner les noeuds maîtres qui pourront forger des bloques dans la sidechain de la Dapp.

Le consensus sidechain est maintenu dans le top 101 des noeuds maîtres avec la méthode DPoS utilisée pour sécuriser la blockchain de Lisk. C'est ce qui permet à chaque noeud maître de récupérer une partie des taxes par la sécurisation d'une sidechain.

L'objectif de ce mécanisme de consensus est de prévenir des dépassement de taille des bloques au sein de la blockchain et de conserver les sidechain autonomes, tandis que l'intégrité de chaque sidechain est assurée.

Il est à noter qu'une alternative future est prévue, les Dapps de Lisk pourront plutôt être sécurisées par la blockchain de Bitcoin avec la même méthode DPoS. 

### 6. Les noeuds maîtres

Les noeuds maîtres d'une Dapp sont des noeuds de Lisk avec la Dapp installée et qui génèrent des bloques spécifiquement pour la Dapp. Les propriétaires de Dapps doivent approuver chaque compte pour qu'ils soient des noeuds maîtres. Ces noeuds peuvent ensuite contrôller les transactions et générer de nouveaux bloques conformes à la blockchain de Lisk, ces noeuds sont les fondations d'une Dapp. 

### 7. L'enregistrement de Dapps

Il est possible d'enregistrer des Dapps dans n'importe quel réseau, centralisé ou décentralisé. Cependant, le réseau doit fournir un lien de téléchargement vers une archive ZIP. C'est nécessaire car un utilisateur qui veut utiliser la Dapp doit être capable de la télécharger en premier lieu.

Lorsque Lisk aura évolué IPFS[[10]](https://ipfs.io) sera nativement intégré à Lisk comme un système d'enregistrement décentralisé. 

### 8. Le crédit et le débit avec une Dapp

Les développeurs peuvent utiliser soit LISK soit BTC avec leur Dapps. Les utilisateurs d'une Dapp peuvent créditer ou débiter des fonds depuis n'importe quelle Dapp. Lorsque des LISK ou des BTC sont envoyés à une adresse Dapp, les fonds apparaissent dans les comptes de la Dapp. Ces fonds sont ensuite disponibles dans la Dapp. Cela fonctionne de la même manière avec le débit. Les BTC sont envoyés à une adresse spéciale de la Dapp puis apparaissent dans le portefeuille Bitcoin de la Dapp.

Un compte Dapp est un compte spécial créé par le propriétaire de la Dapp. Tous les crédits LISK ou BTC sont enregistrés sur l'adresse associée. Pour des raisons de sécurité, seulement la multi-signature est autorisée pour la gestion des comptes d'une Dapp.

Les débits depuis une Dapp sont contrôllés par les noeuds maîtres. Lorsque un débit est demandé, le noeud maître l'opère et déplace les fonds vers l'adresse spécifiée dans la blockchain Lisk ou la blockchain Bitcoin.

### 9. La monnaie d'une Dapp

Les développeurs devraient intégrer leur propre monnaie dans leur Dapp, et elle sera utilisée comme monnaie d'échange au sein de la Dapp. Ces monnaies peuvent être utilisées de la même façon que LISK ou BTC, mais ces monnaies ne peuvent être directement déplacées d'une sidechain à une autre. Elles ne peuvent que circuler sur la blockchain de Lisk.

## 6. Appendice

### Écrit par

* Max Kordek  
* Oliver Beddows  

### Traduit de l'anglais au français par

* Jonathan Serra

### Date de lancement

* 1er février 2016 (v1.0)  

## 7. Sources  

* [1] [node.js Organization.](https://nodejs.org)  
* [2] [nw.js](https://github.com/nwjs/nw.js)  
* [3] [Electron](https://github.com/atom/electron)  
* [4] [Bitshares DPoS.](http://wiki.bitshares.org/index.php/BitShares)  
* [5] [Peer-to-Peer Wikipedia Article](https://en.wikipedia.org/wiki/Peer-to-peer)  
* [6] [Seccomp Wikipedia Article](https://en.wikipedia.org/wiki/Seccomp)  
* [7] [npm.js](http://npmjs.org)  
* [8] [David Johnston. Decentralized Applications.](https://github.com/DavidJohnstonCEO/DecentralizedApplications/blob/master/README.md)  
* [9] [Factom. Merkle tree.](https://github.com/FactomProject/FactomDocs/blob/master/Factom_Whitepaper.pdf)  
* [10] [IPFS. A decentralized storage solution.](https://ipfs.io)  
* [11] [Sidechains. Deposit/withdrawal sidechain.](https://www.blockstream.com/sidechains.pdf)  
