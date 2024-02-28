1、input、textarea自动回填默认值。


注：可通过属性 autocomplete="off" 来取消这个行为。

这个行为浏览器并没有暴漏出回调，所以，无法知道这个行为的发生时机。

通过自测，发现window.onload事件里也取不到这个值（这个时候还没有回填），但是下一个宏任务可以取到这个值。

因此，如果想要拿这个值做一些初始化操作，可以这么处理：
```javascript
<script>
  setTimeout(()=>{
    
   const text = document.querySelector("input");
   /**  拿到回填值做一些处理 */
   console.log(text.value)
  },16);
</script>
```

2、中文输入法，不点击空格键，点击屏幕其他地方，不触发keyup事件。

导致如果是从keyup事件拿的值，在这个场景下，最后拿到的值不是正确的，拿到的是一串字母（尽管页面上输入框里可能没有值）。
