# Cloud & IA Accelerator — Plan business

*Version du 25 septembre 2026*

## 1. Les maths du million

1 M€/an = environ 930 ventes de la formation, 80 clients premium et 17 contrats entreprise. C'est atteignable, mais rarement en année 1 : un objectif réaliste est 150–300 k€ la première année, puis 1 M€ en année 2–3 si l'audience grandit.

| Offre | Prix | Ventes / an | CA / an |
| --- | --- | --- | --- |
| Accelerator Core — Europe | 997 € (ou 3 × 349 €) | 450 | 448 650 € |
| Accelerator Core — Afrique francophone (prix régional) | 397 € | 400 | 158 800 € |
| Accelerator Premium (cohorte + coaching) | 2 497 € | 80 | 199 760 € |
| Formation entreprise (équipe jusqu'à 10) | 12 000 € | 17 | 204 000 € |
| **Total** | | | **1 011 210 €** |

**Ce qu'il faut en amont.** Avec une conversion liste email → achat de 1,5 %, 930 ventes Core demandent environ 62 000 inscrits par an, soit ~5 200 par mois. C'est LE chiffre qui décide de tout : le business, c'est l'audience.

**Coûts à prévoir.** Publicité 20–25 % du CA, plateforme et outils ~150 €/mois, frais de paiement ~3 %, TVA sur les ventes aux particuliers UE (régime OSS), et le temps consacré aux lives et au coaching. Marge nette visée : 50–60 %.

**Les leviers les plus rapides :** le B2B (un contrat = 12 ventes Core) et l'Afrique francophone, où le coût d'acquisition est bien plus bas et la demande en compétences cloud forte.

## 2. Positionnement et offre

**Promesse :** en 12 semaines, passe de profil IT classique à Cloud & IA Engineer, avec 4 projets réels déployés sur Azure et un portfolio qui décroche des entretiens et des missions.

**Marque :** Cloud & IA Accelerator, par SoftlyStack. Le nom SoftlyStack porte déjà le positionnement « experts IT Europe–Afrique ».

**Client idéal :** professionnel IT francophone de 25–40 ans (développeur, admin système, DBA, support, analyste) en Europe ou en Afrique francophone. Il sait que le cloud et l'IA sont l'avenir, se perd dans les tutos YouTube, et veut un salaire plus élevé, un poste remote ou ses premières missions freelance.

**Pourquoi vous (l'avantage que les concurrents n'ont pas) :**

- Loïc : Azure Cloud Architect et chercheur AI/ML — l'infra et l'IA vues par quelqu'un qui les conçoit.
- Jai : DBA senior Oracle & PostgreSQL, migrations de bases vers le cloud — la partie données, que 90 % des formations IA survolent.
- Deux experts en poste dans l'industrie, pas des créateurs de contenu à plein temps.

**Les offres :**

| Offre | Prix | Contenu |
| --- | --- | --- |
| Core | 997 € / 3 × 349 € (Afrique : 397 €) | 8 modules, 4 projets guidés, templates Terraform et code, communauté, 1 live Q&A par mois, accès à vie |
| Premium | 2 497 € | Core + cohorte de 12 semaines, 1 live par semaine, revue de code de chaque projet, 2 sessions 1:1, coaching CV/LinkedIn/entretien |
| Entreprise | à partir de 12 000 € | Programme adapté à la stack du client, jusqu'à 10 personnes, ateliers live, projet sur leur cas métier |

**Garantie :** 30 jours satisfait ou remboursé, à condition d'avoir suivi les modules 0 et 1 et rendu le premier projet. Elle rassure sans attirer les touristes.

**Règle d'honnêteté :** aucune promesse de salaire ou d'emploi garanti, et zéro faux témoignage. Les premiers témoignages viendront d'une cohorte bêta.

## 3. Le programme

8 modules sur 12 semaines, environ 40 leçons et 4 projets qui forment le portfolio. Tout se fait sur un compte Azure personnel avec alertes de budget dès le jour 1. Le contenu complet est dans [`../formation/`](../formation/).

| Module | Semaines | Leçons clés | Livrable |
| --- | --- | --- | --- |
| 0. Démarrage | S1 | Compte Azure, alertes de coût, VS Code, Git, CLI, méthode d'apprentissage | Environnement prêt |
| 1. Fondamentaux Cloud & Azure | S1–S2 | Régions, identité (Entra ID, RBAC), réseaux (VNet, NSG), compute, stockage, facturation | **Projet 1 :** app web hébergée et sécurisée |
| 2. Infrastructure as Code & DevOps | S3–S4 | Terraform et Bicep, GitHub Actions, Docker, environnements dev/prod | Projet 1 redéployé en un clic |
| 3. Les données dans le cloud | S5–S6 | PostgreSQL managé, migration Oracle → PostgreSQL, sauvegardes, performance | **Projet 2 :** migration d'une base vers Azure |
| 4. IA générative en production | S7–S8 | APIs de LLM sur Azure, prompt engineering, embeddings, RAG avec pgvector | **Projet 3 :** assistant IA sur documents d'entreprise |
| 5. MLOps et agents IA | S9–S10 | Déploiement, évaluation, agents avec outils, suivi des coûts | Assistant IA évalué et monitoré |
| 6. Sécurité, gouvernance, FinOps | S11 | Key Vault, identités managées, RGPD et données, optimisation des coûts | Audit sécurité et coûts |
| 7. Capstone et carrière | S12 | Projet final, portfolio GitHub, CV et LinkedIn, entretiens, missions freelance | **Projet 4 :** plateforme IA de bout en bout |

**Production :** tourner d'abord les vidéos des modules 0–2, lancer une cohorte bêta, puis produire les suivantes au rythme de la cohorte. On ne tourne jamais 80 vidéos avant d'avoir vendu.

## 4. Acquisition : trouver 5 000 inscrits par mois

Le contenu gratuit amène la confiance, la masterclass convertit, la pub accélère ce qui marche déjà. Ne jamais payer de pub avant d'avoir un taux de conversion mesuré sur du trafic gratuit.

| Canal | Action | Rythme | Objectif |
| --- | --- | --- | --- |
| YouTube (chaîne SoftlyStack dédiée) | Tutos « Azure + IA » concrets, 1 projet par vidéo | 1 vidéo/semaine + 3 Shorts | Le canal principal à long terme |
| LinkedIn | Retours d'expérience terrain, schémas d'architecture, coulisses | 3 posts/semaine | Leads B2B et crédibilité |
| Masterclass live | « Ton premier assistant IA sur Azure » | 2 fois/mois | Conversion principale |
| Partenariats Afrique francophone | Écoles, bootcamps, communautés tech (Douala, Yaoundé, Abidjan, Dakar…) : masterclass gratuite + commission 20 % | 2 nouveaux partenaires/mois | Volume à bas coût |
| Affiliation | 30 % aux anciens élèves et créateurs tech | Permanent | Croissance organique |
| Publicité Meta + YouTube | Vers la masterclass uniquement | 1 500 €/mois en test, puis selon rentabilité | Coût par inscrit cible : < 3 € Europe, < 1 € Afrique |
| B2B | Prospection LinkedIn des ESN, DSI et PME ; offre « atelier IA de 2 h » comme porte d'entrée | 20 contacts/semaine | 17 contrats/an |

**Levier France en année 2 :** la certification Qualiopi puis un enregistrement au Répertoire spécifique permettraient le financement CPF. C'est un gros accélérateur en France, mais la démarche est longue et exigeante : à étudier une fois le produit validé.

## 5. Stack et plan 90 jours

**Stack :** une plateforme tout-en-un francophone (type Systeme.io : cours, pages, emails, affiliation) pour démarrer à bas coût ; Stripe et PayPal pour l'Europe ; un agrégateur mobile money (type CinetPay ou FedaPay) pour l'Afrique ; softlystack.com (WordPress) pour le blog et le SEO ; Zoom ou YouTube Live pour les masterclass ; Discord ou Circle pour la communauté.

**À vérifier avant de vendre :** le contrat de travail (en Allemagne, une activité annexe se déclare souvent à l'employeur), la structure juridique de SoftlyStack, la TVA sur les produits numériques (OSS), les CGV et le RGPD. Un Steuerberater pour 1 heure évite beaucoup d'erreurs.

| Période | Objectif | Actions |
| --- | --- | --- |
| Semaines 1–2 | Valider la demande | 20 appels avec des profils IT du réseau, liste d'attente, premiers posts LinkedIn |
| Semaines 3–4 | Aimant à leads prêt | Checklist, page de capture, séquence email branchée, 1re masterclass live |
| Semaines 5–6 | Prévente bêta | Cohorte bêta de 15–20 personnes à 497 € contre témoignages ; objectif ~8 000 € |
| Semaines 7–10 | Produire en direct | Tourner les modules 0–3 au rythme de la cohorte, 1 vidéo YouTube/semaine |
| Semaines 11–12 | 1er vrai lancement | Page de vente avec témoignages réels, séquence de 7 emails, 2 masterclass |
| Semaine 13 | Analyser | Conversion, coût par inscrit, retours ; décider du budget pub et du 1er contact B2B |

**Le seul indicateur à suivre chaque semaine :** le nombre de nouveaux inscrits email. Tout le reste en découle.
