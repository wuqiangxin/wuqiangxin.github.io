####  Vue 项目 运行步骤 和 提交代码



###### 1. 首先克隆 代码

~~~js
// 拉取代码 
git clone https://github.com/sl1673495/vue-netease-music.git (这是项目地址)

// 提交代码 步骤
git status  // 查看仓库文件状态
git add .   // 将所有的修改文件全部都提交到暂存区
git commit -m '注释所提交的代码' // 添加注释
git pull  // 拉取远端代码
// 这里要注意， 如果拉取代码后有冲突，需要在 VS code 里面先手动的解决冲突后，再提交代码 (很重要)
git push  // 最后提交到远端仓库

// 创建分支
git branch dev 

// 切换分支
git checkout dev

// 合并分支之前要先切换到主分子后在切换
git checkout master

git merge dev
~~~



###### 2. 克隆代码后运行项目

~~~js
// 1. 先查看 package.json 文件里面的 scripts 对象里面会有提示 如何运行项目
// 一般情况下都是 用 npm 或者 yarn 
npm i   或者   yarn i   // 先把第三方的包 全部都下载到项目中
npm run dev   // 然后运行项目 
yarn serve     // 运行项目   运行项目的具体方法 是根据 package.json 里面的 scripts 提示来操作的
~~~



###### 3. git 提交时 忽略文件

~~~js
.DS_Store
node_modules
/dist
~~~



###### 4. vue 中 router.js 文件

~~~js
import Vue from 'vue'
import Router from 'vue-router'
// 代码结尾是不需要家分号的（;）
// vue 文件结尾也是不需要带上（.vue）的

const Discovery = () => import(/* webpackChunkName: "Discovery" */ '@/page/discovery')
const Login = () => import(/* webpackChunkName: "Search" */ '@/page/Login')

// 需要显示在侧边栏菜单的页面
export const menuRoutes = [
  // 注意： 这里的组件 一定要先定义（很重要）
   {
    path: '/discovery',
    name: 'discovery',
    component: Discovery,
    meta: {
      title: '发现音乐',
      icon: 'music',
    },
   },
]

Vue.use(Router)

export default new Router({
  routes: [
    // redirect 重定向 当路径 为 / 时则跳转到 /Login 路径的页面
    {
      path: '/',
      redirect: '/Login'
    },
    {
      path: '/Login',
      name: 'Login',
      component: Login
    },
    // 这里表示 和 menuRoutes 拼接到一起
    ...menuRoutes,
})

~~~
