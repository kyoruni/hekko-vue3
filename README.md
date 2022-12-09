# hello-vue3
Vue3 のおためし

- Node.js 18.12.1
- Vue3
- Vite

## 起動

```console
$ docker-compose build
$ docker-compose up -d
```

## 作成方法メモ

```console
$ docker-compose build
$ docker-compose up -d
$ docker-compose exec vue bash

# npm init vue@latest
Need to install the following packages:

  create-vue@3.4.1

Ok to proceed? (y) y

✔ **Project name:** … hello-vue3
✔ **Add TypeScript?** … Yes
✔ **Add JSX Support?** … No
✔ **Add Vue Router for Single Page Application development?** … No
✔ **Add Pinia for state management?** … No
✔ **Add Vitest for Unit Testing?** … No
✔ **Add an End-to-End Testing Solution?** › No
✔ **Add ESLint for code quality?** … Yes
✔ **Add Prettier for code formatting?** … Yes

# cd hello-vue3
# npm install
# npm run dev
```