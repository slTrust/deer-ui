### slot 插槽

```
// 组件里
<template>
  <button class="g-button">
    <slot></slot>
  </button>
</template>


// 页面上
<div id="app">
  <g-button>我爱JS</g-button>
</div>
```

### props

- 组件传值

> 普通用法

```
// 组件里
export default {
  name:'',
  props:['icon','iconPosition']
}

// 页面里
<g-button icon="settings">
我爱JS
</g-button>
```

> 高级用法

- 指定默认值
- 指定类型
- 指定验证规则

```
export default {
  name:'',
  props:{
    icon:{},
    iconPosition:{
      type:String,
      default:'left',
      validator(value){
        return value === 'left' && value === 'right'
      }
    }
  }
}
```
