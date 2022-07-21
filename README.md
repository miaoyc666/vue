# vue

### 这是什么
vue学习脚本和工具集合，从v3开始学习

### 安装
#### 安装npm
```bash
# 官方文档：https://github.com/nodesource/distributions
curl -fsSL https://rpm.nodesource.com/setup_18.x | sudo bash -
sudo yum install -y nodejs
```
#### 安装vue
```bash
sudo npm install vue@next
```

#### 安装vue-cli
```bash
sudo npm install -g @vue/cli # 或 yarn global add @vue/cli
```

#### 创建应用
```bash
vue create helloVue
cd hellovue
npm run serve
```

#### 问题整理
##### 1.vue和nodejs是什么关系？
nodejs是一个运行环境，vue是前端框架，vue运行在nodejs构建的环境上。

##### 2.nvm和npm是什么关系？
npm是包管理器，nodejs的包管理器是npm。nvm是用来管理npm的管理器，例如同时需要管理多个项目时，需要nvm管理npm。

##### 3.vue创建项目Invalid project name的原因是什么？
vue命令无法创建命名包含大写字母的项目

##### 4.nginx做代理服务器，访问时显示：Invalid Host header?
修改host检查，修改vue.config.js，添加如下内容
```json
devServer: { 
    historyApiFallback: true,
    allowedHosts: "all",
  }
```


