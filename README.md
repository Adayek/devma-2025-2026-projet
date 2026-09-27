# EcoBudget 🌿

Dépôt de base pour le projet du cours de développement mobile avancé.

# Module shared
    * New module Java or Kotlin library
    * Supprission du contenu ./build.gradle.kts et synchronisation 
    * suppression du repertoire Main du dossier shared/src
    * Ajout des plugins dans build.gradle.kts
    * Ajout des dépendances dans build.gradle.kts

# Création du module commonMain, androidMain, iosMain

# Module app
    * ajout du module implementation(project(":shared")) pour faire la liaison entre les modules app et shared
    * synchronisation des dépendances dans build.gradle.kts

# Suppression de la dependence implementation(libs.kotlinx.coroutines.core)

# Migration des models vers le module shared
    * Migration des models

# Ajout du module composeRessources dans commonMain
    - Ajoute de string.xml

# Problème rencontrés
    * Erreur rencontrés suite à la synchronisation de builde.gradle;
    * Problème lors de la migration du model categorie suite au code android pure présent dans le model
    * Problème lors de la migration de yearMonth suite à la bibliothèque Calandar qui est propre à android

# Solution trouvée
    - Correction apporter dans build.gradle.kts : Rétirer le bloc android du block kotklin 
    - Intégrer ComposeMultiPlatform
    - Faire clean project puis synchroniser le project
    - Importer les ressources dans catégorie.kt
    - Remplacer la fonction calandar d'android par des bibliothèques date de Kotlin


