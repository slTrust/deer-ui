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