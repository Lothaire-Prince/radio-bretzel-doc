# Concepts Principaux
## Niveaux applicatifs
### Instance Applicative
L'_Instance_ désigne l'ensemble du service fournit par l'application. Elle est régie par **l'Administrateur Global**, et englobe toutes les composantes logicielles (application web, base de données, serveur proxy, stockage, streams ...).

### Team
La _Team_ désigne un groupe restreint d'utilisateurs et un espace de partage de musique. Elles sont indépendantes les unes des autres, et sont administrées par un _Chief_. Une _Team_ est associée à un **Pool**, l'ensemble des fichiers audio mis en commun par ses membres, et peut contenir plusieurs _Channels_.

### Channel
Le _Channel_ désigne un salon virtuel à l'intérieur d'une _Team_ que les utilisateurs peuvent rejoindre pour écouter de la musique et en discuter en même temps.

## Niveaux de Rôles
### Administrateur
L'_Administrateur_ de l'application a tous les droits possibles. Il est le propriétaire de l'_Instance_, et est le seul à pouvoir créer une _Team_ et promouvoir un utilisateur comme _Chef_. Il surveille et attribue les resources physiques et logiques de l'_Instance_ aux différentes _Team_.

### Chef
Le _Chef_ désigne "l'administrateur de la _Team_", sur laquelle il a tous les droits, hors mis les limites imposées par l'_Adminsitrateur_ (nombre d'utilisateur maximum, bande passante, stockage ...). Le _Chef_ peut inviter des utilisateurs, gérer leurs droits et créer des _Channels_, gérer le _Pool_ de musiques, éditer les méta-data et gérer les comportements des différents _Streams_.

### Utilisateur
L'_Utilisateur_ désigne l'utilisateur final de l'application. Il ne peut appartenir qu'à une seule _Team_ (une personne ayant 2 Teams devra créer 2 comptes). Un _Utilisateur_ non authentifié ne peut rien faire, hors mis demander de rejoindre ou créer une _Team_ Après authentification, l'_Utilisateur_ peut accéder à tous les _Channels_ de la _Team_, y poster des messages, et écouter le flux radio. Enfin, il peut aussi uploader de la musique et venir garnir le _Pool_.
