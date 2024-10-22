# CNQuake2
基于`HTML`+`JavaScript`+`css`的一个中国地震信息可视化`PWA`软件
如果此软件侵犯了您的权益，请发 Issue 或 联系我 liujh5913@petalmail.com
将会尽快处理

## 注意
需要在一个`https`环境里运行，且需要`SSL证书`，不能以`file`打开，因为有以下几点：
1. 腾讯地图不允许，因为`CORS`跨域问题，否则地图上的所有图标都为默认`Marker`。
2. 只有安全的连接才能使用`PWA`和`Service worker`，才能发送通知。

### 准备开发的功能
1. 设置-本地烈度触发阀值
2. 多震适配
3. `以上还是你们来写吧`

### 部分连接需要自己去补充
例如ICL API、繁转简API

## 免责声明
请勿完全依赖此软件，由于依赖此软件造成的问题作者概不负责。
由于此软件造成的任何人力物力财力等损失与作者无关

## API 源 使用
[Wolfx 防灾API](https://wolfx.jp/apidoc)
