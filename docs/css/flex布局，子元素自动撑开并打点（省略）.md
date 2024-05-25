<img width="230" alt="image" src="https://github.com/hututuhu/blog/assets/37233828/11f7f509-e4ff-4466-abf8-8e93386a6c01">

```css
    .box {
      display: flex;
      align-items: center;
      width: 200px;
    }
    .label {
      margin-right: 4px;
      background-color: #ccc;
      color: #fff;
      white-space: nowrap;
    }
    .desc {
      flex: 1;/** 自动撑开 */
      width: 0;/** 设置了省略才生效 */
      white-space: nowrap;
      text-overflow: ellipsis;
      overflow: hidden;
    }
```

```html
<div class="box">
    <span class="label">标签：</span>
    <div class="desc">我是描诉的味道的点点滴滴点点滴滴点点滴滴点点滴滴的</div>
  </div>
```
