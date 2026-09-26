# EcoBudget 🌿

Dépôt de base pour le projet du cours de développement mobile avancé.

# Module shared
    * New module Java or Kotlin library
    * Supprission du contenu ./build.gradle.kts et synchronisation 
    * suppression du repertoire Main du dossier shared/src
    * Ajout des plugins dans build.gradle.kts
    * Ajout des dépendances dans build.gradle.kts

# Probleme rencontrés
    * Erreur rencontrés suite à la synchronisation de builde.gradle;
    - Correction apporter dans build.gradle.kts : Rétirer le bloc android du block kotklin 

# Création du module commonMain, androidMain, iosMain

# Module app
    * ajout du module implementation(project(":shared")) pour faire la liaison entre les modules app et shared
    * synchronisation des dépendances dans build.gradle.kts

# Suppression de la dependence implementation(libs.kotlinx.coroutines.core)

