####  1. react 初始化项目步骤  注意： 等待时间稍微有点长
```js
npx create-react-app hkzf-mobile

cd hkzf-mobile
yarn start  或者 npm start
```

<br />

####  2. 优化项目结构
![](https://img2020.cnblogs.com/blog/2113686/202111/2113686-20211125213128722-1738520344.png)
![](https://img2020.cnblogs.com/blog/2113686/202111/2113686-20211125213134316-1551311737.png)

<br />

####  3. 引入 [antd-mobile组件库](https://www.bookstack.cn/read/antd-mobile-v2.3.1/10ef185f0d5b2c83.md#%E5%BF%AB%E9%80%9F%E4%B8%8A%E6%89%8B)
![](https://img2020.cnblogs.com/blog/2113686/202111/2113686-20211126151007560-104162202.png)

<br />

####  4. 配置 react 基础路由  注意： 重新加载路由后， 需要重启项目
![](https://img2020.cnblogs.com/blog/2113686/202111/2113686-20211126180420159-813592011.png)
```js
// 注意： react 路由版本的问题 https://www.cnblogs.com/fuct/p/15517038.html

1.  yarn add react-router-dom  或者  npm i react-router-dom@5.2.0

2.  import { BrowserRouter as Router, Route, Link } from 'react-router-dom'  // 在 app.js

function App() {
  return (
    <Router>
      <div className="App">
        {/* 根组件123
        <Button>登录</Button> */}
        {/* 路由入口 */}
        <ul>
          <li><Link to='/home'>首页</Link></li>
          <li><Link to='/cityList'>城市选择</Link></li>
        </ul>

        {/* 配置路由 */}
        <Route path='/home' component={Home}></Route>
        <Route path='/cityList' component={cityList}></Route>
      </div>
    </Router>
  );
}
```

<br />

####  5. 外观和样式调整
![](https://img2020.cnblogs.com/blog/2113686/202111/2113686-20211126203142663-2103089716.png)
```js

html, body {
  height: 100%;
  font-family: 'Microsoft YaHei';
  color: #333;
  background-color: #fff;
}

* {
  box-sizing: border-box;
}

```

<br />

####  6. 嵌套路由 实现 TabBar 页面
![](https://img2020.cnblogs.com/blog/2113686/202111/2113686-20211126210603332-1878207134.png)
![](https://img2020.cnblogs.com/blog/2113686/202111/2113686-20211126210609434-43591677.png)

<br />

####  7. 修改 TabBar 外观样式 看官方文档  使用第三方字体图标教程
![](https://img2020.cnblogs.com/blog/2113686/202111/2113686-20211126215621339-1957891128.png)
```js
1. 将 fonts 字体图标文件 放在 assets 文件夹下

2. 在 index.js 文件中 引入 字体图标的样式
// 导入字体图标的 css 样式
import './assets/fonts/iconfont.css'

3. 在 TabBar 组件里面修改 icon 图标
<i className="iconfont icon-my" />
```

<br />

####  8. TabBar 配合路由进行使用
![](https://img2020.cnblogs.com/blog/2113686/202111/2113686-20211126225438837-1140613444.png)
![](https://img2020.cnblogs.com/blog/2113686/202111/2113686-20211126225443938-1416208645.png)

<br />

####  9. TabBar 代码重构 注意: 重复的代码 用遍历（循环）
![](https://img2020.cnblogs.com/blog/2113686/202111/2113686-20211126231042939-1627072527.png)