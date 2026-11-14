# Guide de réalisation des tâches d’authentification

## 1. Développement de l’interface de connexion

### Objectif
Mettre en place une interface permettant à un utilisateur de se connecter à l’application à l’aide de ses identifiants.

### Étapes de réalisation

1. **Analyser l’interface existante**
   - Repérer l’organisation du frontend, les pages et les composants déjà disponibles.
   - Identifier le système de navigation et les conventions graphiques du projet.
   - Réutiliser les composants et styles existants lorsque c’est possible.

2. **Créer la page de connexion**
   - Ajouter un champ pour l’identifiant de l’utilisateur (adresse e-mail ou autre identifiant défini par l’application).
   - Ajouter un champ pour le mot de passe.
   - Ajouter un bouton de connexion.
   - Prévoir une présentation claire et cohérente avec le reste de l’application.

3. **Gérer les données du formulaire**
   - Récupérer les valeurs saisies par l’utilisateur.
   - Vérifier que les champs obligatoires sont renseignés.
   - Afficher un message lorsque les informations saisies sont invalides.
   - Empêcher les soumissions répétées pendant le traitement de la demande.

4. **Connecter l’interface au service d’authentification**
   - Envoyer les identifiants au backend à l’aide d’une requête HTTP.
   - Transmettre les données dans le format attendu par l’API.
   - Traiter la réponse reçue.
   - En cas de connexion réussie, conserver l’état d’authentification selon le mécanisme prévu par l’application et rediriger l’utilisateur.
   - En cas d’échec, afficher un message explicite sans révéler d’informations sensibles.

5. **Tester l’interface**
   - Vérifier le comportement lorsque les champs sont vides.
   - Tester avec des identifiants incorrects.
   - Tester avec des identifiants valides.
   - Vérifier les messages d’erreur, l’état de chargement et la redirection.
   - Vérifier que l’affichage reste utilisable sur les différentes tailles d’écran ciblées.

### Résultat attendu
Une page de connexion fonctionnelle, intégrée à l’application et capable de communiquer avec le service d’authentification.

---

## 2. Développement de l’API d’authentification

### Objectif
Développer un service backend qui reçoit les identifiants, vérifie leur validité et retourne le résultat de la tentative de connexion.

### Étapes de réalisation

1. **Analyser le backend**
   - Identifier le framework et l’organisation du code.
   - Repérer le modèle utilisateur, les routes et les contrôleurs existants.
   - Vérifier si un mécanisme d’authentification est déjà présent afin de le réutiliser si nécessaire.

2. **Définir la route de connexion**
   - Déterminer l’URL et la méthode HTTP utilisées pour la connexion.
   - Définir les données que le frontend doit transmettre.
   - Définir la structure des réponses en cas de réussite ou d’échec.
   - Maintenir le même format de données entre le frontend et le backend.

3. **Valider les données reçues**
   - Vérifier que les champs obligatoires sont présents.
   - Contrôler le format des données.
   - Retourner une réponse adaptée lorsque les données sont invalides.
   - Éviter de communiquer des détails internes ou des informations sensibles dans les messages d’erreur.

4. **Vérifier les identifiants**
   - Rechercher l’utilisateur à partir de l’identifiant fourni.
   - Comparer le mot de passe saisi avec le mot de passe chiffré par hachage enregistré en base de données.
   - Refuser la connexion lorsque l’utilisateur n’existe pas ou que le mot de passe ne correspond pas.
   - Ne jamais enregistrer ni manipuler les mots de passe en clair dans les journaux.

5. **Gérer le résultat de l’authentification**
   - Si les identifiants sont corrects, créer une session ou générer un token selon le mécanisme retenu dans le projet.
   - Retourner les informations nécessaires à l’application, sans exposer de données confidentielles.
   - Prévoir la gestion de l’expiration de l’authentification et de la déconnexion si elles font partie du périmètre.

6. **Tester l’API**
   - Envoyer une requête avec des identifiants valides.
   - Tester un utilisateur inexistant.
   - Tester un mot de passe incorrect.
   - Tester les champs manquants ou mal formatés.
   - Vérifier les codes de réponse HTTP et la structure des réponses.
   - S’assurer qu’aucun mot de passe ou secret n’est retourné.

### Résultat attendu
Un endpoint d’authentification opérationnel, sécurisé et utilisable par l’interface de connexion.

---

## 3. Intégration et vérification du parcours de connexion

Après la réalisation de l’interface et de l’API, il faut vérifier leur fonctionnement commun.

1. Vérifier que l’URL appelée par le frontend correspond à la route définie dans le backend.
2. Vérifier que les noms et les formats des champs transmis sont identiques à ceux attendus par l’API.
3. Vérifier que le frontend interprète correctement les réponses du backend.
4. Effectuer un test complet : saisie des identifiants, envoi de la requête, vérification des informations et affichage du résultat.
5. Vérifier la configuration des échanges entre le frontend et le backend, notamment CORS lorsque les deux parties utilisent des origines différentes.

### Conclusion

La réalisation de ces deux tâches permet de mettre en place un parcours de connexion complet. L’interface permet à l’utilisateur de saisir ses identifiants et l’API assure leur vérification ainsi que la gestion de l’authentification. Les deux parties doivent utiliser un format d’échange commun et être testées ensemble pour garantir le bon fonctionnement de la connexion.

> Les choix techniques précis (framework, route, noms des champs et mécanisme de session ou de token) doivent être adaptés à l’architecture et aux conventions du projet.
