### npm i 的参数

```$xslt
# 这个依赖开发者使用 , 如 webpack ,parcel-bundler
npm i -D xxx

#  这个是默认的 意思是  用户和你都使用
npm i --save
```

### script引入的 vue 如何定义组件

```$xslt
Vue.component('g-button',{
  template:`
    <button class="g-button">hi</button>
   `
})
```

### 一些CSS定义方式

```
<style>
*{margin:0;padding:0; box-sizing: border-box;}
:root{
  --button-height: 32px;
  --font-size: 14px;
  --button-bg: white;
  --button-active-bg: #eee;
  --border-radius: 4px;
  --color: #333;
  --border-color: #999;
  --border-color-hover: #666;
}
body {
  font-size: var(--font-size);
}
#app {
  margin: 20px;
}
</style>
<style>
.g-button {
  font-size: var(--font-size);
  height: var(--button-height);
  padding: 0 1em;
  border-radius: var(--border-radius);
  border: 1px solid var(--border-color);
  background: var(--button-bg);
}
.g-button:hover {
  border-color: var(--border-color-hover);
}
.g-button:active {
  background-color: var(--button-active-bg);
}
.g-button:focus {
  outline: none;
}
</style>
```

### 使用parcel遇到的问题

```
npm i -D parcel-bundler

# 如何使用 parcel
./node_modules/.bin/parcel index.html

# 也可以
npx parcel index.html

```

#### parcel 的坑

- 有的时候报错，是因为使用了上次的缓存文件

```$xslt
npx parcel index.html --no-cache
```

### `:root` 有兼容问题吗？

- 任何你不确定的特性 https://caniuse.com/ 里搜
- 实在担心你可以用 html

```
html{
 ...你的样式
}
```

### 学习的套路

- 不要妄图掌握所有知识点
- 不要妄图掌握所有知识点
- 不要妄图掌握所有知识点

webpack/scss/less 等，新工具出来这些一年就过时了，你精通了有啥用？
