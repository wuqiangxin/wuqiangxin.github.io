#### 前端 接口封装 步骤



~~~js
// 导入 axios
import axios from 'axios'
// 配置请求的跟路径
axios.defaults.baseURL = 'http://127.0.0.1:8888/api/private/v1/'


Vue.prototype.$http = axios



// 获取所有的菜单
    async getMenuList() {
      const { data: res } = await this.$http.get('menus')
      if (res.meta.status !== 200) return this.$message.error(res.meta.msg)
      this.menulist = res.data
      console.log(res)
    },
        
        
methods: {
    // 获取权限列表
    async getRightsList() {
      const { data: res } = await this.$http.get('rights/list')
      if (res.meta.status !== 200) {
        return this.$message.error('获取权限列表失败！')
      }

      this.rightsList = res.data
      console.log(this.rightsList)
    }
  }
~~~



####  rem 响应式布局

~~~js
// 就是将 px 转化为 rem 单位
1. 先用到 flexible.js + rem 技术做适配
拓展  cssrem 设置 root根 字体大小 font size 80px
easy less 自动生成css文件代码

2. 完成后要重启 VS code 才能生效


检验： 打开网页，HTML 的字体大小会随屏幕的大小变化发生变化
~~~













#### 媒体查询

~~~js
@media screen and (min-width: 320px) {
    html {font-size: 14px;}
}
@media screen and (min-width: 360px) {
    html {font-size: 16px;}
}
@media screen and (min-width: 400px) {
    html {font-size: 18px;}
}
~~~



#### 百分比布局



#### Flex 布局
