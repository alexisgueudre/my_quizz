# Projet : My Quizz
___
### Objectif :
Développer un site proposant des quizzs sur divers sujets.
### Restriction :
L'utilisation de Javascript est proscrite.
Les réponses ne doivent pas être visible dans le code source.
Le projet doit être réalisé en Symfony 3 ou supérieur.
___
# Fonctionnalités :
### Fonctionnalités de base :
- *( Done )* Il doit être possible de répondre à des **Quizzs**.
- *( Done )* Il doit être possible de consulter l'**Historique** des quizzs passés ainsi que le **Score** sur chaque **Quizz** passé.
- *( Done )* Il doit être possible de s'**Inscrire**.
- *( Done )* Il doit être nécessaire de **Valider** son compte en cliquant sur un lien d'**Activation** envoyé par mail.
- *( Done )* Il doit être possible de se **Connecter**.
- *( Done )* Il doit être possible de **Modifier** son **Adresse Email**.
- *( Done )* Il doit être possible de **Modifier** son **Mot de passe**.
- *( Done )* Il doit être nécessaire de **Réactiver** le **Compte** après une mise à jour de l'**Adresse Email**.
- *( Done )* Il doit être possible de **Créer** un **Quizz**.
- *( Done )* Il doit être possible de **Modifier** un compte utilisateur en tant qu'**Administrateur**.
- *( Done )* Il doit être possible de **Supprimer** une **Catégorie de Quizz** ou un **Quizz** en tant qu'**Administrateur**.
- *( Done )* Il doit être possible d'accorder le rôle d'**Administrateur** à un utilisateur en tant qu'**Administrateur**.
- ~~*( Done )* Il doit être possible d'envoyer des mails aux utilisateurs.~~
- ~~*( Done )* Il doit être possible de consulter des **Statistiques** détaillées.~~
- ~~*( Done )* Il doit être possible de consulter des **Graphiques** détaillés.~~
___
# Équipe :
Ci-dessous, l'équipe en charge du projet.
### Matrix Team :
- *Morpheus* : [Alexis Gueudre](https://www.linkedin.com/in/alexis-gueudre/)
- *Neo* : [Amine Belkheiri](https://www.linkedin.com/in/amine-belkheiri/)
- *Tank* : [Daniel Cadeau](https://www.linkedin.com/in/daniel-cadeau-dev/)
___
# How To :
Suivez bien les étapes ci-dessous !
### Étape 1 :
- Pour pouvoir profiter de notre projet, vous devrez créer une base de données nommée **my_quizz**.
### Étape 2 :
- Clonez ensuite le repository.
### Étape 3 :
- Une fois le repository cloné, vous devrez créer un fichier **.env** à la racine du projet.
- Collez-y le code ci-dessous :
```
# In all environments, the following files are loaded if they exist,
# the latter taking precedence over the former:
#
# * .env contains default values for the environment variables needed by the app
# * .env.local uncommitted file with local overrides
# * .env.$APP_ENV committed environment-specific defaults
# * .env.$APP_ENV.local uncommitted environment-specific overrides
#
# Real environment variables win over .env files.
#
# DO NOT DEFINE PRODUCTION SECRETS IN THIS FILE NOR IN ANY OTHER COMMITTED FILES.
#
# Run "composer dump-env prod" to compile .env files for production use (requires symfony/flex >=1.2).
# https://symfony.com/doc/current/best_practices.html#use-environment-variables-for-infrastructure-configuration

###> symfony/framework-bundle ###
APP_ENV=dev
APP_SECRET=5e63911e5562c4ebb9d1f9be5f62a09a
###< symfony/framework-bundle ###

###> symfony/mailer ###
# MAILER_DSN=smtp://localhost
MAILER_URL=
###< symfony/mailer ###

###> doctrine/doctrine-bundle ###
# Format described at https://www.doctrine-project.org/projects/doctrine-dbal/en/latest/reference/configuration.html#connecting-using-a-url
# IMPORTANT: You MUST configure your server version, either here or in config/packages/doctrine.yaml
#
# DATABASE_URL="sqlite:///%kernel.project_dir%/var/data.db"
DATABASE_URL="mysql://root:@127.0.0.1:3306/my_quizz?serverVersion=mariadb-10.4.18"
# DATABASE_URL="postgresql://db_user:db_password@127.0.0.1:5432/db_name?serverVersion=13&charset=utf8"
###< doctrine/doctrine-bundle ###
```
- Gardez à l'esprit qu'en fonction de votre **SGBD** vous aurez potentiellement besoin de modifier la ligne **DATABASE_URL**. Nous vous invitons à utiliser **Google** ainsi que l'interface utilisateur de vos **SGBD** afin de déterminer ce qu'il faudra attribuer comme valeur à cette constante d'environnement.
- Il vous faudra aussi attribuer une valeur à la constante **MAILER_URL** afin de profiter du système d'envoi de mail via **SwiftMailer**.
- Une fois ceci fait, vous devrez effectuer la commande suivante sur votre terminal :
```
composer install
```
- Cette commande vous permettra d'installer les dépendances nécessaires au bon fonctionnement du projet.
### Étape 3.1 :
- Une fois les dépendances installées, effectuez la commande ci-dessous :
```
php bin/console doctrine:migrations:migrate
```
- Cette commande vous permettra de générer les tables de la base de données créée précédemment ( pour rappel il s'agit de **my_quizz** ).
- Pensez à modifier vos identifiants de connexion à **MySQL** dans le fichier .env ( Constante **DATABASE_URL**, revoir l'**Étape 3** si besoin ).
### Étape 4 :
- Vous pouvez à présent profiter pleinement du projet !
___
<footer style="display: flex; justify-content: center; align-items: center; width: 100%;">
    <p>Powered by - <span style="color: #009FFC;">Matrix Team</span></p>
</footer>
