# 🏛️ Site Web — Commune Territoriale Bni Chegdal

> Plateforme web officielle de la Commune Territoriale de Bni Chegdal,
> Province de Fquih Ben Saleh, Maroc.

---

## 📋 Description

Site web institutionnel complet permettant aux citoyens de la commune de
consulter les actualités, projets de développement, documents administratifs
et d'envoyer des réclamations en ligne. Dispose d'un espace d'administration
sécurisé pour la gestion du contenu.

---

## ✨ Fonctionnalités

### 🌐 Espace Public
- Actualités & événements de la commune
- Projets de développement en cours et réalisés
- Présentation des élus et du conseil communal
- Téléchargement de documents & formulaires PDF
- Galerie photos
- Formulaire de contact / réclamations
- Carte interactive Google Maps
- Interface bilingue (Arabe / Français)

### 🔐 Espace Administration
- Tableau de bord avec statistiques
- Gestion CRUD des actualités
- Gestion des projets
- Gestion des élus et membres du conseil
- Upload de documents PDF
- Gestion de la galerie
- Consultation des messages et réclamations
- Gestion des comptes administrateurs

---

## 🛠️ Technologies utilisées

| Couche      | Technologie                        |
|-------------|------------------------------------|
| Frontend    | HTML5, CSS3, Bootstrap 5           |
| Logique UI  | JavaScript (Vanilla)               |
| Backend     | PHP 8                              |
| Base de données | MySQL (via PDO)               |
| Email       | PHPMailer                          |
| PDF         | FPDF / TCPDF                       |
| Cartes      | Google Maps API                    |
| Sécurité    | CSRF, XSS filter, password_hash()  |

---

## 📁 Structure du projet

```
commune-bni-chegdal/
├── public/                 # Pages publiques
│   ├── index.php           # Accueil
│   ├── actualites.php
│   ├── projets.php
│   ├── elus.php
│   ├── services.php
│   ├── documents.php
│   ├── galerie.php
│   └── contact.php
├── admin/                  # Espace administration (protégé)
│   ├── login.php
│   ├── dashboard.php
│   ├── actualites/
│   ├── projets/
│   ├── elus/
│   └── messages/
├── assets/
│   ├── css/
│   ├── js/
│   ├── img/
│   └── uploads/
├── includes/
│   ├── db.php              # Connexion PDO
│   ├── header.php
│   ├── footer.php
│   └── functions.php
├── lang/                   # Fichiers de traduction
│   ├── ar.php
│   └── fr.php
└── config.php
```

---

## ⚙️ Installation

### Prérequis
- PHP >= 8.0
- MySQL >= 5.7
- Serveur Apache (XAMPP / WAMP / cPanel)
- Composer (optionnel, pour PHPMailer)

### Étapes

```bash
# 1. Cloner le dépôt
git clone https://github.com/votre-username/commune-bni-chegdal.git

# 2. Placer dans le répertoire web
cp -r commune-bni-chegdal/ /var/www/html/

# 3. Importer la base de données
mysql -u root -p < database/commune.sql

# 4. Configurer la connexion
cp config.example.php config.php
# Modifier config.php avec vos identifiants DB
```

### Configuration `config.php`

```php
define('DB_HOST', 'localhost');
define('DB_NAME', 'commune_bni_chegdal');
define('DB_USER', 'votre_user');
define('DB_PASS', 'votre_mot_de_passe');
define('SITE_URL', 'http://localhost/commune-bni-chegdal');
define('ADMIN_EMAIL', 'admin@commune.ma');
```

---

## 🔒 Sécurité

- Protection contre les injections SQL (PDO Prepared Statements)
- Protection XSS (`htmlspecialchars`)
- Tokens CSRF sur tous les formulaires
- Hashage des mots de passe (`password_hash` / `PASSWORD_BCRYPT`)
- Certificat SSL (Let's Encrypt en production)
- Sessions PHP sécurisées pour l'administration

---

## 📊 Diagrammes UML

| Diagramme       | Description                                 |
|-----------------|---------------------------------------------|
| Use Case        | Acteurs: Visiteur, Admin, Système Email     |
| Class Diagram   | 7 classes: Admin, Actualite, Projet, Elu... |
| Sequence        | Scénario: envoi réclamation end-to-end      |

---
<img width="488" height="408" alt="image" src="https://github.com/user-attachments/assets/13c53d8a-be80-46b0-b5f4-ab061de9184e" />
<img width="339" height="333" alt="image" src="https://github.com/user-attachments/assets/620809e2-2a82-4b86-b65e-f05521bff130" />
<img width="393" height="361" alt="image" src="https://github.com/user-attachments/assets/fd3a28ab-9b90-4252-8e5e-f5138e4c2f04" />


## 🗺️ Localisation

> **Commune Territoriale de Bni Chegdal**
> Province de Fquih Ben Saleh
> Région Béni Mellal-Khénifra, Maroc

---

## 📄 Licence

Ce projet est développé pour usage institutionnel.
© 2025 Commune Territoriale Bni Chegdal — Tous droits réservés.

---

## 👤 Développeur

Développé dans le cadre d'un projet de développement territorial local.
Pour toute question technique, ouvrir une [issue](../../issues).
