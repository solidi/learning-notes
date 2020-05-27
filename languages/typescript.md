# TypeScript

## Philosophy

- Save time by adding strong/static type checking. Is a superset of JavaScript.
- The more information you give, the better it will help you.

## How

- Transpiler to JavaScript.
- Widely Supported - ES Current - ES Future. Use future features today.
- Catches errors before runtime.
- Better tooling, and autocompletion.

## Installation and Running

- `npm install -g typescript`
- `tsc helloworld.tsc`

## Fresh Project

- Add tsconfig.json to the project root.
    - Compiler Options
        - `"target": "es6"` - which version to compile against.
        - `"outputDir": "dist"` - where to place transpiled files.
        - `"allowJs": true` - extend support to JS files.
        - `"checkJs": true` - check for issues with JS files.
        - `"lib": ["webworker"...]` - libs will be available in target environments.
- Run `tsc -w` to watch for changes.

## Basics

- `let var: <type> = "string"`
    - 7 primitive types. [string, boolean, number, bigint, null, undefined, symbol]
    - And object type
- Functions: `function foo(param: <type>): <return type>`
    - `void` type as well.
    - Can break out to specific type information with attributes.
        - `function foo(): {
            param1: string,
            param2: boolean
        }`
- Type inference and gradual typing. Use `any` key for flexibility.
- Union types: 
    `type Thing = number | string`

## Interfaces

```typescript
interface Cool {
    param1?: string; // optional.
    param2: string;
    readonly param3: string; // immutable after assignment.

    add?: (param: string) => string;
}
```

- Inline type / brace type can be casted as an `interface` type.
    - Is not in transpiled code, is more meta data to find mistakes.

## Enums

```typescript
enum Things {
    This = "this",
    That = that"
}
```
or the pipe character for literal types.

```typescript
interface whatever { 
    yes: "this" | "that";
}
```

## Classes

- Define fields at top of the class.
- Use `static` for fields that are defined for class.
- Access modifiers are available. `private`, `protected`, and `public`

## Generics

Are available in TypeScript. 

```typescript
    function here<T, U>(param: T, param2: U): T {
        ...
    }
```

## Third Party APIs

Meta data for types are needed.

- `declare var Vue: any`

## Trivia

- Visual Studio code is written in TypeScript.

## Resources

1. [DefinitivelyTyped](http://www.definitelytyped.org)
