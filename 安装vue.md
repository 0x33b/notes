# VUE+element-ui
## nodejs 安装
直接从官方下载网站下载安装
## 配置cnpm
安装好nodejs就已经安装了npm，但是使用npm下载组件会比较慢，所以可以安装淘宝镜像。
```
npm install -g cnpm --registry=https://registry.npm.taobao.org
```
## npm install 报错无法加载文件***\npm.ps1，因为再次系统上禁止运行脚本
```
npm install vue-cli -g
npm : 无法加载文件 *\npm.ps1，因为在此系统上禁止运行脚本。有关详细信息，请参阅 https:/go.microsoft.com/fwl
ink/?LinkID=135170 中的 about_Execution_Policies。
```
//报错解释
这个错误表明你的系统策略设置不允许执行未签名的PowerShell脚本。从Windows PowerShell 3.0开始，默认的执行策略被设置为“Restricted”，这意味着默认情况下不允许任何脚本运行。
//解决方法：
1. 以管理员身份打开PowerShell。
2. 执行以下命令来查看当前的执行策略：
``` Powershell
Get-ExecutionPolicy
```
3. 如果返回结果是Restricted，你可以设置一个更宽松的执行策略，如RemoteSigned（运行本地脚本和已签名的远程脚本）：
``` Powershell
Set-ExecutionPolicy RemoteSigned
```
或者，如果你确信脚本是安全的，可以暂时设置为Unrestricted（允许所有脚本运行）：
``` Powershell
Set-ExecutionPolicy Unrestricted
```
4. 当系统提示确认时，输入Y并回车以确认更改。

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
