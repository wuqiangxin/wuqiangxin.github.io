####  1.   设置 屏幕最小 宽度

```css
html, body, #app {
    height: 100%;
    margin: 0;
    padding: 0;
    /* 设置屏幕最小宽度 */
    min-width: 1100px;
}

当打开控制台后， 屏幕宽度小于最小宽度时，则会添加滚动条
```

<br />

#### 2. 将两个数组拼接到一个数组

```js
// 展开运算符可以合并两个数组  ...arr1 表示将 arr1 里的数据全部展开并添加到一个新的数组里
const arr1 = [1, 2]
const arr2 = [3, 4]
const all = [...arr1, ...arr2]
console.log(all)
// all  [1, 2, 3, 4]
```

<br />

####  3. 表格  tree-table 树形表格组件 [tree-table 地址：](https://www.npmjs.com/package/vue-table-with-tree-grid)

```js
npm i vue-table-with-tree-grid -S   版本 0.2.4

// vue-table-with-tree-grid  直接搜索会有 文档教程
// main.js 中 导入
// 引入表格
import TreeTable from 'vue-table-with-tree-grid'
// 注册成为全局组件
Vue.component('tree-table', TreeTable)

// vue 文件中使用
<tree-table></tree-table>
```
![](https://img2020.cnblogs.com/blog/2113686/202109/2113686-20210913122903957-528437896.png)



<br />

####  4.  作用域插槽  template

```js
<template slot="opt" slot-scope="scope">
                <pre>
                    {{scope.row}}
                </pre>
            </template>

// <pre></pre> 文件预览   slot 表示 作用域插槽的 名字
```

<br />

#### 5. 作用域插槽 template 常用在表单里面
```js
//  scope.row  表示 一整行的数据
<el-table-column label="操作">
              <template slot-scope="scope">
                <el-button size="mine" type="primary" icon="el-icon-edit"
                  @click="showEditDialog((scope.row.attr_id))">编辑</el-button
                >
                <el-button size="mine" type="danger" icon="el-icon-delete"
                  >删除</el-button
                >
              </template>
            </el-table-column>
```