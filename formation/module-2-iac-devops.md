# Module 2 — Infrastructure as Code & DevOps (Semaines 3–4 · Intermédiaire)

À la fin du module, le Projet 1 se recrée entièrement par du code et se redéploie automatiquement à chaque modification sur GitHub.

## Leçon 2.1 — Pourquoi l'Infrastructure as Code

**Explication :** cliquer dans le portail, c'est impossible à reproduire, à relire ou à annuler. Écrire son infrastructure en code (Terraform ou Bicep), c'est pouvoir la versionner dans Git, la relire en équipe et la recréer à l'identique en quelques minutes. C'est ce que les recruteurs vérifient en premier.

## Leçon 2.2 — Terraform : le cycle init → plan → apply → destroy

**Explication :** `terraform init` prépare le dossier, `plan` montre ce qui va changer sans rien toucher, `apply` exécute, `destroy` supprime tout. Le fichier d'état (*state*) est la mémoire de Terraform : ne jamais le perdre, ne jamais le mettre dans un dépôt public.

**À suivre (dans l'ordre) :** [Tutoriels officiels HashiCorp — Get Started Azure](https://developer.hashicorp.com/terraform/tutorials/azure-get-started) : installer, construire, modifier, détruire, variables, sorties, état distant. Complément en texte : [Terraform on Azure — guide DataCamp](https://www.datacamp.com/tutorial/terraform-on-azure).

**Exercice :** crée un groupe de ressources par Terraform, ajoute-lui un tag, puis détruis-le.

## Leçon 2.3 — Variables, modules et environnements

**Explication :** on ne duplique jamais le code pour dev et prod. On utilise des variables (nom, région, taille) et un fichier par environnement. Un *module* est un bloc réutilisable, par exemple « une app web sécurisée ».

**Exercice :** transforme le Projet 1 en module Terraform avec deux environnements, `dev` et `prod`.

## Leçon 2.4 — Bicep, l'alternative native Azure

**Explication :** Bicep fait la même chose que Terraform mais uniquement pour Azure, avec une syntaxe plus courte. Terraform est multi-cloud et plus demandé sur le marché ; Bicep est très présent dans les entreprises 100 % Microsoft. Connaître les deux est un plus, maîtriser Terraform est la priorité.

## Leçon 2.5 — Conteneurs avec Docker

**Explication :** un conteneur emballe ton application et tout ce dont elle a besoin. Il tourne pareil sur ton PC et dans le cloud. On écrit un `Dockerfile`, on construit une image, on la pousse dans un registre (Azure Container Registry).

**Exercice :** conteneurise l'application du Projet 1.

## Leçon 2.6 — CI/CD avec GitHub Actions

**Explication :** un *workflow* GitHub Actions s'exécute à chaque `git push` : il teste, construit et déploie. Pour s'authentifier auprès d'Azure, Microsoft recommande OpenID Connect, avec des jetons de courte durée plutôt qu'un mot de passe stocké.

**À suivre :** [Documentation Microsoft — Déployer sur App Service avec GitHub Actions](https://learn.microsoft.com/en-us/azure/app-service/deploy-github-actions) · [Dépôt officiel des actions App Service](https://github.com/Azure/appservice-actions).

## Projet 1 v2 — Déploiement en un clic

**Mission :** le Projet 1 est entièrement décrit en Terraform, conteneurisé, et redéployé automatiquement par GitHub Actions à chaque push sur `main`.

**Tu as réussi si :** tu peux faire `terraform destroy`, puis tout recréer avec `terraform apply` + un push, sans ouvrir le portail Azure.
