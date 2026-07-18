# Research Notes

一个面向科研工作者的 Hugo + PaperMod 个人博客模板，使用 GitHub Actions 自动部署到 GitHub Pages。

## 已包含

- PaperMod Profile 首页
- 黑白对半的研究主页封面
- 关于、论文、项目、文章、归档与搜索
- 文章目录、阅读时间、代码复制、面包屑与 RSS
- 适合实验记录的文章 archetype
- GitHub Pages 自动构建和发布

## 本地预览

项目内已经下载过便携版 Hugo，当前工作区可直接运行：

```powershell
.\work\tools\hugo-0.164.0\hugo.exe server -D
```

浏览器打开 `http://localhost:1313/`。

如果换到另一台电脑，请先安装 Hugo 0.146.0 或更高版本，再运行：

```powershell
hugo server -D
```

## 写一篇新文章

```powershell
hugo new content posts/my-new-note/index.md
```

编辑生成的 Markdown 文件，把 `draft: true` 改为 `draft: false` 后提交。

## 个性化

主要信息集中在 `hugo.yaml`：

- `title`：站点标题
- `params.author`：作者名
- `params.profileMode`：主页标题、副标题和按钮
- `params.socialIcons`：GitHub、Scholar、ORCID 等链接
- `menu.main`：顶部导航

主页中央的 `R` 标记由 `assets/css/extended/custom.css` 生成，后续可以替换为太极阴阳图形。

## 发布

仓库推送到 `aspirationer/aspirationer.github.io` 后，在 GitHub 仓库的 **Settings → Pages** 中把 Source 设为 **GitHub Actions**。之后每次推送到 `main` 分支都会自动重新构建并发布。

