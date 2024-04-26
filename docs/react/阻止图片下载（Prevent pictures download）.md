原生、 React都适用：
```javascript
const img = document.querySelector(".img");
/** 防止右键保存 */
img.addEventListener("contextmenu",(e)=>{
  e.preventDefault();
});
/** 防止拖拽保存 */
img.addEventListener("mousedown",(e)=>{
  e.preventDefault();
})
```
