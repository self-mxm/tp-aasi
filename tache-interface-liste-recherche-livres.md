# Développer l'interface de liste et de recherche des livres

**Étiquette :** Must
**Échéance :** 15 nov., 09h00

## Objectif
Permettre à l'utilisateur de consulter la liste des livres et de rechercher rapidement un livre.

## Étapes

1. **Concevoir la maquette**
   Esquisser la page : barre de recherche en haut, liste (tableau ou cartes) en dessous.

2. **Créer la structure de la page**
   Composants/sections : en-tête, champ de recherche, liste des livres, message « aucun résultat ».

3. **Afficher la liste des livres**
   Récupérer les livres via `GET /api/livres` et afficher titre, auteur, catégorie, disponibilité.

4. **Ajouter la recherche**
   Champ de saisie qui filtre par titre, auteur ou ISBN (via paramètre `?q=` ou filtre côté client).

5. **Gérer les états de l'interface**
   Chargement, liste vide, erreur de connexion à l'API.

6. **Soigner l'affichage**
   Mise en page responsive (mobile et ordinateur), styles cohérents, pagination si la liste est longue.

7. **Tester**
   Vérifier avec plusieurs recherches (résultat trouvé, aucun résultat, champ vide).

8. **Livrer**
   Commit sur la branche de la tâche, puis déplacer la carte Trello.
