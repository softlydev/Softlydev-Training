# Module 3 — Les données dans le cloud (Semaines 5–6 · Intermédiaire)

À la fin du module, l'élève opère une base PostgreSQL managée sur Azure et a migré un schéma Oracle vers elle (Projet 2). C'est le module qui distingue cette formation des autres : l'IA ne vaut rien sans des données bien gérées.

## Leçon 3.1 — Base managée ou base sur VM ?

**Explication :** sur une VM, tu gères tout : patchs, sauvegardes, haute disponibilité. Avec Azure Database for PostgreSQL flexible server, Azure s'en charge et tu te concentres sur les données. On choisit la VM seulement si on a besoin d'un accès total au système.

## Leçon 3.2 — Créer son serveur PostgreSQL

**Explication :** trois gammes : *Burstable* (dev et tests, le moins cher), *General Purpose* (production), *Memory Optimized* (grosses charges). Pour la formation, prends toujours Burstable et arrête le serveur quand tu ne t'en sers pas.

**À suivre :** [Quickstart Microsoft — Créer un serveur flexible PostgreSQL](https://learn.microsoft.com/en-us/azure/postgresql/flexible-server/quickstart-create-server) (portail, CLI ou ARM) · [Version Azure CLI](https://learn.microsoft.com/hr-hr/azure/postgresql/flexible-server/quickstart-create-server-cli).

**Exercice :** crée le serveur avec Terraform (réutilise le module 2), en accès privé via le VNet.

## Leçon 3.3 — Sécuriser l'accès

**Explication :** pas d'IP publique ouverte à tout Internet, connexion chiffrée (SSL), authentification via Entra ID de préférence au mot de passe, un utilisateur applicatif avec des droits limités. Le compte admin ne sert qu'à l'administration.

## Leçon 3.4 — Sauvegardes et restauration

**Explication :** Azure sauvegarde automatiquement et permet une restauration à un instant précis (*point-in-time restore*). Une sauvegarde qu'on n'a jamais testée n'existe pas.

**Exercice :** supprime volontairement une table, puis restaure le serveur à la minute d'avant.

## Leçon 3.5 — Performance : index et plans d'exécution

**Explication :** 80 % des lenteurs viennent d'un index manquant. `EXPLAIN ANALYZE` montre comment PostgreSQL exécute une requête : un *Seq Scan* sur une grosse table est souvent le coupable.

**Exercice :** charge 1 million de lignes, mesure une requête lente, ajoute un index, mesure à nouveau.

## Leçon 3.6 — Migrer d'Oracle vers PostgreSQL

**Explication :** l'outil libre Ora2Pg se connecte à Oracle, analyse le schéma, estime la complexité de migration et génère les scripts SQL pour PostgreSQL. Les étapes : évaluation → export du schéma → correction manuelle (PL/SQL, types, séquences) → import des données → validation des volumes et des objets.

**À suivre :** [Guide Microsoft — Migrer Oracle vers Azure PostgreSQL avec Ora2Pg](https://learn.microsoft.com/azure/postgresql/migrate/oracle-migration/how-to-migrate-oracle-ora2pg) · [Retour d'expérience d'un projet de plusieurs téraoctets](https://medium.com/@chbasani/oracle-db-migration-to-azure-database-for-postgres-pg-69ee8ce34e07) (niveau Avancé).

## Projet 2 — Migration d'une base vers Azure

**Mission :** à partir d'une base Oracle XE en conteneur Docker avec un schéma d'exemple, migrer schéma et données vers le serveur PostgreSQL Azure avec Ora2Pg, puis brancher l'app du Projet 1 dessus.

**Tu as réussi si :** le nombre de lignes par table est identique des deux côtés, l'app lit les données migrées, et ton README documente les 3 problèmes rencontrés et leur correction. Ce README est ton meilleur argument en entretien.
