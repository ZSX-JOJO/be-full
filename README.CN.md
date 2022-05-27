# be-full [![NPM Version][npm-image]][npm-url] [![Size][size-image]][size-url]

[npm-image]: https://badgen.net/npm/v/be-full
[npm-url]: https://npmjs.org/package/be-full
[size-image]: https://badgen.net/bundlephobia/minzip/be-full
[size-url]: https://bundlephobia.com/result?p=be-full

**全屏显示**, 支持PC/移动端, 不到**1kb**. [:rocket:在线演示](https://any86.github.io/be-full/example/)

## 语言
**中文** | [English](README.md)

## 安装

```shell
npm i -S be-full
```

## ⚡ 快速开始

##### 网页全屏
```javascript
import {beFull} from 'be-full';
beFull();
```
##### 元素全屏
```javascript
const el = document.getElementById('video');
beFull(el);
```

#### 设置 css 属性":fullscreen"

当元素全屏后如果出现"黑色"间隙(也可能其他颜色),通过第二个参数可设置成指定颜色.
```javascript
const el = document.getElementById("video");
beFull(el, "#fff");
```
**注意:** 执行"**exitFull**"或"**toggleFull**"后会自动取消":fullscreen"的设置.

## 🔥 API

##### exitFull(退出全屏)
```javascript
exitFull();
```

##### toggleFull(切换全屏/退出)
使用方法同`beFull`, 只是第二次点击会执行`exitFull`
```javascript
toggleFull();

// 切换指定元素全屏/退出
toggleFull(document.getElementById('video'));
```

##### isFull(元素是否全屏)
```javascript
isFull(document.getElementById('video')); // true或者false
```