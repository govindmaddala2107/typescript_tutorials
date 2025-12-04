## Typescript
### Installation
```
npm i -g typescript
```
### Compilation:
- Go to the typescript file (sandbox.ts) path location and run 
    ```
    tsc sandox.ts
    ```
- If above one is not working, try using **npx**.
    ```
    npx tsc sandox.ts
    ```
- In watch mode, we can run like:
    ```
    npx tsc sandbox.ts -w
    ```

### Type Basics:
- In Sandbox.ts
    ```
    let myname: string = "govind";
    let age: number = 29;
    let isMajor: boolean = true;
    function doubleNumber(num: number): number{
        return num * 2;
    }

    export {};
    ```
- Above code compiles to:
    ```
    "use strict";
    Object.defineProperty(exports, "__esModule", { value: true });
    var myname = "govind";
    var age = 29;
    var isMajor = true;
    function doubleNumber(num) {
        return num * 2;
    }
    ```

### Object & Arrays:
