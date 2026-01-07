# Contributing to AGES

Merci de votre intérêt pour contribuer à AGES. Ce document détaille les bonnes pratiques pour signaler des problèmes, proposer des fonctionnalités et soumettre des contributions.

## Signaler un bug
- Avant d'ouvrir un ticket, vérifiez la page des **Releases** pour voir si une version récente corrige votre problème.
- Utilisez le template **Bug report** en cliquant sur _New issue_ → _Bug report_. Fournissez : étapes de reproduction, comportement attendu/observé, environnement, captures et logs.

## Proposer une fonctionnalité
- Utilisez le template **Feature request** (New issue → Feature request). Décrivez le besoin, la motivation, une proposition détaillée et l'impact attendu.

## Pull Requests (PR)
- Forkez le dépôt public et créez une branche descriptive : `feat/<short-desc>` ou `fix/<short-desc>`.
- Avant de soumettre une PR :
  - Exécutez `flutter format` sur les fichiers modifiés.
  - Exécutez `dart run build_runner build --delete-conflicting-outputs` si votre changement affecte du code généré.
  - Lancez les tests pertinents : `flutter test` (ou `./build_all.sh -t` pour batterie complète).
- Rédigez une description claire dans la PR : but, changements principaux, impact sur l'utilisateur et étapes de validation.

## Standards de code
- Langage : **Dart / Flutter**. Respectez les règles de lint du dépôt (`analysis_options.yaml`).
- Gardez les modifications ciblées et évitez les refactorings globaux non demandés.

## Badges et README
- Les URLs de badges (Shields) doivent pointer vers votre user/repo public. Remplacez les placeholders par votre `user` et `repo` pour que les images s'affichent correctement (ex. `https://img.shields.io/github/v/release/<votre-user>/<votre-repo-public>`).

## Publication des Releases
- Les releases sont publiées automatiquement depuis le dépôt privé vers le dépôt public via GitHub Actions.
- Pour permettre la création de releases sur le dépôt public, le workflow utilise un secret `PUBLIC_REPO_TOKEN` (PAT GitHub) avec scope `repo` :

  1. Générez un Personal Access Token depuis votre compte GitHub.
  2. Dans le dépôt privé, allez dans _Settings > Secrets and variables > Actions_ et créez `PUBLIC_REPO_TOKEN`.

## Issues et Support
- Si la fonctionnalité Issues n'est pas activée pour le dépôt public : _Settings > General > Features_ → cochez **Issues**.
- Nous fournissons des templates d'issues pour structurer les rapports et accélérer le support.

## Code of Conduct
- Respectez les autres contributeurs. Nous suivons un code de conduite standard — ouvrez une issue si vous avez des préoccupations.

Merci pour votre aide — chaque contribution compte pour améliorer AGES.
