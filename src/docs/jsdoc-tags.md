# JSDoc tags

* SUPPORTED JSDoc tags 
  * Reason: 🧠due to [TypeScript compiler limitations](https://github.com/Microsoft/TypeScript/wiki/JSDoc-support-in-JavaScript) 🧠

- `@deprecated Deprecated description`
    ```js
    /**
     * This is my class
     * @deprecated This class is deprecated
     */
    class MyClass {}
    ```
- `@returns {Type} Description`
    ```js
    /**
     * @param {string} target  The target to process
     * @returns The processed target number
     */
    function processTarget(target:string):number;
    ```
-   `@ignore`, `@internal`
  - == symbol | your code / should NEVER appear | documentation
  - `@ignore`
    - ALLOWED |
      - class,
      - component
      - injectable,
      - ENTIRE component

    ```js
    // 1. | component
    /**
     * @ignore
     */
    @Component({
        selector: 'app-root',
        templateUrl: './app.component.html',
        styleUrls: ['./app.component.css'],
    })
    export class AppComponent {}
    ```

    ```js
    // 2. | class' elements
    /**
     * Footer component
     */
    @Component({
        selector: 'the-footer',
        templateUrl: './footer.component.html',
        styleUrls: ['./footer.component.css'],
    })
    export class FooterComponent {
        /**
         * @ignore
         */
        ignoredProperty: string;
    
        /**
         * @ignore
         */
        @Input() ignoredInput: string;
    
        /**
         * @ignore
         */
        @Output() ignoredOutput;
    
        /**
         * @ignore
         */
        ignoredFunction() {}
    }
    ```
- `@param {Type} Name Description`
    ```js
    /**
     * @example
     * This is a good example
     * processTarget('yo')
     *
     * @param {string} target  The target to process see {@link Todo}
     * @returns The processed target number
     */
    function processTarget(target:string):number;
    ```
- `@link`
    ```js
    // 1. | internal reference
    {@link Todo}
    [Todo]{@link Todo}
    {@link Todo|TodoClass}
    
    Anchors are supported : [Todo]{@link Todo#myproperty}
    
    // 2. | external link
    [Google]{@link http://www.google.com}
    {@link http://www.apple.com|Apple}
    {@link https://github.com GitHub}
    ```
- `@example` or markdown
  - ALLOWED |
    - directives,
    - components
    - pipes decorators

# TS indentation
* if you want to keep a level of indentation -> put >=13 space characters
  * Reason: 🧠internal margin / NEW lines 🧠

```js
/**
 * Shows all events on a given day. Example usage:
 *
 * `` `
 * &lt;mwl-calendar-day-view
 *             [viewDate]="viewDate"
 *             [events]="events"&gt;
 * &lt;/mwl-calendar-day-view&gt;
 * `` `
 */

/**
 * Shows all events on a given day. Example usage:
 *
 * @example
 * <mwl-calendar-day-view
 *             [viewDate]="viewDate"
 *             [events]="events">
 * </mwl-calendar-day-view>
 */
```
