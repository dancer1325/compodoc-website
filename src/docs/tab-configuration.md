# Customizing tab order and labels

* `navTabConfig`
  * == [] of tab configuration objects
  * == superset of tabs / -- shown for -- various dependencies | your project
  * allows
    * specifying tabs'
      * ordering / left-to-right
      * labels text 
* ways to specify
  * | compodoc configuration file or
  * `compodoc` CLI command's argument

# how to define a tab?

* `id`
  * == tab | apply the CUSTOM placement & label
  * ALLOWED values
    * __"info"__,
      * applicable | ALL dependency types
    * __"readme"__,
      * applicable | ALL dependency types
      * requirements
        * dependencies / specify content for it
    * __"source"__,
      * applicable | ALL dependency types
    * __"templateData"__,
      * applicable | components
      * requirements
        * dependencies / specify content for it
    * __"tree"__,
      * applicable | components
    * __"example"__
      * applicable | Component, Directive, Injectable, and Pipe dependencies
      * requirements
        * dependencies / specify content for it
```
{
  "id": "info",
  "label": "Custom Label"
}
```

# Examples
## Example1:_ | configuration file

```
{
    "navTabConfig": [
        {
            "id": "example",
            "label": "Overview"
        },
        {
            "id": "info",
            "label": "API"
        },
        {
            "id": "source",
            "label": "Source"
        },
        {
            "id": "tree",
            "label": "DOM Tree"
        }
    ],
    "tsconfig": "./src/tsconfig.json"
}
```

## _Example2:_ | CLI argument

* `"` -- MUST be escaped via -- "\\"

```
 compodoc --navTabConfig '[{\"id\": \"example\",\"label\": \"Overview\"},{\"id\": \"info\",\"label\": \"API\"},{\"id\": \"source\",\"label\": \"Source\"}]' -p src/tsconfig.json -n 'Documentation Name' -s
```
