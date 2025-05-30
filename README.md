# OnlineRestaurantWebApp

OnlineRestaurantWebApp
Description
OnlineRestaurantWebApp est une application web développée avec le framework Django (Python) qui permet à un restaurant de gérer les commandes en ligne de ses clients. Les utilisateurs peuvent s'inscrire, parcourir le menu du restaurant, personnaliser leurs plats (par exemple choisir la taille d'une pizza et ajouter des options supplémentaires), ajouter des articles à un panier virtuel puis passer leur commande. Du côté administrateur, le restaurateur peut gérer le catalogue (ajouter, modifier ou supprimer des éléments du menu via l'interface d'administration Django) et consulter la liste des commandes passées.
Prérequis
Avant de commencer, assurez-vous d'avoir installé sur votre système :
Python 3.x – Le projet est écrit en Python 3.
Django – Framework web Python utilisé par le projet (installé via les dépendances du projet).
pip – Gestionnaire de paquets Python (généralement inclus avec Python).
Git – Pour cloner le dépôt du projet (ou téléchargez le code source ZIP depuis GitHub).
(Optionnel) Environnement virtuel – Recommandé pour isoler les dépendances du projet.
Installation
Pour installer et exécuter le projet en local, suivez ces étapes :
Cloner le dépôt : Récupérez le code source du projet depuis GitHub en clonant ce dépôt dans votre dossier de travail.
git clone https://github.com/votre-utilisateur/OnlineRestaurantWebApp.git
Remplacez votre-utilisateur par le nom du compte GitHub approprié si nécessaire.
Se déplacer dans le répertoire du projet :
cd OnlineRestaurantWebApp
Créer et activer un environnement virtuel (recommandé) :
Sur macOS/Linux :
python3 -m venv env
source env/bin/activate
Sur Windows :
python -m venv env
env\Scripts\activate
Cela permet d'isoler les dépendances Python du projet dans un environnement dédié.
Installer les dépendances Python :
Assurez-vous que votre environnement virtuel est activé, puis installez les paquets requis (y compris Django) à l'aide de pip et du fichier requirements.txt fourni :
pip install -r requirements.txt
Initialiser la base de données :
Le projet utilise une base de données SQLite (fichier db.sqlite3). Vous pouvez utiliser la base de données fournie ou en créer une nouvelle. Pour créer les tables nécessaires (si vous partez d'une base vide ou si vous avez supprimé le fichier existant), appliquez les migrations Django :
python manage.py migrate
Cette commande crée le schéma de base de données requis par le projet.
Importer des données de démonstration (optionnel) :
Si vous souhaitez charger des données initiales (par exemple le menu du restaurant) dans la base de données, un script Python import.py et des fichiers CSV sont fournis. Vous pouvez exécuter ce script pour peupler la base de données avec des données de menu par défaut. Par exemple :
python manage.py shell < import.py
(Cette étape est optionnelle — le fichier db.sqlite3 fourni contient peut-être déjà des données d'exemple.)
Lancement de l'application
Une fois l'installation terminée, vous pouvez lancer le serveur de développement Django pour tester l'application en local :
Démarrer le serveur web :
Depuis le répertoire du projet (avec l'environnement virtuel activé le cas échéant), exécutez :
python manage.py runserver
Par défaut, cette commande démarre le serveur sur l'adresse http://127.0.0.1:8000/ (localhost).
Ouvrir l'application :
Dans votre navigateur web, accédez à l'URL http://127.0.0.1:8000/. Vous devriez voir la page d'accueil de l'application. À partir de là, vous pouvez créer un compte utilisateur, parcourir le menu, ajouter des éléments au panier et passer une commande pour tester le fonctionnement.
Accéder à l'interface d'administration (optionnel) :
Pour accéder à l'interface d'administration Django (permettant de gérer le menu et les commandes), rendez-vous sur http://127.0.0.1:8000/admin/. Vous devrez vous authentifier avec un compte administrateur (superutilisateur). Si aucun compte admin n'existe encore, créez-en un avec la commande :
python manage.py createsuperuser
Après avoir créé le superutilisateur, connectez-vous à l'interface d'administration pour gérer les données du site.
Technologies utilisées
Django – Framework web Python utilisé côté serveur pour développer l'application.
SQLite – Base de données relationnelle légère utilisée par défaut (fichier SQLite inclus dans le projet).
NB : Ce projet est conçu pour être exécuté localement en mode développement. Pour plus d'informations sur Django, consultez la documentation officielle de Django.
