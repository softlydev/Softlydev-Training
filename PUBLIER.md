# Mettre ce dossier dans https://github.com/softlydev/Claude-AI

## Option A — Sans ligne de commande (le plus simple)

1. Décompresse `Claude-AI.zip` sur ton ordinateur.
2. Ouvre https://github.com/softlydev/Claude-AI et clique **Add file → Upload files**.
3. Glisse le **contenu** du dossier (README.md, business/, formation/, marketing/, site/) dans la zone.
4. Message de commit : `Cloud & IA Accelerator — version complète`, puis **Commit changes**.

## Option B — Avec Git

```bash
unzip Claude-AI.zip
cd Claude-AI
git remote add origin https://github.com/softlydev/Claude-AI.git
git branch -M main
git pull origin main --allow-unrelated-histories   # seulement si le dépôt contient déjà des fichiers
git push -u origin main
```

## Avant de pousser

- Mets le dépôt en **privé** (Settings → General → Danger Zone → Change visibility) : il contient la formation payante.
