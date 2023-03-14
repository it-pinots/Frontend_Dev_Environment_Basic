# Frontend_Dev_Environment_Basic

## Table des matières

- [About](#about)
- [Installing](#getting_started)

## Apropos <a name = "about"></a>

Angular et React sont couramment utilisés pour le développement en Frontend, mais pour des **POC** (Proof Of Concept), il n'est pas nécessaire de les utiliser, cela permet d'éviter la complexité. L'idée est de maintenir la simplicité et de réutiliser cette approche pour d'autres projets.

### 1.0 Installation <a name = "getting_started"></a>

- Créer une archive **git** (git-repo) pour le projet. Ajouter les fichiers `ReadMe` et `.gitignore`.

<br>

- Créer un fichier `index.html`

    En suivant ces étapes, vous disposerez d'un point de départ pour tester votre idée

<br>

- Initialiser **npm** >> `npm init` dans votre projet

<br>

- Installer **lite-server** >> `npm install -save-dev lite-server`

<br>

- Ajouter le fichier de configuration de **lite-server** >> `bs-config.json`

<br>

```json title=bs-config.json
#Inside bs-config.json
    {
        "port": 3000,
        "files" : "./src/**/*.{js, html, css}",
        "server" : {
            "baseDir": ["./", "./src" ]
        }
    }
```

<br>

- **Mettre à jour** le script >> `npm update`

<br>

- Ajouter le `main` dans le fichier `package.json`

```json
# Inside package.json...
  "main": "index.html",
```

- Et ajoutez une `script` dans le fichier `package.json` de votre projet :

```json
# Inside package.json...
  "scripts": {
    "start": "npm run lite",
    "lite" : "lite-server",
    "dev": "lite-server",
    "test": "echo \"Error: no test specified\" && exit 1"
  },
```

- Pour lancer le server >> `npm start`

<br>

- Sercer local `http://localhost:3000`

<br>

- Pour la documentation >> [**NPM LITE-SERVER**](https://www.npmjs.com/package/lite-server)

<br>

### 2.0  Dependance

#### 2.1 Framework CSS

<details open>
    <summary><span><code>npm install - save bulma-start</code></span></summary>
        <br>
        <ul>
            <li>
                <p>Bulma est un framework CSS gratuit et open source basé sur Flexbox et construit avec Sass. Il est 100% réactif, entièrement modulaire et disponible gratuitement.</p>
            </li>
            <br>
            <li>
                <a href="https://www.npmjs.com/package/bulma-start" ><span><strong>NPM - Bulma</strong></span></a>
            </li>
            <li>
                <a href="https://www.jsdelivr.com/package/npm/bulma-start" ><span><strong>CDN - Bulma</strong></span></a>
            </li>
        </ul>
</details>

<br>

#### 2.2 Bibliothèques JavaScript

<details open>
    <summary><span><code>npm install - save jquery</code></span></summary>
        <br>
        <ul>
            <li>
                <p>jQuery est une bibliothèque JavaScript rapide, petite et riche en fonctionnalités.</p>
            </li>
            <br>
            <li>
                <a href="https://www.npmjs.com/package/jquery" ><span><strong>NPM - Jquery</strong></span></a>
            </li>
            <li>
                <a href="https://www.jsdelivr.com/package/npm/jquery" ><span><strong>CDN - Jquery</strong></span></a>
            </li>
        </ul>
</details>

<br>

#### 2.3  Iconic Awesome

<details open>
    <summary><span><code>npm install - save font-awesome</code></span></summary>
        <br>
        <ul>
            <li>
                <p>Font Awesome est une suite complète de 675 icônes pictographiques pour des graphiques vectoriels</p>
            </li>
            <br>
            <li>
                <a href="https://www.npmjs.com/package/font-awesome" ><span><strong>NPM - Font Awesome</strong></span></a>
            </li>
            <li>
                <a href="https://www.jsdelivr.com/package/npm/font-awesome" ><span><strong>CDN - Font Awesome</strong></span></a>
            </li>
        </ul>
</details>

<br>

#### 2.4  Fonts

<details open>
    <summary><span><code>Google Fonts</code></span></summary>
        <br>
        <ul>
            <li>
                <p>Ce paquet vous permet d'utiliser la famille de polices de Google Fonts dans votre application.</p>
            </li>
            <br>
            <li>
                <a href="https://www.jsdelivr.com/package/npm/@fontsource/roboto" ><span><strong>CDN - @fontsource/roboto (Minor) </strong></span></a>
                <span><pre>https://cdn.jsdelivr.net/npm/@fontsource/roboto@4.5/index.min.css</pre></span>
            </li>
            <br>
            <li>
                <a href="https://www.jsdelivr.com/package/npm/font-awesome" ><span><strong>CDN - @fontsource/open-sans (Minor)</strong></span></a>
                <span><pre>https://cdn.jsdelivr.net/npm/@fontsource/open-sans@4.5/index.min.css</pre></span>
            </li>
            <br>
            <li>
                <a href="https://www.jsdelivr.com/package/npm/font-awesome" ><span><strong>CDN - @fontsource/montserrat(Minor)</strong></span></a>
                <span><pre>https://cdn.jsdelivr.net/npm/@fontsource/montserrat@4.5/700.min.css</pre></span>
            </li>
        </ul>
</details>

<br>

#### 2.4.0 Fails de Sécurités pour le Content Delivery Network, CDN

##### SRI - Subresource Integrity

Le **SRI** est une nouvelle spécification du **W3C** qui permet aux développeurs web de s'assurer que les ressources hébergées sur des serveurs tiers n'ont pas été altérées. L'utilisation de la **SRI** est recommandée comme meilleure pratique lorsque des bibliothèques sont chargées à partir d'une source tierce.

<br>

##### Exemple

```html
<link   rel="stylesheet"
        href="https://cdn.jsdelivr.net/npm/@fontsource/montserrat@4.5/700.min.css"
        integrity="sha384-8jo1WzZMb0o3J9j5EvaMPXX4P8/bPEfDKutqmqwP5vt7N+GDrNYs8qY2FIb/PRGk"
        crossorigin="anonymous">
```

<br>

- [SRI - W3C Recommendation 23 June 2016](https://www.w3.org/TR/sri/)
- [SRI -  Hash Generator](https://www.srihash.org)

<br>

#### 2.4.1 Google Fonts

##### Pourquoi l'utilisation de Google Fonts pourrait-elle violer les obligations du RGPD ?

Le problème avec Google Fonts est que si un propriétaire d'un site web décide d'intégrer les polices d'une façon dynamique sur son site web, **l'adresse IP de chaque visiteur du site sera transmise aux serveurs de Google**.

Or, **les adresses IP des internautes représentent des données à caractère personnel** car elles indiquent la provenance et la destination des données et permettent ainsi d'identifier une personne réelle. Par conséquent, **la collecte et le stockage par Google d'adresses IP ne devrait être possible qu'après avoir recueilli le consentement préalable des utilisateurs**. Cela peut donc s'avérer très problématique, si le site web concerné n'informe pas les visiteurs du traitement de leurs données personnelles par Google et ne leur demande pas leur consentement au préalable.
