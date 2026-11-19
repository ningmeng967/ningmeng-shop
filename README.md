# 宁萌商行 · 商品展示页

纯静态网页，无外部依赖（图片全部在 `assets/`，不引用国外 CDN），国内打开速度正常。

## 目录

```
shop-site/
├── index.html        页面（样式和逻辑都在这一个文件里）
├── assets/           商品图片（SVG，可换成你自己的 jpg/png）
└── README.md
```

## 怎么改内容

打开 `index.html`，找到 `/* ====== 配置开始 ====== */` 下面的 `SHOP`：

```js
const SHOP = {
  name:   "宁萌商行",          // 店名
  slogan: "精选好物 · 微信咨询下单",
  wechat: "待填写",            // 微信号，换成你的
  qr:     "",                  // 二维码图片，例如 "assets/qr.png"；留空则不显示
  footer: "© 2026 宁萌商行"
};
```

- **加商品**：在 `PRODUCTS` 数组里加一行 `{ name, category, image }`，图片放进 `assets/`。
- **加分类**：在 `CATEGORIES` 数组里加名字，商品 `category` 对应上即可。
- **换图片**：把图片放进 `assets/`，`image` 写成 `"assets/文件名.jpg"`。

## 本地预览

```bash
cd shop-site && python3 -m http.server 8080
# 浏览器打开 http://127.0.0.1:8080
```
