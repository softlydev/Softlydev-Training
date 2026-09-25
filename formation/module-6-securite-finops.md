# Module 6 — Sécurité, gouvernance, FinOps (Semaine 11 · Avancé)

À la fin du module, aucun mot de passe ne traîne dans le code des projets, et l'élève sait expliquer et réduire leur coût mensuel.

## Leçon 6.1 — Zéro secret dans le code : Key Vault

**Explication :** un mot de passe dans un fichier finit tôt ou tard sur GitHub. Azure Key Vault stocke les secrets, clés et certificats de façon sécurisée ; l'application vient les y lire au démarrage.

## Leçon 6.2 — Les identités managées

**Explication :** mais comment l'app s'authentifie-t-elle auprès de Key Vault sans… mot de passe ? Grâce à une identité managée : Azure donne à l'App Service une identité automatique. Avec la classe `DefaultAzureCredential`, le même code utilise ton compte Azure CLI en local et l'identité managée une fois déployé.

**À suivre :** [Quickstart Key Vault en Python (documentation Microsoft)](https://github.com/MicrosoftDocs/azure-docs/blob/main/articles/key-vault/keys/quick-create-python.md) · [Exemple officiel App Service + identité managée + Key Vault](https://github.com/Azure-Samples/app-service-msi-keyvault-dotnet).

**Exercice :** déplace la chaîne de connexion PostgreSQL et la clé d'API du modèle IA du Projet 3 dans Key Vault, lues via identité managée.

## Leçon 6.3 — RGPD et IA : les données des clients

**Explication :** questions à se poser avant tout projet IA en Europe : où sont stockées les données (choisir une région UE), qui y accède, combien de temps on les garde, et est-ce que des données personnelles partent dans les prompts. On masque ou on retire les données personnelles avant l'indexation.

## Leçon 6.4 — FinOps : payer le juste prix

**Explication :** les 5 réflexes : éteindre ce qui ne sert pas (serveur de dev la nuit), choisir la bonne taille, taguer chaque ressource par projet, suivre le coût par requête IA, et analyser la facture chaque mois.

**À suivre :** [Module Microsoft Learn — Analyser les coûts et créer des budgets](https://learn.microsoft.com/training/modules/analyze-costs-create-budgets-azure-cost-management) · [Scénario avancé : arrêter automatiquement les VM quand le budget est dépassé](https://learn.microsoft.com/en-us/azure/cost-management-billing/manage/cost-management-budget-scenario) (Avancé).

## Livrable du module — Audit sécurité et coûts

Un document d'une page dans le portfolio : secrets déplacés, droits réduits, coût mensuel avant/après optimisation. **Tu as réussi si** une recherche du mot `password` dans tes dépôts ne renvoie plus rien de sensible.
