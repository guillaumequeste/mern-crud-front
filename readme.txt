1) Créer un dossier 'mern-crud'
2) Créer dossier 'client' (react app)
3) Créer dossier 'server'
4) MongoDB Atlas
5) Mettre en ligne sur heroku
6) Faire fonctionner l'application
7) Session storage


1) Créer un dossier 'mern-crud'

2) -> cd mern-crud
   -> npx create-react-app client
   -> cd client
   -> yarn add axios
   -> yarn add react-quill
   -> yarn add react-render-html
   -> yarn add yarn add react-router-dom

   Créer les fichiers suivants à la racine :
    - '.env'
    - '.gitignore'
    - 'server.js'
    - 'Procfile'

   Créer les fichiers suivants dans le dossier 'src' :
    - 'App.js'
    - 'Create.js'
    - 'helpers.js'
    - 'index.js'
    - 'Login.js'
    - 'Nav.js'
    - 'PrivateRoute.js'
    - 'Routes.js'
    - 'SinglePost.js'
    - 'UpdatePost.js'

    Insérer bootstrap (link css dans le fichier 'index.html' du dossier 'public')

    Supprimer le fichier 'yarn.lock' à la racine

   -> (yarn start)
        Si message d'erreur :
            npm ERR! code ELIFECYCLE
            npm ERR! errno 1
        A la racine de client, créer un fichier '.env' et mettre 'SKIP_PREFLIGHT_CHECK=true'

3) -> cd mern-crud
   -> mkdir server
   -> cd server
   -> yarn init -y (ou 'yarn init')
   -> yarn add express
   -> yarn add mongoose
   -> yarn add jsonwebtoken
   -> yarn add cors
   -> yarn add body-parser
   -> yarn add nodemon
   -> yarn add dotenv
   -> yarn add slugify
   -> yarn add express-jwt
   -> yarn add morgan

   Compléter le fichier 'package.json'
   -> yarn start ('node server.js' au départ avant de changer le script start de 'package.json')
    http://localhost:8000/

    Créer les fichiers suivants à la racine :
    - '.env'
    - '.gitignore'
    - 'server.js'
    - 'Procfile'

    Créer un dossier 'controllers' à la racine avec les fichiers suivants :
    - 'auth.js'
    - 'post.js'

    Créer un dossier 'models' à la racine avec le fichier suivant :
    - 'post.js'

    Créer un dossier 'routes' à la racine avec les fichiers suivants :
    - 'auth.js'
    - 'post.js'

4) voir mongo.txt
    
    si erreur : google -> mongoose deprecation warning

    
5) Metrre el ligne heroku (voir heroku.txt) : https://gui-patrimoine.herokuapp.com/ 
    
6) En local :
    -> cd server
    -> yarn start
    Ouvrir un autre terminal :
    -> cd client
    -> yarn start

    http://localhost:3000/

   En ligne :
    https://gui-react-node-crud.herokuapp.com/

7) inspecteur->Application->Session storage
   inspecteur->Application->Clear Storage