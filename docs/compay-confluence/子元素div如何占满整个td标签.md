答：两种思路。



思路一、放弃表格自带的自适应功能，也就是内容不会自动垂直居中，高度也不会由内容伸展。

将div相对td绝对定位，div的边缘都紧贴td的边缘。

```css
td {
    position:relative;
}
 
div {
    position:abolsute;
    top:0;
    right:0;
    bottom:0;
    left:0;
}
```

思路二

从div溯源父元素，直到父元素是表格，包含div每个元素设置height:100%;
```css
div,td,tr,tbody,table{
    height:100%
}
```