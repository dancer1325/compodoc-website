# Styling the documentation

* by default, Compodoc use [bootstrap](http://getbootstrap.com/) v3.3.7
  * see [bootswatch.com](http://bootswatch.com/)
* ways to customize
  * provide a style.css file / contains at least these imports
    ```
    @import "./reset.css";
    @import "./bootstrap.min.css";
    @import "./bootstrap-card.css";
    @import "./prism.css";
    @import "./ionicons.min.css";
    @import "./compodoc.css";
    @import "./tablesort.css";
    ```
  * if you want to override the default theme -> provide a bootstrap.min.css file / override the default one
      ```
      └── your_theme_styles/
          ├── style.css // the main css file with default imports
          └── bootstrap.min.css // your bootstrap theme
      ```
* way to run
    ```
    compodoc -p tsconfig.doc.json -y your_theme_styles/
    ```

<a id="documentation-of-each-components"></a>

# Documentation of EACH component, module, directives

* Compodoc, | EACH component's root folder OR class' root folder OR module's root folder
  * search for default **xxx.component.md**
  * add it | component page's tab
    ```
    └── my-component/
        ├── my.component.ts
        ├── my.component.spec.ts
        ├── my.component.scss|css
        ├── my.component.html
        └── my.component.md
    ```

* comment description | **xxx.component.ts** / BETWEEN JSDoc comments
  * can be short

<a id="additional-documentation"></a>

# EXTERNAL documentation

* == add EXTERNAL markdown files 
* use cases
  * extend the
    * code comments | your application 
    * main README
* steps
  * create a folder / contain
    * markdown files
    * "summary.json" / explain the structure & files 
        ```
        summary.json
        
        [
            {
                "title": "A TITLE",
                "file": "a-file.md"
            },
            {
                "title": "A TITLE",
                "file": "a-file.md",
                "children": [
                    {
                        "title": "A TITLE",
                        "file": "a-sub-folder/a-file.md"
                    }
                ]
            }
        ]
        ```
  * use `--includes`

<a id="documentation-of-several-apps-in-a-monorepository"></a>

# Documentation of SEVERAL apps | monorepository (==Nx)
 
* 💡run Compodoc / EACH apps seperately 💡 

<a id="syntax-highlighting-in-markdown-files"></a>

# Syntax highlighting | markdown files

* -- via --
  * code block | your markdown / correct language
    * see [Github help](https://help.github.com/articles/creating-and-highlighting-code-blocks/)
    * integrated languages
      * json,
      * bash,
      * javascript,
      * markdown,
      * html,
      * scss,
      * typescript

* Compodoc -- use -- [Marked](https://github.com/chjj/marked) /
  * parse markdown
  * compile to html
* [prismjs.js](http://prismjs.com/)
  * support syntax highlighting

<a id="excluding-files"></a>

# how to exclude files?

* | [**tsconfig.json**](https://www.typescriptlang.org/docs/handbook/tsconfig-json.html),
  * extends `exclude` property

<a id="including-files"></a>

# how to include files?

* | [**tsconfig.json**](https://www.typescriptlang.org/docs/handbook/tsconfig-json.html),
  * extends `include` property
