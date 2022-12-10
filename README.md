#### 配置了各种lint规范的初始化项目

```
npm init
# add "type": "module" in package.json
npm i typescript -D
npx tsc --init
```

> types 配置项是指定编译生成的类型文件，如果 compilerOptions.declarationDir 指定的是dist，也就是源码和 .d.ts 同级，那么types可以省略

```
npm i eslint -D
npx eslint --init
```

```
npm i prettier -D
echo {}> .prettierrc.json

npm i eslint-config-prettier eslint-plugin-prettier -D
```

```
npm i husky -D
npx husky install
npm set-script prepare "husky install"
i lint-staged --save-dev
npx husky add .husky/pre-commit "npx lint-staged"
```

```
npm i commitlint --save-dev
npm i @commitlint/config-conventional --save-dev
npx husky add .husky/commit-msg 'npx --no-install commitlint --edit "$1"'
```
