问题：
像push代码到github，失败
![企业微信截图_17035720958363](https://github.com/hututuhu/blog/assets/37233828/95a55033-cf89-4b6f-a295-c86e13f2e979)

解决方案：
git config --global http.proxy http://127.0.0.1:1080
git config --global https.proxy http://127.0.0.1:1080


注：1080是代理端口，查一下代理的配置
