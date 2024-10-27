# Fullstack Turbo

Trubo monorepo configured with **NextJs** and **NestJs** Applications. Fore more information on turbo monorepo read their [offical docs](https://turbo.build/repo/docs) and to have a better understanding of monorepo in general read this [docs](https://github.com/korfuri/awesome-monorepo) in github.

### To run the application in development environement

```sh
pnpm dev
```

_NextJs web application will run in port 3000 <br/>
NestJs api application will run in port 5000_

### To build the application in development environement

```sh
pnpm build
```

### Apps and Packages

- `api`: a [Nest.js](https://nestjs.com/) application which will be used for **backend**
- `web`: a [Next.js](https://nextjs.org/) application which will be used for **frontend**
- `@repo/ui`: a stub react **component** library shared by both `web` and `docs` applications
- `@repo/eslint-config`: `eslint` **configurations** _(includes `eslint-config-next` and `eslint-config-prettier`)_
- `@repo/typescript-config`: `tsconfig.json`s used throughout the monorepo

Each package/app is 100% [TypeScript](https://www.typescriptlang.org/).

### Utilities

This Turborepo has some additional tools already setup for you:

- [TypeScript](https://www.typescriptlang.org/) for static type checking
- [ESLint](https://eslint.org/) for code linting
- [Prettier](https://prettier.io) for code formatting

### Configure remote cashing

Turborepo can use a technique known as Remote Caching to share cache artifacts across machines, enabling you to share build caches with your team and CI/CD pipelines.

By default, Turborepo will cache locally. To enable Remote Caching you will need an account with Vercel. If you don't have an account you can create one, then enter the following commands:

```sh
npx turbo login
```

Next, you can link your Turborepo to your Remote Cache by running the following command from the root of your Turborepo:

```sh
npx turbo link
```
