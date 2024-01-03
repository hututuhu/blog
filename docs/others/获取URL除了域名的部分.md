获取URL除了域名的其他部分
(https://regex101.com/r/vK4rV7/1)[在线测试]

![Uploading 企业微信截图_17042714317645.png…]()

```
const getPathFromUrl = (url: string = '') => {
  let regex = /(http[s]?:\/\/)?([^\\/\s]+\/)(.*)/;
  return (url.match(regex) || [])[3];
};
```

