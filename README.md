# 2lbj.github.io

hexLi 李婶儿的个人博客，基于 [Hugo](https://gohugo.io/) + [hugo-theme-next](https://github.com/hugo-next/hugo-theme-next) 构建，部署在 GitHub Pages。

## 目录结构

```
.
├── hugo.yaml                  # Hugo 主配置文件
├── content/
│   └── posts/                 # 博客文章（Markdown）
├── static/
│   └── imgs/
│       ├── avatar.png         # 侧边栏头像
│       └── icons/             # Favicon 图标（像素风格）
├── layouts/
│   └── _partials/
│       └── head/
│           └── meta.html      # 覆盖主题 meta 模板（favicon 缓存破坏）
├── themes/
│   └── hugo-theme-next/       # NexT 主题（git clone）
├── archetypes/
│   └── default.md             # 新建文章默认模板
└── docs/                      # Hugo 构建输出（GitHub Pages 部署目录）
```

## 本地开发

```bash
# 安装 Hugo（需要 extended 版本）
brew install hugo

# 启动本地预览
hugo server -p 1313 --bind 0.0.0.0

# 构建静态文件
hugo
```

## 部署

推送到 `master` 分支后，GitHub Pages 自动从 `docs/` 目录发布。
