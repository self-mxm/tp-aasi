# Développer l'API de gestion des livres (ajout, modification, suppression)

**Étiquette :** Must
**Échéance :** 16 nov., 09h30

## Objectif
Fournir une API REST permettant de gérer les livres : ajouter, modifier et supprimer (CRUD).

## Étapes

1. **Définir le modèle Livre**
   Champs : `id`, `titre`, `auteur`, `isbn`, `categorie`, `annee_publication`, `quantite`, `date_creation`.

2. **Préparer la base de données**
   Créer la table/collection `livres` et la connexion à la base.

3. **Définir les routes**
   - `POST /api/livres` : ajouter un livre
   - `PUT /api/livres/:id` : modifier un livre
   - `DELETE /api/livres/:id` : supprimer un livre
   - (`GET /api/livres` et `GET /api/livres/:id` : fournis pour l'interface de liste)

4. **Implémenter la logique de chaque route**
   Contrôleur + service : lecture des données, insertion, mise à jour, suppression.

5. **Valider les données**
   Champs obligatoires, format de l'ISBN, ISBN unique, retour des codes HTTP adaptés (201, 400, 404, 409).

6. **Gérer les erreurs**
   Message clair si le livre n'existe pas ou si les données sont invalides.

7. **Tester l'API**
   Tester chaque route avec Postman ou Insomnia (cas valides et cas d'erreur).

8. **Documenter et livrer**
   Lister les routes dans le README, commit sur la branche de la tâche, puis déplacer la carte Trello.
