# TPE_Serie2
Ce repository est pour le deuxieme TP sur les Listes chainees
INF231 : Techniques de Conception d’Algorithmes et Structures de Données

## Description
Ce projet regroupe 4 exercices en langage C sur les listes chaînées.
Chaque exercice présente un problème classique de manipulation de listes : suppression, insertion, tri et gestion de variantes (simple, double, circulaire).
Chaque section précise : problème, principe, algorithme et complexité.

## 1. Suppression de toutes les occurrences dans une liste simplement chaînée
 # Problème : Lire un élément x et supprimer toutes ses occurrences dans une liste simplement chaînée.

 # Principe : Parcourir la liste en vérifiant chaque cellule.
  Si la valeur correspond à x, on la supprime en reliant le précédent au suivant.
  Si la tête correspond, on déplace simplement la tête.

 # Algorithme :

  Supprimer les occurrences éventuelles en tête.
  Utiliser deux pointeurs (p courant et t précédent).
  Si p->val == x → suppression et reliaison.
 # Complexité : Temps O(n), espace O(1).

## 2. Insertion dans une liste simplement chaînée triée
 # Problème : Insérer des éléments dans une liste et maintenir l’ordre croissant.
 # Principe : On insère en tête, puis on trie la liste par tri à bulles après chaque insertion.
 # Algorithme :
  Ajouter l’élément en tête.
  Parcourir la liste avec deux boucles imbriquées.
  Échanger les valeurs si elles sont dans le mauvais ordre.
 # Complexité :
  Insertion en tête : O(1)
  Tri à bulles : O(n²)

## 3. Insertion dans une liste doublement chaînée triée
 # Problème : Insérer des éléments dans une liste doublement chaînée et maintenir l’ordre croissant.
 # Principe : Chaque cellule contient deux pointeurs : prec (précédent) et suiv (suivant).
   Insertion en tête → puis tri à bulles en parcourant dans le sens suiv.

 # Algorithme : Créer une nouvelle cellule avec prec = NULL.
   L’insérer en tête (mise à jour des pointeurs).
   Appliquer le tri à bulles comme pour la liste simple.
   Complexité : Temps O(n²), espace O(1).

## 4. Insertion en tête et en queue dans une liste simplement chaînée circulaire
 # Problème : Construire une liste circulaire avec insertion en tête et en queue.
 # Principe :
   Dans une liste circulaire, le dernier élément pointe vers le premier.
   Pour l’insertion en tête → on insère après le dernier mais on retourne ce dernier.
   Pour l’insertion en queue → on insère après le dernier puis on retourne le nouvel élément.
## Algorithme : Insertion en tête :
   Créer une nouvelle cellule.
   Si liste vide → pointeur vers lui-même.
   Sinon → insérer après l->suiv, mettre à jour.
 # Insertion en queue :
   Même principe que l’insertion en tête.
   Retourner le nouvel élément (qui devient le dernier).
# Complexité
   Temps : O(1) (pas de parcours).
   Espace : O(1) (une seule cellule).

## 5. Insertion en tête et en queue dans une liste doublement chaînée circulaire
 # Problème : Construire une liste circulaire avec insertion en tête et en queue.
 # Principe:
   Une liste circulaire : head->prev pointe vers le dernier et last->next vers head.
   Pour insérer : créer une cellule t, la placer entre l’ancien dernier (head->prev) et head.
   Cas spécial : si la liste est vide, t->next = t->prev = t.

# Algorithme
   On travaille avec une liste doublement chaînée circulaire :
   Chaque élément (cellule) a deux liens :
   prev → vers l’élément précédent
   next → vers l’élément suivant
   Le dernier élément pointe vers le premier (et inversement), ce qui rend la liste circulaire.
   Problème
# Complexité
   Temps : O(1) (pas de parcours).
   Espace : O(1) (une seule cellule).
