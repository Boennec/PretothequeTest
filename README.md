# création du projet 
 symfony new --full PretothequeTest

 # se positionner dans le projet et ouvrir VisualStudio code
  cd PretothequeTest/
  code .

# initier un dépot git
  git init

# vérifier la connexion au server en localhost
  symfony serve -d

# créer un controller principal "Main"
 php bin/console make:controller MainController

# créer la base de données
  php bin/console doctrine:database:create
    `Pretotest`

# gérer les dépôts git
git status
git add .
git commit -m "initialisation projet"
git branch -M main
git remote add origin https://github.com/Boennec/PretothequeTest.git
git push -u origin main

# Créer l'entity Admin
php bin/console make:user
Admin

# Procéder aux migrations
php bin/console make:migration
php bin/console doctrine:migrations:migrate

# Créer un formulaire d'authentification
php bin/console make:auth
login form auth
class AdminAuthenticator
controller SecurityController
generate a logout

# rediriger vers la page home une fois enregistré
 Finish the redirect "TODO" in the ?[32mApp\Security\AdminAuthenticator::onAuthenticationSuccess()?[39m method.
return new RedirectResponse($this->urlGenerator->generate('home'));

# créer un formulaire d'authentification avec la class Admin
php bin/console make:registration-form  pas d'envoi de mail, rediriger vers home


