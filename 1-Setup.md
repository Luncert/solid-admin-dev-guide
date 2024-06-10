# 搭建项目框架

1.初始化空项目

```
npm create vite@latest --template solid-ts
```

2.添加依赖

在``package.json``中的``devDependencies``添加以下内容:
```
"autoprefixer": "^10.4.16",
"daisyui": "^3.9.3",
"postcss": "^8.4.31",
"tailwindcss": "^3.3.5",
```
在``dependencies``添加：
```
"daisyui": "^3.9.3",
```
终端运行：
```
npm install
```
其他推荐库：
- [solid-new-bucket](https://www.npmjs.com/package/solid-new-bucket) 根据 SolidJS Signal 封装的更简单易用的状态管理API

3.配置tailwindcss

将``index.css``的内容替换为：
```
@tailwind base;
@tailwind components;
@tailwind utilities;
```
在根目录添加``./tailwind.config.js``：
```
module.exports = {
  content: ['./src/**/*.{js,ts,jsx,tsx}'],
  plugins: [require("daisyui")],
};
```
在根目录添加``./postcss.config.cjs``：
```
module.exports = {
  plugins: [require('tailwindcss'), require('autoprefixer')],
};
```