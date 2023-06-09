# **配置**

## Eslint

| 依赖 | 作用描述 |
| :----: | :---- |
|eslint|                            ESLint 核心库|
|eslint-config-prettier|            关掉所有和 Prettier 冲突的 ESLint 的配置|
|eslint-plugin-prettier|            将 Prettier 的 rules 以插件的形式加入到 ESLint 里面|
|eslint-plugin-vue|                 为 Vue 使用 ESlint 的插件|
|@typescript-eslint/eslint-plugin|  ESLint 插件，包含了各类定义好的检测 TypeScript 代码的规范|
|@typescript-eslint/parser|         ESLint 的解析器，用于解析 TypeScript，从而检查和规范 TypeScript 代码|

## StyleLint

| 依赖| 作用描述 |
| :----: | :---- |
|stylelint|                         stylelint 核心库|
|stylelint-config-html|             Stylelint 的可共享 HTML（和类似 HTML）配置，捆绑 postcss-html 并对其进行配置。|
|stylelint-config-recommended-scss| 扩展 stylelint-config-recommended 共享配置，并为 SCSS 配置其规则|
|stylelint-config-recommended-vue|  扩展 stylelint-config-recommended 共享配置，并为 Vue 配置其规则|
|stylelint-config-standard|         打开额外的规则来执行在规范和一些 CSS 样式指南中发现的通用约定，包括：惯用 CSS 原则，谷歌的 CSS 样式指南，Airbnb 的样式指南，和 @mdo 的代码指南。|
|stylelint-config-standard-scss|    扩展 stylelint-config-standard 共享配置，并为 SCSS 配置其规则|
|stylelint-config-recess-order|     属性的排序（插件包）|
|stylelint-config-prettier|         关闭所有不必要的或可能与 Prettier 冲突的规则|
|postcss|                           postcss-html 的依赖包|
|postcss-html|                      用于解析 HTML（和类似 HTML）的 PostCSS 语法|

## package.json

``` {
  "scripts": {
    // 本地运行(dev环境)
    "dev": "vite",
    // 本地运行(dev环境)
    "serve": "vite",
    // 构建打包(dev环境)
    "build:dev": "vue-tsc && vite build --mode development",
    // 构建打包(test环境)
    "build:test": "vue-tsc && vite build --mode test",
    // 构建打包(pro环境)
    "build:pro": "vue-tsc && vite build --mode production",
    // 检查项目 ts 类型
    "type:check": "vue-tsc --noEmit --skipLibCheck",
    // 本地环境预览构建后的 dist
    "preview": "npm run build:dev && vite preview",
    // 执行 eslint 校验
    "lint:eslint": "eslint --fix --ext .js,.ts,.vue ./src",
    // 执行 prettier 格式化
    "lint:prettier": "prettier --write "src/**/*.{js,ts,json,tsx,css,less,scss,vue,html,md}"",
    // 执行 stylelint 格式化
    "lint:stylelint": "stylelint --cache --fix "**/*.{vue,less,postcss,css,scss}" --cache --cache-location node_modules/.cache/stylelint/",
    // 执行 lint-staged.config.js 文件下的命令
    "lint:lint-staged": "lint-staged",
    // 初始化 husky 配置
    "prepare": "husky install",
    // 自动更新版本
    "release": "standard-version",
    // 提交代码(可自定义配置执行命令)
    "commit": "git add -A && czg && git push"
  }``` 
}
