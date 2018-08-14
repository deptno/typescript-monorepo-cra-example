# typescript-monorepo-cra-example

> 🙉 TypeScript Monorepo Sample  
Required TypeScript@3 above

## Create monorepo with create-react-app

### Prerequisition
`create-react-app`, `yarn`

### Create monorepo
```bash
$ create-react-app typescript-monorepo/packages/react-app --react-scripts=react-scripts-ts
$ cd typescript-monorepo
$ rm -r packages/react-app/node_modules
```

- create [packages.json](packages.json)
- create [packages/tsconfig.json](packages/tsconfig.json)
- create [packages/tsconfig.base.json](packages/tsconfig.base.json)

### Create component

- create [packages/component-a](packages/component-a) - 3 files

```bash
$ cd packages/component-a
$ yarn link
$ cd ../react-app
$ yarn link component-a
$ cd ../..
```

### Edit react-app

- edit [packages/react-app/src/app.tsx](packages/react-app/src/app.tsx)

```bash
$ yarn
$ yarn build:packages
$ yarn start
```

### 👌

![<ComponentA>](assets/component-a.png)
