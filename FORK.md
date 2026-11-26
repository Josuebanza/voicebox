# Voicebox — fork de Josuebanza

Ce dépôt est un fork de [jamiepine/voicebox](https://github.com/jamiepine/voicebox), le studio vocal IA open source (clonage de voix, synthèse vocale, dictée et voix pour agents, le tout en local).

La documentation complète du projet se trouve dans le [README d'origine](README.md) et sur [docs.voicebox.sh](https://docs.voicebox.sh).

## Pourquoi ce fork

- Expérimenter avec le code de Voicebox.
- Préparer des contributions (corrections, fonctionnalités) à proposer au projet original par pull request.

## Organisation des remotes

| Remote     | Dépôt                                                          | Usage                                   |
|------------|----------------------------------------------------------------|-----------------------------------------|
| `origin`   | [Josuebanza/voicebox](https://github.com/Josuebanza/voicebox)  | Ce fork : on y pousse nos branches      |
| `upstream` | [jamiepine/voicebox](https://github.com/jamiepine/voicebox)    | Projet original : source des mises à jour |

Pour configurer `upstream` après un clone :

```bash
git remote add upstream https://github.com/jamiepine/voicebox.git
```

## Garder le fork à jour

```bash
git fetch upstream
git checkout main
git merge upstream/main
git push origin main
```

On peut aussi cliquer sur **Sync fork** sur la page GitHub du fork.

## Proposer une contribution

1. Partir d'un `main` à jour et créer une branche : `git checkout -b ma-branche`.
2. Faire les modifications, puis lancer les vérifications : `just check`.
3. Pousser la branche sur le fork : `git push -u origin ma-branche`.
4. Ouvrir une pull request de `Josuebanza/voicebox:ma-branche` vers `jamiepine/voicebox:main`.

Les règles de contribution du projet sont dans [CONTRIBUTING.md](CONTRIBUTING.md).

## Démarrage rapide

```bash
just setup   # crée l'environnement Python et installe les dépendances
just dev     # lance le serveur et l'application de bureau
```

Prérequis : Bun, Rust, Python 3.12 et les prérequis de Tauri (plus Xcode sur macOS). Voir le [README d'origine](README.md) pour le détail par plateforme.

## Licence

Comme le projet original, ce fork est distribué sous licence [MIT](LICENSE).
