获取URL除了域名的其他部分
(https://regex101.com/r/vK4rV7/1)[在线测试]

![企业微信截图_17042714317645](https://github.com/hututuhu/blog/assets/37233828/06dd5757-9a46-46a8-8261-6d6a0655dd53)


```
const getPathFromUrl = (url: string = '') => {
  let regex = /(http[s]?:\/\/)?([^\\/\s]+\/)(.*)/;
  return (url.match(regex) || [])[3];
};
```

