# Projet de gestion de matrices en C

🧾 Description générale:
Ce programme en C permet d’effectuer différentes opérations sur des matrices (addition, multiplication, transposition, déterminant, trace, etc.) à partir de fichiers texte contenant des matrices. Deux versions du programme sont fournies :

    main_static : version statique (sans dépendance externe),

    main_dynamic : version dynamique liée à la bibliothèque libMatrices.so.


📦 Installation:
    -Télécharger le paquet .deb fourni.
    -Installer le paquet avec les privilèges administrateur, sur ubuntu la commande est :
    ````` sudo dpkg -i programme-matrices.deb  `````
    Cela installe Les exécutables main_static et main_dynamic dans /usr/local/bin/
    et la bibliothèque dynamique libMatrices.so dans /usr/local/lib/ 


🛠️ Utilisation:

    L’exécutable s’utilise en ligne de commande :

    ````` main_static opération fichier1 fichier2 fichier_resultat ````` pour la librairie statique

    ou

    `````main_dynamic opération fichier1 fichier2 fichier_resultat  ````` pour la librairie dynamique

    Pour afficher l’aide :

        ````` main_static --help `````


🔧 Opérations disponibles

Opération :	Description
addition	:Additionne deux matrices de deux fichiers differents
multiplication:	Multiplie deux matrices de deux fichiers differents
transpose :	Transpose la matrice du premier fichier
determinant	: Calcule le déterminant (si matrice carrée) de la matrice du premier fichier 
trace :	Calcule la trace (somme des éléments diagonaux) de la matrice du premier fichier 
estSymetrique :	Vérifie si la matrice du premier fichier est symétrique 
egales	: Vérifie si les deux matrices de deux fichiers differents sont identiques

Exemples d'utilisation :

main_static addition matrice1.txt matrice2.txt addition.txt
main_static transpose matrice1.txt matrice1.txt transpose.txt

NB : pour les opérations unaires (comme transpose ou determinant), entrez deux fois le même fichier en argument.
    Et pour certaines operations qui ne necessitent pas les fichiers sont pas crées bien qu'éntrés(trace,determinant...).


🗂️ Format des fichiers de matrices:
    Les matrices sont enregistrées dans des fichiers .txt avec les éléments séparés par des points-virgules (;). Exemple :

    1;2;3
    4;8;3
    5;8;9
Ces fichiers sont stockés dans le dossier datas/.


📁 Structure du projet

Matrices/
│
├── matrices.h //declaration des fonctions de chargement de matrice depuis un fichier et affichage.
├── matrices.c //definition des fonctions de matrices.h
├── operations.h //declaration des operations sur les matrices(addition,multiplication,...)
├── operations.c //definition des fonctions de operations.h
├── main.c  // prog principal qui prend en entrée des arguments pour etre executé
├── Makefile //prog qui permet la compilation automatique du projet
│
├── librairies/
│   ├── libMatrices.a //librairie statique
│   └── libMatrices.so // librairie dynamique
│
└── datas/
    ├── matrice1.txt //fichier d'une matrice
    ├── matrice2.txt
    ├── addition.txt // fichier du resultat de l'adiition de matrice1 et matrice2
    └── ...


👤 Auteur

ANOU NJIAZA VANELLE – Département d’Informatique
Université de Yaoundé I – INF361.2
Encadrants : Dr. Adamou Hamza, Gildas Ngouanfo.
Année universitaire 2024–2025# Operations-sur-les-matrices
