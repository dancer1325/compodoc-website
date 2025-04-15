# Configuration file

* search by default, the files
  * .compodocrc,
  * .compodocrc.json,
  * .compodocrc.yaml
  * compodoc property | your package.json 
* recommendations   
  * place | your project folder's root 
* [JSON schema](./node_modules/@compodoc/compodoc/src/config/schema.json)

# | Windows, options & quotes

* TODO:
Keep in mind that using options with multiple words need quotes around your sentence.

```bash
compodoc -p tsconfig.doc.json -n 'My app documentation'
```

Using npm scripts, the command is hosted in package.json file. Don't forget to escape with double quotes for Windows systems. (with npm 6.x)

```bash
{
   ...
   "doc": "npx compodoc -p tsconfig.doc.json -n \"My app documentation\""
   ...
}
```

# How to render the documentation?

* documentation generated | default output folder

```bash
compodoc -p tsconfig.doc.json
```

# How to render documentation / -- provide -- source folder?

```bash
compodoc src -p tsconfig.doc.json
```

# How to serve generated documentation -- via -- compodoc?

*
    ```bash
    compodoc -s
    ```
* | browser, http://localhost:8080

# How to render documentation & serve it -- via -- compodoc?

* 
    ```bash
    compodoc -p tsconfig.doc.json -s
    ```
* | browser, http://localhost:8080
