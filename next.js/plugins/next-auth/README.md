# NextAuth.js

## Links

- [Code Repository](https://github.com/nextauthjs/next-auth)
- [Main Website](https://next-auth.js.org/)

## Guides

- [Tutorials and Explainers](https://next-auth.js.org/tutorials)
- [Configuration / Options](https://next-auth.js.org/configuration/options)
- [Configuration / Pages](https://next-auth.js.org/configuration/pages)

## Examples

- [NextAuth.js Typescript TypeScript - Example App](https://github.com/nextauthjs/next-auth-typescript-example)

## Library

### Installation

<!--
npm install @prisma/client @next-auth/prisma-adapter@canary
npm install prisma --save-dev
-->

```sh
# With NPM
npm install next-auth
npm install @types/next-auth --save-dev

# With Yarn
yarn add next-auth
yarn add @types/next-auth --dev
```

### Issues

#### TBD

```log
This expression is not callable. Type 'typeof import("/")' has no call signatures. ts(2349)
```

TODO

#### Any Type

```log
Binding element 'a' implicitly has an 'any' type. ts(7031)
```

```ts
function test({ a }: { a: any }) {
  // ...
}
```

<!--
next-auth.d.ts

import 'next-auth/jwt'

declare module 'next-auth/jwt' {
  interface JWT {
    userRole?: 'admin'
  }
}
-->
