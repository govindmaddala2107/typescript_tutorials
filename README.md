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
#### Arrays:
    ```
    let numArr = [12,3,5];
    // numArr.push("dshghf") // Argument of type 'string' is not assignable to parameter of type 'number'.ts(2345)
    numArr.push(10);

    let stringArr = ["a", "b"];
    stringArr.push("c");
    // stringArr.push(true); // Argument of type 'boolean' is not assignable to parameter of type 'string'.ts(2345)

    let mixedArr = ["ABC", 10];
    mixedArr.push("BCD");
    mixedArr.push(20);
    // mixedArr.push(true); // Argument of type 'boolean' is not assignable to parameter of type 'string | number'.ts(2345)

    ```
- Here numArr is assigned with array with numbers but when we try to push a string, it throws an error.
    - Argument of type 'string' is not assignable to parameter of type 'number'.ts(2345)
- Same for other types also.
- When an array is having multiple data types (here string and number), but when I try to push boolean, it throws following error:
    - Argument of type 'boolean' is not assignable to parameter of type 'string | number'.ts(2345)

#### Objects:
    ```
    let details = {
        name: "govind",
        age: 30,
        hobbies: ["coding", "cooking"]
    }

    // details.age = "29"; // Type 'string' is not assignable to type 'number'.ts(2322)
    details.age = 29;

    // details.hobbies.push(20); // Argument of type 'number' is not assignable to parameter of type 'string'.ts(2345)

    // details.location = "Banglore"; // Property 'location' does not exist on type '{ name: string; age: number; hobbies: string[]; }'.ts(2339)
    ```
- Here details object's key age is number type but when we assign string, following error comes:
    - Type 'string' is not assignable to type 'number'.ts(2322)
- Here when we try to add location key to details object, following error comes:
    - Property 'location' does not exist on type '{ name: string; age: number; hobbies: string[]; }'.ts(2339)
