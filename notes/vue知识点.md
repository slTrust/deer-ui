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

### `<g-button>` 的click事件如何传递

```
// 调用的时候
<g-button :loading="loading1" @click="loading1 = !loading1">
 
// 组件内部
<template>
  <button @click="$emit('click')">
  </button>
</template> 

// 等价于
<template>
  <button @click="xxx">
  </button>
</template> 
<script>
  export default {
    method:{
      xxx(){
        this.$emit('click')    
      }
    }
  }
</script>
```
