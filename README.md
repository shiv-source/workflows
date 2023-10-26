# workflows

### Deploy angular build to GitHub Pages with pnpm package manager and pnpm cache

```yml
name: Deploy Angular app with PNPM to GitHub Pages

on:
  push:
    branches:
      - "master"

jobs:
  deploy:
    permissions:
      contents: write
    uses: shiv-source/workflows/.github/workflows/angular-pnpm-gh-pages.yml@master
    with:
      ANGULAR_BUILD_DIR: ./dist/my-angular-app/ # you can change this as per your folder name like ./dist/ or ./dist/project1/
      ANGULAR_BUILD_COMMAND: pnpm build:prod # default value = pnpm build. Not a required input
```
