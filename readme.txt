1) Créer dossier 'client' (react app)
2) Créer dossier 'server'


1) cd mern-crud
    npx create-react-app client
    cd client
    yarn start
    Si message d'erreur :
        npm ERR! code ELIFECYCLE
        npm ERR! errno 1
    A la racine de client, créer un fichier '.env' et mettre 'SKIP_PREFLIGHT_CHECK=true'

2) cd mern-crud
    mkdir server
    cd server
    yarn init -y
    compléter le fichier 'package.json'
    yarn add express
    yarn add mongoose
    yarn add jsonwebtoken
    yarn add cors
    tarn add body-parser
    yarn add nodemon
    yarn add dotenv
    yarn add slugify
    yarn add express-jwt
    yarn add morgan
    yarn start ('node server.js' au départ avant de changer le script start de 'package.json')
    http://localhost:8000/
    mongodb atlas
    fichier '.env'
    fichier '.gitignore'
    comppléter le fichier 'server.js' avec connection à database mongodb (//db)
    si erreur : google -> mongoose deprecation warning

    dossier 'routes' -> 'post.js'
    dossier 'controllers' -> 'post.js'
    dossier 'models' -> 'post.js'

3) yarn add react-router-dom
    client : dossier 'src' -> 'Routes.js'
    index.js
    App.js
    yarn add axios
    .env
    
    Navigation
    Nav.js
    App.js

    Afficher tous les posts
    server
    routes->post.js
    controllers->post.js
    client
    App.js

    Afficher un single post
    server
    routes->post.js
    controllers->post.js
    client
    App.js
    Routes.js
    SinglePost.js

    Préparer update delete
    client
    App.js

    Update post
    server
    routes->post.js
    controllers->post.js
    client
    Routes.js
    UpdatePost.js

    Delete post
    client
    App.js

    page login
    client
    Login.js
    Routes.js

    login server
    server
    dossier 'routes'->'auth.js'
    server.js
    dossier 'controllers'->'auth.js'
    .env
    client
    Login.js
    Nav.js

    session storage
    client
    helpers.js
    Login.js
    inspecteur->Application->Session storage
    inspecteur->Application->Clear Storage

    logout
    client
    Nav.js
    Login.js

    private route
    client
    PrivateRoute.js
    Routes.js

    rich text editor
    client
    yarn add react-quill
    Create.js

    render html
    client
    yarn add react-render-html
    Create.js
    App.js
    SinglePost.js

    rich text editor on update
    client
    UpdatePost.js

    update delete by logged in user
    client
    App.js

    require signin middleware
    server
    dossier 'controllers'->'auth.js'
    dossier 'routes'->'post.js'

    sending bearer token from client
    client
    Create.js
    UpdatePost.js
    App.js

    deploiement sur heroku
    dossier 'server'->'.gitignore'
    dossier 'client'->'.gitignore' avec .env dedans
    heroku.com
    login
    en haut à droite, 'new'->'create new app'
    App name : gui-react-node-crud-api
    choose a region : Europe
    ->create app
    en haut à gauche cliquer sur 'heroku'
    cliquer sur l'app (ici 'gui-react-node-crud-api')
    ->settings
    ->reveal config vars
        -> rentrer les variables :
            KEY : DATABASE
            VALUE : mongodb+...
            KEY : JWT_SECRET
                |
                |
    google -> install heroku cli
    -> https://devcenter.heroku.com/articles/heroku-cli
    -> macOS->download the installer
    installer heroku
    cd client
    heroku (taper la commande)
    dossier 'server', à la racine ->créer un fichier 'Procfile' (web: node server.js)
    terminal -> heroku login
             -> press any key to login...
    une page s'ouvre : cliquer sur 'Log In'
    terminal : Logged in as gui...
                -> cd ..
                -> ls
                -> cd server
                -> git init
                -> git add .
                -> git commit -m "first commit"
                -> heroku git:remote -a gui-react-node-crud-api
                -> git push heroku master
                -> heroku open
                (s'il y a des erreurs
                    -> heroku ps:restart; heroku logs --tail) // pour vois les erreurs
            A l'adresse :
            https://gui-react-node-crud-api.herokuapp.com/
                -> CANNOT GET
            on peut voir les posts        
            https://gui-react-node-crud-api.herokuapp.com/api/posts
                -> cd ..
                -> ls
                -> cd client
    cliquer en haut à gauche sur 'heroku'
    cliquer en haut à droite sur 'new'->'create a new app'
    App name : gui-react-node-crud
    choose a region : Europe
    ->create app
    cliquer sur 'settings'
    cliquer sur 'reveal config vars'
        KEY : REACT_APP_API
        VALUE : https://gui-react-node-crud-api.herokuapp.com/api
    dossier 'client', à la racine ->créer un fichier 'Procfile' (web: node server.js)
    dossier 'client', à la racine ->créer un fichier 'server.js'
    dans le dossier 'client', supprimer le fichier 'yarn.lock'
    terminal : -> cd ..
               -> ls
               -> cd client
               -> heroku login
               -> press any key...
    une page s'ouvre, cliquer sur 'Log In'
               -> heroku apps (pour voir mes projets heroku)
               -> git init
               -> git add .
               -> git commit -m "first commit"
               -> heroku git:remote -a gui-react-node-crud
               -> git push heroku master
               -> heroku open

    
    En local :
    cd server
    yarn start
    cd client
    yarn start
    http://localhost:3000/

    En ligne :
    https://gui-react-node-crud.herokuapp.com/




Pour ajouter des images :
- stocker les images dans 'google images'
- chaque image a une adresse url
- 'server' -> 'models' -> 'post.js'     (rajouter imgurl)
           ->'controllers' -> 'post.js' (rajouter imgurl)
- 'client' -> 'App.js'                  (rajouter imgurl)
           -> 'Create.js'               (rajouter imgurl)
           -> 'SinglePost.js'           (rajouter imgurl)
           -> 'UpdatePost.js'           (rajouter imgurl)
- pour afficher l'image : <img src={`${post.imgurl}`} />