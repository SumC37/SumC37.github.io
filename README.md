# myWeb (Hexo)

这是一个 Hexo 静态站点工程，主题为 `hexo-theme-academia`。

## 环境要求

- Node.js（建议 18+ 或 20+）
- Git（用于 `hexo deploy` 推送）

## 本地启动

```bash
npm install
npm run server
```

然后访问：`http://localhost:4000/`

## 本地构建

```bash
npm run clean
npm run build
```

构建产物在 `public/`。

## 部署（Git 推送）

本项目已安装 `hexo-deployer-git`，并在 `_config.yml` 配置了：

- `deploy.repo`
- `deploy.branch`

执行：

```bash
npm run deploy
```

### GitHub Pages 常见注意事项

- 如果仓库是 `username.github.io` 形式，通常部署到默认分支（你这里是 `main`）。
- 首次部署前，确保你本机 Git 已配置凭据（推荐使用 GitHub Token）。
- 站点域名与根路径需要与你的 Pages 设置一致：
  - `_config.yml` 的 `url`（例如 `https://SumC37.github.io`）
  - `_config.yml` 的 `root`（项目页常为 `/repo/`，用户页常为 `/`）

## 内容约定（本主题）

- 首页只展示 front-matter 带 `academia: true` 的文章（主题模板逻辑）。
- Obsidian Callouts 语法（例如 `> [!note]`）由 `hexo-renderer-markdown-it-plus` + `markdown-it-obsidian-callouts` 渲染。

