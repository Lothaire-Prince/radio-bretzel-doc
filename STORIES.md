# Radio Bretzel - Stories

EPIC ID | STORY ID | STORY PURPOSE | PRIORITY | ESTIMATION | COMMENTS
--------|---------|--------------|----------|------------|---------
1 | 1-1 | Générer un flux radio à partir d’une liste de fichiers | 1090 |  | La fonctionnalité permettra de fournir plusieurs flux audio simultanés générés par un seul script LiquidSoap, servant de modèle.
1 | 1-2 | Faire une liste de lecture dynamique | 1080 | | Le script LiquidSoap prendra en argument obligatoire un identifiant de source. Le script devra, avant la fin de la lecture de chaque morceau, envoyer une requête HTTP renseignant son identifiant de source à un serveur web qui lui renverra l'URI du prochain morceau à jouer.
1 | 1-3 | Permettre à l'utilisateur de se connecter à un flux audio au travers d'un navigateur Web | 1070 | | Le script devra envoyer le flux audio généré vers un serveur web, qui le diffusera en HTTP (proxy)
1 | 1-5 | Permettre à l'utilisateur de démarrer ou arrêter la génération du flux audio | 1060 | | Des instances containérisées de LiquidSoap devront pouvoir être **créés** puis **détruits** à la volée par l'application.
1 | 1-6 | Relancer automatiquement un flux audio défaillant | 1050 | |  Les données de tous les containers lancés devront être enregistrées et régulièrement mises à jour. L'application devra sonder en permanence l'état des containers LiquidSoap, et les relancer avec les mêmes paramètres en cas de chute
2 | 2-1 | Création des schémas de données ‘Tracks’ | 990 | |
2 | 2-2 | Permettre l'ajout de fichier audio sur le server | 980 | |
2 | 2-3 | Effectuer une vérification des fichiers (sécurité) | 970 | | Les fichiers devront être testés dans un nouveau container.
2 | 2-4 | Permettre au flux audio de lire tous les morceaux ajoutés (liste de lecture dynamique) | 960 | | L'algorithme de sélection du prochain morceau doit tenir compte des fichiers récemment uploadés et dont les tests se sont passé sans erreur.
3 | 3-1 | Créer les schémas de données 'User' et 'Team' | 890 | | Un User ne peut avoir **qu'une seule Team**
3 | 3-2 | Attacher automatiquement les Tracks à une Team lors de leur upload | 880 | | Chaque Team a son propre _Pool_ de musique, indépendant de celui des autres Teams
3 | 3-3 | Attacher un flux audio à chaque Team créée, généré à partir des Tracks associées | 870 | |
4 | 4-1 | Permettre à l'utilisateur de réaliser une demande de création de Team, en renseignant une série d'informations sur lui et la Team qu'il souhaite créer | 790 | |
4 | 4-2 | Donner à l’administrateur la possibilité de valider ou non la demande et d’en informer l’utilisateur | 780 | |
4 | 4-3 | Permettre à l'administrateur de restreindre les ressources physiques et logiques d'une Team | 770 | |
4 | 4-4 | Donner à l’utilisateur la possibilité de compléter et de modifier ses informations relatives à la création de son compte et celui de la Team qu'il souhaite créer | 760 | |
5 | 5-1 | Permettre à l'utilisateur de réaliser une demande de création de compte au sein d'une Team, en renseignant une série d'informations sur lui | 690 | |
5 | 5-2 | Donner au Chief de la Team la possibilité de valider ou non la demande et d'en informer l'utilisateur | 680 | |
5 | 5-3 | Donner à l'utilisateur la possibilité de compléter et modifier ses informations relatives à la création de son compte. | 670 | |
6 | 6-1 | Mettre en place un système d'authentification sécurisé. | 590 | |
6 | 6-2 | Restreindre l'accès aux informations des Teams pour les utilisateurs non authentifiées sur celles-ci | 580 | |
6 | 6-3 | Restreindre l'accès aux flux audio propre à une Team aux seuls utilisateurs authentifiés sur celle-ci | 570 | |
7 | 7-1 | Créer le schéma de données 'Channel' | 490 | |
7 | 7-2 | Permettre au Chief d'une Team de créer plusieurs Channels attachés à sa Team | 480 | |
7 | 7-3 | Permettre au Chief de créer un nouveau flux radio à assigner à un Channel | 470 | |
7 | 7-4 | Permettre au Chief de gérer les listes de lectures des flux audios rattachés aux Channels en choisissant directement les Tracks à associer à ce Channel. | 460 | |
7 | 7-5 | Permettre au Chief d'une Team de restreindre l'accès des Channels à certains utilisateurs de sa Team. | 450 | |
7 | 7-6 | Permettre à tous les utilisateurs d'un Channel d'accéder à l'historique des morceaux joués dans ce Channel. | 440 | |
8 | 8-1 | Permettre aux utilisateurs connectés dans un même Channel de discuter ensemble en temps réel  | 390 | |
8 | 8-2 | Permettre aux utilisateurs d'une même Team de s'envoyer des messages privés | 380 | |
9 | 9-1 | Créer les schémas de données 'Artist' et 'Album' | 290 | |
9 | 9-2 | Lors de l'ajout de morceaux, associer automatiquement les Albums et Artists d'après les métadatas des fichiers ajoutés. Créer les Artits et Albums au besoin | 280 | |
9 | 9-3 | Permettre à l'utilisateur de renseigner ou de modifier les métadatas des morceaux qu'il a ajouté. | 270 | |
9 | 9-4 | Permettre au Chief d'accorder des droits de modification de métadatas à des utilisateurs | 260 | |
10 | 10-1 | Permettre à l'utilisateur de réagir à l'écoute d'un morceau par un système de "Up Vote" ou "Down Vote" | 190 | |
10 | 10-2 | Permettre à l'utilisateur de consulter la liste des morceaux auxquels il a réagi | 180 | |
11 | 11-1 | Fournir un flux audio par Channel en fonction du nombre de Up Vote et Down Vote des utilisateurs du Channel | 90 | |
11 | 11-2 | Permettre aux utilisateurs de consulter la liste des morceaux les plus populaires dans leur Team | 80 | |
11 | 11-3 | Permettre au Chief de consulter la liste des morceaux les plus mal notés. | 70 | |