### 如何把 icon 搞进 Button里

- 我们需要借助 [iconfont](https://www.iconfont.cn/)
- 选择你要的icon 然后添加到项目 
    - 批量去色
    - 选择 symbol
    - 生成 js 然后就可以在你的项目里用


### 如何让icon旋转

```
@keyframes spin {
  0% { transform: rotate(0deg); }
  100% { transform: rotate(360deg); }
}
.loading{
  animation: spin 2s infinite linear;
}
```

### 检测 button-group 的子元素是不是 button

- mounted 里检查挂载元素

```
<template>
  <div class="g-button-group">
    <slot></slot>
  </div>
</template>
<script>
  export default {
    mounted(){
      for (let node of this.$el.children) {
        let name = node.nodeName.toLowerCase()
        if (name !== 'button') {
          console.warn(`g-button-group 的子元素应该全是 g-button，但是你写的是 ${name}`)
        }
      }
    }
  }
</script>
```