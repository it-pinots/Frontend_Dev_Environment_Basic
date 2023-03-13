# Frontend_Dev_Environment_Basic

## Table of Contents

- [About](#about)
- [Installing](#getting_started)

## About <a name = "about"></a>

Angular et React sont couramment utilisés pour le développement en Frontend, mais pour des **POC** (Proof Of Concept), il n'est pas nécessaire de les utiliser, cela permet d'éviter la complexité. L'idée est de maintenir la simplicité et de réutiliser cette approche pour d'autres projets.

### Installing <a name = "getting_started"></a>

- Créer une archive **git** (git-repo) pour le projet. Ajouter les fichiers `ReadMe` et `.gitignore`.
- Initialiser **npm** >> `npm init`
- Installer **lite-server** >> `npm install -save-dev lite-server`
- Ajouter le fichier de configuration de **lite-server** : `bs-config.json` et **mettre à jour** le script `npm-start: lite-server`

    ```json title=bs-config.json
    {
        "files" : "./src/**/*.{js, html, css}",
        "server" : {
            "baseDir": ["./", "./src" ]
        }
    }
    ```

- Installer quelques dépendances initiales :

<detail open>
    <summary><h3>npm install - save bulma</h3></summary>
        <ul>
            <li><a href="https://www.npmjs.com/package/bulma" ><span><strong>NPM</strong></span></a></li>
        </ul>
        <ul>
            <li><a href="https://www.jsdelivr.com/package/npm/bulma" ><span><strong>CDN</strong></span></a></li>
        </ul>
        <p>Bulma is a modern CSS framework based on Flexbox.</p>
</detail>


  - `npm install - save jquery`

  - `npm install - save font-awesome`
