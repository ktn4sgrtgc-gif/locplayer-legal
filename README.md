# Locplayer 商店网站（可直接托管）

这个目录是 App Store Connect 需要的三个公开页面：

- `privacy.html`：隐私政策 URL
- `terms.html`：使用条款
- `support.html`：支持 URL
- `index.html`：三个页面的入口

全部是静态文件，不需要服务器、数据库或构建步骤。

## 已填写的主体信息

- 开发者：`Weiqing Li（Locplayer）`
- 邮箱：`lwq55550731@163.com`
- 版权：`© 2026 Weiqing Li`

生效日期已经填为 **2026 年 10 月 23 日**；如果实际发布日期不同，请一起修改。

## 已部署地址

- 仓库：https://github.com/ktn4sgrtgc-gif/locplayer-legal
- 隐私政策：https://ktn4sgrtgc-gif.github.io/locplayer-legal/privacy.html
- 使用条款：https://ktn4sgrtgc-gif.github.io/locplayer-legal/terms.html
- 技术支持：https://ktn4sgrtgc-gif.github.io/locplayer-legal/support.html

替换后可以检查是否还有残留：

```bash
grep -R "\[开发者姓名/公司\]\|\[联系邮箱\]" .
```

## 方式一：GitHub Pages（免费）

1. 在 GitHub 新建一个 **Public** 仓库，例如 `qingying-legal`。
2. 把本目录的 5 个文件（4 个 HTML + `style.css`）上传到仓库根目录。
3. 仓库 Settings → Pages → Build and deployment：
   - Source 选 `Deploy from a branch`
   - Branch 选 `main`，目录选 `/ (root)`
4. 等待 1–2 分钟，得到：
   - `https://<你的GitHub用户名>.github.io/qingying-legal/privacy.html`
   - `https://<你的GitHub用户名>.github.io/qingying-legal/terms.html`
   - `https://<你的GitHub用户名>.github.io/qingying-legal/support.html`

## 方式二：Netlify Drop（最快）

1. 打开 <https://app.netlify.com/drop>
2. 把整个 `Web` 文件夹拖进去
3. 得到形如 `https://qingying-legal.netlify.app/privacy.html` 的地址

## 方式三：Cloudflare Pages

1. Cloudflare Dashboard → Workers & Pages → Create → Pages
2. 连接 Git 仓库，或直接上传本目录
3. 构建命令留空，输出目录填 `/`

## App Store Connect 填写

- 支持 URL：`https://.../support.html`
- 隐私政策 URL：`https://.../privacy.html`
- 营销 URL：`https://.../`（可选）

检查方式：用浏览器的**无痕窗口**打开三个地址，确认不登录也能访问、中文显示正常、页脚联系方式不是占位符。
