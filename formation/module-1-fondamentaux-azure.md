# Module 1 — Fondamentaux Cloud & Azure (Semaines 1–2 · Débutant)

À la fin du module, l'élève explique les modèles cloud et déploie une application web sécurisée (Projet 1).

## Leçon 1.1 — Qu'est-ce que le cloud ?

**Explication :** le cloud, c'est louer de l'informatique à la demande au lieu de l'acheter. Trois modèles : **IaaS** (tu loues une machine virtuelle, tu gères le système), **PaaS** (tu déposes ton code, Azure gère le serveur), **SaaS** (tu utilises un logiciel fini, comme Outlook). Plus tu montes, moins tu gères. C'est le *modèle de responsabilité partagée*.

**À suivre :** [Parcours Microsoft — Describe cloud concepts](https://learn.microsoft.com/en-us/training/paths/microsoft-azure-fundamentals-describe-cloud-concepts/) et son module [Describe cloud computing](https://learn.microsoft.com/en-us/training/modules/describe-cloud-compute/).

**Exercice :** classe 10 services que tu connais (Gmail, une VM, Netflix, une base PostgreSQL managée…) en IaaS, PaaS ou SaaS.

## Leçon 1.2 — L'infrastructure Azure : régions et zones

**Explication :** Azure est réparti en régions (ex. France Central, Germany West Central). Chaque région a souvent plusieurs zones de disponibilité : des datacenters séparés. On choisit la région la plus proche de ses utilisateurs et conforme à leurs règles de données (RGPD).

**À suivre :** [Parcours — Describe Azure architecture and services](https://learn.microsoft.com/en-us/training/paths/azure-fundamentals-describe-azure-architecture-services/) (infrastructure, compute, réseau, stockage, identité).

## Leçon 1.3 — Identité et accès : Entra ID et RBAC

**Explication :** Entra ID gère *qui* tu es. RBAC gère *ce que* tu as le droit de faire, et *où*. Principe clé : le moindre privilège. On donne le rôle le plus faible possible, au périmètre le plus petit possible.

**Exercice :** donne à un compte test le rôle Lecteur sur un seul groupe de ressources.

## Leçon 1.4 — Réseau : VNet et NSG

**Explication :** un réseau virtuel (VNet) isole tes ressources. Un groupe de sécurité réseau (NSG) est un pare-feu qui autorise ou bloque le trafic par port. Règle de base : n'ouvrir que ce qui est nécessaire (443 pour un site web).

## Leçon 1.5 — Compute et stockage : choisir le bon service

**Explication :** VM (contrôle total, plus de maintenance), App Service (héberger une app web sans gérer de serveur), Functions (du code qui ne tourne qu'à la demande), Storage Account (fichiers, images, sauvegardes).

## Leçon 1.6 — Gouvernance et coûts

**À suivre :** [Parcours — Describe Azure management and governance](https://learn.microsoft.com/en-us/training/paths/describe-azure-management-governance/).

## Vidéos récapitulatives

| Vidéo | Durée | Niveau | Quand la regarder |
| --- | --- | --- | --- |
| [John Savill — AZ-900 Exam Cram](https://www.youtube.com/watch?v=8n-kWJetQRk) | long format | Débutant | En fin de module, pour tout consolider |
| [freeCodeCamp — cours AZ-900 complet par Andrew Brown](https://www.freecodecamp.org/news/azure-fundamentals-certification-az-900-exam-course/) | ~8 h | Débutant | En complément, par chapitre |

## Projet 1 — App web sécurisée sur Azure

**Mission :** déployer une petite application web (le code fourni ou la tienne) sur App Service, dans un groupe de ressources dédié, en HTTPS uniquement, avec les droits limités à ce groupe.

**Tu as réussi si :** l'app répond en HTTPS, le HTTP est refusé, tu as un schéma d'architecture dans ton README et une capture du coût estimé.

**Bonus certification :** ce module couvre l'essentiel du programme de l'examen AZ-900.
