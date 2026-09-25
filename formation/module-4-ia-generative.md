# Module 4 — IA générative en production (Semaines 7–8 · Intermédiaire → Avancé)

À la fin du module, l'élève a construit un assistant qui répond aux questions à partir de documents d'entreprise, en citant ses sources (Projet 3). C'est le projet phare du portfolio.

**Ressource principale du module :** le cours gratuit [Generative AI for Beginners de Microsoft](https://microsoft.github.io/generative-ai-for-beginners/). Chaque leçon contient une courte vidéo, un texte et du code Python ou TypeScript. On en suit une sélection, dans l'ordre ci-dessous.

## Leçon 4.1 — Comment fonctionne un LLM (Débutant)

**Explication :** un grand modèle de langage prédit le mot suivant, token par token. Il ne « sait » rien de tes données privées et peut inventer (halluciner). Tout le module consiste à contourner ces deux limites.

**À suivre :** leçon 01 (Introduction to Generative AI and LLMs) du cours Microsoft.

## Leçon 4.2 — Appeler un modèle depuis Azure (Intermédiaire)

**Explication :** on déploie un modèle dans Azure, on récupère un point de terminaison, et on l'appelle par API depuis Python. Paramètres clés : le message système (le rôle donné au modèle), la température (créativité), le nombre maximal de tokens (coût).

**Exercice :** un script Python qui résume en 3 phrases n'importe quel texte collé.

## Leçon 4.3 — Prompt engineering (Intermédiaire)

**Explication :** un bon prompt donne un rôle, un contexte, une tâche précise, un format de sortie et des exemples. Pour une application, on demande souvent une réponse en JSON, plus facile à traiter par le code.

**À suivre :** les leçons sur le prompt engineering du cours Microsoft.

## Leçon 4.4 — Embeddings et recherche vectorielle (Intermédiaire)

**Explication :** un embedding transforme un texte en une liste de nombres. Deux textes au sens proche ont des vecteurs proches. L'extension pgvector permet de stocker ces vecteurs dans PostgreSQL et de chercher les plus proches, avec un index HNSW pour aller vite. Tu réutilises directement ton serveur du module 3.

**À suivre :** la leçon sur la recherche avec des bases vectorielles du cours Microsoft.

## Leçon 4.5 — Le pattern RAG (Avancé)

**Explication :** 1) on découpe les documents en morceaux, 2) on calcule leurs embeddings et on les stocke, 3) à chaque question on retrouve les morceaux les plus proches, 4) on les envoie au modèle avec la consigne de ne répondre qu'à partir d'eux et de citer la source. Sur Azure PostgreSQL, l'extension `azure_ai` permet même de générer les embeddings directement en SQL.

**Vidéo :** [RAG on PostgreSQL — Microsoft Reactor](https://developer.microsoft.com/pl-pl/reactor/events/23331/) : pgvector, puis l'extension azure_ai, présentés par l'équipe Azure PostgreSQL (1 h, Avancé).

**Pour aller plus loin :** [Solution accelerator Microsoft — construire un copilot IA sur Postgres](http://aka.ms/pg-byoac-docs/) : RAG, re-ranking sémantique, agents LangChain, GraphRAG (Avancé).

## Projet 3 — Assistant IA sur documents d'entreprise

**Mission :** un assistant web qui répond aux questions sur un lot de 20 à 50 documents (règlement intérieur, docs produit…), avec PostgreSQL + pgvector comme mémoire, déployé sur App Service via le pipeline du module 2.

**Tu as réussi si :** chaque réponse cite le document source, l'assistant répond « je ne sais pas » quand l'info n'existe pas, et le coût par question est mesuré dans le README.
