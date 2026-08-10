# 内容初稿生产 Agent 展示页部署说明

这个目录是一个纯静态网页，可部署成公开链接。

## 文件

- `index.html`：完整单页展示网站，已内置 CSS 和 JavaScript。
- `README_DEPLOY.md`：部署说明。

## 安全说明

该网页是公开展示页，不连接真实 Agent，不访问飞书，不调用 API，不保存用户输入。

页面里的“模拟运行”只使用前端写死的演示数据：

- 无后端
- 无数据库
- 无 API Key
- 无飞书 CLI 调用
- 无 Codex / Hermes 调用
- 无用户数据上传

## 最快部署方式：Netlify Drop

1. 打开 Netlify Drop 页面。
2. 把整个 `content-draft-agent-showcase` 文件夹拖进去。
3. Netlify 会自动生成一个公开网址。
4. 如果需要自定义域名，再在 Netlify 后台绑定域名。

适合：最快拿到公开展示链接。

## 推荐部署方式：Vercel

1. 新建一个 GitHub 仓库。
2. 把 `index.html` 上传到仓库根目录。
3. 打开 Vercel，选择该仓库导入。
4. Framework Preset 选择 `Other` 或默认静态项目。
5. 部署完成后获得公开链接。

适合：长期维护展示页。

## GitHub Pages 部署方式

1. 新建 GitHub 仓库，例如 `content-draft-agent-showcase`。
2. 上传 `index.html` 到仓库根目录。
3. 进入仓库 Settings → Pages。
4. Source 选择 `Deploy from a branch`。
5. Branch 选择 `main`，目录选择 `/root`。
6. 保存后等待 GitHub Pages 生成公开链接。

适合：免费、稳定、简单展示。

## 上线前建议替换的内容

页面中有“成功运行截图区域”，建议替换成真实截图：

1. Codex / Hermes 运行成功截图，带时间戳。
2. 飞书文档创建成功截图，能看到文档标题和目录。
3. 输出内容截图，能看到标题、正文、标签、配图建议。

如果要放图片，可以新建 `assets` 文件夹，然后在 `index.html` 中把截图占位卡替换为：

```html
<img src="assets/run-success.png" alt="运行成功截图">
```

## 推荐公开标题

内容初稿生产 Agent｜从素材到可打磨初稿的自动化工作流

## 推荐公开说明

这是一个公开展示页，只展示 Agent 的功能、规范、工作流和边界。页面中的模拟体验不连接真实 Agent、不访问飞书、不接 API、不读取私有数据。
