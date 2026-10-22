# Pelakai 博客

基于 Hugo + PaperMod 的静态博客。

访问：https://blog.tszheoi-law.top

## 写文章

1. **网页后台**：https://blog.tszheoi-law.top/tsz （输入密码）
2. **改文件**：在 `content/posts/` 新建 `.md`，提交即可

## 结构

```
hugo.toml              站点配置
content/posts/*.md     文章
static/images/         图片
functions/tsz.js       后台服务（Cloudflare Pages Function）
```

## Cloudflare Pages 构建配置

- **构建命令**：`git clone --depth=1 https://github.com/adityatelange/hugo-PaperMod themes/PaperMod && hugo --gc --minify`
- **输出目录**：`public`
- **环境变量**：
  - `HUGO_VERSION` = `0.128.0`
  - `ADMIN_PASSWORD` = 后台密码
  - `ADMIN_SECRET` = 任意长随机串
  - `GITHUB_TOKEN` = GitHub PAT（repo 权限）
  - `GITHUB_REPO` = `pelakai/blog`
  - `GITHUB_BRANCH` = `main`

主题不在仓库里，构建时自动克隆最新版。