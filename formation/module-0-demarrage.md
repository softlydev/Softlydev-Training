# Module 0 — Démarrage (Semaine 1 · Débutant)

À la fin du module, l'élève a un compte Azure protégé par une alerte de budget et sait où trouver chaque ressource du parcours.

## Leçon 0.1 — Comment réussir ce programme

**Objectif :** comprendre la méthode. On apprend en construisant : chaque module se termine par un livrable concret, pas par un quiz. Rythme conseillé : 6–8 h par semaine, réparties en 4 sessions courtes plutôt qu'une longue.

**Exercice :** bloque tes créneaux d'étude dans ton agenda pour les 12 semaines.

## Leçon 0.2 — Créer son compte Azure

**Objectif :** ouvrir un compte gratuit ou à l'usage. Une carte bancaire est demandée à l'inscription, même pour l'essai gratuit.

**Explication :** un compte Azure contient un ou plusieurs *abonnements* (la facturation), qui contiennent des *groupes de ressources* (des dossiers), qui contiennent les *ressources* (serveurs, bases, etc.). Retiens ces 3 niveaux : tout le reste du programme s'appuie dessus.

**À lire :** la page d'accueil du parcours officiel [Describe cloud concepts](https://learn.microsoft.com/en-us/training/paths/microsoft-azure-fundamentals-describe-cloud-concepts/), qui propose l'inscription.

## Leçon 0.3 — Protéger son portefeuille : l'alerte de budget

**Objectif :** ne jamais recevoir de facture surprise. C'est la leçon la plus importante du module.

**Explication :** un budget Azure envoie un email quand tes dépenses réelles ou prévues dépassent un seuil. Attention : il **n'arrête pas** tes ressources, il te prévient seulement. Les données de coût arrivent avec 8 à 24 h de retard. Sur un abonnement tout neuf, la fonction peut n'être disponible qu'après 48 h.

**À faire :** [Exercice officiel — Créer ton premier budget](https://learn.microsoft.com/en-us/training/modules/analyze-costs-create-budgets-azure-cost-management/6-exercise-create-budget) · **Référence :** [Tutoriel Microsoft sur les budgets](https://learn.microsoft.com/uk-ua/azure/cost-management-billing/costs/tutorial-acm-create-budgets) · **Vidéo :** [Learn Live — Analyser les coûts et créer des budgets](https://learn.microsoft.com/en-us/shows/learn-live/learn-live--ignite-analyze-costs-and-create-budgets-with-azure-cost-management)

**Exercice :** crée un budget mensuel de 10 € avec des alertes à 50 %, 80 % et 100 %.

**Tu as réussi si** ton budget apparaît dans Abonnements → Budgets avec ton email en destinataire.

## Leçon 0.4 — La règle d'or : tout supprimer après chaque projet

**Explication :** crée chaque projet dans son propre groupe de ressources. Quand tu as fini, supprimer le groupe supprime tout ce qu'il contient, en un clic.

**Exercice :** crée un groupe de ressources `rg-test-module0`, puis supprime-le.

## Leçon 0.5 — Ton poste de travail

**Objectif :** installer VS Code, Git, Azure CLI et créer un compte GitHub. Ce sera ton portfolio.

**Exercice :** crée un dépôt GitHub public `cloud-ia-portfolio` avec un README qui présente ton objectif.

**Livrable du module :** compte Azure + budget actif + dépôt GitHub.
