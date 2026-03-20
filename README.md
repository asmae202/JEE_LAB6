# Intégration Spring Boot & Thymeleaf

![Spring Boot](https://img.shields.io/badge/SpringBoot-6DB33F?style=flat&logo=spring&logoColor=white)
![Thymeleaf](https://img.shields.io/badge/Thymeleaf-005F0F?style=flat&logo=thymeleaf&logoColor=white)
![MySQL](https://img.shields.io/badge/MySQL-4479A1?style=flat&logo=mysql&logoColor=white)
![GitHub](https://img.shields.io/badge/GitHub-181717?style=flat&logo=github&logoColor=white)
![License](https://img.shields.io/badge/License-MIT-green)

---


## 💻 Objectif

- Créer une application web CRUD complète pour gérer des utilisateurs.  
- Comprendre la gestion des dépendances Maven et l’injection de dépendances Spring.  
- Implémenter la persistance avec Spring Data JPA et Hibernate.  
- Développer une interface web dynamique avec Thymeleaf.  
- Valider les entrées utilisateur avec Hibernate Validator.  
- Connecter et interagir avec une base de données MySQL.

---

## 💻 Contexte

- **Spring Boot** : simplifie la création d’applications Java avec configuration minimale.  
- **Thymeleaf** : moteur de template HTML pour générer des pages web dynamiques.  
- **Spring Data JPA / Hibernate** : gestion automatique du CRUD et mapping ORM.  
- **MySQL** : base relationnelle pour stocker les entités `User`.  
- **Maven** : gestion centralisée des dépendances et build du projet.  

---

## 💻 Structure du projet


<img width="280" height="402" alt="image" src="https://github.com/user-attachments/assets/be839323-979c-411a-8790-e74d3bdba3e5" />



---


---

## 💻 Explication des classes

### Entité User
- `@Entity` : classe persistable par JPA.  
- `@Id` et `@GeneratedValue` : identifiant auto-incrémenté.  
- Champs : `name`, `email`.  
- Validation : `@NotBlank` pour les champs obligatoires.  
- Constructeur par défaut + getters/setters.  

### Repository UserRepository
- Étend `CrudRepository<User, Long>`.  
- Fournit automatiquement `save()`, `findAll()`, `delete()`.  

### Contrôleur UserController
- Routes principales :  
  - `/signup` : afficher formulaire d’ajout.  
  - `/adduser` : ajouter utilisateur.  
  - `/edit/{id}` : modifier utilisateur.  
  - `/update/{id}` : mettre à jour utilisateur.  
  - `/delete/{id}` : supprimer utilisateur.  
- Liaison des données via `Model` et validation via `@Valid`.  

### Templates Thymeleaf
- `index.html` : liste des utilisateurs avec boutons Edit/Delete.  
- `add-user.html` : formulaire d’ajout utilisateur.  
- `update-user.html` : formulaire de modification utilisateur.  
- Utilisation de `th:object`, `th:field`, `th:each`, `th:text`.

---

## 💻 Base de données

- Nom de la base : `thymeleaf`  
- Table principale : `user`  

### Structure de la table User

<img width="755" height="410" alt="image" src="https://github.com/user-attachments/assets/50ffa224-a265-496d-86d8-014155c0493e" />

---

## 💻 Exécution & Résultats

### Lancer l’application
- Importer le projet dans l’IDE (IntelliJ, Eclipse, VS Code).  
- Lancer la classe `DemothymeleafApplication.java`.  
- Accéder à : [http://localhost:8080](http://localhost:8080)  

### Résultats dans le navigateur


https://github.com/user-attachments/assets/c6df8161-9cd3-48bb-9b55-3fc0fbf88ce8

---

## 💻 Concepts clés

- **Spring IoC** : inversion de contrôle et injection de dépendances.  
- **Spring Data JPA** : simplification du CRUD et mapping ORM avec Hibernate.  
- **Thymeleaf** : templates HTML dynamiques et liaison avec entités Java.  
- **Hibernate Validator** : validation des champs avant persistance.  
- **Maven** : gestion des dépendances et build du projet.  

---

