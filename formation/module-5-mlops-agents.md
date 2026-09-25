# Module 5 — MLOps et agents IA (Semaines 9–10 · Avancé)

À la fin du module, l'assistant du Projet 3 est évalué automatiquement, surveillé en production, et capable d'agir via des outils.

**Ressource principale :** le cours gratuit [AI Agents for Beginners de Microsoft](https://github.com/microsoft/ai-agents-for-beginners) : chaque leçon a un texte, une courte vidéo et du code Python. Une traduction française existe dans le dépôt (dossier `translations/fr`).

## Leçon 5.1 — Qu'est-ce qu'un agent ?

**Explication :** un chatbot répond. Un agent **agit** : il dispose d'outils (chercher en base, appeler une API, envoyer un email), décide lequel utiliser, observe le résultat et recommence jusqu'à accomplir la tâche.

**À suivre :** leçons *Intro to AI Agents* et *Exploring AI Agentic Frameworks* du cours Microsoft.

## Leçon 5.2 — Le pattern « usage d'outils »

**Explication :** on décrit chaque outil au modèle (nom, rôle, paramètres). Le modèle renvoie l'appel qu'il veut faire, ton code l'exécute et lui renvoie le résultat. Règle de sécurité : un outil qui modifie des données demande toujours une validation humaine.

**À suivre :** leçons *Tool Use Design Pattern* et *Agentic RAG*.

**Exercice :** donne à l'assistant du Projet 3 un outil `creer_ticket_support` qui insère une ligne en base quand il ne trouve pas la réponse.

## Leçon 5.3 — Évaluer une IA

**Explication :** on ne met pas en production une IA qu'on n'a pas mesurée. On construit un jeu de 30 à 50 questions avec les réponses attendues, puis on mesure à chaque changement : la réponse est-elle correcte, fidèle aux sources, la bonne source est-elle citée ? On ajoute ce test au pipeline GitHub Actions.

## Leçon 5.4 — MLOps : déployer et surveiller

**Explication :** en production, on suit la latence, le coût par requête, le taux d'erreurs et le taux de « je ne sais pas ». Azure Machine Learning sert à entraîner, versionner et déployer ses propres modèles ; pour une application basée sur un LLM, on versionne surtout les prompts, le jeu d'évaluation et les données indexées.

**À suivre :** leçons *Building Trustworthy AI Agents* et *AI Agents in Production*.

## Leçon 5.5 — Agents multiples et planification (Avancé, optionnel)

**À suivre :** leçons *Planning Design Pattern* et *Multi-Agent Design Pattern*.

## Livrable du module

L'assistant v2 : un outil d'action, un jeu d'évaluation exécuté automatiquement à chaque push, et un tableau de bord coût/latence dans Azure Monitor. **Tu as réussi si** un changement de prompt qui fait baisser le score d'évaluation bloque le déploiement.
