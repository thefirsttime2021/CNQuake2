# CNQuake2
基于[`HTML`](https://developer.mozilla.org/zh-CN/docs/Web/HTML)+[`JavaScript`](https://developer.mozilla.org/zh-CN/docs/Learn/JavaScript)+[`css`](https://developer.mozilla.org/zh-CN/docs/Web/CSS)的一个中国地震信息可视化[`PWA`](https://developer.mozilla.org/zh-CN/docs/Web/Progressive_web_apps)软件
如果此软件侵犯了您的权益，请发[`Issue`](https://github.com/thefirsttime2021/CNQuake2/issues/new)或 联系我 liujh5913@petalmail.com
将会尽快处理

## 注意
需要在一个`https`环境里运行，且需要[`SSL`](https://info.support.huawei.com/info-finder/encyclopedia/zh/SSL.html)证书，不能以`file`打开，因为有以下几点：
1. 腾讯地图不允许，因为[`CORS`](https://developer.mozilla.org/zh-CN/docs/Web/HTTP/CORS)跨域问题，否则地图上的所有图标都为默认`Marker`。
2. 只有安全的连接才能使用`PWA`和[`Service worker`](https://developer.mozilla.org/zh-CN/docs/Web/API/Service_Worker_API)，才能发送通知。

### 准备开发的功能
1. 设置-本地烈度触发阀值
2. 多震适配
3. 用 其他方式 画地震波，而不是用官方的[`MultiCircle`](https://lbs.qq.com/webApi/javascriptGL/glDoc/glDocVector#13)，要贴合地球。
4. **以上还是你们来写吧**

### 存在的一些问题
1. 因为腾讯地图的圆是标准的圆，并没有贴和地球，所以到了北边的地方没有畸变，不符合地震波传播的路径，因此地图上的地震波仅供参考，具体以右下角预警框的倒计时为准。
2. 由于腾讯地图的圆不是贴和地球的圆，并且圆没有`getCircleBounds()`，所以`getWaveBounds()`是自行写的，因此地图越缩小视角的中心就越靠北。
3. 腾讯地图的圆有最大半径限制。如果超过最大半径之后，那么控制台就会输出经纬度不在范围内。所以，如果 P波 或者 S波 到达了最大半径，那么它就会停在最大半径的地方静止不动。

### 部分连接需要自己去补充
例如: [ICL API](http://www.365icl.com/index.asp)（在`index.js`中的`2～4`行中补充，最低补充一个，否则不启用ICL(正常人请忽略，不影响正常运行。除非你知道该怎么做，否则不用管它)）

## 免责声明
请勿完全依赖此软件，由于依赖此软件造成的问题作者概不负责。
由于此软件造成的任何人力物力财力等损失与作者无关

## API 源 使用
[Wolfx 防灾API](https://wolfx.jp/apidoc)

## License

本软件基于 [GPL-v3](LICENSE) 协议授权

```
    China Quake 2 (CNQuake2)
    Copyright (C) 2024  HomoOS

    This program is free software: you can redistribute it and/or modify
    it under the terms of the GNU General Public License as published by
    the Free Software Foundation, either version 3 of the License, or
    (at your option) any later version.

    This program is distributed in the hope that it will be useful,
    but WITHOUT ANY WARRANTY; without even the implied warranty of
    MERCHANTABILITY or FITNESS FOR A PARTICULAR PURPOSE.  See the
    GNU General Public License for more details.

    You should have received a copy of the GNU General Public License
    along with this program.  If not, see <https://www.gnu.org/licenses/>.
```
