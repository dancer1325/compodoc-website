# Node.js versions

* | january 2025,
  * ⚠️compatible ONLY with Node.JS last [active versions](https://nodejs.org/en/about/previous-releases) ⚠️ 
    * v16.x, 
    * v18.x,
    * v20.x

* [Angular version vs Node.Js version](https://angular.dev/reference/versions)

# Angular-CLI

* | january 2025,
  * supports Angular-CLI v19.x

# How to install?
## Globally

* ways
  * -- via -- Angular CLI
    ```bash
    ng add @compodoc/compodoc
    ```
  * -- via -- npm
    ```bash
    npm install -g @compodoc/compodoc
    
    # | Powershell
    npm install -g "@compodoc/compodoc"
    ```

## Locally

* ways
  * -- via -- Angular CLI
    ```bash
    ng add @compodoc/compodoc
    ```
    * structure
      ```
      .
      ├── src
      │ ├── app
      │ │ ├── app.component.ts
      │ │ └── app.module.ts
      │ ├── main.ts
      │ └── ...
      ├── tsconfig.app.json
      ├── tsconfig.doc.json
      └── tsconfig.json
      ```
    * -> create npm scripts + special tsconfig.doc.json file
  * -- via -- npm
    ```bash
    npm install --save-dev @compodoc/compodoc
    ```

# How to run?

* create `tsconfig.doc.json` / 
  * 👀contain the key `include` / -- points to -- `src/` 👀 
  * ALSO valid `exclude`
  ```
  {
    "include": ["src/**/*.ts"],
    "exclude": ["src/test.ts", "src/**/*.spec.ts", "src/app/file-to-exclude.ts"]
  }
  ```
* | your package.json (npm 6.x)
  ```bash
  "scripts": {
    "compodoc": "npx compodoc -p tsconfig.doc.json"
  }
  ```
* run
  ```bash
  npm run compodoc
  
  # OR
  npx @compodoc/compodoc ...
  ```
