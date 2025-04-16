# General information

* provide const / type `Routes`
  * == follow [Angular's routing guide](https://angular.dev/guide/routing/common-router-tasks)
    ```js
    const APP_ROUTES: Routes = [
        { path: 'about', component: AboutComponent },
        { path: '', component: HomeComponent}
    ];
    
    ...
    
    RouterModule.forRoot(APP_ROUTES)
    ```

* _Example:_
  ![screenshot](../assets/img/screenshots/routing.png)
