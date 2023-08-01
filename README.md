# blog

# 项目来源
本项目来源于[《腾讯云 Cloud Studio 实战训练营》](https://marketing.csdn.net/p/06a21ca7f4a1843512fa8f8c40a16635)的参赛作品
该作品在腾讯云 [Cloud Studio](https://www.cloudstudio.net/?utm=csdn) 中运行无误。



# 数据大屏项目

欢迎来到 数据大屏项目！这是一个基于 Nuxt.js 构建的数据大屏应用。


# 项目结构


```
|-- webProject                       # webProject 根目录
    |-- .editorconfig                # 编辑器配置文件
    |-- .gitignore                   # Git 忽略文件列表
    |-- README.md                    # 项目说明文档
    |-- nuxt.config.js               # Nuxt.js 配置文件
    |-- package-lock.json            # 包版本锁定文件
    |-- package.json                 # 项目依赖配置文件
    |-- assets                       # 静态资源目录
    |   |-- bg.png                   # 背景图片文件
    |   |-- common.css               # 公共样式文件
    |   |-- data                     # 数据目录
    |       |-- data.json            # 数据文件
    |-- components                   # 组件目录
    |   |-- LeftChart.vue            # 左侧图表组件
    |   |-- Map.vue                  # table表组件
    |   |-- ScrollBoard.vue          # 滚动板组件
    |   |-- activeChart.vue          # 活动图表组件
    |-- pages                        # 页面目录
    |   |-- index.vue                # 首页 Vue 页面文件
    |-- plugins                      # 插件目录
    |   |-- datav.js                 # 数据可视化插件文件
    |   |-- element-ui.js            # Element UI 插件文件
    |-- static                       # 静态文件目录
    |   |-- favicon.ico              # 网站图标文件
    |-- store                        # 状态管理目录
        |-- README.md                # 状态管理目录的说明文档



```
 
## 使用方法

1. 克隆或下载本项目到您的本地环境。

2. 在命令行中进入项目根目录。

3. 使用nvm 下载安装node 版本 
    - nvm install 19.0.0
    - nvm use 19.0.0
 

4. 执行以下命令安装依赖：

```shell
npm install
```

5. 在项目根目录中执行以下命令以启动开发服务器：

```shell
npm run dev
```

6. 打开浏览器，访问 `http://localhost:3000` 即可预览博客应用程序。

7. 如果是在`Cloud Studio` 中运行的话, 直接点击右下角的弹窗中的新窗口打开即可

## 功能介绍

基于datav 创建的一个对csdn 参赛文章分析的数据大屏项目

## 技术栈

- Vue.js：JavaScript 框架
- Nuxt.js：Vue.js 的通用应用框架
- Element UI：基于 Vue.js 的 UI 组件库
= Datav : 数据可视化的组件库

## 贡献

如果您对该项目有任何改进意见或功能建议，欢迎提交 Issue 或 Pull Request。
 