# VUE+element-ui
## nodejs 安装
直接从官方下载网站下载安装
## 配置cnpm
安装好nodejs就已经安装了npm，但是使用npm下载组件会比较慢，所以可以安装淘宝镜像。
```
npm install -g cnpm --registry=https://registry.npm.taobao.org
```

## vue安装
```
npm install vue-cli -g
```
## 初始化项目
```
vue init webpack projectName(项目名称)
```
中间选择如下
```
? Project name vue-project
? Project description A Vue.js project
? Author author
? Vue build standalone
? Install vue-router? Yes
? Use ESLint to lint your code? No
? Set up unit tests No
? Setup e2e tests with Nightwatch? No
? Should we run `npm install` for you after the project has been created? (recom
mended) (Use arrow keys)
❯ Yes, use NPM
  Yes, use Yarn
  No, I will handle that myself
```
## element-ui 安装
```
cd vue-project

# 安装依赖
cnpm install

# 安装element-ui
cnpm i element-ui -S

# 测试/启动项目
npm run dev

```