### 前情：
1、我有一个Editor组件，Editor里有一个子组件Download
目的：我想把Download组件里的download方法暴露出去，想让其他地方也可以触发download方法
2、由于我的Editor和Download组件都是函数组件，因此，需要使用useImperativeHandle和forwardRef结合达到目的

### 问题：
拿不到对应download方法
![image](https://github.com/hututuhu/blog/assets/37233828/69214456-8e03-487d-8520-798a445ce48d)
![image](https://github.com/hututuhu/blog/assets/37233828/1a84db46-6bd5-4d81-877b-2e76e3c3cc79)

### 解决方案：
![image](https://github.com/hututuhu/blog/assets/37233828/de1b8848-efd6-44be-8826-fe8dcf8726e4)

### 使用：
```
<Editor ref={editorRef} />
```
```
editorRef.current.downloadRef.current.download()
```
