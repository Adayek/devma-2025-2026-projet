# EcoBudget 🌿

Application de gestion de budget, développée dans le cadre du cours de développement mobile avancé.

## Réalisé par

ADAYÉ Kouamé Appoh Éric Stéphane

## Description du projet

EcoBudget permet de suivre les dépenses, visualiser le budget restant et organiser les catégories de dépenses sur une période donnée. Le projet a été conçu avec une architecture multi-platform, en séparant la logique métier et les couches de présentation.


## Étapes de mise en place

### Module shared
- Création du module Kotlin library
- Suppression du contenu du fichier `build.gradle.kts` et synchronisation
- Suppression du dossier `Main` dans `shared/src`
- Ajout des plugins nécessaires
- Ajout des dépendances requises

### Création des modules commonMain, androidMain et iosMain
- Mise en place de la structure Kotlin Multiplatform
- Préparation des sources selon les cibles de compilation

### Module app
- Ajout de la dépendance `implementation(project(":shared"))`
- Synchronisation des dépendances dans le module `app`

### Nettoyage et migration
- Suppression de la dépendance `implementation(libs.kotlinx.coroutines.core)`
- Migration des modèles vers le module `shared`
- Ajout du module `composeResources` dans `commonMain`
- Migration des couches Data et Presentation
- Intégration des ressources partagées (`string.xml`)

## Problèmes rencontrés et solutions

- Erreur lors de la synchronisation du fichier `build.gradle.kts`
  - Correction : suppression du bloc `android` dans le bloc `kotlin`

- Problème lors de la migration du modèle `categorie` à cause de code Android pur
  - Solution : nettoyer le projet puis resynchroniser
  - Ajout de `ComposeMultiplatform`

- Problème lié à `YearMonth` et à la bibliothèque `Calendar` propre à Android
  - Solution : remplacement par les bibliothèques de date de Kotlin
  - Import des ressources nécessaires dans `categorie.kt`

- Problème d'importation du modèle `Transaction`
  - Solution : ajout de l'annotation `@Immutable` sur le `data class Transaction`

- Problème lié à la génération des UUID
  - Solution : mise en place d'un module partagé `utils` pour assurer la compatibilité Android/iOS

- Problème avec les ressources partagées
  - Solution : ajout de fichiers de ressources pour l'interface utilisateur

## Capture de l'application

![Capture EcoBudget](./WhatsApp%20Image%202026-09-27%20at%2020.07.26.jpeg)

## Conclusion

Ce projet a permis de mettre en pratique les bonnes pratiques de développement Kotlin Multiplatform, la gestion des ressources partagées et l’architecture d’une application mobile orientée budget.
