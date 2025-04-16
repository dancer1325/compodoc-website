# General information

* Documentation coverage
  * == | ALL file's statement (INCLUDED decorators) / EXCEPT TO
    * private functions
  * if you want to text | CI context -> use `--coverageTest` command 
  * _Example:_
    ![screenshot](../assets/img/screenshots/8.png)
  * if you pass `--coverageTestThresholdFail` command -> returns `boolean`
    * `true` == warn
    * `false` == error
  * if you pass `--coverageMinimumPerFile` command -> specify a MINIMUM of coverage / file

## Test coverage | commit process

1. install [lint-staged](https://github.com/okonet/lint-staged) 
  ```
  npm i -d lint-staged
  ```
2. | `package.json`, add the configuration
    ```json
    "devDependencies": {
        ...
    },
    "lint-staged": {
        "linters": {
            "*.ts": ["compodoc --coverageMinimumPerFile 25"]
        }
    }
    ```
