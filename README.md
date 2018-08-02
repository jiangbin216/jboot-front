# jboot-front

### 在线Demo 
http://www.jiangbin.net.cn
### 后台项目地址：[JBoot](https://github.com/jiangbin216/jboot)
### 项目简介
- 项目基于 Vue-Cli 创建
- 后台加载动态权限菜单 权限控制至按钮
- 多语言切换
- iView使用图标库 [ionicons](http://ionicons.com/) 
- 额外图标库 [vue-awesome](https://github.com/Justineo/vue-awesome)

### 主要所用技术
- [Vue 2.5.x](https://cn.vuejs.org/)
- [iView](https://www.iviewui.com/)
- [iview-admin](https://github.com/iview/iview-admin)
- [iview-area](https://github.com/iview/iview-area)：城市级联组件
- [Vuex](https://vuex.vuejs.org/zh-cn/)
- Vue Router
- ES6
- webpack
- axios
- echarts
- cookie
- 第三方插件
    - [hotjar]一体化分析和反馈

### 本地开发构建运行

- 启动后端 [jboot](https://github.com/jiangbin216/jboot) 项目后，在 `config/index.js` 中修改你的后端接口地址代理配置
- 在项目根文件夹下先后执行命令 `npm install` 、 `npm run dev`
- 前台端口默认9999 http://localhost:9999

### 部署
- 先后执行命令 `npm install` 、 `npm run build` 将打包生成的 `dist` 静态文件放置服务器中，并配置路由代理

### 开发指南
- 组件使用详见[iView官网文档](https://www.iviewui.com/docs/guide/install)
- 权限按钮或其他内容显示控制自定义标签：`v-has`，使用示例：
    ```
    <Button v-has="'add'">添加按钮</Button>
    <Button v-has="'edit'">编辑按钮</Button>
    <Button v-has="'delete'">删除按钮</Button>
    <div v-has="'view'">需要view权限的界面内容</div>
    ```
    - 表格中[Render渲染函数](https://cn.vuejs.org/v2/guide/render-function.html)权限判断示例
    ```
    render: (h, params) => {
        if(this.$route.meta.permTypes.includes("edit")){
            return ... ...
        }else{
            return ... ...
        }
    }
    ```
